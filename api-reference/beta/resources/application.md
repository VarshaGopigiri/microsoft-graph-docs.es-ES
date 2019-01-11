---
title: tipo de recurso de aplicación
description: 'Representa una aplicación. Cualquier aplicación que subcontrata autenticación para Azure Active Directory (AD Azure) se debe registrar en un directorio. Registro de aplicaciones implica que informará Azure AD acerca de la aplicación, incluida la dirección URL donde ha localizado, la dirección URL para enviar las respuestas después de la autenticación, el identificador URI para identificar la aplicación y mucho más. Para obtener más información, vea Conceptos básicos de registro de una aplicación en Azure AD. Se hereda de directoryObject. '
localization_priority: Priority
ms.openlocfilehash: b64de5670ccb9deebbabe32bb691d15b5a621f30
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805673"
---
# <a name="application-resource-type"></a>tipo de recurso de aplicación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una aplicación. Cualquier aplicación que subcontrata autenticación para Azure Active Directory (AD Azure) se debe registrar en un directorio. Registro de aplicaciones implica que informará Azure AD acerca de la aplicación, incluida la dirección URL donde ha localizado, la dirección URL para enviar las respuestas después de la autenticación, el identificador URI para identificar la aplicación y mucho más. Para obtener más información, vea [Conceptos básicos de registro de una aplicación en Azure AD](https://azure.microsoft.com/documentation/articles/active-directory-authentication-scenarios/#basics-of-registering-an-application-in-azure-ad). Se hereda de [directoryObject](directoryobject.md). 

> **Nota:** Los cambios realizados en el tipo de recurso de aplicación se encuentran actualmente en desarrollo. Para obtener más información, vea [problemas conocidos con Microsoft Graph](/graph/known-issues#application-and-serviceprincipal-api-changes).

Este recurso admite:

- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/application-delta.md).

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Obtener la aplicación](../api/application-get.md) | aplicación |Leer las propiedades y las relaciones del objeto application.|
|[Crear la aplicación](../api/application-post-applications.md) | aplicación | (Registros) se crea una nueva aplicación.|
|[Aplicaciones de lista](../api/application-list.md) | aplicación | Recuperar la lista de aplicaciones en la organización. |
|[Actualizar la aplicación](../api/application-update.md) | aplicación |Actualizar el objeto application. |
|[Eliminación de aplicación](../api/application-delete.md) | Ninguno |Eliminar el objeto application. |
|[Directivas de la lista asignada](../api/policy-list-assigned.md)| colección de [directivas](policy.md)| Obtenga todas las directivas asignadas a este objeto.|
|[Crear propietario](../api/application-post-owners.md) |[directoryObject](directoryobject.md)| Crear un nuevo propietario por la publicación de la colección de los propietarios.|
|[Enumerar propietarios](../api/application-list-owners.md) |Colección [directoryObject](directoryobject.md)| Obtenga a un propietario de la colección de objetos.|
|[delta](../api/application-delta.md)|colección de la aplicación| Obtener cambios incrementales para aplicaciones. |
|[Crear llamada](../api/application-post-calls.md)|[llamada](call.md)|Crear una nueva llamada por la publicación de la colección de las llamadas.|
|[Crear reunión en línea](../api/application-post-onlinemeetings.md)|[onlineMeeting](onlinemeeting.md)|Crear una nueva reunión en línea mediante la publicación de la colección onlineMeetings.|

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:---------------|:--------|:----------|
|API|[API](api.md)| Especifica la configuración para una aplicación de API. |
|appId| cadena | El identificador único para la aplicación que se asigna a una aplicación por Azure AD. No admite valores NULL. Solo lectura. |
|appRoles|colección de [función de aplicación](approle.md)|La colección de funciones de aplicación que se puede declarar una aplicación. Estos roles pueden asignarse a usuarios, grupos o entidades de seguridad del servicio. No admite valores NULL.|
|createdDateTime|DateTimeOffset| La fecha y la hora que se registró la aplicación. |
|deletedDateTime|DateTimeOffset| La fecha y la hora que se ha eliminado la aplicación. |
|displayName|Cadena|El nombre para mostrar para la aplicación. |
|id|Cadena|El identificador único para la aplicación. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura. |
|identifierUris|Colección String| El URI que identifica la aplicación. Para obtener más información, vea [objetos de la aplicación y los objetos a principales de servicio](https://azure.microsoft.com/documentation/articles/active-directory-application-objects/). El operador *any* es necesario para las expresiones de filtro en las propiedades multivalor. No admite valores NULL. |
|Info|[informationalUrl](informationalurl.md)| Información de perfil básico de la aplicación. |
|isFallbackPublicClient|Booleano| Especifica el tipo de aplicación de reserva como pública cliente, como una aplicación instalada que se ejecutan en un dispositivo móvil. El valor predeterminado es *false* lo que significa que el tipo de aplicación de reserva es cliente confidencial, como la aplicación web. Hay ciertos escenarios donde Azure AD no puede determinar el tipo de aplicación de cliente (por ejemplo, [ROPC](https://tools.ietf.org/html/rfc6749#section-4.3) flujo de dónde se configura sin especificar un URI de redireccionamiento). En esos casos Azure AD interpretará el tipo de aplicación en función del valor de esta propiedad.|
|keyCredentials|colección de [keyCredential](keycredential.md)|La colección de credenciales claves asociadas con la aplicación no acepta valores NULL. |
|logo|Stream|El logotipo principal para la aplicación. No admite valores NULL. |
|optionalClaims|optionalClaims| Reservado para uso futuro. |
|orgRestrictions|Colección String| Reservado para uso futuro. |
|parentalControlSettings|[parentalControlSettings](parentalcontrolsettings.md) |Especifica la configuración de control parental para una aplicación.|
|passwordCredentials|colección de [passwordCredential](passwordcredential.md)|La colección de credenciales de contraseña asociada con la aplicación. No admite valores NULL.|
|publicClient|[publicClient](publicclient.md)| Especifica la configuración para los clientes instalados como dispositivos de escritorio o portátiles. |
|publisherDomain| Cadena | El dominio comprobado publisher para la aplicación. Solo lectura.|
|requiredResourceAccess|colección de [requiredResourceAccess](requiredresourceaccess.md)|Especifica los recursos que esta aplicación requiere acceso a y el conjunto de ámbitos de OAuth de permisos y funciones de las aplicaciones que necesita en cada uno de esos recursos. Esta configuración previa a la de acceso a los recursos necesarios unidades de la experiencia de consentimiento. No admite valores NULL.|
|signInAudience | Cadena | Especifica qué cuentas de Microsoft son compatibles con la aplicación actual. Los valores admitidos son:<ul><li>**AzureADMyOrg**: los usuarios con un Microsoft funciona o escuela cuenta en el inquilino de Azure AD de mi organización (es decir, inquilino único)</li><li>**AzureADMultipleOrgs**: los usuarios con un Microsoft funciona o escuela cuenta en el inquilino de Azure AD de la organización (es decir, varios inquilino)</li> <li>**AzureADandPersonalMicrosoftAccount**: los usuarios con una cuenta Microsoft personal o una cuenta de trabajo o escuela en el inquilino de Azure AD de la organización</li></ul> | `AzureADandPersonalMicrosoftAccount` |
|de cierre|Colección String| Cadenas personalizadas que se pueden usar para clasificar e identificar la aplicación. |
|web|[Web](web.md)| Especifica la configuración para una aplicación web. |

## <a name="relationships"></a>Relaciones

| Relación | Tipo | Description |
|:---------------|:--------|:----------|
|llamadas           |colección [de llamadas](call.md)                  |Solo lectura. Admite valores NULL.|
|connectorGroup|[connectorGroup](connectorgroup.md)| El connectorGroup está usando la aplicación con el Proxy de aplicación de Azure AD. Admite valores NULL.|
|createdOnBehalfOf|[directoryObject](directoryobject.md)| Solo lectura.|
|onlineMeetings  |colección de [onlineMeeting](onlinemeeting.md)|Solo lectura. Admite valores NULL.|
|owners|Colección [directoryObject](directoryobject.md)|Objetos de Active Directory que son propietarios de la aplicación. Los propietarios son un conjunto de usuarios sin permisos de administrador que tienen permiso para modificar este objeto. Requiere la versión 2013-11-08 o más reciente. Solo lectura. Admite valores NULL.|
|directiva|colección de [directivas](policy.md)|Las directivas asignadas a esta aplicación.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "createdOnBehalfOf",
    "owners"
  ],
  "@odata.type": "microsoft.graph.application"
}-->

```json
{
  "api": {"@odata.type": "microsoft.graph.apiApplication"},
  "appId": "String",
  "appRoles": [{"@odata.type": "microsoft.graph.appRole"}],
  "createdDateTime": "String (timestamp)",
  "deletedDateTime": "String (timestamp)",
  "displayName": "String",
  "id": "String (identifier)",
  "identifierUris": ["String"],
  "info": {"@odata.type": "microsoft.graph.informationalUrl"},
  "isFallbackPublicClient": true,
  "keyCredentials": [{"@odata.type": "microsoft.graph.keyCredential"}],
  "logo": "Stream",
  "optionalClaims": [{"@odata.type": "microsoft.graph.optionalClaims"}],
  "orgRestrictions": ["Guid"],
  "parentalControlSettings": [{"@odata.type": "microsoft.graph.parentalControlSettings"}],
  "passwordCredentials": [{"@odata.type": "microsoft.graph.passwordCredential"}],
  "preAuthorizedApplications": [{"@odata.type": "microsoft.graph.preAuthorizedApplication"}],
  "publicClient": {"@odata.type": "microsoft.graph.publicClientApplication"},
  "publisherDomain": "String",
  "requiredResourceAccess": [{"@odata.type": "microsoft.graph.requiredResourceAccess"}],
  "signInAudience": "String",
  "tags": ["String"],
  "web": {"@odata.type": "microsoft.graph.webApplication"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "application resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
