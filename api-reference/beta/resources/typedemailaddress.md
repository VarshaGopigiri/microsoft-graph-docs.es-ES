---
title: tipo de recurso typedEmailAddress
description: Representa el nombre, direcciones de correo electrónico y su correspondiente tipo de dirección de correo electrónico de un contacto.
ms.openlocfilehash: 3f40add32fbc219606b6d78041552fc108803d1c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091075"
---
# <a name="typedemailaddress-resource-type"></a>tipo de recurso typedEmailAddress

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el nombre, direcciones de correo electrónico y su correspondiente tipo de dirección de correo electrónico de un [contacto](contact.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|address|String|La dirección de correo electrónico de un contacto.|
|name|String|El nombre para mostrar de un contacto.|
|type |String |El tipo de dirección de correo electrónico. Los valores posibles son: `unknown`, `work`, `personal`, `main` y `other`. El valor predeterminado es `unknown`, lo que significa **dirección** no se ha establecido como un tipo específico. |
|otherLabel |String  |Para especificar un tipo de dirección de correo electrónico personalizado, establezca el **tipo** en `other`y asignar **otherLabel** en una cadena personalizada. Por ejemplo, puede usar una dirección de correo electrónico específica para las actividades de voluntarias. Establecer **tipo de** `other`y establecer **otherLabel** en una cadena personalizada como `Volunteer work`. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.typedEmailAddress"
}-->

```json
{
  "address": "string",
  "name": "string",
  "type": "string",
  "otherLabel": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "emailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
