---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Lista
ms.openlocfilehash: ba0c01ce1887a32bd8b671cf511104e9128b5efb
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="list-resource"></a>Recurso de lista

El recurso **list** representa una lista en un [sitio][].
Este recurso contiene las propiedades de nivel superior de la lista, incluidas las definiciones de plantilla y campo.

## <a name="tasks-on-a-list"></a>Tareas en una lista

Las tareas siguientes están disponibles para los recursos list.
**Nota**: Esta versión beta solo permite navegar por listas, no permite crearlas ni actualizarlas.
En cambio, puede crear o actualizar [elementos de lista][listItem].

Todos los ejemplos siguientes son relativos a un sitio, por ejemplo: `https://graph.microsoft.com/beta/sites/{site-id}`.

| Tarea común               | Método HTTP
|:--------------------------|:------------------------------
| [Obtener lista][]              | GET /lists/{list-id}
| [Enumerar elementos de lista][]  | GET /lists/{list-id}/items
| [Actualizar elemento de lista][]      | PATCH /lists/{list-id}/items/{item-id}
| [Eliminar elemento de lista][]      | DELETE /lists/{list-id}/items/{item-id}
| [Crear elemento de lista][]      | POST /lists/{list-id}

[Obtener lista]: ../api/list_get.md
[Enumerar elementos de lista]: ../api/listitem_list.md
[Actualizar elemento de lista]: ../api/listItem_update.md
[Eliminar elemento de lista]: ../api/listItem_delete.md
[Crear elemento de lista]: ../api/listItem_create.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **list**.

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.list",
       "keyProperty": "id", 
       "optionalProperties": [ "items", "drive"] } -->

```json
{
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "displayName": "title of list",
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "items": [ { "@odata.type": "microsoft.graph.listItem" } ],
  "list": {
    "@odata.type": "microsoft.graph.listInfo",
    "hidden": false,
    "template": "documentLibrary | genericList | survey | links | announcements | contacts ..."
  },
  "system": false,

  /* inherited from baseItem */
  "id": "string",
  "name": "name of list",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "description": "description of list",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "webUrl": "url to visit the list in a browser"
}
```

## <a name="properties"></a>Propiedades

El recurso **list** tiene las siguientes propiedades.

| Nombre de propiedad    | Tipo                             | Descripción
|:-----------------|:---------------------------------|:---------------------------
| **columns**      | Collection([columnDefinition][]) | La colección de definiciones de campo de esta lista.
| **contentTypes** | Collection([contentType][])      | La colección de tipos de contenido presentes en esta lista.
| **displayName**  | string                           | El título que se puede mostrar de la lista.
| **list**         | [listInfo][]                     | Proporciona detalles adicionales sobre la lista.
| **system**       | [systemFacet][]                  | Si está presente, indica que se trata de una lista administrada por el sistema. Solo lectura.

Las siguientes propiedades se heredan de **[baseItem][]**.

| Nombre de propiedad            | Tipo             | Descripción
|:-------------------------|:-----------------|:-------------------------------
| **id**                   | cadena           | El identificador único del elemento. Solo lectura.
| **name**                 | string           | Nombre del elemento.
| **createdBy**            | [identitySet][]  | Identidad del creador de este elemento. Solo lectura.
| **createdDateTime**      | DateTimeOffset   | La fecha y la hora de creación del elemento. Solo lectura.
| **description**          | string           | Texto descriptivo del elemento.
| **lastModifiedBy**       | [identitySet][]  | Identidad del usuario que modificó por última vez este elemento. Solo lectura.
| **lastModifiedDateTime** | DateTimeOffset   | Fecha y hora de la última modificación del elemento. Solo lectura.
| **webUrl**               | string (url)     | Dirección URL que muestra el elemento en el explorador. Solo lectura.

## <a name="relationships"></a>Relaciones

El recurso **list** tiene las siguientes relaciones con otros recursos.

| Nombre de la relación | Tipo                        | Descripción
|:------------------|:----------------------------|:------------------------------
| **drive**         | [drive][]                   | Solo está presente en bibliotecas de documentos. Permite el acceso a la lista como un recurso [drive][] con objetos [driveItems][driveItem].
| **items**         | Collection([listItem][])    | Todos los elementos que se incluyen en la lista.

[baseItem]: baseItem.md
[contentType]: contentType.md
[drive]: drive.md
[driveItem]: driveItem.md
[columnDefinition]: columnDefinition.md
[identitySet]: identitySet.md
[listInfo]: listInfo.md
[listItem]: listItem.md
[site]: site.md
[systemFacet]: systemFacet.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/Lists",
  "tocBookmarks": {
    "Lists": "#"
  }
} -->
