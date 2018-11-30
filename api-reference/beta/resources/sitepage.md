---
author: rahmit
ms.author: rahmit
ms.date: 03/15/2018
title: SitePage
ms.openlocfilehash: 65cfe61dadd1708abffe2d01abbbb15f40d158ef
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088804"
---
# <a name="sitepage-resource"></a>recursos de sitePage

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Este recurso representa una página en la [lista][]de SitePages.
Contiene una colección de [webPart][], diseño y el título.

## <a name="tasks-on-a-page"></a>Tareas de una página

Las siguientes tareas están disponibles para los recursos de **sitePage** .
Todos los ejemplos siguientes son con respecto a un [sitio][], por ejemplo: `https://graph.microsoft.com/{api-version}/sites/{site-id}`.

| Tarea común                     | Método HTTP
|:--------------------------------|:------------------------------
| [Enumerar páginas][]                  | OBTENER /pages
| [Obtener página][]                    | OBTENER /pages/ {página-id}
| [Create][]                      | POST /pages
| [Delete][]                      | ELIMINAR /pages/ {página-id}
| [Publish][]                     | REGISTRAR /pages/ {página-id} / publicar

[Enumerar páginas]: ../api/sitepage-list.md
[Obtener página]: ../api/sitepage-get.md
[Create]: ../api/sitepage-create.md
[Delete]: ../api/sitepage-delete.md
[Publish]: ../api/sitepage-publish.md

## <a name="json-representation"></a>Representación JSON

Aquí es una representación JSON de un recurso de **sitePage** .

<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.sitePage"
}-->

```json
{
  "contentType": { "@odata.type": "microsoft.graph.contentTypeInfo" },

  /* page content */
  "title": "string",
  "pageLayout": "Article",
  "webParts": [{ "@odata.type": "microsoft.graph.sitePageWebParts" }],

  /* authoring metadata */
  "publishingState": { "@odata.type": "microsoft.graph.publicationFacet" },

  /* inherited from baseItem */
  "id": "string",
  "name": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "datetime",
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

El recurso **sitePage** tiene las siguientes propiedades.

| Nombre de propiedad    | Tipo                         | Descripción
|:-----------------|:-----------------------------|:---------------------------
| contentType      | [contentTypeInfo][]          | El tipo de contenido de la página.

## <a name="page-content"></a>Contenido de la página

El recurso **sitePage** tiene los siguientes campos de contenido.

| Nombre de propiedad      | Tipo                       | Descripción
|:-------------------|:---------------------------|:---------------------------
| title              | string                     | El título de la página.
| pageLayout         | string                     | El nombre del diseño de página de la página.
| elementos Web           | [elemento Web][]                | Los elementos web en la página.

## <a name="authoring-metadata"></a>Creación de metadatos

El recurso **sitePage** tiene los siguientes metadatos relacionados con la creación. La propiedad publishingState reflejará el estado desprotegido like o publicado de creación de páginas.

| Nombre de propiedad          | Tipo                   | Descripción
|:-----------------------|:-----------------------|:---------------------------
| publishingState        | [publicationFacet][]   | El estado de publicación y la versión MM.mm de la página.

Las siguientes propiedades se heredan de **[baseItem][]**.

| Nombre de propiedad        | Tipo              | Descripción
|:---------------------|:------------------|:----------------------------------
| id                   | string            | El identificador único del elemento. Solo lectura.
| name                 | string            | Nombre o título del elemento.
| createdBy            | [identitySet][]   | Identidad del creador de este elemento. Solo lectura.
| eTag                 | string            | ETag para el elemento. Solo lectura.
| lastModifiedBy       | [identitySet][]   | Identidad del usuario que modificó por última vez este elemento. Solo lectura.
| lastModifiedDateTime | DateTimeOffset    | Fecha y hora de la última modificación del elemento. Solo lectura.
| parentReference      | [itemReference][] | Fecha y hora de la última modificación del elemento. Solo lectura.
| webUrl               | string (url)      | Dirección URL que muestra el elemento en el explorador. Solo lectura.

## <a name="relationships"></a>Relaciones

El recurso **sitePage** no tiene relaciones con otros recursos.

[baseItem]: baseitem.md
[contentTypeInfo]: contenttypeinfo.md
[columnDefinition]: columndefinition.md
[identitySet]: identityset.md
[itemReference]: itemreference.md
[list]: list.md
[listInfo]: listinfo.md
[listItem]: listitem.md
[publicationFacet]: publicationfacet.md
[site]: site.md
[elemento Web]: webpart.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/Page",
  "tocBookmarks": {
    "Page": "#"
  }
} -->

<!--
TODO:
* Define {page-id}
* Update examples
    * Be consistent with other URLs in the documentation.
    * Try to use the same site, library, etc.
    * Add the URL to the underlying list item resource in the API
* PATCH for list item patches /item/{item-id}/fields.
-->
