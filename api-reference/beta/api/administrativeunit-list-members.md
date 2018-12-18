---
title: Enumerar miembros
description: Utilice esta API para obtener los miembros de lista (de usuario y de grupo) en una unidad administrativa.
author: lleonard-msft
ms.openlocfilehash: d373c8353928d8e8d5d8b398aa09e62d457ba665
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311665"
---
# <a name="list-members"></a>Enumerar miembros

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Utilice esta API para obtener los miembros de lista (de usuario y de grupo) en una unidad administrativa.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Directory.Read.All, Directory.ReadWrite.All |

> Nota: Para obtener una lista de los miembros de una pertenencia oculta en una unidad administrativa, es necesario el permiso Member.Read.Hidden.

## <a name="http-request"></a>Solicitud HTTP

```http
GET /administrativeUnits/{id}/members
GET /administrativeUnits/{id}/members/$ref
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [usuario](../resources/user.md) o [grupo](../resources/group.md) en el cuerpo de la respuesta.  En su lugar, si coloca `$ref` al final de la solicitud, la respuesta contendrá una colección de `@odata.id` vínculos y direcciones URL a los miembros.

## <a name="examples"></a>Ejemplos
##### <a name="list-member-objects"></a>Objetos de lista de miembros
La solicitud siguiente enumeran a los miembros de la unidad administrativa, devuelve una colección de usuarios o grupos.

```http
GET https://graph.microsoft.com/beta/administrativeUnits/{id}/members
```

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
 
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "value":[
    {
      "@odata.type":"#microsoft.graph.user",
      "id":"492c5308-59fd-4740-9c83-4b3db07a6d70"
      "accountEnabled":true,
      "businessPhones":[],
      "companyName":null,
      "displayName":"Demo User"
    },
    {
      "@odata.type":"#microsoft.graph.group",
      "id":"07eaa5c7-c9b6-45cf-8ff7-3147d5122caa",
      "description":"This group is the best ever",
      "displayName":"Awesome group"
    }
  ]
}
```

##### <a name="list-member-references"></a>Referencias de miembro de lista
La siguiente solicitud mostrará una lista de las referencias de miembro de la unidad administrativa, devuelve una colección de `@odata.id` referencias a los miembros.
```
GET https://graph.microsoft.com/beta/administrativeUnits/{id}/members/$ref
```
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
 
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "value":[
    {
      "@odata.id": "https://graph.microsoft.com/beta/directoryObjects/492c5308-59fd-4740-9c83-4b3db07a6d70"
    },
    {
      "@odata.id": "https://graph.microsoft.com/beta/directoryObjects/07eaa5c7-c9b6-45cf-8ff7-3147d5122caa"
    }
  ]
}
```
