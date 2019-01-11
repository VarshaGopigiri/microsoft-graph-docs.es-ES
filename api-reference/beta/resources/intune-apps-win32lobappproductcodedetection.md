---
title: tipo de recurso win32LobAppProductCodeDetection
description: Contiene las propiedades de código y la versión de producto para detectar una aplicación de Win32
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a3a461661d2b2a37cd7f4e9a37561ea682ea0e0f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812476"
---
# <a name="win32lobappproductcodedetection-resource-type"></a>tipo de recurso win32LobAppProductCodeDetection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de código y la versión de producto para detectar una aplicación de Win32

Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|productCode|Cadena|El código de producto de aplicación de línea de negocio (LoB) de Win32.|
|productVersionOperator|[win32LobAppDetectionOperator](../resources/intune-apps-win32lobappdetectionoperator.md)|El operador para detectar la versión del producto. Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.|
|productVersion|Cadena|La versión del producto de aplicación de línea de negocio (LoB) de Win32.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppProductCodeDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppProductCodeDetection",
  "productCode": "String",
  "productVersionOperator": "String",
  "productVersion": "String"
}
```





