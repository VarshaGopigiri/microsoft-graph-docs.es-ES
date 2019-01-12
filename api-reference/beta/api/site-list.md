---
title: Enumerar sitios
description: El [de] [sitios] disponibles en una organización que coinciden con los criterios de filtro proporcionado y las opciones de consulta de la lista.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 05c3480181126d528657d0efacde97051a178bfd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939570"
---
# <a name="enumerate-sites"></a>Enumerar sitios

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Lista de los [sitios][] disponibles en una organización que coinciden con los criterios de filtro proporcionado y las opciones de consulta.

Actualmente se admiten las siguientes opciones de consulta:

| Instrucción de filtro             | Instrucción SELECT        | Descripción
|:-----------------------------|:------------------------|:--------------------
|`siteCollection/root ne null` | `siteCollection,webUrl` | Se enumeran todas las colecciones de sitios de nivel raíz de la organización. Es útil para descubrir el sitio principal para cada zona geográfica.

Además, puede usar una consulta de **[búsqueda][]** en la colección '/ sites' para encontrar los sitios que coincidan con las palabras clave al indicar.

[búsqueda]: site-search.md
[sites]: ../resources/site.md

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)
|:--------------------------------------|:-------------------------------------
|Delegado (cuenta profesional o educativa)     | Sites.Read.All, Sites.ReadWrite.All
|Delegado (cuenta personal de Microsoft) | No admitida.
|Aplicación                            | Sites.Read.All, Sites.ReadWrite.All

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET https://graph.microsoft.com/beta/sites?filter=siteCollection/root ne null
```

## <a name="example"></a>Ejemplo

#### <a name="request"></a>Solicitud

<!-- { "blockType": "request", "name": "list-sites" } -->

```http
GET https://graph.microsoft.com/beta/sites?select=siteCollection,webUrl&filter=siteCollection/root%20ne%20null
```

#### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "isCollection": true, "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740",
      "name": "Contoso USA",
      "root": { },
      "siteCollection": {
        "hostname": "contoso.sharepoint.com",
        "dataLocationCode": "NAM",
        "root": { }
      },
      "webUrl": "https://contoso.sharepoint.com"
    },
    {
      "id": "contoso-jpn.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851",
      "name": "Contoso Japan",
      "root": { },
      "siteCollection": {
        "hostname": "contoso-jp.sharepoint.com",
        "dataLocationCode": "JPN",
        "root": { }
      },
      "webUrl": "https://contoso-jp.sharepoint.com"
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Site/List sites"
} -->
