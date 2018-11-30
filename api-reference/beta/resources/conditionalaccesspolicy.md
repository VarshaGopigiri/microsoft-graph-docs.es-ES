---
title: tipo de recurso conditionalAccessPolicy
description: Indica los atributos relacionados con una directiva de acceso condicional o las directivas que se desencadena la actividad de inicio de sesión correspondiente
ms.openlocfilehash: 56a06d6b5fcba96dc472eb63fe24ba3920b0dd09
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090876"
---
# <a name="conditionalaccesspolicy-resource-type"></a>tipo de recurso conditionalAccessPolicy
Indica los atributos relacionados con una directiva de acceso condicional o las directivas que se desencadena la actividad de inicio de sesión correspondiente



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String|Hace referencia al nombre de la directiva de acceso condicional (ejemplo: "Requieren MFA para fuerza de ventas").|
|enforcedGrantControls|Colección String|Hace referencia a los controles de grant aplicados por la directiva de acceso condicional (ejemplo: "Requieren autenticación multifactor").|
|enforcedSessionControls|Colección String|Hace referencia a los controles de sesión aplicados por la directiva de acceso condicional (ejemplo: "Requiere un control aplicación exigido").|
|id|String|GUID único de la directiva de acceso condicional|
|result|String| Indica el resultado de la directiva de entidad emisora de certificados que se desencadenó. Los valores posibles son:<br/> `success` <br/> `failure` <br/> `notApplied`-Directiva no se aplica porque no se cumplieron las condiciones de la directiva. <br/> `notEnabled`-Esto es debido a la directiva en estado deshabilitado.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.conditionalAccessPolicy"
}-->

```json
{
  "displayName": "String",
  "enforcedGrantControls": ["String"],
  "enforcedSessionControls": ["String"],
  "id": "String",
  "result": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conditionalAccessPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->