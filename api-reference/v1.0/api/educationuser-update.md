---
title: Actualizar propiedades de educationUser
description: Actualice las propiedades de un objeto **educationuser**.
localization_priority: Normal
ms.openlocfilehash: aef8640f49ad6ff4d91755fd5200000f4a0e856d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856662"
---
# <a name="update-educationuser-properties"></a>Actualizar propiedades de educationUser

Actualice las propiedades de un objeto **educationuser**.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  No admitida.  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | EduRoster.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/me
PATCH /education/users/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName| String| Nombre para mostrar del usuario.|
|givenName| String | Nombre. |
|middleName| String | Segundo nombre del usuario.|
|surname| String | Apellido del usuario.|
|mail| String| Dirección de correo electrónico.|
|mobilePhone| String | Número de móvil del usuario. |
|externalSource|string| Los valores posibles son: `sis`, `manual`, `enum_sentinel`.|
|externalSource|string| Indica desde dónde se ha creado este usuario.  Los valores posibles son: `sis`, `manual`, `enum_sentinel`.|
|mailingAddress|[physicalAddress](../resources/physicaladdress.md)| Dirección de correo del usuario.|
|residenceAddress|[physicalAddress](../resources/physicaladdress.md)| Dirección donde reside el usuario.|
|primaryRole|string| Rol predeterminado de un usuario.  Puede que el rol del usuario sea distinto en una clase individual. Los valores posibles son: `student`, `teacher`, `enum_sentinel`.|
|student|[educationStudent](../resources/educationstudent.md)| Si el rol principal es alumno, este bloque contendrá datos específicos de alumnos.|
|teacher|[educationTeacher](../resources/educationteacher.md)| Si el rol principal es profesor, este bloque contendrá datos específicos de profesores.|


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [educationUser](../resources/educationuser.md) actualizado en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_educationuser"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/users/{user-id}
Content-type: application/json
Content-length: 508

{
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 508

{
  "id": "13020",
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
  "mail": "rogelioC@contoso.com",
  "mobilePhone": "+1 (253) 555-0101",
  "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
  },
  "externalSource": "sis",
  "mailingAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
  "primaryRole": "student",
  "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
  "student": {
      "externalId": "13005",
      "birthDate": "2001-01-01T00:00:00Z"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationuser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
