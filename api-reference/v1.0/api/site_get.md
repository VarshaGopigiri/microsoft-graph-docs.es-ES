---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un sitio de SharePoint
ms.openlocfilehash: f3153845a0ce117c5442b5e66d1e96a388ac6720
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23264066"
---
# <a name="get-a-site-resource"></a>Obtener un recurso site

Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.

[site]: ../resources/site.md

Un recurso **site** se resuelve con un identificador único compuesto de los siguientes valores:

* Nombre de host de la colección de sitios (contoso.sharepoint.com)
* Identificador único (GUID) de la colección de sitios
* Identificador único (GUID) del sitio

También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz de un destino especificado de la manera siguiente:

* `/sites/root`: El sitio raíz del inquilino.
* `/groups/{group-id}/sites/root`: Sitio del grupo.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Sites.Read.All, Sites.ReadWrite.All |

## <a name="get-the-tenants-root-site"></a>Obtener el sitio raíz del inquilino

Para obtener acceso al sitio de SharePoint de raíz dentro de un inquilino:

<!-- { "blockType": "ignored" } -->

```http
GET /sites/root
GET /sites/contoso.sharepoint.com
```

## <a name="access-a-site-by-server-relative-url"></a>Obtener acceso a un sitio mediante la dirección URL relativa al servidor

Si tiene la dirección URL relativa al servidor de un recurso **site**, puede construir una solicitud de la manera siguiente:

```http
GET /sites/{hostname}:/{server-relative-path}
```

## <a name="access-a-group-team-site"></a>Obtener acceso a un sitio de grupo

Para obtener acceso al sitio de grupo de un grupo:

```http
GET /groups/{group-id}/sites/root
```

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

<!-- { "blockType": "request", "name": "get-site", "scopes": "sites.read.all" } -->

```http
GET /sites/{site-id}
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "contoso.sharepoint.com,2C712604-1370-44E7-A1F5-426573FDA80A,2D2244C3-251A-49EA-93A8-39E1C3A060FE",
  "displayName": "OneDrive Team Site",
  "name": "1drvteam",
  "createdDateTime": "2017-05-09T20:56:00Z",
  "lastModifiedDateTime": "2017-05-09T20:56:01Z",
  "webUrl": "https://contoso.sharepoint.com/teams/1drvteam"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites/Get by ID"
} -->
