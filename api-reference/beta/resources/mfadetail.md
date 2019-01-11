---
title: tipo de recurso mfaDetail
description: 'Indica los detalles MFA para una sesión específica. Incluye el método de autenticación usado para iniciar sesión, así como detalles de autenticación (por ejemplo: teléfono, SMS o correo de voz) '
localization_priority: Normal
ms.openlocfilehash: 5069045fd202d443a94a80f7333f12ab5e707ada
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883744"
---
# <a name="mfadetail-resource-type"></a>tipo de recurso mfaDetail
Indica los detalles MFA para una sesión específica. Incluye el método de autenticación usado para iniciar sesión, así como detalles de autenticación (por ejemplo: teléfono, SMS o correo de voz) 



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|authDetail|Cadena|Indica el detalle de la autenticación MFA para la actividad de inicio de sesión correspondiente cuando el MFA requerido es "Sí".|
|método authMethod|Cadena|Indica los métodos de autenticación MFA (SMS, teléfono, aplicación Authenticator son algunas del valor) para la actividad de inicio de sesión correspondiente cuando el campo MFA necesario es "Yes".|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mfaDetail"
}-->

```json
{
  "authDetail": "String",
  "authMethod": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mfaDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
