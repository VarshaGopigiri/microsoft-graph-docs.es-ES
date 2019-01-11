---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Sitio
localization_priority: Priority
ms.openlocfilehash: fb91e9bada227f1a22cf862726ea0b6f658fe469
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871025"
---
# <a name="site-resource-type"></a>tipo de recurso de sitio

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **site** proporciona metadatos y relaciones para un sitio de SharePoint.

## <a name="methods"></a>Métodos

| Método                         | Ruta de acceso a REST
|:-------------------------------|:--------------------------------------------
| [Obtener sitio raíz][]              | GET /sites/root
| [Obtener sitio][]                   | GET /sites/{site-id}
| [Obtener sitio por su ruta de acceso][]           | GET /sites/{hostname}:/{site-path}
| [Obtener sitio para un grupo][]       | GET /groups/{group-id}/sites/root
| [Obtener análisis][]              | GET/Sites / {identificador de sitio} / análisis
| [Obtener las actividades por intervalo][] | GET/Sites / {identificador de sitio} / getActivitiesByInterval
| [Enumerar páginas][]                 | GET/Sites / {identificador de sitio} / páginas
| [Enumerar los sitios raíz][]            | / Sites GET? filtro = raíz ne null & select = siteCollection, webUrl
| [Buscar sitios][]           | GET /sites?search={query}

[Obtener sitio]: ../api/site-get.md
[Obtener sitio raíz]: ../api/site-get.md
[Obtener sitio por su ruta de acceso]: ../api/site-getbypath.md
[Obtener sitio para un grupo]: ../api/site-get.md
[Obtener análisis]: ../api/itemanalytics-get.md
[Obtener las actividades por intervalo]: ../api/itemactivity-getbyinterval.md
[Enumerar páginas]: ../api/sitepage-list.md
[Enumerar los sitios raíz]: ../api/site-list.md
[Buscar sitios]: ../api/site-search.md


## <a name="properties"></a>Propiedades

| Nombre de la propiedad            | Tipo               | Descripción
|:-------------------------|:-------------------|:-----------------------------
| **id**                   | string             | El identificador único del elemento. Solo lectura.
| **createdDateTime**      | DateTimeOffset     | La fecha y la hora de creación del elemento. Solo lectura.
| **description**          | string             | Texto descriptivo del sitio.
| **eTag**                 | string             | ETag para el elemento. Solo lectura.                                                                  |
| **displayName**          | string             | El título completo del sitio. Solo lectura.
| **lastModifiedDateTime** | DateTimeOffset     | Fecha y hora de la última modificación del elemento. Solo lectura.
| **name**                 | string             | Nombre o título del elemento.
| **root**                 | [root][]           | Si está presente, indica que se trata del sitio raíz de la colección de sitios. Solo lectura.
| **sharepointIds**        | [sharepointIds][]  | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.
| **siteCollection**       | [siteCollection][] | Proporciona detalles sobre la colección de sitios del sitio. Solo disponible en el sitio raíz. Solo lectura.
| **webUrl**               | string (url)       | Dirección URL que muestra el elemento en el explorador. Solo lectura.

## <a name="relationships"></a>Relaciones

| Nombre de la relación | Tipo                             | Description
|:------------------|:---------------------------------|:----------------------
| **análisis**     | recursos de [itemAnalytics][]       | Análisis acerca de las actividades de vista que tuvieron lugar en este sitio.
| **columns**       | Collection([columnDefinition][]) | La colección de definiciones de columna reutilizables en listas en este sitio.
| **contentTypes**  | Collection([contentType][])      | La colección de tipos de contenido definidos para este sitio.
| **drive**         | [drive][]                        | La unidad predeterminada (biblioteca de documentos) para este sitio.
| **drives**        | Collection([drive][])            | La colección de unidades (bibliotecas de documentos) de este sitio.
| **items**         | Collection([baseItem][])         | Se utiliza para resolver cualquier elemento contenido en este sitio. Esta colección no se puede enumerar.
| **lists**         | Collection([list][])             | La colección de listas en este sitio.
| **páginas**         | Colección ([sitePage][])         | La colección de páginas en la lista SitePages en este sitio.
| **sites**         | Collection([site][])             | La colección de subsitios de este sitio.

[columnDefinition]: columndefinition.md
[baseItem]: baseitem.md
[contentType]: contenttype.md
[drive]: drive.md
[identitySet]: identityset.md
[itemAnalytics]: itemanalytics.md
[lista]: list.md
[sitePage]: sitepage.md
[root]: root.md
[site]: site.md
[sharepointIds]: sharepointids.md
[siteCollection]: sitecollection.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **site**.

El recurso **site** deriva de [**baseItem**](baseitem.md) y hereda sus propiedades.

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "root",
    "sharepointIds",
    "siteCollection",
    "drive",
    "drives",
    "sites"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.site"
}-->

```json
{
  "id": "string",
  "root": { "@odata.type": "microsoft.graph.root" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "siteCollection": {"@odata.type": "microsoft.graph.siteCollection"},
  "displayName": "string",

  /* relationships */
  "analytics": { "@odata.type": "microsoft.graph.itemAnalytics" },
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "drives": [ { "@odata.type": "microsoft.graph.drive" }],
  "items": [ { "@odata.type": "microsoft.graph.baseItem" }],
  "lists": [ { "@odata.type": "microsoft.graph.list" }],
  "sites": [ { "@odata.type": "microsoft.graph.site"} ],
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],

  /* inherited from baseItem */
  "name": "string",
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedDateTime": "datetime",
  "webUrl": "url"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites",
  "tocBookmarks": { "Resources/Site": "#" }
} -->
