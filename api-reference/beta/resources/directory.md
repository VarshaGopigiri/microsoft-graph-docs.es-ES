---
title: Tipo de recurso directory (elementos eliminados)
description: . Los elementos eliminados seguirán estando disponible para su restauración durante 30 días. Después de 30 días, los elementos se eliminan permanentemente.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 2593603afa145d30b5e26a240bb5cd471eab9942
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966555"
---
# <a name="directory-resource-type-deleted-items"></a>Tipo de recurso directory (elementos eliminados)

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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

## <a name="properties"></a>Propiedades
| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|id|String| Identificador único del objeto; por ejemplo, 12345678-9abc-def0-1234-56789abcde. Clave. No admite valores NULL. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|deleteditems|Colección [directoryObject](directoryobject.md)| Elementos eliminados recientemente Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
  "id": "String (identifier)"
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
