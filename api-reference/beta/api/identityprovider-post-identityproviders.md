---
title: Crear identityProvider
description: Crear un nuevo identityProvider especificando el nombre para mostrar, identityProvider tipo, identificador de cliente y el secreto de cliente.
ms.openlocfilehash: 8786cbf6676567a0c6aaef5bf497f50cff1ce9a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087693"
---
# <a name="create-identityprovider"></a>Crear identityProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear un nuevo [identityProvider](../resources/identityprovider.md) especificando el nombre para mostrar, identityProvider tipo, identificador de cliente y el secreto de cliente.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)|IdentityProvider.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)| No admitida.|
|Aplicación|No admitida.|

La cuenta de trabajo o escuela debe ser un administrador global del inquilino.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```http
POST /identityProviders
```

## <a name="request-headers"></a>Encabezados de solicitud

|Nombre|Descripción|
|:---------------|:----------|
|Authorization|{token} de portador. Obligatorio.|
|Content-Type|application/json. Obligatorio.|

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcionan una representación JSON del objeto [identityProvider](../resources/identityprovider.md) . Todas las propiedades enumeradas en la siguiente tabla son necesarias.

|Propiedad|Tipo|Descripción|
|:---------------|:--------|:----------|
|clientId|String|El identificador de cliente para la aplicación. Este es el identificador de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.|
|clientSecret|String|El secreto de cliente para la aplicación. Este es el secreto de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.|
|name|String|El nombre para mostrar del proveedor de identidad.|
|type|String|El tipo de proveedor de identidad. Debe ser uno de los siguientes valores: <ul><li/>Microsoft<li/>Google<li/>Amazon<li/>LinkedIn<li/>Facebook</ul>|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `201 Created` objeto de código y [identityProvider](../resources/identityprovider.md) de respuesta en el cuerpo de la respuesta. Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se crea un **identityProvider**.

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "create_identityprovider_from_identityproviders"
}-->
```http
POST https://graph.microsoft.com/beta/identityProviders
Content-type: application/json

{
    "name": "Login with Amazon",
    "type": "Amazon",
    "clientId": "56433757-cadd-4135-8431-2c9e3fd68ae8",
    "clientSecret": "000000000000"
}
```

##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.IdentityProvider"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "Amazon-OAUTH",
    "name": "Login with Amazon",
    "type": "Amazon",
    "clientId": "56433757-cadd-4135-8431-2c9e3fd68ae8",
    "clientSecret": "*****"
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
