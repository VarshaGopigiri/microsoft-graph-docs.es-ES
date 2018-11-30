---
title: tipo de recurso signInStatus
description: Proporciona el inicio de sesión de estado (correcto o error) de inicio de sesión de
ms.openlocfilehash: cafa0dffe1b1d798d87225ac82901cf041d5e4fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089989"
---
# <a name="signinstatus-resource-type"></a>tipo de recurso signInStatus
Proporciona el inicio de sesión de estado (correcto o error) de inicio de sesión de



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|additionalDetails|String|Proporciona detalles adicionales acerca de la actividad de inicio de sesión|
|errorCode|Int32|Proporciona el código de error 5-6digit que se genera durante un error de inicio de sesión. Revise la [lista de códigos de error y los mensajes](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).|
|failureReason|String|Proporciona el mensaje de error o el motivo del error para la actividad de inicio de sesión correspondiente. Revise la [lista de códigos de error y los mensajes](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInStatus"
}-->

```json
{
  "additionalDetails": "String",
  "errorCode": 1024,
  "failureReason": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->