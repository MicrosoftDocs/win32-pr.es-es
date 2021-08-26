---
description: Al crear un paquete de instalación, puede usar la función MsiViewModify o el método View.Modify para asegurarse de que los datos que especifique son sintácticamente correctos.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Validación interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44184a87f7d8bd28b3603d81bb83ae28ec68471e6c9c849bf9322dc5e968c886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043305"
---
# <a name="internal-validation"></a>Validación interna

Al crear un paquete de instalación, puede usar la función [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o el método View.Modify para asegurarse de que los datos que escriba son sintácticamente correctos. Para obtener más información, vea [**Modify method**](view-modify.md). En el nivel más bajo, la columna de una tabla de base de datos puede almacenar enteros (cortos o largos), cadenas o datos binarios. Sin embargo, un paquete de instalación requiere enteros o cadenas específicos en determinadas tablas. Estas especificaciones se mantienen en la [ \_ tabla Validación](-validation-table.md). Por ejemplo, la columna FileName de la [tabla File](file-table.md) es una columna de cadena, pero almacena específicamente un nombre de archivo. Por lo tanto, no solo debe ser una cadena, sino que también debe seguir los requisitos para asignar nombres a los archivos.

Los distintos valores de enumeración de validación usados [**con la función MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) permiten la validación inmediata en distintos niveles. La enumeración MSIMODIFY \_ VALIDATE FIELD se puede usar para validar campos \_ individuales de un registro. No valida las claves externas. La enumeración MSIMODIFY \_ VALIDATE valida una fila completa e incluye la validación de clave externa. Si va a insertar una nueva fila en una tabla, use la enumeración MSIMODIFY VALIDATE NEW para comprobar que va a agregar datos válidos y que usa claves \_ \_ principales únicas. Se produce un error en una inserción si las claves principales no son únicas. Si una llamada a **MsiViewModify** con una de las enumeraciones de validación devuelve un error, puede realizar llamadas repetidas a [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) para diagnosticar el problema. **MsiViewGetError indica** la columna donde se produjo el error, así como el valor de enumeración para ayudar a corregir el problema. Para obtener más información, vea [**GetError method**](view-geterror.md).

También puede usar la validación interna para asegurarse de que otros autores escriban los datos correctamente en la tabla personalizada. Agregue cada una de las columnas de la tabla personalizada a la tabla Validación con el nombre de la tabla personalizada y el nombre de \_ columna como clave principal. Proporcione una descripción o propósito de cada columna de la columna Descripción de la \_ tabla Validación. Escriba los requisitos aplicables para cada columna mediante las columnas Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Category y Set:

-   Si la columna acepta valores NULL, escriba una "Y". Si no es así, escriba "N".
-   Si la columna es una columna de enteros y puede contener un intervalo de enteros, escriba ese intervalo mediante las columnas MinValue y MaxValue.
-   Las columnas de clave externa se identifican mediante las columnas KeyTable y KeyColumn.
-   Para las columnas de cadena, especifique una categoría como Nombre de archivo, GUID o Identificador. Para obtener más información, vea tipos [de datos de columna](column-data-types.md).
-   Si los datos solo pueden pertenecer a un número específico de valores (cadena o entero), use la columna Set para enumerar los valores aceptables.

A continuación se muestra una lista de las columnas (además de Tabla, Columna y Descripción) de la tabla Validación que se pueden rellenar si la columna es del \_ tipo especificado. (Tenga en cuenta que no tiene que rellenar todas las columnas).



| Tipo    | Columnas                                                          |
|---------|------------------------------------------------------------------|
| Entero | Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Set           |
| String  | Nullable, KeyTable, KeyColumn, Category, Set, MinValue, MaxValue |
| Binary  | Categoría que acepta valores NULL (la categoría debe ser "Binary")                   |



 

Los entornos de creación pueden usar MSIMODIFY \_ VALIDATE \_ DELETE. En esta enumeración se da por supuesto que desea eliminar la fila. No se realiza ninguna validación de campo o clave externa. Esta enumeración realiza realmente una validación de clave externa inversa. Comprueba en la tabla Validation las referencias de las columnas KeyTable y KeyColumn de la tabla a la que pertenece la \_ fila "eliminada". Si hay columnas que muestran la tabla que contiene la fila "eliminada" como una posible clave externa, recorrerá esa columna para ver si alguno de los valores hace referencia a los valores de la fila "eliminada". Una devolución de error significa que se rompe la integridad relacional de la base de datos mediante la eliminación de la fila.

 

 



