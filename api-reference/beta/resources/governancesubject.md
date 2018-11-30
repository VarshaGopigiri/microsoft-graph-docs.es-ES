---
title: tipo de recurso governanceSubject
description: Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).
ms.openlocfilehash: c2129a0da488d4e7f425d6ef3596a955269e0da8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083771"
---
# <a name="governancesubject-resource-type"></a>tipo de recurso governanceSubject

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).


## <a name="properties"></a>Propiedades
| Propiedad  | Tipo       |Descripción|
|:----------|:----------|:----------|
|id         |String     | El identificador del tema.|
|type       |String     |El tipo de objeto. El valor puede ser ``User``, ``Group``, y ``ServicePrincipal``.|
|displayName|String     |El nombre para mostrar del asunto.|
|email      |String     |La dirección de correo electrónico del sujeto del usuario. Si el asunto es en otros tipos, está vacío.|
|principalName|String   |El nombre principal del objeto de usuario. Si el asunto es en otros tipos, está vacío.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceSubject"
}-->

```json
{
  "id": "String",  
  "displayName": "String",
  "email": "String",
  "principalName": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceSubject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->