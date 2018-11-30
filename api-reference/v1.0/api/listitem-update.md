---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Actualizar un registro en una lista de SharePoint
ms.openlocfilehash: fdd43cebf83e802441552be5476659677e41e8e5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029684"
---
# <a name="update-an-item-in-a-list"></a>Actualizar un elemento en una lista

Actualice las propiedades de un recurso **[listItem][]**.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
```

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre       | Valor | Descripción
|:-----------|:------|:--------------------------------------------------------
| _if-match_ | etag  | Si se incluye el encabezado de la solicitud y la ETag proporcionada no coincide con la ETag actual del elemento, se devuelve una respuesta `412 Precondition Failed` y el elemento no se actualizará.


## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione una representación JSON de un recurso [fieldValueSet][] especificando los campos que quiere actualizar.

## <a name="example"></a>Ejemplo

Aquí tiene un ejemplo que actualiza los campos Color y Quantity (Cantidad) del elemento de lista con los nuevos valores.
Todos los demás valores de listItem quedan solos. 

<!-- { "blockType": "request", "name": "update-listitem", "scopes": "sites.readwrite.all" } -->

```json
PATCH https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}/items/{item-id}/fields
Content-Type: application/json

{
    "Color": "Fuchsia",
    "Quantity": 934
}
```

## <a name="response"></a>Respuesta

Si se realiza correctamente, este método devuelve un valor [fieldValueSet][] en el cuerpo de la respuesta del elemento de lista actualizado.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.fieldValueSet", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "Name": "Widget",
  "Color": "Fuchsia",
  "Quantity": 934
}
```

[fieldValueSet]: ../resources/fieldvalueset.md
[listItem]: ../resources/listitem.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Update"
} -->
