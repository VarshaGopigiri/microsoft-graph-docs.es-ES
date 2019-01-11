---
title: Tipo de recurso omaSettingInteger
description: Definición del entero de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f40d5d225c2b4b99573c482b39f886bcd463e9fe
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860455"
---
# <a name="omasettinginteger-resource-type"></a>Tipo de recurso omaSettingInteger

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición del entero de la configuración de OMA.

Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|descripción|Cadena|Descripción. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|omaUri|cadena|OMA. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|valor|Int32|Valor.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingInteger"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingInteger",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": 1024
}
```



