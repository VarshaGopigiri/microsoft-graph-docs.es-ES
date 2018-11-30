---
title: recursos de onenoteEntityHierarchyModel
description: Éste es un tipo base para las entidades de OneNote.
ms.openlocfilehash: 78c651e6d480d3c809c6ca432cd37cb7f9f97926
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032443"
---
# <a name="onenoteentityhierarchymodel-resource"></a>recursos de onenoteEntityHierarchyModel

Éste es un tipo base para las entidades de OneNote.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.onenoteEntitySchemaObjectModel",
  "optionalProperties": [
    "self"
  ],
  "@odata.type": "microsoft.graph.onenoteEntityHierarchyModel"
}-->

```json
{
  "displayName": "string",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)"
}

```
## <a name="properties"></a>Propiedades
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String|El nombre del bloc de notas.|
|createdBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|lastModifiedBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|

<!-- uuid: 8b1af557-1a7c-4432-86eb-94989c2d4b54
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->