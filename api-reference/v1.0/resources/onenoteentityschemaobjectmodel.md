---
title: recursos de onenoteEntitySchemaObjectModel
description: Éste es un tipo base para las entidades de OneNote.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 168359bbdaa659db461aa33af96e402a4a81783d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978714"
---
# <a name="onenoteentityschemaobjectmodel-resource"></a>recursos de onenoteEntitySchemaObjectModel

Éste es un tipo base para las entidades de OneNote.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.onenoteEntityBaseModel",
  "optionalProperties": [
    "self"
  ],
  "@odata.type": "microsoft.graph.onenoteEntitySchemaObjectModel"
}-->

```json
{
  "createdDateTime": "String (timestamp)"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|

<!-- uuid: bfb567de-2a2a-4b81-bf47-a55626a0c166
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
