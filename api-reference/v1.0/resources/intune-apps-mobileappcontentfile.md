---
title: Tipo de recurso mobileAppContentFile
description: Contiene las propiedades de un archivo instalador único que está asociado a una versión de mobileAppContent determinada.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6f745367a61a61511cdab35e556538631fa93962
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986092"
---
# <a name="mobileappcontentfile-resource-type"></a>Tipo de recurso mobileAppContentFile

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de un archivo instalador único que está asociado a una versión de mobileAppContent determinada.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileAppContentFiles](../api/intune-apps-mobileappcontentfile-list.md)|Colección [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)|Enumere las propiedades y las relaciones de los objetos [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).|
|[Obtener mobileAppContentFile](../api/intune-apps-mobileappcontentfile-get.md)|[mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)|Lea las propiedades y las relaciones del objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).|
|[Crear mobileAppContentFile](../api/intune-apps-mobileappcontentfile-create.md)|[mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)|Cree un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).|
|[Eliminar mobileAppContentFile](../api/intune-apps-mobileappcontentfile-delete.md)|Ninguna|Elimina un [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).|
|[Actualizar mobileAppContentFile](../api/intune-apps-mobileappcontentfile-update.md)|[mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)|Actualice las propiedades de un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).|
|[Acción commit](../api/intune-apps-mobileappcontentfile-commit.md)|Ninguna|Confirma un archivo de una aplicación determinada.|
|[Acción renewUpload](../api/intune-apps-mobileappcontentfile-renewupload.md)|Ninguna|Renueva el URI de SAS para una carga de un archivo de la aplicación.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|azureStorageUri|String|El URI de Azure Storage.|
|isCommitted|Booleano|Un valor que indica si el archivo está confirmado.|
|id|Cadena|El Id. de archivo.|
|createdDateTime|DateTimeOffset|La hora en que se ha creado el archivo.|
|name|String|El nombre del archivo.|
|size|Int64|El tamaño del archivo antes del cifrado.|
|sizeEncrypted|Int64|El tamaño del archivo después del cifrado.|
|azureStorageUriExpirationDateTime|DateTimeOffset|La hora en que expira el URI de Azure Storage.|
|manifiesto|Binario|La información del manifiesto.|
|uploadState|[mobileAppContentFileUploadState](../resources/intune-apps-mobileappcontentfileuploadstate.md)|El estado de la solicitud de carga actual. Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed` y `commitFileTimedOut`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppContentFile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppContentFile",
  "azureStorageUri": "String",
  "isCommitted": true,
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "name": "String",
  "size": 1024,
  "sizeEncrypted": 1024,
  "azureStorageUriExpirationDateTime": "String (timestamp)",
  "manifest": "binary",
  "uploadState": "String"
}
```



