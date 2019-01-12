---
title: tipo de recurso educationAssignmentGrade
description: " Sin embargo, todos los tipos de clasificación (puntos, determinantes etc.) son subclases de este"
localization_priority: Normal
author: dipakboyed
ms.prod: education
ms.openlocfilehash: ecdd92c84399ee17d2808301d997830725fb5642
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982361"
---
# <a name="educationassignmentgrade-resource-type"></a>tipo de recurso educationAssignmentGrade

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el objeto de **calificación** en una presentación. Esto es un tipo abstracto que nunca se crearán instancias; Sin embargo, todos los tipos de clasificación (puntos, determinantes etc.) son subclases de este tipo de recurso. Este objeto también realiza un seguimiento de quién va a realizar la clasificación. Esta opción se usa la propiedad **submission.grade** .


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|gradedBy|[identitySet](identityset.md)| Usuario que hizo la clasificación. |
|gradedDateTime|DateTimeOffset| Momento en el tiempo cuando se aplicó la calificación a este objeto de envío. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentGrade"
}-->

```json
{
  "gradedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "gradedDateTime": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentGrade resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
