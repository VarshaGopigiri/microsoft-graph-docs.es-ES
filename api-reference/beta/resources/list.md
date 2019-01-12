---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Lista
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 419f35226c09c1bde500994b6e023f764c54b3cc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953619"
---
# <a name="list-resource"></a>Recurso List

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
| [Obtener actividades recientes][] | GET /lists/{list-id}/activities

[Obtener lista]: ../api/list-get.md
[Enumerar elementos de lista]: ../api/listitem-list.md
[Actualizar elemento de lista]: ../api/listitem-update.md
[Eliminar elemento de lista]: ../api/listitem-delete.md
[Crear elemento de lista]: ../api/listitem-create.md
[Obtener actividades recientes]: ../api/activities-list.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **list**.

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.list",
       "keyProperty": "id", 
       "optionalProperties": [ "items", "drive"] } -->

```json
{
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
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

| Nombre de la propiedad    | Tipo                             | Descripción
|:-----------------|:---------------------------------|:---------------------------
| **columns**      | Collection([columnDefinition][]) | La colección de definiciones de campo de esta lista.
| **contentTypes** | Collection([contentType][])      | La colección de tipos de contenido presentes en esta lista.
| **displayName**  | string                           | El título que se puede mostrar de la lista.
| **list**         | [listInfo][]                     | Proporciona detalles adicionales sobre la lista.
| **system**       | [systemFacet][]                  | Si está presente, indica que se trata de una lista administrada por el sistema. Solo lectura.

Las siguientes propiedades se heredan de **[baseItem][]**.

| Nombre de la propiedad            | Tipo             | Descripción
|:-------------------------|:-----------------|:-------------------------------
| **id**                   | string           | El identificador único del elemento. Solo lectura.
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
| **activities**    | Colección [itemActivity][] | Las actividades recientes que tuvieron lugar en esta lista.
| **drive**         | [drive][]                   | Solo está presente en bibliotecas de documentos. Permite el acceso a la lista como un recurso [drive][] con objetos [driveItems][driveItem].
| **items**         | Collection([listItem][])    | Todos los elementos que se incluyen en la lista.

[baseItem]: baseitem.md
[contentType]: contenttype.md
[drive]: drive.md
[driveItem]: driveitem.md
[columnDefinition]: columndefinition.md
[identitySet]: identityset.md
[itemActivity]: itemactivity.md
[listInfo]: listinfo.md
[listItem]: listitem.md
[site]: site.md
[systemFacet]: systemfacet.md

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
