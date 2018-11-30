---
title: tipo de recurso servicePrincipal
description: Representa una instancia de una aplicación en un directorio. Se hereda de directoryObject.
ms.openlocfilehash: c3a08efb1dea1109bd32d59a479260e14089783d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088513"
---
# <a name="serviceprincipal-resource-type"></a>tipo de recurso servicePrincipal

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una instancia de una aplicación en un directorio. Se hereda de [directoryObject](directoryobject.md).

Este recurso admite:

- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/serviceprincipal-delta.md).

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "appRoleAssignedTo",
    "appRoleAssignments",
    "createdObjects",
    "createdOnBehalfOf",
    "memberOf",
    "oauth2PermissionGrants",
    "ownedObjects",
    "owners"
  ],
  "@odata.type": "microsoft.graph.serviceprincipal"
}-->

```json
{
  "accountEnabled": true,
  "addIns": [{"@odata.type": "microsoft.graph.addIn"}],
  "appDisplayName": "string",
  "appId": "string",
  "appOwnerOrganizationId": "guid",
  "appRoleAssignmentRequired": true,
  "displayName": "string",
  "errorUrl": "string",
  "homepage": "string",
  "id": "string (identifier)",
  "keyCredentials": [{"@odata.type": "microsoft.graph.keyCredential"}],
  "logoutUrl": "string",
  "oauth2Permissions": [{"@odata.type": "microsoft.graph.oAuth2Permission"}],
  "passwordCredentials": [{"@odata.type": "microsoft.graph.passwordCredential"}],
  "preferredTokenSigningKeyThumbprint": "string",
  "publisherName": "string",
  "replyUrls": ["string"],
  "samlMetadataUrl": "string",
  "servicePrincipalNames": ["string"],
  "tags": ["string"]
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo |Descripción|
|:---------------|:--------|:----------|
|accountEnabled|Booleano| **true** si la cuenta de servicio de entidad de seguridad está habilitada; en caso contrario, **false**.            |
|appDisplayName|String|El nombre para mostrar expuesto por la aplicación asociada.|
|appId|cadena|El identificador único para la aplicación asociada (su propiedad **appId** ).|
|appRoleAssignmentRequired|Booleano|Especifica si un **appRoleAssignment** a un usuario o grupo es necesaria antes de Azure AD emitirá un usuario o un token de acceso a la aplicación. No admite valores NULL. |
|appRoles|colección de [función de aplicación](approle.md)|Las funciones de aplicación expuestas por la aplicación asociada. Para obtener más información, vea la definición de la propiedad **appRoles** en la entidad de la [aplicación](application.md) . No admite valores NULL. |
|displayName|String|El nombre para mostrar para la entidad de seguridad de servicio.|
|errorUrl|String|            |
|página principal|String|La dirección URL a la página principal de la aplicación asociada.|
|keyCredentials|colección de [keyCredential](keycredential.md)|La colección de credenciales claves asociado con el servicio de entidad de seguridad. No admite valores NULL.            |
|logoutUrl|String| Especifica la dirección URL que usará el servicio de autorización de Microsoft para cerrar sesión de un usuario mediante [canal de frente](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [back canal](https://openid.net/specs/openid-connect-backchannel-1_0.html) o protocolos de cierre de sesión SAML.  |
|oauth2Permissions|colección de [oAuth2Permission](oauth2permission.md)|Los permisos de OAuth 2.0 expuestos por la aplicación asociada. Para obtener más información, vea la definición de la propiedad **oauth2Permissions** en la entidad de la [aplicación](application.md) . No admite valores NULL.            |
|id|String|El identificador único para la entidad de seguridad de servicio. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|passwordCredentials|colección de [passwordCredential](passwordcredential.md)|La colección de credenciales de contraseña asociada con la entidad de seguridad de servicio. No admite valores NULL. |
|preferredTokenSigningKeyThumbprint|String|Reservado sólo para uso interno. No escribir ni en caso contrario, se basan en esta propiedad. Puede quitarse en versiones futuras. |
|publisherName|cadena|El nombre para mostrar del inquilino en el que se especifica la aplicación asociada.|
|replyUrls|Colección String|Las direcciones URL que los tokens de usuario se envían a para el inicio de sesión con la aplicación asociada o el redireccionamiento de códigos de autorización de los URI que OAuth 2.0 y tokens de acceso se envían a para la aplicación asociada. No admite valores NULL. |
|samlMetadataUrl|String| |
|servicePrincipalNames|Colección String|El URI que identifica la aplicación asociada. Para obtener más información, vea [objetos de la aplicación y los objetos a principales de servicio](https://msdn.microsoft.com/library/azure/dn132633.aspx). El operador **any** es necesario para las expresiones de filtro en las propiedades multivalor.  No admite valores NULL. |
|de cierre|Colección String| No admite valores NULL. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo |Descripción|
|:---------------|:--------|:----------|
|appRoleAssignedTo|[appRoleAssignment](approleassignment.md)|Entidades de seguridad (usuarios, grupos y entidades de seguridad de servicio) que se asignan a esta entidad de seguridad de servicio. Solo lectura.|
|appRoleAssignments|colección de [appRoleAssignment](approleassignment.md)|Aplicaciones que se asigna la entidad de seguridad de servicio a. Solo lectura. Admite valores NULL.|
|createdObjects|Colección [directoryObject](directoryobject.md)|Objetos de directorio creados por la entidad de seguridad de este servicio. Solo lectura. Admite valores NULL.|
|memberOf|Colección [directoryObject](directoryobject.md)|Funciones de la entidad de seguridad de este servicio es un miembro de. Métodos HTTP: GET como de solo lectura. Admite valores NULL.|
|oauth2PermissionGrants|colección de [oAuth2PermissionGrant](oauth2permissiongrant.md)|Concede a suplantación de usuario asociado con esta entidad de seguridad de servicio. Solo lectura. Admite valores NULL.|
|ownedObjects|Colección [directoryObject](directoryobject.md)|Objetos de Active Directory que pertenecen a esta entidad de seguridad de servicio. Solo lectura. Admite valores NULL.|
|owners|Colección [directoryObject](directoryobject.md)|Objetos de Active Directory que son propietarios de esta entidad de seguridad de servicio. Los propietarios son un conjunto de usuarios sin permisos de administrador que tienen permiso para modificar este objeto. Solo lectura. Admite valores NULL.|
|directiva|colección de [directivas](policy.md)|Las directivas asignadas a esta entidad de seguridad de servicio.|

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener servicePrincipal](../api/serviceprincipal-get.md) | [servicePrincipal](serviceprincipal.md) |Leer las propiedades y las relaciones del objeto servicePrincipal.|
|[Lista servicePrincipals](../api/serviceprincipal-list.md) | colección de [servicePrincipal](serviceprincipal.md) | Recuperar una lista de objetos de servicePrincipal. |
|[Crear appRoleAssignment](../api/serviceprincipal-post-approleassignments.md) |[appRoleAssignment](approleassignment.md)| Crear un nuevo appRoleAssignment por la publicación de la colección appRoleAssignments.|
|[Lista appRoleAssignments](../api/serviceprincipal-list-approleassignments.md) |colección de [appRoleAssignment](approleassignment.md)| Obtener una colección de objetos appRoleAssignment.|
|[Enumerar createdObjects](../api/serviceprincipal-list-createdobjects.md) |Colección [directoryObject](directoryobject.md)| Obtener una colección de objetos createdObject.|
|[Enumerar memberOf](../api/serviceprincipal-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Obtener los grupos que este servicio principal es miembro directo de la propiedad de navegación de miembro.|
|[Miembro de lista transitiva](../api/serviceprincipal-list-transitivememberof.md) |Colección [directoryObject](directoryobject.md)| Incluya los grupos que esta entidad de seguridad de servicio es un miembro de. Esta operación es transitiva e incluye los grupos que este servicio principal es un miembro anidado de. |
|[Directivas de la lista asignada](../api/policy-list-assigned.md)| colección de [directivas](policy.md)| Obtenga todas las directivas asignadas a este objeto.|
|[Lista oauth2PermissionGrants](../api/serviceprincipal-list-oauth2permissiongrants.md) |colección de [oAuth2PermissionGrant](oauth2permissiongrant.md)| Obtener una colección de objetos oAuth2PermissionGrant.|
|[Enumerar ownedObjects](../api/serviceprincipal-list-ownedobjects.md) |Colección [directoryObject](directoryobject.md)| Obtener una colección de objetos ownedObject.|
|[Agregar propietario](../api/serviceprincipal-post-owners.md) |[directoryObject](directoryobject.md)| Crear un nuevo propietario por la publicación de la colección de los propietarios.|
|[Enumerar propietarios](../api/serviceprincipal-list-owners.md) |Colección [directoryObject](directoryobject.md)| Obtener al propietario de una colección de objetos.|
|[Update](../api/serviceprincipal-update.md) | [servicePrincipal](serviceprincipal.md)  |Actualizar el objeto servicePrincipal. |
|[Delete](../api/serviceprincipal-delete.md) | Ninguno |Eliminar el objeto servicePrincipal. |
|[checkMemberGroups](../api/serviceprincipal-checkmembergroups.md)|Colección string||
|[getMemberGroups](../api/serviceprincipal-getmembergroups.md)|Colección string||
|[getMemberObjects](../api/serviceprincipal-getmemberobjects.md)|Colección string||
|[delta](../api/serviceprincipal-delta.md)|colección de servicePrincipal| Obtener cambios incrementales para entidades de seguridad del servicio. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePrincipal resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
