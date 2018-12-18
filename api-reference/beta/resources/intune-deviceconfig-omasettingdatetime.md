---
title: Tipo de recurso omaSettingDateTime
description: Definición de DateTime de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: 2bf55308c230ec848f7ee58f66e710f1b31c1692
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307990"
---
# <a name="omasettingdatetime-resource-type"></a>Tipo de recurso omaSettingDateTime

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de DateTime de la configuración de OMA.

Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|descripción|String|Descripción. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|omaUri|cadena|OMA. Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)|
|value|DateTimeOffset|Valor.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingDateTime"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingDateTime",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String (timestamp)"
}
```





