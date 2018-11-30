---
title: Tipo de recurso directoryObject
description: Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.
ms.openlocfilehash: 0981584bb86b71d06e29de4efc379c84bacac51d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032304"
---
# <a name="directoryobject-resource-type"></a>Tipo de recurso directoryObject

Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get directoryObject](../api/directoryobject-get.md) | [directoryObject](directoryobject.md) |Lee las propiedades de un objeto directory.|
|[Delete directoryObject](../api/directoryobject-delete.md) | None |Elimina un objeto directory. |
|[checkMemberGroups](../api/directoryobject-checkmembergroups.md)|Colección string|Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.|
|[getMemberGroups](../api/directoryobject-getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.|
|[getMemberObjects](../api/directoryobject-getmemberobjects.md)|Colección string| Devuelve todos los grupos y roles de directorio de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva. |
|[getByIds](../api/directoryobject-getbyids.md) | Colección [directoryObject](directoryobject.md) | Obtenga un conjunto de objetos de directorio basados en un conjunto de identificadores proporcionados. |

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|id|String|Guid que es el identificador único para el objeto; por ejemplo, 12345678-9abc-def0-1234-56789abcde. Clave. No admite valores NULL. Solo lectura.|

## <a name="relationships"></a>Relaciones

Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directoryObject",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
