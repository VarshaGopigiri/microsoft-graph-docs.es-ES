---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListInfo
ms.openlocfilehash: da8398bbb87111648ea561e1799e062ed46b0ee6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030160"
---
# <a name="listinfo-resource"></a>Recurso ListInfo

El tipo complejo **ListInfo** proporciona información adicional sobre un recurso [list][].

[list]: list.md

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.listInfo"
}-->

```json
{
  "contentTypesEnabled": false,
  "hidden": false,
  "template": "documentLibrary | genericList | tasks | survey | links | announcements | contacts | ..."
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad           | Tipo    | Descripción
|:------------------------|:--------|:------------------------------------------------
| **contentTypesEnabled** | Booleano | Si es `true`, indica que los tipos de contenido están habilitados para esta lista.
| **hidden**              | Booleano | Si es `true`, indica que la lista no es visible normalmente en la experiencia del usuario de SharePoint.
| **template**            | Cadena  | Un valor enumerado que representa la plantilla de lista base usada al crear la lista. Los valores posibles incluyen `documentLibrary`, `genericList`, `task`, `survey`, `announcements`, `contacts` y más.

### <a name="remarks"></a>Comentarios

Mientras que la mayoría de las listas creadas por usuarios tendrán uno de los valores mencionados anteriormente, también son posibles otros valores.
La aplicación debe estar preparada para controlar los valores que no figuran aquí.
Para los desarrolladores familiarizados con las API de OMSC de SharePoint, el valor `template` corresponde a la enumeración `SPListTemplateType`.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/listinfo.md:
      Found potential enums in resource example that weren't defined in a table:(documentLibrary,genericList,tasks,survey,links,announcements,contacts,...) are in resource, but () are in table"
  ],
  "tocPath": ""
}-->
