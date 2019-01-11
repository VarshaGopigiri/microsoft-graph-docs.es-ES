---
title: Tipo de recurso omaSettingString
description: Definición de la cadena de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 890d636afb29fbfb188e9c1b514eecc6360001b3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841352"
---
# <a name="omasettingstring-resource-type"></a>Tipo de recurso omaSettingString

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de la cadena de la configuración de OMA.

Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|descripción|Cadena|Descripción. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|omaUri|cadena|OMA. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|valor|cadena|Valor.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingString"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingString",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String"
}
```



