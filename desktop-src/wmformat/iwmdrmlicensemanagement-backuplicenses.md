---
title: Método IWMDRMLicenseManagement BackupLicenses (Wmdrmsdk.h)
description: El método BackupLicenses crea una copia de seguridad de las licencias en el almacén de licencias local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- BackupLicenses, método windows Media Format
- Método BackupLicenses windows Media Format , interfaz IWMDRMLicenseManagement
- IWMDRMLicenseManagement interfaz windows Media Format , Método BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3905f8fd464645f7fcd22551360e6a9610913eeea7f191d7e770e24f5ea8cd49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027653"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>IWMDRMLicenseManagement::BackupLicenses (Método)

El **método BackupLicenses** crea una copia de seguridad de las licencias en el almacén de licencias local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrBackupDirectory* \[ En\]
</dt> <dd>

Ruta de acceso UNC de la ubicación en la que se realizará la copia de seguridad de las licencias.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican las opciones de copia de seguridad que se usarán. La única marca admitida actualmente es WMDRM BACKUP OVERWRITE, que configura el método para sobrescribir los archivos de copia de seguridad \_ \_ existentes en el directorio.

</dd> <dt>

*piqueCancelationCookie* \[ out\]
</dt> <dd>

Puntero que recibe un puntero a la **interfaz IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al [**método IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método se ejecuta de forma asincrónica. Devuelve inmediatamente después de llamarse y, a continuación, genera una serie de eventos **MEWMDRMLicenseBackupProgress** seguidos de un evento **MEWMDRMLicenseBackupCompleted** cuando se completa el procesamiento. El valor de cada uno de los eventos **MEWMDRMLicenseBackupProgress obtenidos** mediante una llamada a **IMFMediaEvent::GetValue** es un **puntero IUnknown.** Puede llamar al **método QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la [**interfaz IWMDRMLicenseBackupRestoreStatus.**](iwmdrmlicensebackuprestorestatus.md)

Para obtener más información sobre el uso de los métodos asincrónicos de Windows MEDIA DRM Client Extended API, vea [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

No se permite realizar una copia de seguridad de todas las licencias. Este método solo hace una copia de seguridad de las licencias que lo permiten.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





