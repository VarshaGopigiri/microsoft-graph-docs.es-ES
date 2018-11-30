---
title: Tipo de recurso directory (elementos eliminados)
description: . Los elementos eliminados seguirán estando disponible para su restauración durante 30 días. Después de 30 días, los elementos se eliminan permanentemente.
ms.openlocfilehash: e83ace1a50998b6645e059fe0f63e3922497c1cd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031657"
---
# <a name="directory-resource-type-deleted-items"></a>Tipo de recurso directory (elementos eliminados)

Representa un elemento eliminado en el directorio. Cuando se elimina un elemento, se agrega al "contenedor" de elementos eliminados. Los elementos eliminados seguirán estando disponible para su restauración durante 30 días. Después de 30 días, los elementos se eliminan permanentemente.

Actualmente, la funcionalidad de elementos eliminados solo es compatible con los [grupos](group.md) y [usuarios](users.md) de Office 365.

## <a name="methods"></a>Métodos

| Método         | Tipo de valor devuelto | Descripción |
|:---------------|:------------|:------------|
|[Obtener elemento eliminado](../api/directory-deleteditems-get.md) | [directoryObject](directoryobject.md) | Obtiene las propiedades de un elemento eliminado. |
|[Restaurar elemento eliminado](../api/directory-deleteditems-restore.md) |[directoryObject](directoryobject.md)| Restaura un elemento eliminado recientemente. |
|[Enumerar elementos eliminados](../api/directory-deleteditems-list.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de elementos eliminados recientemente. |
|[Eliminar permanentemente un elemento](../api/directory-deleteditems-delete.md) | Ninguno | Elimina permanentemente un elemento. |
|[Lista de los elementos eliminados que pertenecen a un usuario](../api/directory-deleteditems-user-owned.md) | Colección [directoryObject](directoryobject.md) | Se enumeran los elementos de Active directory que pertenecen a un usuario. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|deletedItems|Colección [directoryObject](directoryobject.md)| Elementos eliminados recientemente Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
}
```

## <a name="example"></a>Ejemplo

<!--{"blockType": "request"}-->
```http
GET https://graph.microsoft.com/v1.0/directory
```

<!--{"blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.directory"}-->
```json
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directory resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->