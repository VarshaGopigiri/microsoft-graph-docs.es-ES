---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: FolderView
localization_priority: Normal
ms.openlocfilehash: 717dd93d82f109926cabf0168e4e176d7c68cd35
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861540"
---
# <a name="folderview-resource-type"></a>Tipo de recurso FolderView

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **FolderView** proporciona o establece recomendaciones sobre la experiencia de usuario de una carpeta.

Está disponible desde la propiedad [folder][folder-facet] de los recursos [driveItem][item-resource].

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.folderView" } -->

```json
{
  "sortBy": "default | name | type | size | takenOrCreatedDateTime | lastModifiedDateTime | sequence",
  "sortDescending": "ascending | descending",
  "viewType": "default | icons | details | thumbnails"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad         | Tipo   | Descripción
|:----------------------|:-------|:--------------------------------------------
| **sortBy**            | string | El método mediante el que se ordena la carpeta.
| **sortOrder**         | string | Si es True, indica que los elementos deben ordenarse en orden descendente. De otro modo, los elementos deben ordenarse en orden ascendente.
| **viewType**          | string | El tipo de vista que se debe usar para representar la carpeta.

Puede usar la propiedad _sortBy_ para controlar el criterio de ordenación de los elementos en aplicaciones que respetan la faceta **viewType**.

### <a name="sortby-values"></a>Valores sortBy

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


### <a name="sortorder-values"></a>Valores sortOrder

Los siguientes valores se definen para la propiedad **sortOrder**.

| Valor        | Descripción
| ------------ | --------------------------------------------------------------
| `ascending`  | Los elementos deben organizarse en orden ascendente.
| `descending` | Los elementos deben organizarse en orden descendente.


### <a name="viewtype-values"></a>Valores viewType

Los siguientes valores se definen para la propiedad **viewType**.

| Valor        | Descripción
| ------------ | --------------------------------------------------------------
| `default`    | El tipo de vista predeterminado para la aplicación.
| `icons`      | Una vista que usa iconos para representar driveItems.
| `details`    | Una vista con varias columnas que proporcionan detalles adicionales sobre cada elemento.
| `thumbnails` | Una vista que usa miniaturas más grandes de driveItems para representar los elementos.


[item-resource]: driveitem.md
[folder-facet]: folder.md

<!-- uuid: f9e446fd-190b-4692-a605-bb60e78f1f19
2017-05-03 02:34:40 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "folderView resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
