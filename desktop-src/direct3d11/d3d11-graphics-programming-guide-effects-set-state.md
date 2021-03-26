---
title: Establecer el estado del efecto (Direct3D 11)
description: Algunas constantes Effect solo deben inicializarse.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df65e164c2df01f78ae9ea9ab83a547b977335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531912"
---
# <a name="set-effect-state-direct3d-11"></a>Establecer el estado del efecto (Direct3D 11)

Algunas constantes Effect solo deben inicializarse. Una vez inicializado, el estado del efecto se establece en el dispositivo para todo el bucle de representación. Es necesario actualizar otras variables cada vez que se llama al bucle de representación. A continuación se muestra el código básico para establecer las variables de efecto, para cada uno de los tipos de variables.

Un efecto encapsula todo el estado de representación necesario para realizar una fase de representación. En lo que respecta a la API, hay tres tipos de estado encapsulados en un efecto.

-   [Estado constante](#constant-state)
-   [Estado del sombreador](#shader-state)
-   [Estado de textura](#texture-state)

## <a name="constant-state"></a>Estado constante

En primer lugar, declare las variables en un efecto mediante los tipos de datos de HLSL.


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



En segundo lugar, declare las variables de la aplicación que se pueden establecer en la aplicación y, a continuación, actualice las variables de efecto.


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

    
OnD3D11CreateDevice()
{
  ...
    g_pLightDir = g_pEffect11->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect11->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect11->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect11->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect11->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect11->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect11->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect11->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



En tercer lugar, use los métodos de actualización para establecer el valor de las variables de la aplicación en las variables de efecto.


```
           
OnD3D11FrameRender()
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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>Dos maneras de obtener el estado en una variable de efecto

Hay dos maneras de obtener el estado contenido en una variable de efecto. Dado un efecto que se ha cargado en la memoria.

Una manera es obtener el estado de la muestra de un [**ID3DX11EffectVariable**](id3dx11effectvariable.md) que se ha convertido en una interfaz de muestra.


```
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid() )
        hr = (l_pD3D11EffectVariable->GetBackingStore( 0, 
            &sampler_desc );
}
```



La otra forma es obtener el estado de la muestra de un [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).


```
ID3D11SamplerState* l_ppSamplerState = NULL;
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid )
    {
        hr = l_pD3D11EffectVariable->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a>Estado del sombreador

El estado del sombreador se declara y se asigna en una técnica de efecto, dentro de un paso.


```
VertexShader vsRenderScene = CompileShader( vs_4_0, RenderSceneVS( 1, true, true );  
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( vsRenderScene );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



Esto funciona igual que si no estuviera usando ningún efecto. Hay tres llamadas, una para cada tipo de sombreador (vértice, geometría y píxel). El primero, SetVertexShader, llama a [**ID3D11DeviceContext:: VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader). CompileShader es una función especial de efecto que toma el perfil de sombreador (vs \_ 4 \_ 0) y el nombre de la función de sombreador de vértices (RenderVS). En otras palabras, cada una de estas llamadas CompileShader compila su función de sombreador asociada y devuelve un puntero al sombreador compilado.

Tenga en cuenta que no se debe establecer todo el estado del sombreador. Este paso no incluye ninguna llamada a SetHullShader o SetDomainShader, lo que significa que el casco y los sombreadores de dominio actualmente enlazados no se modificarán.

## <a name="texture-state"></a>Estado de textura

El estado de la textura es un poco más complejo que establecer una variable, ya que los datos de la textura no se leen simplemente como una variable, se muestra a partir de una textura. Por lo tanto, debe definir la variable de textura (al igual que una variable normal, excepto que usa un tipo de textura) y debe definir las condiciones de muestreo. A continuación se muestra un ejemplo de una declaración de variable de textura y la declaración de estado de muestreo correspondiente.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Este es un ejemplo de cómo establecer una textura desde una aplicación. En este ejemplo, la textura se almacena en los datos de la malla, que se cargó al crear el efecto.

El primer paso es obtener un puntero a la textura del efecto (desde la malla).


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



El segundo paso consiste en especificar una vista para tener acceso a la textura. La vista define una manera general de tener acceso a los datos del recurso de textura.


```
   
OnD3D11FrameRender()
{
  ID3D11ShaderResourceView* pDiffuseRV = NULL;

  ...
  pDiffuseRV = g_Mesh11.GetMaterial(pSubset->MaterialID)->pDiffuseRV11;
  g_ptxDiffuse->SetResource( pDiffuseRV );
  ...
}   
```



Desde la perspectiva de la aplicación, las vistas de acceso desordenados se controlan de forma similar a las vistas de recursos del sombreador. Sin embargo, en el efecto sombreador de píxeles y las funciones del sombreador de cálculo, los datos de vista de acceso desordenados se leen o se escriben directamente en. No se puede muestrear desde una vista de acceso desordenado.

Para obtener más información sobre cómo ver recursos, vea [recursos](overviews-direct3d-11-resources.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un efecto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




