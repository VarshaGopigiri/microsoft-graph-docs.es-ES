---
title: Tipo de recurso auditProperty
description: Una clase que contiene las propiedades de la propiedad de auditoría.
ms.openlocfilehash: eaffa5552d611ac2ef8bb236009b9520d1134586
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032043"
---
# <a name="auditproperty-resource-type"></a>Tipo de recurso auditProperty

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades de la propiedad de auditoría.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar.|
|oldValue|cadena|Valor antiguo.|
|newValue|cadena|Valor nuevo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditProperty"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditProperty",
  "displayName": "String",
  "oldValue": "String",
  "newValue": "String"
}
```



