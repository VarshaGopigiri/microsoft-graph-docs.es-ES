---
title: 'grupo: validateProperties'
description: Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura. Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **Actualizar** un grupo de Office 365. Para validar las propiedades antes de crear un grupo, utilice la función validateProperties para los objetos de Active directory.
ms.openlocfilehash: d7f2767908e6cbf9116bec769a1abc32731e4758
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083947"
---
# <a name="group-validateproperties"></a>grupo: validateProperties

Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura. Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **Actualizar** un grupo de Office 365. Para validar las propiedades antes de crear un grupo, use la [función validateProperties](directoryobject-validateproperties.md) para los objetos de Active directory.

Se realizan las siguientes validaciones para las propiedades de alias para mostrar, nombre y correo: 
1. Validar el prefijo y el sufijo de directiva de nomenclatura
2. Validar la directiva de las palabras no permitidas personalizadas

Esta API devuelve con el primer error encontrado. Si una o más propiedades producirá un error en varias validaciones, se devuelve sólo la propiedad con el primer error de validación. Sin embargo, puede validar el alias de correo y el nombre para mostrar y recibir una colección de errores de validación si solo va a validar el prefijo y el sufijo de directiva de nomenclatura.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.Read.All, Group.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.Read.All, Group.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
``` http
POST /groups/<id>/validateProperties
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre           | Descripción      |
|:---------------|:-----------------|
| Autorización  | Portador {código}    |
| Content-Type   | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String| El nombre para mostrar del grupo para validar. La propiedad no es necesaria individualmente. Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria. |
|mailNickname|String| El alias de correo del grupo para validar. La propiedad no es necesaria individualmente. Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria. |
|onBehalfOfUserId|Guid| El identificador de objeto del usuario para suplantar al llamar a la API. Los resultados de validación son para los atributos y los roles de la onBehalfOfUserId. |

## <a name="response"></a>Respuesta
Si se realiza correctamente y no hay ningún error de validación, el método devuelve `204 No Content` código de respuesta. No devuelve nada en el cuerpo de la respuesta.

Si la solicitud no es válida, el método devuelve `400 Bad Request` código de respuesta. Se devuelve un mensaje de error con detalles acerca de la solicitud no válida en el cuerpo de la respuesta.

Si se ha producido un error de validación. El método devuelve `422 Unprocessable Entity` código de respuesta. Se devuelve un mensaje de error y una colección de detalles del error en el cuerpo de la respuesta.

## <a name="examples"></a>Ejemplos

Éste es un ejemplo de una solicitud de validación correcta.

### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "group_validateproperties"
}-->
``` http
POST https://graph.microsoft.com/beta/groups/{id}/validateProperties
Content-type: application/json
Content-length: 132

{
  "displayName": "Myprefix_test_mysuffix",
  "mailNickname": "Myprefix_test_mysuffix",
  "onBehalfOfUserId": "onBehalfOfUserId-value"
}
```

### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": true,
} -->
```http
HTTP/1.1 204 No Content
```

Éste es un ejemplo de una solicitud con errores de validación.

### <a name="request"></a>Solicitud
``` http
POST https://graph.microsoft.com/beta/groups/{id}/validateProperties
Content-type: application/json
Content-length: 128

{
  "displayName": "MyPrefix_test_mysuffix",
  "mailNickname": "MyPrefix_test_mysuffix"
}
```

### <a name="response"></a>Respuesta
```http
HTTP/1.1 422
Content-type: application/json
Content-length: 223

{
  "error": {
    "code": "Request_UnprocessableEntity",
    "message": "The values provided contain one or more validation errors.",
    "innerError": {
      "request-id": "id-value",
      "date": "date-value"
    },
    "details": [
      {
        "target": "mailNickname",
        "code": "PropertyConflict",
        "message": "Another object with the same value for property mailNickname already exists."
      }
    ]
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: validateProperties",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
