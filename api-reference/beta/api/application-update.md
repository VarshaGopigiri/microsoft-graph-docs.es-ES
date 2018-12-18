---
title: Actualizar la aplicación
description: Actualizar las propiedades del objeto application.
author: lleonard-msft
ms.openlocfilehash: e664e212f81bab9f4e8b49bce60b4ec045fa5787
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316691"
---
# <a name="update-application"></a>Actualizar la aplicación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades del objeto application.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Application.ReadWrite.OwnedBy, Application.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /applications/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Type | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowPublicClient|Boolean| Especifica si la aplicación puede actuar como un cliente público. Por ejemplo, una aplicación instalada que se ejecutan en un dispositivo móvil. El valor predeterminado es *false*. |
|API|[API](../resources/api.md)| Especifica la configuración para una aplicación de API. |
|appRoles|colección de [función de aplicación](../resources/approle.md)|La colección de funciones de aplicación que se puede declarar una aplicación. Estos roles pueden asignarse a usuarios, grupos o entidades de seguridad del servicio. No admite valores NULL.|
|applicationAliases|Colección String| El URI que identifica la aplicación. Para obtener más información, vea [objetos de la aplicación y los objetos a principales de servicio](https://azure.microsoft.com/documentation/articles/active-directory-application-objects/). El operador *any* es necesario para las expresiones de filtro en las propiedades multivalor. No admite valores NULL. |
|createdDateTime|DateTimeOffset| La fecha y la hora que se registró la aplicación. |
|deletedDateTime|DateTimeOffset| La fecha y la hora que se ha eliminado la aplicación. |
|displayName|String|El nombre para mostrar para la aplicación. |
|id|String|El identificador único para la aplicación. Heredado de [directoryObject](../resources/directoryobject.md). Clave. No admite valores NULL. Solo lectura. |
|Info|[informationalUrl](../resources/informationalurl.md)| Información de perfil básico de la aplicación. | Especifica la configuración para los clientes instalados como dispositivos de escritorio o portátiles. |
|keyCredentials|colección de [keyCredential](../resources/keycredential.md)|La colección de credenciales claves asociadas con la aplicación no acepta valores NULL. |
|logo|Stream|El logotipo principal para la aplicación. No admite valores NULL. |
|orgRestrictions|Colección String| El tenantIds organizativa a la que la aplicación está restringida.  Si la colección está vacía, la aplicación es varios inquilino (no restringido). Si la colección contiene tenantIds, la aplicación está restringida a la tenantIds organizativa en la colección. Especificación de otros inquilinos pero no el tenantId donde se registró la aplicación implica que el tenantId de la aplicación es indirectamente incluye. |
|passwordCredentials|colección de [passwordCredential](../resources/passwordcredential.md)|La colección de credenciales de contraseña asociada con la aplicación. No admite valores NULL.|
|preAuthorizedApplications|colección de [preAuthorizedApplication](../resources/preauthorizedapplication.md)| Enumera las aplicaciones y los permisos solicitados para consentimiento implícito. Requiere un administrador que se ha proporcionado el consentimiento a la aplicación. preAuthorizedApplications no requieren el usuario da su consentimiento a los permisos solicitados. Los permisos enumerados en preAuthorizedApplications no requieren el consentimiento de usuario. Sin embargo, los permisos solicitados adicionales no aparece en preAuthorizedApplications requieren el consentimiento de usuario. |
|requiredResourceAccess|colección de [requiredResourceAccess](../resources/requiredresourceaccess.md)|Especifica los recursos que esta aplicación requiere acceso a y el conjunto de ámbitos de OAuth de permisos y funciones de las aplicaciones que necesita en cada uno de esos recursos. Esta configuración previa a la de acceso a los recursos necesarios unidades de la experiencia de consentimiento. No admite valores NULL.|
|de cierre|Colección String| Cadenas personalizadas que se pueden usar para clasificar e identificar la aplicación. |
|web|[Web](../resources/web.md)| Especifica la configuración para una aplicación web. |

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `204 No Content` código de respuesta y no devuelve nada en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_application"
}-->
```http
PATCH https://graph.microsoft.com/beta/applications/{id}
Content-type: application/json
Content-length: 72

{
  "allowPublicClient": false,
  "displayName": "New display name"
}
```
##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update application",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->