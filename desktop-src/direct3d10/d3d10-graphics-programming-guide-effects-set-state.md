---
description: Solo es necesario inicializar algunas constantes de efecto. Consulte el código básico para establecer variables de efecto en Direct3D 10.
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: Establecer estado de efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df7133276b6392abca8d75eed16de896fb58f84
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404728"
---
# <a name="set-effect-state-direct3d-10"></a><span data-ttu-id="9fbbd-104">Establecer estado de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9fbbd-104">Set Effect State (Direct3D 10)</span></span>

<span data-ttu-id="9fbbd-105">Solo es necesario inicializar algunas constantes de efecto.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-105">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="9fbbd-106">Una vez inicializado, el estado del efecto se establece en el dispositivo para todo el bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-106">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="9fbbd-107">Es necesario actualizar otras variables cada vez que se llama al bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-107">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="9fbbd-108">A continuación se muestra el código básico para establecer variables de efecto para cada uno de los tipos de variables.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-108">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="9fbbd-109">Un efecto encapsula todo el estado de representación necesario para realizar un paso de representación.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-109">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="9fbbd-110">En cuanto a la API, hay tres tipos de estado encapsulados en un efecto.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-110">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="9fbbd-111">Estado constante</span><span class="sxs-lookup"><span data-stu-id="9fbbd-111">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="9fbbd-112">Estado del sombreador</span><span class="sxs-lookup"><span data-stu-id="9fbbd-112">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="9fbbd-113">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="9fbbd-113">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="9fbbd-114">Estado constante</span><span class="sxs-lookup"><span data-stu-id="9fbbd-114">Constant State</span></span>

<span data-ttu-id="9fbbd-115">En primer lugar, declare variables en un efecto mediante tipos de datos HLSL.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-115">First, declare variables in an effect using HLSL data types.</span></span>


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



<span data-ttu-id="9fbbd-116">En segundo lugar, declare variables en la aplicación que la aplicación pueda establecer y, a continuación, actualizará las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-116">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D10CreateDevice()
{
  ...
    g_pLightDir = g_pEffect10->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect10->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect10->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect10->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect10->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect10->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect10->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect10->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="9fbbd-117">En tercer lugar, use los métodos de actualización para establecer el valor de las variables de la aplicación en las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-117">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D10FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="9fbbd-118">Dos maneras de obtener el estado en una variable de efecto</span><span class="sxs-lookup"><span data-stu-id="9fbbd-118">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="9fbbd-119">Hay dos maneras de obtener el estado contenido en una variable de efecto.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-119">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="9fbbd-120">Dado un efecto que se ha cargado en la memoria.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-120">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="9fbbd-121">Una manera es obtener el estado del muestreador de una interfaz [**ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) que se ha convertido como una interfaz sampler.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-121">One way is to get the sampler state from an [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) that has been cast as a sampler interface.</span></span>


```
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
        hr = (l_pD3D10EffectVariable->AsSampler())->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="9fbbd-122">La otra manera es obtener el estado del sampler de una [**interfaz ID3D10SamplerState**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span><span class="sxs-lookup"><span data-stu-id="9fbbd-122">The other way is to get the sampler state from an [**ID3D10SamplerState Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span></span>


```
ID3D10SamplerState* l_ppSamplerState = NULL;
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
    {
        hr = (l_pD3D10EffectVariable->AsSampler())->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="9fbbd-123">Estado del sombreador</span><span class="sxs-lookup"><span data-stu-id="9fbbd-123">Shader State</span></span>

<span data-ttu-id="9fbbd-124">El estado del sombreador se declara y asigna en una técnica de efecto, dentro de un paso.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-124">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="9fbbd-125">Esto funciona igual que lo haría si no usara ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-125">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="9fbbd-126">Hay tres llamadas, una para cada tipo de sombreador (vértice, geometría y píxel).</span><span class="sxs-lookup"><span data-stu-id="9fbbd-126">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="9fbbd-127">El primero, SetVertexShader, llama a [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="9fbbd-127">The first one, SetVertexShader, calls [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span></span> <span data-ttu-id="9fbbd-128">CompileShader es una función de efecto especial que toma el perfil del sombreador (frente a 4 0) y el nombre de la función de sombreador de vértices \_ \_ (RenderVS).</span><span class="sxs-lookup"><span data-stu-id="9fbbd-128">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="9fbbd-129">En otras palabras, cada una de estas llamadas a SetXXXShader compila su función de sombreador asociada y devuelve un puntero al sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-129">In other words, each of these SetXXXShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

## <a name="texture-state"></a><span data-ttu-id="9fbbd-130">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="9fbbd-130">Texture State</span></span>

<span data-ttu-id="9fbbd-131">El estado de textura es un poco más complejo que establecer una variable, ya que los datos de textura no se leen simplemente como una variable, sino que se muestrea a partir de una textura.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-131">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="9fbbd-132">Por lo tanto, debe definir la variable de textura (al igual que una variable normal, excepto que usa un tipo de textura) y debe definir las condiciones de muestreo.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-132">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="9fbbd-133">Este es un ejemplo de una declaración de variable de textura y la declaración de estado de muestreo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-133">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="9fbbd-134">Este es un ejemplo de cómo establecer una textura desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-134">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="9fbbd-135">En este ejemplo, la textura se almacena en los datos de malla que se cargaron cuando se creó el efecto.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-135">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="9fbbd-136">El primer paso es obtener un puntero a la textura desde el efecto (desde la malla).</span><span class="sxs-lookup"><span data-stu-id="9fbbd-136">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="9fbbd-137">El segundo paso es especificar una vista para acceder a la textura.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-137">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="9fbbd-138">La vista define una manera general de acceder a los datos desde el recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="9fbbd-138">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D10FrameRender()
{
  ID3D10ShaderResourceView* pDiffuseRV = NULL;

   ...
   pDiffuseRV = g_Mesh10.GetMaterial(pSubset->MaterialID)->pDiffuseRV10;
   g_ptxDiffuse->SetResource( pDiffuseRV );
   ...
}   
```



<span data-ttu-id="9fbbd-139">Para obtener más información sobre cómo ver recursos, vea [Vistas de textura (Direct3D 10).](d3d10-graphics-programming-guide-resources-access-views.md)</span><span class="sxs-lookup"><span data-stu-id="9fbbd-139">For more information about viewing resources, see [Texture Views (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fbbd-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fbbd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fbbd-141">Representación de un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9fbbd-141">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



