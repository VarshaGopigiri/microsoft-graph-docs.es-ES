---
title: Obtener objetos de directorio a partir de una lista de identificadores
description: Seleccione ' opción de consulta no está disponible para esta operación.
author: lleonard-msft
localization_priority: Priority
ms.openlocfilehash: b504fc69deecd6688f61c20c30e17133f80b1dc8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889652"
---
# <a name="get-directory-objects-from-a-list-of-ids"></a>Obtener objetos de directorio a partir de una lista de identificadores

Devuelve los objetos de directorio especificados en una lista de identificadores.  NOTA: Los objetos de directorio devueltos son los objetos completos que contienen **todas** sus propiedades. La opción de consulta `$select` no está disponible para esta operación.

Algunos usos comunes de esta función son:

* Resolver identificadores devueltos por funciones (que devuelven colecciones de identificadores) como [getMemberObjects](directoryobject-getmemberobjects.md) o [getMemberGroups](directoryobject-getmembergroups.md) a sus objetos del directorio de copia de seguridad.
* Resolver identificadores que conserva la aplicación en un almacén externo para sus objetos del directorio de copia de seguridad.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.Read.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Directory.Read.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /directoryObjects/getByIds
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |
| Content-Type  | string | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro   | Tipo |Descripción|
|:---------------|:--------|:----------|
|ids|Colección string| Una colección de identificadores para devolverles objetos. Se pueden especificar hasta 1000 identificadores. |
|types|Colección string| Una colección de tipos de recursos que especifica el conjunto de colecciones de recursos para buscar. Si no se especifica, el valor predeterminado es [directoryObject](../resources/directoryobject.md), que contiene todos los tipos de recursos definidos en el directorio. Cualquier objeto que se deriva de `directoryObject` pueden especificarse en la colección; Por ejemplo: [usuario](../resources/user.md), [grupo](../resources/group.md), [dispositivo](../resources/device.md)y así sucesivamente. Los valores no distinguen mayúsculas de minúsculas.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "directoryobject_getById"
}-->

```http
POST https://graph.microsoft.com/v1.0/directoryObjects/getByIds
Content-type: application/json

{
    "ids":["84b80893874940a3-97b7-68513b600544","5d6059b6368d-45f8-91e18e07d485f1d0"],
    "types":["user"]
}
```

##### <a name="response"></a>Respuesta

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#directoryObjects",
    "value": [
      {
        "@odata.type": "#microsoft.graph.user",
        "id": "84b80893-8749-40a3-97b7-68513b600544",
        "accountEnabled": true,
        "displayName": "Trevor Jones"
      },
      {
        "@odata.type": "#microsoft.graph.user",
        "id": "84b80893-8749-40a3-97b7-68513b600544",
        "accountEnabled": true,
        "displayName": "Billy Smith"
      }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: getById",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
