---
title: Trabajar con sitios de SharePoint en Microsoft Graph
description: 'La API de SharePoint en Microsoft Graph admite los siguientes escenarios principales:'
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: 9edab0f8e4207dac2a88943a0a2cd1cbe58b97e3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945737"
---
# <a name="working-with-sharepoint-sites-in-microsoft-graph"></a>Trabajar con sitios de SharePoint en Microsoft Graph

La API de SharePoint en Microsoft Graph admite los siguientes escenarios principales:

* Acceso a los **sitios**, las **listas** y las **unidades** (bibliotecas de documentos) de SharePoint
* Soporte de solo lectura de los recursos del **sitio** (sin capacidad para crear nuevos sitios)
* Compatibilidad de lectura y escritura para recursos **list**, **listItem** y **driveItem**
* Recursos de dirección por la ruta de acceso relativa, URL o id. de SharePoint

La API de SharePoint expone tres tipos principales de recursos:

* [Site](site.md) _(objeto de nivel superior)_
* [Lista](list.md)
* [ListItem](listitem.md)

A continuación se muestra un ejemplo de un recurso listItem.

```json
{
  "fields": {
    "Title": "Access card",
    "Employee": "Ryan Gregg",
    "EmployeeId": "10",
    "CardSerial": "01235492",
    "Alias": "RGregg",
    "ID": 1,
    "ContentType": "Item",
    "Modified": "2016-09-19T23:15:25-07:00",
    "Created": "2016-09-19T23:15:25-07:00"
  },
  "createdBy": {
    "user": {
      "id": "b757fdcb-0271-4807-b243-504139e4ba04",
      "displayName": "Ryan Gregg"
    }
  },
  "createdDateTime": "2016-09-20T06:15:25Z",
  "eTag": "48e941c3-9515-4c48-9760-c07c90c79d48,1",
  "id": "4",
  "lastModifiedBy": {
    "user": {
      "id": "b757fdcb-0271-4807-b243-504139e4ba04",
      "displayName": "Ryan Gregg"
    }
  },
  "lastModifiedDateTime": "2016-09-20T06:15:25Z",
}
```

Los recursos exponen los datos de tres maneras diferentes:

* _Propiedades_ (como **id** y **name**) exponen valores simples.
* _Facetas_ (como **fields** y **createdBy**) exponen valores complejos.
* _Referencias_ (como **items**) indican colecciones de otros recursos.

Puede ampliar las referencias en la dirección URL con el parámetro de consulta _expand_, por ejemplo, `?expand=fields`.
Puede solicitar propiedades y facetas específicas con el parámetro de consulta _select_, por ejemplo, `?select=id,name`.
De manera predeterminada, la mayoría de las propiedades y las facetas se devuelve mientras que todas las referencias se ocultan.
Por motivos de eficacia, recomendamos que especifique _select_ y _expand_ para que solo devuelvan los datos que le interesen.

## <a name="sharepoint-api-root-resources"></a>Recursos raíz de las API de SharePoint

Los ejemplos siguientes son relativos al `https://graph.microsoft.com/beta`.

| Ruta de acceso                                   | Descripción
|:---------------------------------------|:------------------------------------
| /sites/root                            | [Sitio][] predeterminado de la organización.
| /sites/{site-id}                       | Acceso a un [sitio][] específico por su id.
| /sites/{site-id}/drive                 | Acceso a la [unidad](drive.md) predeterminada (biblioteca de documentos) para este [sitio][].
| /sites/{site-id}/drives                | Enumerar las [unidades](drive.md) (bibliotecas de documentos) en el [sitio][].
| /sites/{site-id}/sites                 | Enumerar los sitios secundarios en [sitio][].
| /sites/{site-id}/lists                 | Enumerar las [listas](list.md) en el [sitio](site.md).
| /sites/{site-id}/lists/{list-id}/items | Enumerar los [listItems](listitem.md) en la [lista](list.md).
| /groups/{group-id}/sites/root          | Acceso a un [sitio][] de equipo de grupo.

Los sitios también pueden dirigirse a través de la ruta al utilizar el nombre de host de SharePoint, seguido de dos puntos y la ruta de acceso relativa al sitio. Opcionalmente, puede hacer la transición de vuelta mientras dirige el modelo de recursos al colocar otro signo de dos puntos al final.

| Ruta de acceso                                           | Descripción
|:-----------------------------------------------|:-----------------------------------
| /sites/contoso.sharepoint.com:/teams/hr        | El sitio asociadohttps://contoso.sharepoint.com/teams/hr
| /sites/contoso.sharepoint.com:/teams/hr:/drive | Acceso a la [unidad](drive.md) predeterminada para este sitio.

## <a name="note-for-existing-sharepoint-developers"></a>Nota para los desarrolladores de SharePoint existentes

La API de SharePoint de Microsoft Graph tiene algunas diferencias clave con las API de CSOM. El recurso del [sitio][] se asigna a `SPWeb`. El [sitio][] raíz (`SPWeb`) en un sitio de la colección tiene una faceta de [colecciónDeSitios](sitecollection.md), que contiene información acerca de `SPSite`. Debido a que los identificadores para los sitios solo son únicos dentro de su colección de sitios, el direccionamiento a un sitio a través del id. requiere proporcionar el identificador de la colección de sitios y el identificador del sitio.

```http
GET https://graph.microsoft.com/beta/sites/{hostname},{spsite-id},{spweb-id}/
```
Una dirección URL creada solo con el nombre de host apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.

```http
GET https://graph.microsoft.com/beta/sites/{hostname}
```

Una dirección URL creada solo con el nombre de host y el id. de siteCollection (`SPSite`) apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.

```http
GET https://graph.microsoft.com/beta/sites/{hostname},{spsite-id}
```

[site]: site.md
[list]: list.md
[drive]: drive.md
[siteCollection]: sitecollection.md

<!-- {
  "type": "#page.annotation",
  "description": "Getting started programming with the SharePoint API",
  "keywords": "getting started sharepoint rest api programming C# ios android rest http",
  "section": "documentation",
  "tocPath": "Getting Started",
  "tocIndex": -100
} -->
