---
title: 'directoryObject: validateProperties'
description: Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura.  Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **crear** un grupo de Office 365. Para validar las propiedades de un grupo existente, utilice la función validateProperties para grupos.
localization_priority: Normal
ms.openlocfilehash: 1f38a30d86cf5b28eea6b9891687c4dbca4b78fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879824"
---
# <a name="directoryobject-validateproperties"></a>directoryObject: validateProperties

Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura.  Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **crear** un grupo de Office 365. Para validar las propiedades de un grupo existente, use la [función validateProperties](group-validateproperties.md) para grupos.

Se realizan las siguientes validaciones para las propiedades de alias para mostrar, nombre y correo: 
1. Validar el prefijo y el sufijo de directiva de nomenclatura
2. Validar la directiva de las palabras no permitidas personalizadas
3. Validar el correo sobrenombre es único

Esta API devuelve con el primer error encontrado. Si una o más propiedades producirá un error en varias validaciones, se devuelve sólo la propiedad con el primer error de validación. Sin embargo, puede validar el alias de correo y el nombre para mostrar y recibir una colección de errores de validación si solo va a validar el prefijo y el sufijo de directiva de nomenclatura.

## <a name="prerequisites"></a>Requisitos previos

Se requiere el siguiente **permiso** para ejecutar esta API: *Group.Read.All*

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
``` http
POST /directoryObjects/validateProperties
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre           | Descripción      |
|:---------------|:-----------------|
| Autorización  | Portador {código}    |
| Content-Type   | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Description|
|:---------------|:--------|:----------|
|entityType|Cadena| `Group`es el tipo de entidad compatibles sólo. |
|displayName|Cadena| El nombre para mostrar del grupo para validar. La propiedad no es necesaria individualmente. Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria. |
|mailNickname|Cadena| El alias de correo del grupo para validar. La propiedad no es necesaria individualmente. Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria. |
|onBehalfOfUserId|Guid| El identificador de objeto del usuario para suplantar al llamar a la API. Los resultados de validación son para los atributos y los roles de la onBehalfOfUserId. |

## <a name="response"></a>Respuesta

Si se realiza correctamente y no hay ningún error de validación, el método devuelve `204 No Content` código de respuesta. No devuelve nada en el cuerpo de la respuesta.

Si la solicitud no es válida, el método devuelve `400 Bad Request` código de respuesta. Se devuelve un mensaje de error con detalles acerca de la solicitud no válida en el cuerpo de la respuesta.

Si hay un error de validación, el método devuelve `422 Unprocessable Entity` código de respuesta. Se devuelve un mensaje de error y una colección de detalles del error en el cuerpo de la respuesta.

## <a name="examples"></a>Ejemplos

Éste es un ejemplo de una solicitud de validación correcta.

### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "directoryobject_validateproperties"
}-->
``` http
POST https://graph.microsoft.com/directoryObjects/validateProperties
Content-type: application/json
Content-length: 164

{
  "entityType": "Group",
  "displayName": "Myprefix_test_mysuffix",
  "mailNickname": "Myprefix_test_mysuffix",
  "onBehalfOfUserId": "onBehalfOfUserId-value"
}
```

### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

Éste es un ejemplo de una solicitud con errores de validación.

### <a name="request"></a>Solicitud
```http
POST https://graph.microsoft.com/directoryObjects/validateProperties
Content-type: application/json
Content-length: 164

{
  "entityType": "Group",
  "displayName": "test",
  "mailNickname": "test",
  "onBehalfOfUserId": "onBehalfOfUserId-value"
}
```

### <a name="response"></a>Respuesta
```http
HTTP/1.1 422 
Content-Type: application/json

{
  "error": {
    "code": "Request_UnprocessableEntity",
    "message": "The values provided contain one or more validation errors.",
    "innerError": {
      "request-id": "request-id-value",
      "date": "date-value"
    },
    "details": [
      {
        "target": "displayName",
        "code": "MissingPrefixSuffix",
        "message": "Property mailNickname is missing a required prefix/suffix per your organization's Group naming requirements.",
        "prefix": "Myprefix_",
        "suffix": "_mysuffix"
      },
      {
        "target": "mailNickname",
        "code": "MissingPrefixSuffix",
        "message": "Property mailNickname is missing a required prefix/suffix per your organization's Group naming requirements.",
        "prefix": "Myprefix_",
        "suffix": "_mysuffix"
      }
    ]
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: validateProperties",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
