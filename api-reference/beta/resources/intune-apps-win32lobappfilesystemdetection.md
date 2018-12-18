---
title: tipo de recurso win32LobAppFileSystemDetection
description: Contiene la ruta de acceso de archivo o carpeta para detectar una aplicación de Win32
author: tfitzmac
ms.openlocfilehash: 26d65c8a1fcf70032c780b3e6e00a198a8ff2c30
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306877"
---
# <a name="win32lobappfilesystemdetection-resource-type"></a>tipo de recurso win32LobAppFileSystemDetection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene la ruta de acceso de archivo o carpeta para detectar una aplicación de Win32

Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|ruta de acceso|String|La ruta de acceso de archivo o carpeta para detectar la aplicación de línea de negocio (LoB) de Win32|
|fileOrFolderName|String|El nombre de archivo o carpeta para detectar la aplicación de línea de negocio (LoB) de Win32|
|check32BitOn64System|Boolean|Un valor que indica si este archivo o carpeta para comprobar la aplicación de 32 bits en el sistema de 64 bits|
|tipo de detección|[win32LobAppFileSystemDetectionType](../resources/intune-apps-win32lobappfilesystemdetectiontype.md)|El tipo de detección del sistema de archivos. Los valores posibles son: `notConfigured`, `exists`, `modifiedDate`, `createdDate`, `version`, `sizeInMB`.|
|operator|[win32LobAppDetectionOperator](../resources/intune-apps-win32lobappdetectionoperator.md)|El operador para la detección de archivos o carpetas. Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.|
|detectionValue|String|El valor de detección de archivo o carpeta|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppFileSystemDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppFileSystemDetection",
  "path": "String",
  "fileOrFolderName": "String",
  "check32BitOn64System": true,
  "detectionType": "String",
  "operator": "String",
  "detectionValue": "String"
}
```





