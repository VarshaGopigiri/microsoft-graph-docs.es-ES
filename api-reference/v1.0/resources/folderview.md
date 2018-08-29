---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: FolderView
ms.openlocfilehash: e73846a18f8576af8fe3cf5949e8ca5c63891837
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23265158"
---
# <a name="folderview-resource-type"></a>Tipo de recurso FolderView

El recurso **FolderView** proporciona o establece recomendaciones sobre la experiencia de usuario de una carpeta.

Está disponible desde la propiedad [folder][folder-facet] de los recursos [driveItem][item-resource].

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.folderView" } -->

```json
{
  "sortBy": "default | name | type | size | takenOrCreatedDateTime | lastModifiedDateTime | sequence",
  "sortOrder": "ascending | descending",
  "viewType": "default | icons | details | thumbnails"
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad         | Tipo   | Descripción
|:----------------------|:-------|:--------------------------------------------
| **sortBy**            | cadena | El método mediante el que se ordena la carpeta.
| **sortOrder**         | cadena | Si es True, indica que los elementos deben ordenarse en orden descendente. De otro modo, los elementos deben ordenarse en orden ascendente.
| **viewType**          | cadena | El tipo de vista que se debe usar para representar la carpeta.

Puede usar la propiedad _sortBy_ para controlar el criterio de ordenación de los elementos en aplicaciones que respetan la faceta **viewType**.

### <a name="sortby-options"></a>Opciones de sortBy

Los siguientes valores se definen para la propiedad **sortBy**.

| Valor                    | Descripción
| ------------------------ | --------------------------------------------------
| `default`                | El criterio de ordenación predeterminado de la aplicación.
| `name`                   | Los elementos deben organizarse por la propiedad **name** de los elementos.
| `type`                   | Los elementos deben organizarse por el tipo de los elementos.
| `size`                   | Los elementos deben organizarse por la propiedad **size** de los elementos.
| `takenOrCreatedDateTime` | Los elementos deben organizarse por la propiedad **takenDateTime** de la faceta **photo**. Si no está disponible, debe usarse la propiedad **createdDateTime**.
| `lastModifiedDateTime`   | Los elementos deben organizarse por la propiedad **lastModifiedDateTime** de los elementos.
| `sequence`               | Los elementos siguen una secuencia personalizada especificada por el usuario.


### <a name="sortorder-options"></a>Opciones de sortOrder

Los siguientes valores se definen para la propiedad **sortOrder**.

| Valor        | Descripción
| ------------ | --------------------------------------------------------------
| `ascending`  | Los elementos deben organizarse en orden ascendente.
| `descending` | Los elementos deben organizarse en orden descendente.


### <a name="viewtype-options"></a>Opciones de viewType

Los siguientes valores se definen para la propiedad **viewType**.

| Valor        | Descripción
| ------------ | --------------------------------------------------------------
| `default`    | El tipo de vista predeterminado para la aplicación.
| `icons`      | Una vista que usa iconos para representar driveItems.
| `details`    | Una vista con varias columnas que proporcionan detalles adicionales sobre cada elemento.
| `thumbnails` | Una vista que usa miniaturas más grandes de driveItems para representar los elementos.


[item-resource]: driveitem.md
[folder-facet]: folder.md

<!-- {
  "type": "#page.annotation",
  "description": "The FolderView facet provides or sets recommendations on the user-experience of a folder.",
  "keywords": "view, folderview, sortby, sortorder, viewtype, coversourceid, folder",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/folderview.md:
      Found potential enums in resource example that weren't defined in a table:(default,icons,details,thumbnails) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/folderview.md:
      Found potential enums in resource example that weren't defined in a table:(default,name,type,size,takenOrCreatedDateTime,lastModifiedDateTime,sequence) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/folderview.md:
      Found potential enums in resource example that weren't defined in a table:(ascending,descending) are in resource, but () are in table"
  ],
  "tocPath": "Facets/FolderView"
} -->
