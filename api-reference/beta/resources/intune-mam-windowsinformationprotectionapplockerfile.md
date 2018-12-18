---
title: Tipo de recurso windowsInformationProtectionAppLockerFile
description: Archivo de bloqueo de aplicaciones de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: d4ba3fbbcefd780bb90f525b41e7bdc541843a30
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341156"
---
# <a name="windowsinformationprotectionapplockerfile-resource-type"></a>Tipo de recurso windowsInformationProtectionAppLockerFile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Archivo de bloqueo de aplicaciones de Windows Information Protection
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsInformationProtectionAppLockerFiles](../api/intune-mam-windowsinformationprotectionapplockerfile-list.md)|Colección [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)|Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).|
|[Obtener windowsInformationProtectionAppLockerFile](../api/intune-mam-windowsinformationprotectionapplockerfile-get.md)|[windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)|Lea las propiedades y las relaciones del objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).|
|[Crear windowsInformationProtectionAppLockerFile](../api/intune-mam-windowsinformationprotectionapplockerfile-create.md)|[windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)|Cree un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).|
|[Eliminar windowsInformationProtectionAppLockerFile](../api/intune-mam-windowsinformationprotectionapplockerfile-delete.md)|Ninguna|Elimina un [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).|
|[Actualizar windowsInformationProtectionAppLockerFile](../api/intune-mam-windowsinformationprotectionapplockerfile-update.md)|[windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)|Actualice las propiedades de un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|El nombre descriptivo|
|fileHash|String|Hash del archivo SHA256|
|file|Binario|Archivo como una matriz de bytes|
|id|String|Clave de la entidad.|
|version|String|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtectionAppLockerFile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "String",
  "fileHash": "String",
  "file": "binary",
  "id": "String (identifier)",
  "version": "String"
}
```





