---
title: Actualizar grupo de calendario
description: Actualiza las propiedades del objeto calendargroup.
author: angelgolfer-ms
ms.openlocfilehash: 24b09f3cd3dc23daf799eac70e59e0c4e32d7079
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324769"
---
# <a name="update-calendargroup"></a>Actualizar grupo de calendario

Actualiza las propiedades del objeto calendargroup.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso                        | Permisos (de menos a más privilegiados) |
| :------------------------------------- | :------------------------------------------ |
| Delegado (cuenta profesional o educativa)     | Calendars.ReadWrite                         |
| Delegado (cuenta personal de Microsoft) | Calendars.ReadWrite                         |
| Aplicación                            | Calendars.ReadWrite                         |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.

```http
PATCH /me/calendarGroups/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado        | Valor                       |
| :------------ | :-------------------------- |
| Authorization | {token} de portador. Obligatorio.   |
| Content-Type  | application/json. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad | Tipo   | Descripción     |
| :------- | :----- | :-------------- |
| name     | String | Nombre del grupo. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "update_calendargroup"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
Content-type: application/json
Content-length: 30

{
  "name": "name-value"
}
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 110

{
  "name": "name-value",
  "classId": "11b0131d-43c8-4bbb-b2c8-e80f9a50834a",
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "Update calendargroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
