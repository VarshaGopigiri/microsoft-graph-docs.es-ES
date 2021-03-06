---
title: tipo de recurso win32LobAppRegistryDetection
description: Contiene las propiedades del registro para detectar una aplicación de Win32
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 23362d7613d198bdd848205cbf20944e9a592f04
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923904"
---
# <a name="win32lobappregistrydetection-resource-type"></a>tipo de recurso win32LobAppRegistryDetection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del registro para detectar una aplicación de Win32

Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|check32BitOn64System|Booleano|Un valor que indica si esta ruta de acceso del registro para comprobar la aplicación de 32 bits en el sistema de 64 bits|
|ruta de acceso clave|Cadena|La ruta de la clave del registro para detectar la aplicación de línea de negocio (LoB) de Win32|
|Valor|Cadena|El nombre del valor del registro|
|tipo de detección|[win32LobAppRegistryDetectionType](../resources/intune-apps-win32lobappregistrydetectiontype.md)|El tipo de detección de datos del registro. Los valores posibles son: `notConfigured`, `exists`, `doesNotExist`, `string`, `integer`, `version`.|
|operator|[win32LobAppDetectionOperator](../resources/intune-apps-win32lobappdetectionoperator.md)|El operador para la detección de datos del registro. Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.|
|detectionValue|Cadena|El valor de detección del registro|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppRegistryDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppRegistryDetection",
  "check32BitOn64System": true,
  "keyPath": "String",
  "valueName": "String",
  "detectionType": "String",
  "operator": "String",
  "detectionValue": "String"
}
```





