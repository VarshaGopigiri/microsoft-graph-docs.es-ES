---
title: Tipo de recurso emailAddress
description: Representa el nombre y la dirección SMTP de una instancia de entidad, por ejemplo, un mensaje destinatario o el calendario de propietario.
ms.openlocfilehash: f607fe4ce01b9a3c3f5e7af5aa1638fef3840177
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084180"
---
# <a name="emailaddress-resource-type"></a>Tipo de recurso emailAddress

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el nombre y la dirección SMTP de una instancia de entidad, por ejemplo, un mensaje destinatario o el calendario de propietario.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|address|String|La dirección de correo electrónico de una instancia de entidad.|
|name|String|El nombre para mostrar de una instancia de entidad.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.emailAddress"
}-->

```json
{
  "address": "string",
  "name": "string"
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
