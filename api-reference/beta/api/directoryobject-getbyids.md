---
title: Obtener objetos de directorio a partir de una lista de identificadores
description: Seleccione ' opción de consulta no está disponible para esta operación.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 4c63ea85113ec54dec8e5d818c3add1005aebb19
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888063"
---
# <a name="get-directory-objects-from-a-list-of-ids"></a>Obtener objetos de directorio a partir de una lista de identificadores

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Devuelve los objetos de directorio especificados en una lista de identificadores.  NOTA: Los objetos de directorio devueltos son los objetos completos que contienen **todas** sus propiedades. La opción de consulta `$select` no está disponible para esta operación.

Algunos usos comunes de esta función son:

* Resolver identificadores devueltos por funciones (que devuelven colecciones de identificadores) como [getMemberObjects](/graph/api/directoryobject-getmemberobjects.md?view=graph-rest-beta) o [getMemberGroups](/graph/api/directoryobject-getmembergroups.md?view=graph-rest-beta) a sus objetos del directorio de copia de seguridad.
* Resolver identificadores que conserva la aplicación en un almacén externo para sus objetos del directorio de copia de seguridad.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.Read.All    |
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
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro   | Tipo |Descripción|
|:---------------|:--------|:----------|
|ids|Colección string| Una colección de identificadores para devolverles objetos. Se pueden especificar hasta 1000 identificadores. |
|types|Colección string| Una colección de tipos de recursos que especifica el conjunto de colecciones de recursos para buscar. Si no se especifica, el valor predeterminado es [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta), que contiene todos los tipos de recursos definidos en el directorio. Cualquier objeto que se deriva de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta) puede especificarse en la colección; Por ejemplo: [usuario](/graph/api/resources/user?view=graph-rest-beta), [grupo](/graph/api/resources/group?view=graph-rest-beta), [dispositivo](/graph/api/resources/device?view=graph-rest-beta)y así sucesivamente. Para buscar referencias a un socio de [Proveedor de soluciones de nube](https://partner.microsoft.com/en-us/cloud-solution-provider) organización especificar [directoryObjectPartnerReference](/graph/api/resources/directoryobjectpartnerreference?view=graph-rest-beta). Si no se especifica, el valor predeterminado es [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta), que contiene todos los tipos de recursos definidos en el directorio, excepto para las referencias a una organización asociada de [Proveedor de soluciones de nube](https://partner.microsoft.com/en-us/cloud-solution-provider) . Los valores no distinguen mayúsculas de minúsculas.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "directoryobject_getByIds"
}-->

```http
POST https://graph.microsoft.com/beta/directoryObjects/getByIds
Content-type: application/json

{
    "ids":["84b80893-8749-40a3-97b7-68513b600544","5d6059b6-368d-45f8-91e1-8e07d485f1d0"],
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
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#directoryObjects",
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
