---
title: Tipo de recurso educationUser
description: Usuario del sistema. Se trata de una variante específica del ámbito educativo del usuario con el mismo `id` que devolverá Microsoft Graph desde el punto de conexión `/users` no específico del ámbito educativo.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 6c0dce86c06036424e7be64f1864d900fef368fd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968172"
---
# <a name="educationuser-resource-type"></a>Tipo de recurso educationUser

Usuario del sistema. Se trata de una variante específica del ámbito educativo del usuario con el mismo `id` que devolverá Microsoft Graph desde el punto de conexión `/users` no específico del ámbito educativo.
Este objeto ofrece un subconjunto de destino de propiedades del objeto [user](user.md) principal y agrega un conjunto de propiedades específicas del ámbito educativo tales como `primaryRole`, alumno y datos de profeso.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener educationUser](../api/educationuser-get.md) | [educationUser](educationuser.md) |Lea las propiedades y relaciones de un objeto **educationUser**.|
|[Enumerar clases](../api/educationuser-list-classes.md) |Colección [educationClass](educationclass.md)| Obtenga la colección de objetos **educationClass** de la que el usuario es miembro.|
|[Enumerar centros educativos](../api/educationuser-list-schools.md) |Colección [educationSchool](educationschool.md)| Obtenga la colección de objetos **educationSchool** de la que el usuario es miembro.|
|[Obtener usuario](../api/educationuser-get-user.md) |[user](user.md)| Obtenga el directorio simple **user** correspondiente a este objeto **educationUser**.|
|[Actualizar](../api/educationuser-update.md) | [educationUser](educationuser.md)   |Actualice un objeto **educationUser**. |
|[Eliminar](../api/educationuser-delete.md) | Ninguno |Elimine un objeto **educationUser**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|accountEnabled|Boolean| **true** si la cuenta está habilitada; en caso contrario, **false**. Esta propiedad es necesaria cuando se crea un usuario. Es compatible con $filter.    |
|assignedLicenses|Colección [assignedLicense](assignedlicense.md)|Las licencias asignadas al usuario. No admite valores NULL.            |
|assignedPlans|Colección [assignedPlan](assignedplan.md)|Planes que se asignan al usuario. Solo lectura. No admite valores NULL. |
|businessPhones|String collection|Números de teléfono del usuario. **Nota:** Aunque se trata de una colección de cadenas, solo se puede establecer un número para esta propiedad.|
|createdBy|[identitySet](identityset.md)| Entidad que ha creado el usuario. |
|department|Cadena|El nombre del departamento en el que trabaja el usuario. Es compatible con $filter.|
|displayName|Cadena|Nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria al crearse un usuario y no puede borrarse durante las actualizaciones. Es compatible con $filter y $orderby.|
|externalSource|`educationExternalSource`| Indica desde dónde se ha creado este usuario. Los valores posibles son: `sis`, `manual`, `unkownFutureValue`.|
|givenName|Cadena|Nombre (nombre de pila) del usuario. Es compatible con $filter.|
|id|String|Identificador único del usuario. Se hereda de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|mail|String|Dirección SMTP del usuario (por ejemplo: "jeff@contoso.onmicrosoft.com"). Solo lectura. Es compatible con $filter.|
|mailingAddress|[physicalAddress](physicaladdress.md)| Dirección de correo del usuario.|
|mailNickname|Cadena|Alias de correo del usuario. Esta propiedad debe especificarse al crear un usuario. Es compatible con $filter.|
|middleName| String | Segundo nombre del usuario.|
|mobilePhone|Cadena|Número de teléfono móvil principal del usuario.|
|passwordPolicies|Cadena|Especifica las directivas de contraseña del usuario. Este valor es una enumeración con un valor posible de "DisableStrongPassword" y permite especificar contraseñas menos seguras que la directiva predeterminada. También se puede especificar "DisablePasswordExpiration". Pueden especificarse los dos juntos; (por ejemplo: "DisablePasswordExpiration, DisableStrongPassword").|
|passwordProfile|[PasswordProfile](passwordprofile.md)|Especifica el perfil de contraseña del usuario. El perfil contiene la contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. La contraseña del perfil debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies**. De manera predeterminada, se requiere una contraseña segura.|
|preferredLanguage|Cadena|Idioma preferido del usuario. Debe seguir el código ISO 639-1 (por ejemplo, "en-US").|
|primaryRole|educationUserRole| Rol predeterminado de un usuario. Puede que el rol del usuario sea distinto en una clase individual. Los valores posibles son: `student`, `teacher`, `unknownFutureValue`. Es compatible con $filter.|
|provisionedPlans|Colección [ProvisionedPlan](provisionedplan.md)|Planes que se aprovisionan para el usuario. Solo lectura. No admite valores NULL. |
|residenceAddress|[physicalAddress](physicaladdress.md)| Dirección donde reside el usuario.|
|student|[educationStudent](educationstudent.md)| Si el rol principal es alumno, este bloque contendrá datos específicos de alumnos.|
|surname|Cadena|Apellido (o apellidos) del usuario. Es compatible con $filter.|
|teacher|[educationTeacher](educationteacher.md)| Si el rol principal es profesor, este bloque contendrá datos específicos de profesores.|
|usageLocation|String|Código de país de dos letras (norma ISO 3166). Es necesario para los usuarios a quienes se van a asignar licencias debido a un requisito legal de comprobación de disponibilidad en los países o las regiones. Estos son algunos ejemplos: "US", "JP" y "GB". No admite valores NULL. Es compatible con $filter.|
|userPrincipalName|String|El nombre principal del usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de Internet del usuario basado en la norma RFC 822. Por convención, se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@dominio, donde el dominio debe estar presente en la colección de dominios verificados del inquilino. Esta propiedad es necesaria cuando se crea un usuario. Se puede acceder a los dominios verificados del inquilino desde la propiedad **verifiedDomains** en [organización](organization.md). Es compatible con $filter y $orderby.
|userType|Cadena|Un valor de cadena que puede utilizarse para clasificar los tipos de usuario en el directorio. Por ejemplo: "Miembro" e "Invitado". Es compatible con $filter.          |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classes|Colección [educationClass](educationclass.md)| Clases a las que pertenece el usuario. Admite valores NULL.|
|schools|Colección [educationSchool](educationschool.md)| Centros educativos a los que pertenece el usuario. Admite valores NULL.|
|assignments| [educationAssignment](/graph/api/resources/educationassignment?view=graph-rest-beta)| Lista de las asignaciones para el usuario. Admite valores NULL.|
|usuario|[user](user.md)| El usuario de Active directory correspondiente a este usuario.|

>**Nota:** **educationassignment** es un recurso de versión /beta. Si usa este recurso, asegúrese de revisar periódicamente el [registro de cambios](/graph/changelog). Al publicar recursos de la API de Microsoft Graph en el punto de conexión /v1.0, se indica la versión en el registro de cambios. Si la aplicación usa el recurso **educationassignment**, habrá que declarar las direcciones URL de la solicitud base, tal y como se muestra en el siguiente bloque de código:  
```JavaScript
var v1BaseUrl = “https://graph.microsoft.com/v1.0/education”;
var betaBaseUrl = “https://graph.microsoft.com/beta/education”;  // for administrativeUnit and educationOrganization
```


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.educationUser"
}-->

```json
{
  "id": "string",
  "accountEnabled": true,
  "assignedLicenses": [{"@odata.type": "microsoft.graph.assignedLicense"}],
  "assignedPlans": [{"@odata.type": "microsoft.graph.assignedPlan"}],
  "businessPhones": ["555-555-6568"],
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "middleName": "string",
  "surname": "string",
  "mail": "string",
  "mailNickname": "string",
  "mobilePhone": "string",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "externalSource": "string",
  "mailingAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "passwordPolicies": "string",
  "passwordProfile": {"@odata.type": "microsoft.graph.passwordProfile"},
  "preferredLanguage": "string",
  "primaryRole": "string",
  "provisionedPlans": [{"@odata.type": "microsoft.graph.provisionedPlan"}],
  "residenceAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "student": {"@odata.type": "microsoft.graph.educationStudent"},
  "teacher": {"@odata.type": "microsoft.graph.educationTeacher"},
  "usageLocation": "string",
  "userPrincipalName": "string",
  "userType": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationUser resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Error: microsoft.graph.educationUser/assignments:
      Referenced type microsoft.graph.educationAssignment is not defined in the doc set! Potential suggestion: UNKNOWN"
  ],
  "tocPath": ""
}-->
