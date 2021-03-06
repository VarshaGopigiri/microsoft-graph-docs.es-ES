---
title: Actualizar identityProvider
description: Actualizar las propiedades en un identityProvider existente.
localization_priority: Normal
ms.openlocfilehash: ebe49fb562f77004edfa3504130fbf50f4d40003
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832812"
---
# <a name="update-identityprovider"></a>Actualizar identityProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades en una existente [identityProvider](../resources/identityprovider.md).

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
PATCH /identityProviders/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

|Nombre|Descripción|
|:---------------|:----------|
|Authorization|{token} de portador. Obligatorio.|
|Content-Type|application/json. Obligatorio.|

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con una o varias propiedades que necesitan actualizarse.

|Propiedad|Tipo|Description|
|:---------------|:--------|:----------|
|clientId|Cadena|El identificador de cliente para la aplicación. Este es el identificador de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.|
|clientSecret|Cadena|El secreto de cliente para la aplicación. Este es el secreto de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.|
|name|Cadena|El nombre para mostrar del proveedor de identidad.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se actualiza la definición de la duración del token **identityProvider** y se establece como el valor predeterminado de la organización.

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "update_identityprovider"
}-->
```http
PATCH https://graph.microsoft.com/beta/identityProviders/Amazon-OAuth
Content-type: application/json
Content-length: 41

{
    "clientSecret": "1111111111111"
}
```

##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
