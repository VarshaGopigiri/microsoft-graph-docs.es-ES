---
title: Actualizar usuario
description: Actualiza las propiedades de un objeto de usuario.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 00efdeed6fdb85aeccde5fae63e813b8b5e65961
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939115"
---
# <a name="update-user"></a>Actualizar usuario

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualiza las propiedades de un objeto de usuario.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.ReadWrite, User.ReadWrite.All, Directory.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | User.ReadWrite    |
|Aplicación | User.ReadWrite.All, Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor|
|:-----------|:------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|aboutMe|Cadena|Un campo de entrada de texto de forma libre para que el usuario se describa a sí mismo.|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. Esta propiedad es necesaria cuando se crea un usuario. Es compatible con $filter.    |
|assignedLicenses|Colección [assignedLicense](../resources/assignedlicense.md)|Las licencias asignadas al usuario. No admite valores NULL.            |
|birthday|DateTimeOffset|El cumpleaños del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|city|Cadena|La ciudad en la que se encuentra el usuario. Es compatible con $filter.|
|country|Cadena|El país o la región en la que se encuentra el usuario. Por ejemplo: "US" o "UK". Es compatible con $filter.|
|department|Cadena|El nombre del departamento en el que trabaja el usuario. Es compatible con $filter.|
|displayName|Cadena|El nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria cuando se crea un usuario y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|employeeId|Cadena|El identificador de empleado asignado al usuario por la organización. Es compatible con $filter.|
|givenName|Cadena|El nombre (nombre de pila) del usuario. Es compatible con $filter.|
|hireDate|DateTimeOffset|La fecha de contratación del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|interests|Colección string|Una lista para que el usuario describa sus intereses.|
|jobTitle|Cadena|El puesto del usuario. Es compatible con $filter.|
|mailNickname|Cadena|El alias de correo del usuario. Esta propiedad debe especificarse al crear un usuario. Es compatible con $filter.|
|mobilePhone|Cadena|El número de teléfono móvil principal del usuario.|
|mySite|Cadena|La dirección URL del sitio personal del usuario.|
|officeLocation|Cadena|La ubicación de la oficina del lugar de trabajo del usuario.|
|onPremisesImmutableId|String|Esta propiedad se utiliza para asociar una cuenta local de usuario de Active Directory a su objeto de usuario de Azure AD. Esta propiedad debe especificarse al crear una nueva cuenta de usuario en Graph si utiliza un dominio federado para la propiedad **userPrincipalName** (UPN) del usuario. **Importante**: Los caracteres **$** y **_** no se pueden utilizar a la hora de especificar esta propiedad. Es compatible con $filter.                            |
|passwordPolicies|Cadena|Especifica las directivas de contraseña del usuario. Este valor es una enumeración con un valor posible de "DisableStrongPassword" y permite especificar contraseñas menos seguras que la directiva predeterminada. También se puede especificar "DisablePasswordExpiration". Los dos se pueden especificar a la vez. Por ejemplo: "DisablePasswordExpiration, DisableStrongPassword".|
|passwordProfile|[PasswordProfile](../resources/passwordprofile.md)|Especifica el perfil de contraseña del usuario. El perfil contiene la contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. La contraseña del perfil debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies**. De manera predeterminada, se requiere una contraseña segura.|
|pastProjects|Colección string|Una lista para que el usuario enumere sus últimos proyectos.|
|postalCode|Cadena|El código postal de la dirección del usuario. El código postal es específico del país o de la región del usuario. En Estados Unidos, este atributo contiene el código postal.|
|preferredLanguage|Cadena|El idioma preferido del usuario. Debe seguir el código ISO 639-1. Por ejemplo, "en-US".|
|preferredName|Cadena|El nombre preferido del usuario.|
|responsibilities|Colección string|Una lista para que el usuario enumere sus responsabilidades.|
|schools|Colección string|Una lista para que el usuario enumere las escuelas a las que ha ido.|
|skills|Colección string|Una lista para que el usuario enumere sus aptitudes.|
|state|Cadena|El estado o la provincia de la dirección del usuario. Es compatible con $filter.|
|streetAddress|Cadena|La dirección postal del lugar de trabajo del usuario.|
|surname|Cadena|El apellido (o apellidos) del usuario. Es compatible con $filter.|
|usageLocation|Cadena|Un código de país de dos letras (norma ISO 3166). Es necesario para los usuarios a los que se asignarán licencias debido a un requisito legal para comprobar la disponibilidad de los servicios en los países.  Algunos ejemplos son: "US", "JP" y "GB". No admite valores NULL. Es compatible con $filter.|
|userPrincipalName|String|El nombre principal del usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de Internet del usuario basado en la norma RFC 822. Por convención, se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@dominio, donde el dominio debe estar presente en la colección de dominios verificados del inquilino. Esta propiedad es necesaria cuando se crea un usuario. Se puede acceder a los dominios verificados del inquilino desde la propiedad **verifiedDomains** en [organización](../resources/organization.md). Es compatible con $filter y $orderby.
|userType|Cadena|Un valor de cadena que puede utilizarse para clasificar los tipos de usuario en el directorio. Por ejemplo: "Miembro" e "Invitado". Es compatible con $filter.          |

Puesto que el recurso de **usuario** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una sesión de **usuario** existente.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_user"
}-->
```http
PATCH https://graph.microsoft.com/beta/me
Content-type: application/json
Content-length: 491

{
  "accountEnabled": true,
  "assignedLicenses": [
    {
      "disabledPlans": [ "bea13e0c-3828-4daa-a392-28af7ff61a0f" ],
      "skuId": "skuId-value"
    }
  ],
  "assignedPlans": [
    {
      "assignedDateTime": "2016-10-19T10:37:00Z",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "bea13e0c-3828-4daa-a392-28af7ff61a0f"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value"
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](/graph/extensibility-open-users)
- [Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
