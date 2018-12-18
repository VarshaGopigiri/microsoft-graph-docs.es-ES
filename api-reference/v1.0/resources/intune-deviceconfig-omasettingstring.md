---
title: Tipo de recurso omaSettingString
description: Definición de la cadena de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: a62f6dee2bf0f5a9ca96488625a84ceef5f7c785
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311203"
---
# <a name="omasettingstring-resource-type"></a>Tipo de recurso omaSettingString

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de la cadena de la configuración de OMA.

Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|descripción|String|Descripción. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
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



