---
title: Obtener identityProvider
description: Recuperar las propiedades de un identityProvider existente.
localization_priority: Normal
ms.openlocfilehash: f0d467bde092f84d092dbcee7c54c01e3ef849f7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812974"
---
# <a name="get-identityprovider"></a>Obtener identityProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recuperar las propiedades de una existente [identityProvider](../resources/identityprovider.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)|IdentityProvider.Read.All, IdentityProvider.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)| No admitida.|
|Aplicación|No admitida.|

La cuenta de trabajo o escuela debe ser un administrador global del inquilino.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```http
GET /identityProviders/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

|Nombre|Descripción|
|:---------------|:----------|
|Authorization|{token} de portador. Obligatorio.|

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` código de respuesta y una representación JSON de la [identityProvider](../resources/identityprovider.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se recupera un específico **identityProvider**.

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_identityprovider"
}-->
```http
GET https://graph.microsoft.com/beta/identityProviders/Amazon-OAuth
```

##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.IdentityProvider"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "Amazon-OAUTH",
    "type": "Amazon",
    "name": "Login with Amazon",
    "clientId": "56433757-cadd-4135-8431-2c9e3fd68ae8",
    "clientSecret": "*****"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
