---
title: Actualizar serviceprincipal
description: Actualizar las propiedades del objeto serviceprincipal.
localization_priority: Normal
ms.openlocfilehash: a8d4eebe64ac9c0c658ae9c43e2e92045be67424
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813030"
---
# <a name="update-serviceprincipal"></a>Actualizar serviceprincipal

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades del objeto serviceprincipal.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Application.ReadWrite.OwnedBy, Application.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /servicePrincipals/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|accountEnabled|Booleano|                **true** si la cuenta de servicio de entidad de seguridad está habilitada; en caso contrario, **false**.            |
|appDisplayName|Cadena|El nombre para mostrar expuesto por la aplicación asociada.|
|appId|cadena|El identificador único para la aplicación asociada (su propiedad **appId** ).|
|appRoleAssignmentRequired|Booleano|Especifica si un **appRoleAssignment** a un usuario o grupo es necesaria antes de Azure AD emitirá un usuario o un token de acceso a la aplicación.                            **Notas**: requiere la versión 1.5 o versiones posteriores, no acepta valores NULL.            |
|appRoles|función de aplicación|Las funciones de aplicación expuestas por la aplicación asociada. Para obtener más información, vea la definición de la propiedad **appRoles** en la entidad de aplicación **notas**: requiere la versión 1.5 o versiones posteriores, no acepta valores NULL.            |
|displayName|Cadena|El nombre para mostrar para la entidad de seguridad de servicio.|
|errorUrl|Cadena|            |
|página principal|Cadena|La dirección URL a la página principal de la aplicación asociada.|
|keyCredentials|keyCredential|La colección de credenciales claves asociado con el servicio de entidad de seguridad.                            **Notas**: No admite valores NULL.            |
|logoutUrl|Cadena| Especifica la dirección URL que usará el servicio de autorización de Microsoft para cerrar sesión de un usuario mediante [canal de frente](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [back canal](https://openid.net/specs/openid-connect-backchannel-1_0.html) o protocolos de cierre de sesión SAML. |
|oauth2Permissions|oAuth2Permission|Los permisos de OAuth 2.0 expuestos por la aplicación asociada. Para obtener más información, vea la definición de la propiedad **oauth2Permissions** en la entidad de la aplicación.                            **Notas**: requiere la versión 1.5 o versiones posteriores, no acepta valores NULL.            |
|passwordCredentials|passwordCredential|La colección de credenciales de contraseña asociada con la entidad de seguridad de servicio.                            **Notas**: No admite valores NULL.            |
|preferredTokenSigningKeyThumbprint|Cadena|Reservado sólo para uso interno. No escribir ni en caso contrario, se basan en esta propiedad. Puede quitarse en versiones futuras.                            **Notas**: requiere la versión 1.5 o más reciente.            |
|publisherName|cadena|El nombre para mostrar del inquilino en el que se especifica la aplicación asociada.|
|replyUrls|Cadena|Las direcciones URL que los tokens de usuario se envían a para el inicio de sesión con la aplicación asociada o el redireccionamiento de códigos de autorización de los URI que OAuth 2.0 y tokens de acceso se envían a para la aplicación asociada.                            **Notas**: No admite valores NULL.            |
|samlMetadataUrl|Cadena|            |
|servicePrincipalNames|Cadena|El URI que identifica la aplicación asociada. Para obtener más información, vea [objetos de la aplicación y los objetos a principales de servicio](https://msdn.microsoft.com/library/azure/dn132633.aspx).                            **Notas**: no acepta valores NULL, el operador **any** es necesario para las expresiones de filtro en las propiedades multivalor; Para obtener más información, vea [admiten consultas, filtros y las opciones de paginación](https://msdn.microsoft.com/library/azure/dn727074.aspx).            |
|de cierre|String|                                        **Notas**: no admite valores NULL.            |

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [servicePrincipal](../resources/serviceprincipal.md) objeto en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_serviceprincipal"
}-->
```http
PATCH https://graph.microsoft.com/beta/servicePrincipals/{id}
Content-type: application/json
Content-length: 391

{
  "accountEnabled": true,
  "addIns": [
    {
      "id": "id-value",
      "type": "type-value",
      "properties": [
        {
          "key": "key-value",
          "value": "value-value"
        }
      ]
    }
  ],
  "appDisplayName": "appDisplayName-value",
  "appId": "appId-value",
  "appOwnerOrganizationId": "appOwnerOrganizationId-value",
  "appRoleAssignmentRequired": true
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.serviceprincipal"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 391

{
  "accountEnabled": true,
  "addIns": [
    {
      "id": "id-value",
      "type": "type-value",
      "properties": [
        {
          "key": "key-value",
          "value": "value-value"
        }
      ]
    }
  ],
  "appDisplayName": "appDisplayName-value",
  "appId": "appId-value",
  "appOwnerOrganizationId": "appOwnerOrganizationId-value",
  "appRoleAssignmentRequired": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update serviceprincipal",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
