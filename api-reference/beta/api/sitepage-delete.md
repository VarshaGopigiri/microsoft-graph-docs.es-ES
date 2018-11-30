---
author: rahmit
ms.author: rahmit
ms.date: 05/07/2018
title: Eliminar una página de un sitio de SharePoint
ms.openlocfilehash: c537acec2e205ffd556a35789f75be95e2b94017
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085064"
---
# <a name="delete-page-from-the-site-pages-list-of-a-site"></a>Eliminar la página de la lista de las páginas del sitio de un sitio

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Quita un [sitePage][] de las páginas de sitio [lista][] en un [sitio][].

[sitePage]: ../resources/sitepage.md
[list]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

>**Nota:** Para eliminar un elemento, el usuario debe disponer de acceso de escritura de aplicación en el elemento que se va a eliminar.

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
DELETE /sites/{site-id}/pages/{page-id}
```

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre       | Valor | Descripción
|:-----------|:------|:--------------------------------------------------------
| _if-match_ | etag  | Si se incluye este encabezado de la solicitud y la ETag proporcionada no coincide con la etiqueta actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se eliminará.

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud con este método.
<!-- TODO: should we provide a URL to recover/undelete the file, if one exists? -->

## <a name="response"></a>Respuesta

Si tiene éxito, esta llamada devuelve una `204 No Content` respuesta para indicar que el recurso se eliminó y no había nada para devolver.

## <a name="example"></a>Ejemplo

<!-- { "blockType": "request", "name": "delete-page", "scopes": "files.readwrite sites.readwrite.all" } -->

##### <a name="request"></a>Solicitud

```http
DELETE /sites/{site-id}/pages/{page-id}
```
##### <a name="response"></a>Respuesta

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Delete a page in the SitePages list in a site.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Pages/Delete"
} -->
