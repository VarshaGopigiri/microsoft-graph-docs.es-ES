---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListItem
ms.openlocfilehash: eabb88eb6ad2eee7a032b2486555aa26c557ba1a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="listitem-resource"></a>Recurso ListItem

Este recurso representa un elemento en una **[lista][]** de SharePoint.
Los valores de columna de la lista están disponibles a través del diccionario `fieldValueSet`.

## <a name="tasks-on-a-listitem"></a>Tareas en un recurso listItem

Las tareas siguientes están disponibles para los recursos **listItem**.
Todos los ejemplos siguientes son relativos a una **[lista][]**, por ejemplo: `https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}`.

| Tarea común                    | Método HTTP
|:-------------------------------|:------------------------
| [Obtener][]                        | GET /items/{item-id}
| [Obtener valores de columna][Obtener]       | GET /items/{item-id}?expand=fields
| [Crear][]                     | POST /items
| [Eliminar][]                     | DELETE /items/{item-id}
| [Actualizar][]                     | PATCH /items/{item-id}
| [Actualizar valores de columna][Actualizar] | PATCH /items/{item-id}/fields

[Obtener]: ../api/listItem_get.md
[Crear]: ../api/listItem_create.md
[Eliminar]: ../api/listItem_delete.md
[Actualizar]: ../api/listItem_update.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **listItem**.

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.listItem",
       "keyProperty": "id" } -->

```json
{
  "contentType": { "@odata.type": "microsoft.graph.contentType" },
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },

  /* relationships */
  "driveItem": { "@odata.type": "microsoft.graph.driveItem" },

  /* inherited from baseItem */
  "id": "string",
  "name": "name of resource",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "description": "description of resource",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

El recurso **listItem** tiene las siguientes propiedades.

| Nombre de propiedad | Tipo                | Descripción
|:--------------|:--------------------|:-------------------------------
| contentType   | [contentTypeInfo][] | El tipo de contenido de este elemento de lista
| fields        | [fieldValueSet][]   | Los valores de las columnas establecidos en este elemento de lista.

Las siguientes propiedades se heredan de **[baseItem][]**.

| Nombre de propiedad        | Tipo             | Descripción
|:---------------------|:-----------------|:-----------------------------------
| id                   | string           | El identificador único del elemento. Solo lectura.
| name                 | string           | Nombre o título del elemento.
| createdBy            | [identitySet][]  | Identidad del creador de este elemento. Solo lectura.
| createdDateTime      | DateTimeOffset   | La fecha y la hora de creación del elemento. Solo lectura.
| descripción          | string           | Texto descriptivo del elemento.
| lastModifiedBy       | [identitySet][]  | Identidad del usuario que modificó por última vez este elemento. Solo lectura.
| lastModifiedDateTime | DateTimeOffset   | Fecha y hora de la última modificación del elemento. Solo lectura.
| webUrl               | string (url)     | Dirección URL que muestra el elemento en el explorador. Solo lectura.

## <a name="relationships"></a>Relaciones

 El recurso **listItem** tiene las siguientes relaciones con otros recursos.

| Nombre de la relación | Tipo                        | Descripción
|:------------------|:----------------------------|:-------------------------------
| driveItem         | [driveItem][]               | Para bibliotecas de documentos, la relación **driveItem** expone el recurso listItem como un recurso **[driveItem][]**

[baseItem]: baseItem.md
[contentTypeInfo]: contentTypeInfo.md
[driveItem]: driveItem.md
[fieldValueSet]: fieldValueSet.md
[identitySet]: identitySet.md
[list]: list.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ListItem",
  "tocBookmarks": {
    "ListItem": "#"
  }
} -->
