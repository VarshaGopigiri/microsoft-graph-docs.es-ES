---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListItem
localization_priority: Normal
ms.openlocfilehash: b2e151937d5e8db633edeb5d521d6e0c875b6d78
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866090"
---
# <a name="listitem-resource"></a>Recurso ListItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Este recurso representa un elemento en una **[lista][]** de SharePoint.
Los valores de columna de la lista están disponibles a través del diccionario `fieldValueSet`.

## <a name="tasks-on-a-listitem"></a>Tareas en un recurso listItem

Las tareas siguientes están disponibles para los recursos **listItem**.
Todos los ejemplos siguientes son relativos a una **[lista][]**, por ejemplo: `https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}`.

| Tarea común                    | Método HTTP
|:-------------------------------|:------------------------
| [Obtener][]                        | GET /items/{item-id}
| [Obtener valores de columna][Obtener]       | GET /items/{item-id}?expand=fields
| [Obtener análisis][]              | GET /items/ {identificador de elemento} / análisis
| [Obtener las actividades por intervalo][] | GET /items/ {identificador de elemento} / getActivitiesByInterval
| [Crear][]                     | POST /items
| [Eliminar][]                     | DELETE /items/{item-id}
| [Actualizar][]                     | PATCH /items/{item-id}
| [Actualizar valores de columna][Actualizar] | PATCH /items/{item-id}/fields

[Obtener]: ../api/listitem-get.md
[Obtener análisis]: ../api/itemanalytics-get.md
[Obtener las actividades por intervalo]: ../api/itemactivity-getbyinterval.md
[Create]: ../api/listitem-create.md
[Delete]: ../api/listitem-delete.md
[Actualizar]: ../api/listitem-update.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **listItem**.

<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.listItem"
}-->

```json
{
  "contentType": { "@odata.type": "microsoft.graph.contentTypeInfo" },
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },

  /* relationships */
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "analytics": { "@odata.type": "microsoft.graph.itemAnalytics" },
  "driveItem": { "@odata.type": "microsoft.graph.driveItem" },
  "versions": [{"@odata.type": "microsoft.graph.listItemVersion"}],

  /* inherited from baseItem */
  "id": "string",
  "name": "name of resource",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "description": "description of resource",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "parentReference": { "@odata.type": "microsoft.graph.itemReference"},
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

El recurso **listItem** tiene las siguientes propiedades.

| Nombre de la propiedad | Tipo                | Descripción
|:--------------|:--------------------|:-------------------------------
| contentType   | [contentTypeInfo][] | El tipo de contenido de este elemento de lista

Las siguientes propiedades se heredan de **[baseItem][]**.

| Nombre de la propiedad        | Tipo              | Descripción
|:---------------------|:------------------|:----------------------------------
| id                   | string            | El identificador único del elemento. Solo lectura.
| name                 | string            | Nombre o título del elemento.
| createdBy            | [identitySet][]   | Identidad del creador de este elemento. Solo lectura.
| createdDateTime      | DateTimeOffset    | La fecha y la hora de creación del elemento. Solo lectura.
| descripción          | string            | Texto descriptivo del elemento.
| eTag                 | string            | ETag para el elemento. Solo lectura.                                                          |
| lastModifiedBy       | [identitySet][]   | Identidad del usuario que modificó por última vez este elemento. Solo lectura.
| lastModifiedDateTime | DateTimeOffset    | Fecha y hora de la última modificación del elemento. Solo lectura.
| parentReference      | [itemReference][] | Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.
| sharepointIds        | [sharepointIds][] | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.
| webUrl               | string (url)      | Dirección URL que muestra el elemento en el explorador. Solo lectura.

## <a name="relationships"></a>Relaciones

 El recurso **listItem** tiene las siguientes relaciones con otros recursos.

| Nombre de la relación | Tipo                           | Descripción
|:------------------|:-------------------------------|:-------------------------------
| activities        | Colección [itemActivity][]    | Lista de actividades recientes que tuvieron lugar en este elemento.
| análisis         | recursos de [itemAnalytics][]     | Análisis acerca de las actividades de vista que tuvieron lugar en este elemento.
| driveItem         | [driveItem][]                  | Para bibliotecas de documentos, la relación **driveItem** expone el recurso listItem como un recurso **[driveItem][]**
| fields            | [fieldValueSet][]              | Los valores de las columnas establecidos en este elemento de lista.
| versiones          | colección de [listItemVersion][] | La lista de las versiones anteriores del elemento de lista.

[baseItem]: baseitem.md
[contentTypeInfo]: contenttypeinfo.md
[driveItem]: driveitem.md
[fieldValueSet]: fieldvalueset.md
[identitySet]: identityset.md
[itemActivity]: itemactivity.md
[itemAnalytics]: itemanalytics.md
[itemReference]: itemreference.md
[lista]: list.md
[listItemVersion]: listitemversion.md
[sharepointIds]: sharepointids.md

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
