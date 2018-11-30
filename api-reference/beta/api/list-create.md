---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Crear una lista de SharePoint
ms.openlocfilehash: a1e247722e9e8874a78a1951619e08bff9bd36e8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090527"
---
# <a name="create-a-new-list"></a>Crear una lista

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Cree una [list][] en un [site][].

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|            Tipo de permiso             | Permisos (de menos a más privilegiados) |
| :------------------------------------- | :------------------------------------------ |
| Delegado (cuenta profesional o educativa)     | Sites.Manage.All                            |
| Delegado (cuenta personal de Microsoft) | No admitida.                              |
| Aplicación                            | Sites.ReadWrite.All                         |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST https://graph.microsoft.com/beta/sites/{site-id}/lists
```

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione una representación JSON del recurso [list][] que quiere crear.

## <a name="example"></a>Ejemplo

Aquí se muestra un ejemplo de cómo crear una lista genérica.

<!-- { "blockType": "request", "name": "create-list", "scopes": "sites.readwrite.all" } -->

```http
POST /sites/{site-id}/lists
Content-Type: application/json

{
  "name": "Books",
  "columns": [
    {
      "name": "Author",
      "text": { }
    },
    {
      "name": "PageCount",
      "number": { }
    }
  ],
  "list": {
    "template": "genericList"
  }
}
```

**Nota**: Las columnas personalizadas son opcionales.

Además de las columnas especificadas aquí, se crean listas con columnas definidas en la **plantilla** de referencia.
Si la faceta **list** o la **plantilla** están sin especificar, el valor predeterminado de la lista es la plantilla `genericList`, que incluye una columna _Título_.

## <a name="response"></a>Respuesta

Si se realiza correctamente, este método devuelve un valor [list][] en el cuerpo de la respuesta de la lista creada.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.list", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "22e03ef3-6ef4-424d-a1d3-92a337807c30",
  "createdDateTime": "2017-04-30T01:21:00Z",
  "createdBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  },
  "lastModifiedDateTime": "2016-08-30T08:26:00Z",
  "lastModifiedBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  }
}
```

**Nota:** El objeto Response se trunca para obtener una mayor claridad.
Se devolverán las propiedades predeterminadas de la llamada actual.

[list]: ../resources/list.md
[site]: ../resources/site.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a new SharePoint list.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "List/Create"
} -->
