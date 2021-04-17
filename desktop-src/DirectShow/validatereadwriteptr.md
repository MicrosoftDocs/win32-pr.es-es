---
description: Comprueba que el proceso de llamada tiene acceso de lectura y escritura a un bloque de memoria. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Macro ValidateReadWritePtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681167"
---
# <a name="validatereadwriteptr-macro"></a><span data-ttu-id="0aae2-104">ValidateReadWritePtr (macro)</span><span class="sxs-lookup"><span data-stu-id="0aae2-104">ValidateReadWritePtr macro</span></span>

<span data-ttu-id="0aae2-105">Comprueba que el proceso de llamada tiene acceso de lectura y escritura a un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="0aae2-105">Verifies that the calling process has read/write access to a memory block.</span></span> <span data-ttu-id="0aae2-106">Si no es así, la macro llama a la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="0aae2-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="0aae2-107">Esta macro está en desuso.</span><span class="sxs-lookup"><span data-stu-id="0aae2-107">This macro is deprecated.</span></span> <span data-ttu-id="0aae2-108">En el Windows SDK para Windows Vista (y versiones posteriores), esta macro no hace nada.</span><span class="sxs-lookup"><span data-stu-id="0aae2-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0aae2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aae2-109">Syntax</span></span>


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="0aae2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aae2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aae2-111">*m*</span><span class="sxs-lookup"><span data-stu-id="0aae2-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="0aae2-112">Puntero a un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="0aae2-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="0aae2-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="0aae2-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="0aae2-114">Tamaño del bloque de memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0aae2-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aae2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aae2-115">Return value</span></span>

<span data-ttu-id="0aae2-116">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0aae2-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aae2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aae2-117">Remarks</span></span>

<span data-ttu-id="0aae2-118">Esta macro se omite a menos que se defina DEBUG, \_ Debug o VFWROBUST cuando se incluye el archivo de encabezado de clase base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0aae2-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="0aae2-119">Esta macro puede tener un costo de rendimiento considerable.</span><span class="sxs-lookup"><span data-stu-id="0aae2-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aae2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aae2-120">Requirements</span></span>



| <span data-ttu-id="0aae2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aae2-121">Requirement</span></span> | <span data-ttu-id="0aae2-122">Value</span><span class="sxs-lookup"><span data-stu-id="0aae2-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aae2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aae2-123">Header</span></span><br/> | <dl> <span data-ttu-id="0aae2-124"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aae2-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aae2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aae2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aae2-126">Macros de validación de puntero</span><span class="sxs-lookup"><span data-stu-id="0aae2-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




