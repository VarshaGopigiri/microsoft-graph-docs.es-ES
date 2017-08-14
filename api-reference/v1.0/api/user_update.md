
# <a name="update-user"></a>Actualizar usuario

Actualice las propiedades de un objeto de usuario.
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.ReadWrite; User.ReadWrite.All; Directory.ReadWrite.All*

Al actualizar la propiedad passwordProfile, se necesita el siguiente ámbito: *Directory.AccessAsUser.All*

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

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|aboutMe|String|Un campo de entrada de texto de forma libre para que el usuario se describa a sí mismo.|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. Esta propiedad es necesaria cuando se crea un usuario. Es compatible con $filter.    |
|assignedLicenses|Colección [assignedLicense](../resources/assignedlicense.md)|Las licencias asignadas al usuario. No admite valores NULL.            |
|birthday|DateTimeOffset|El cumpleaños del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|city|String|La ciudad en la que se encuentra el usuario. Es compatible con $filter.|
|country|String|El país o la región en la que se encuentra el usuario. Por ejemplo: "US" o "UK". Es compatible con $filter.|
|department|String|El nombre del departamento en el que trabaja el usuario. Es compatible con $filter.|
|displayName|String|El nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria cuando se crea un usuario y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|givenName|String|El nombre (nombre de pila) del usuario. Es compatible con $filter.|
|hireDate|DateTimeOffset|La fecha de contratación del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|interests|Colección string|Una lista para que el usuario describa sus intereses.|
|jobTitle|String|El puesto del usuario. Es compatible con $filter.|
|mailNickname|String|El alias de correo del usuario. Esta propiedad debe especificarse al crear un usuario. Es compatible con $filter.|
|mobilePhone|String|El número de teléfono móvil principal del usuario.|
|mySite|String|La dirección URL del sitio personal del usuario.|
|officeLocation|String|La ubicación de la oficina del lugar de trabajo del usuario.|
|onPremisesImmutableId|String|Esta propiedad se utiliza para asociar una cuenta local de usuario de Active Directory a su objeto de usuario de Azure AD. Esta propiedad debe especificarse al crear una nueva cuenta de usuario en Graph si utiliza un dominio federado para la propiedad **userPrincipalName** (UPN) del usuario. **Importante**: Los caracteres **$** y **_** no se pueden utilizar a la hora de especificar esta propiedad. Es compatible con $filter.                            |
|passwordPolicies|String|Especifica las directivas de contraseña del usuario. Este valor es una enumeración con un valor posible de "DisableStrongPassword" y permite especificar contraseñas menos seguras que la directiva predeterminada. También se puede especificar "DisablePasswordExpiration". Los dos se pueden especificar a la vez. Por ejemplo: "DisablePasswordExpiration, DisableStrongPassword".|
|passwordProfile|[PasswordProfile](../resources/passwordprofile.md)|Especifica el perfil de contraseña del usuario. El perfil contiene la contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. La contraseña del perfil debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies**. De manera predeterminada, se requiere una contraseña segura.|
|pastProjects|Colección string|Una lista para que el usuario enumere sus últimos proyectos.|
|postalCode|String|El código postal de la dirección del usuario. El código postal es específico del país o de la región del usuario. En Estados Unidos, este atributo contiene el código postal.|
|preferredLanguage|String|El idioma preferido del usuario. Debe seguir el código ISO 639-1. Por ejemplo, "en-US".|
|preferredName|String|El nombre preferido del usuario.|
|responsibilities|Colección string|Una lista para que el usuario enumere sus responsabilidades.|
|schools|Colección string|Una lista para que el usuario enumere las escuelas a las que ha ido.|
|skills|Colección string|Una lista para que el usuario enumere sus aptitudes.|
|state|String|El estado o la provincia de la dirección del usuario. Es compatible con $filter.|
|streetAddress|String|La dirección postal del lugar de trabajo del usuario.|
|surname|String|El apellido (o apellidos) del usuario. Es compatible con $filter.|
|usageLocation|String|Un código de país de dos letras (norma ISO 3166). Es necesario para los usuarios a los que se asignarán licencias debido a un requisito legal para comprobar la disponibilidad de los servicios en los países.  Algunos ejemplos son: "US", "JP" y "GB". No admite valores NULL. Es compatible con $filter.|
|userPrincipalName|String|El nombre principal del usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de Internet del usuario basado en la norma RFC 822. Por convención, se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@dominio, donde el dominio debe estar presente en la colección de dominios verificados del inquilino. Esta propiedad es necesaria cuando se crea un usuario. Se puede acceder a los dominios verificados del inquilino desde la propiedad **verifiedDomains** en [organización](../resources/organization.md). Es compatible con $filter y $orderby.
|userType|String|Un valor de cadena que puede utilizarse para clasificar los tipos de usuario en el directorio. Por ejemplo: "Miembro" e "Invitado". Es compatible con $filter.          |

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
PATCH https://graph.microsoft.com/v1.0/me
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
      "assignedDateTime": "datetime-value",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "bea13e0c-3828-4daa-a392-28af7ff61a0f"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "companyName": "companyName-value"
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
