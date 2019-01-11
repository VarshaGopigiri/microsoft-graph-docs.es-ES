---
title: Tipo de recurso plannerExternalReference
description: El recurso **plannerExternalReference** representa los metadatos de una referencia (los datos adjuntos como archivo, la dirección URL). Es el valor de pares de valor de la propiedad en el objeto externalReferences.
localization_priority: Normal
ms.openlocfilehash: 696cc61b17776382aa0963d2d6d92f558f033bf1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821311"
---
# <a name="plannerexternalreference-resource-type"></a>Tipo de recurso plannerExternalReference

El recurso **plannerExternalReference** representa los metadatos de una referencia (datos adjuntos como archivo, URL, etc.). Es el valor de los pares propiedad-valor del objeto [externalReferences](plannerexternalreferences.md).



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|alias|Cadena|Nombre de alias para describir la referencia.|
|lastModifiedBy|[identitySet](identityset.md)|Solo lectura. Id. del usuario que lo modificó por última vez.|
|lastModifiedDateTime|DateTimeOffset|Solo lectura. Fecha y hora en que se modificó por última vez. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|previewPriority|Cadena|Se usa para establecer el orden de prioridad relativo en el que aparecerá la referencia como una vista previa de la tarea.|
|tipo|Cadena|Se usa para describir el tipo de la referencia. Los tipos son `PowerPoint`, `Word`, `Excel` y `Other`.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerExternalReference"
}-->

```json
{
  "alias": "String",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "previewPriority": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerExternalReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
