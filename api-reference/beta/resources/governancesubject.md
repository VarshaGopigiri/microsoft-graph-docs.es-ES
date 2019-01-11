---
title: tipo de recurso governanceSubject
description: Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).
localization_priority: Normal
ms.openlocfilehash: f3f8762c9136a3ae92269f6c06f52000fb73f710
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832595"
---
# <a name="governancesubject-resource-type"></a>tipo de recurso governanceSubject

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).


## <a name="properties"></a>Propiedades
| Propiedad  | Tipo       |Descripción|
|:----------|:----------|:----------|
|id         |Cadena     | El identificador del tema.|
|type       |Cadena     |El tipo de objeto. El valor puede ser ``User``, ``Group``, y ``ServicePrincipal``.|
|displayName|Cadena     |El nombre para mostrar del asunto.|
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
