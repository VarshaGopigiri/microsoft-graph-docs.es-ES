---
title: Autorización y API de seguridad de Microsoft Graph
description: Los datos de seguridad accesibles a través de la API de seguridad de Microsoft Graph son confidenciales y están protegidos por los permisos y los roles de Azure Active Directory (Azure AD).
ms.openlocfilehash: c69621fa7059a96381bed76b58c4a77e80d984dd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092761"
---
# <a name="authorization-and-the-microsoft-graph-security-api"></a>Autorización y API de seguridad de Microsoft Graph

Los datos de seguridad accesibles a través de la API de seguridad de Microsoft Graph son confidenciales y están protegidos por los permisos y los roles de Azure Active Directory (Azure AD).

La API de seguridad de Microsoft Graph admite dos tipos de autorización:

- **Autorización a nivel de aplicación**: ningún usuario inició sesión (por ejemplo, un escenario SIEM). Los permisos otorgados a la aplicación determinan la autorización. 
    >**Nota:** esta opción también admite casos en los que la aplicación administra el Control de acceso basado en roles (RBAC).
- **Autorización delegada por el usuario**: un usuario miembro del espacio empresarial de Azure AD ha iniciado sesión. El usuario debe ser miembro de un rol de administrador limitado de Azure AD (ya sea lector o administrador de seguridad) y, además, la aplicación debe contar con los permisos necesarios.

Si realiza una llamada a la API de seguridad de Microsoft Graph desde Probador de Graph:

- El administrador del espacio empresarial de Azure AD debe conceder de forma explícita los permisos solicitados a la aplicación del Explorador de Graph.
- El usuario debe ser miembro del rol de administrador limitado del lector de seguridad en Azure AD (ya sea lector o administrador de seguridad).

>**Nota**: el Explorador de Graph no admite la autorización a nivel de aplicación.

Si realiza una llamada a la API de seguridad de Microsoft Graph desde una aplicación propia o personalizada:

- El administrador del espacio empresarial de Azure AD debe conceder de forma explícita los permisos a su aplicación. Esto es necesario tanto para las autorizaciones a nivel de aplicación y delegadas por usuarios.
- Si usa una autorización delegada por usuario, dicha persona debe ser miembro del rol de administrador limitado del lector o administrador de seguridad en Azure AD.

## <a name="manage-authorization-in-security-api-client-applications"></a>Administrar la autorización en las aplicaciones cliente con API de seguridad

Los datos de seguridad proporcionados a través de la API de seguridad de Microsoft Graph son confidenciales y deben estar protegidos por los mecanismos de autorización y autenticación adecuados. La siguiente tabla indica los pasos para registrarse y crear una aplicación cliente que puede acceder a la API de seguridad de Microsoft Graph.

| **Quién** | **Acción** |
|:---------------------|:------------------|
|Propietario o desarrollador de la aplicación|Registra la aplicación como una aplicación de empresa.|
|Administrador de un espacio empresarial|Le concede permisos a la aplicación.|
|Administrador de un espacio empresarial|Asigna roles a los usuarios.|
|Desarrollador de la aplicación|Inicia sesión como usuario y usa la aplicación para acceder a la API de seguridad de Microsoft Graph.|

El registro de la aplicación solo define qué permisos necesita la aplicación para poder ejecutarse. NO le concede los permisos a la aplicación.

El administrador de espacios empresariales de Azure AD DEBE conceder de forma explícita los permisos a la aplicación. Esto debe realizarse por espacio empresarial *cada vez* que se modifican los permisos de aplicación en el portal de registro correspondiente.

Por ejemplo, imagine que tiene una aplicación, dos espacios empresariales de Azure AD (**E1** y **E2**) y dos permisos (**P1** y **P2**). A continuación, se muestra el proceso de autorización:

- La aplicación se registra para exigir el permiso **P1**.
- Cuando los usuarios del espacio empresarial **E1** obtienen un token de Azure AD para esta aplicación, el token no contiene ningún permiso.
- El administrador de Azure AD del espacio empresarial **E1** concede de forma explícita permisos a la aplicación. Cuando los usuarios del espacio empresarial **E1** obtienen un token de Azure AD para la aplicación, el token contendrá el permiso **P1**.
- Cuando los usuarios del espacio empresarial **E2** obtienen un token de Azure AD para la aplicación, el token no contiene ningún permiso, ya que el administrador del espacio empresarial **E2** todavía no le ha concedido permisos a la aplicación. Los permisos deben otorgarse *por espacio empresarial* y *por aplicación*.
- El registro de la aplicación cambia para que ahora se requieran permisos **P1** y **P2**.
- Cuando los usuarios del espacio empresarial **E1** obtienen un token de Azure AD para la aplicación, el token solo contendrá el permiso **P1**. Los permisos concedidos a una aplicación se registran como instantáneas de lo que se le ha concedido: *no cambian automáticamente* después de que cambie el registro (permiso) de la aplicación.
- El administrador del espacio empresarial **E2** le concede permisos **P1** y **P2** a la aplicación. Ahora bien, cuando los usuarios del espacio empresarial **E2** obtienen un token de Azure AD para la aplicación, el token contendrá los permisos **P1** y **P2**.

>**Nota**: Los tokens de Azure AD para la aplicación en el espacio empresarial **E1** y **E2** contienen diferentes permisos, ya que cada administrador del espacio empresarial ha concedido diferentes permisos a la aplicación.

- Para que la aplicación vuelva a funcionar en el espacio empresarial **E1**, el administrador del espacio **E1** debe concederle los permisos **P1** y **P2** de forma explícita a la aplicación.

## <a name="register-an-application-in-the-azure-ad-v20-endpoint"></a>Registrar una aplicación con el punto de conexión de Azure AD (versión 2.0)

Para registrar una aplicación con el punto final de Azure AD (versión 2.0), necesitará lo siguiente:

- **Nombre de la aplicación**: una cadena que se usa para el nombre de aplicación.
- **Dirección URL de redirección**: la dirección URL desde donde se envía la respuesta de autenticación de Azure AD. Para comenzar, puede usar la página principal de prueba de la aplicación web del cliente.
- **Permisos necesarios**: los permisos que necesita su aplicación para poder realizar una llamada a Microsoft Graph.

Para registrar su aplicación, haga lo siguiente:

1. Vaya a https://apps.dev.microsoft.com/ e inicie sesión.
    >**Nota**: No necesita ser administrador de espacios empresariales. Se lo redirigirá a la lista **Mis aplicaciones**.
2. Elija **Agregar una aplicación** y escriba un **Nombre de la aplicación** para crear una nueva aplicación.
3. En la página de registro de la nueva aplicación, elija **Agregar plataforma** > **Web**. En el campo **Dirección URL de redireccionamiento**, escriba la URL correspondiente.
4. En la sección **Permisos para Microsoft Graph**, debajo de **Permisos delegados**, elija **Añadir**. En el cuadro de diálogo, elija los permisos necesarios. Para obtener una lista de permisos, consulte [Permisos de seguridad](permissions-reference.md#security-permissions).

    >La API de seguridad de Microsoft Graph requiere el ámbito SecurityEvents.Read.All para las consultas GET y el ámbito SecurityEvents.ReadWrite.All para las consultas PATCH/POST.

5. Seleccione **Guardar**.

Guarde la siguiente información:

- Id. de aplicación
- Dirección URL de redireccionamiento
- Lita de permisos necesarios

Para obtener más información, consulte [Registrar una aplicación con el punto de conexión v2.0 de Azure AD](auth-register-app-v2.md).

## <a name="grant-permissions-to-an-application"></a>Conceda permisos a la aplicación.

El registro de la aplicación solo define qué permisos necesita la aplicación y no le concede los permisos. Un administrador de espacios empresariales de Azure AD explícitamente debe conceder estos permisos de forma explícita mediante una llamada al punto de conexión de consentimiento de administrador. Para obtener más información, consulte [Usar el punto de conexión de consentimiento de administrador](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-scopes#using-the-admin-consent-endpoint).

Para conceder permisos a una aplicación, necesitará lo siguiente:

- **Id. de aplicación**: el Id. de aplicación del portal de registro de la aplicación.
- **Dirección URL de redireccionamiento**: la cadena que configure en el portal de registro de la aplicación de respuesta de autenticación.

Para conceder los permisos:

- En un editor de texto, cree la siguiente cadena de dirección URL:

    `https://login.microsoftonline.com/common/adminconsent?client_id=<Application Id>&state=12345&redirect_uri=<Redirect URL>`

- En un navegador web, vaya a esta dirección URL e inicie sesión como administrador del espacio empresarial. El cuadro de diálogo muestra la lista de permisos que necesita la aplicación, como se indica en el portal de registro de la aplicación. Elija **Aceptar** para conceder estos permisos a la aplicación.

> **Nota:** Este paso concede permisos a la aplicación, no a los usuarios. Esto significa que a todos los usuarios que pertenezcan al espacio empresarial de Azure AD y que usen esta aplicación se les concederán los permisos, incluso a los usuarios que no son administradores.

## <a name="assign-azure-ad-roles-to-users"></a>Asignar roles de Azure AD a usuarios

Después de que se conceden permisos a una aplicación, todos los usuarios con acceso a ella (es decir, los miembros del espacio empresarial de Azure AD) recibirán los permisos concedidos. Para proteger datos confidenciales de seguridad, la API de seguridad de Microsoft Graph también requiere que a los usuarios se les asigne el rol de **lector de seguridad** de Azure AD. Para obtener más información, consulte [Asignar roles de administrador](https://docs.microsoft.com/es-ES/azure/active-directory/active-directory-assign-admin-roles-azure-portal) y [Asignar un usuario a los roles de administrador](https://docs.microsoft.com/es-ES/azure/active-directory/active-directory-users-assign-role-azure-portal).

>**Nota:** Para realizar este paso, debe ser administrador de un espacio empresarial.

Para asignar roles a usuarios, haga lo siguiente:

- Inicie sesión en [Azure Portal](https://portal.azure.com) (https://portal.azure.com)).
- En el menú, seleccione **Azure Active Directory** > **Usuarios**.
- Seleccione el nombre del usuario.
- Seleccione **Administrar** > **Rol de directorio**.
- Seleccione **Administrador limitado**y elija la casilla de verificación **Lector de seguridad**.
- Elija **Guardar**.

## <a name="create-an-authentication-code"></a>Crear un código de autenticación

Para crear un código de autenticación, necesitará lo siguiente:

- **Id. de aplicación**: el Id. de aplicación del portal de registro de la aplicación.
- **Dirección URL de redirección**: la dirección URL desde donde se envía la respuesta de autenticación de Azure AD. Para comenzar, puede usar https://localhost o la página principal de prueba de la aplicación web del cliente.
- **Tecla de aplicación** (opcional): la tecla de la aplicación. Esto se aplica al desarrollar una aplicación que usará el código de autenticación solo de la aplicación (es decir, que no admitirá la autenticación delegada por el usuario).

En la siguiente tabla se indican los recursos que puede usar para crear un código de autenticación.

|**Tipo de aplicación**|**Biblioteca de autenticación**|
|------------------------|----------------------------|
|[Aplicaciones de escritorio - iOS](https://docs.microsoft.com/es-ES/azure/active-directory/develop/guidedsetups/active-directory-ios)|[MSAL.framework: Biblioteca de autenticación de Microsoft (versión preliminar para iOS)](https://github.com/AzureAD/microsoft-authentication-library-for-objc)|
|[Aplicaciones de escritorio - Android](https://docs.microsoft.com/es-ES/azure/active-directory/develop/guidedsetups/active-directory-android)|[Biblioteca de autenticación de Microsoft (MSAL)](https://javadoc.io/doc/com.microsoft.identity.client/msal)|
|[Aplicaciones de escritorio - .Net](https://docs.microsoft.com/es-ES/azure/active-directory/develop/guidedsetups/active-directory-windesktop)|[Biblioteca de autenticación de Microsoft (MSAL)](https://www.nuget.org/packages/Microsoft.Identity.Client)|
|[Aplicaciones web - JavaScript SPA](https://docs.microsoft.com/es-ES/azure/active-directory/develop/guidedsetups/active-directory-javascriptspa)|[Biblioteca de autenticación de Microsoft para JavaScript (versión preliminar)](https://github.com/AzureAD/microsoft-authentication-library-for-js)|
|[Aplicaciones web - Servidor web de .NET](https://docs.microsoft.com/es-ES/azure/active-directory/develop/guidedsetups/active-directory-aspnetwebapp)|OpenIdConnection, Cookies, SystemWeb|
|[Aplicaciones web - aplicaciones web NodeJS](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-devquickstarts-node-web)||

En el caso de las aplicaciones que no utilizan ninguna de las bibliotecas existentes, consulte [Obtener acceso en nombre de un usuario](auth-v2-user.md).

1. Obtenga un código de Azure AD. La consulta a la llamada contiene el parámetro de Id. de aplicación, Dirección URL de redirección y **los permisos necesarios**.
2. Use el código para obtener un token de acceso.

Si usa una biblioteca de OpenId Connect, consulte [Autenticarse con Azure AD y OpenID Connect](https://docs.microsoft.com/es-ES/azure/architecture/multitenant-identity/authenticate) y realice una llamada a `app.UseOpenIdConnectAuthentication()`.

>**Nota:** Si está solicitando tokens de autenticación delegados por el usuario, el parámetro de la biblioteca es **Ámbitos solicitados**. Use "User.Read" para este parámetro en lugar de lo que requiere la aplicación registrada. El parámetro **Ámbitos solicitados** NO afecta a los permisos que contienen los tokens de autenticación que se muestran. Estos dependen de los permisos que el administrador del espacio empresarial concede a la aplicación.

Por ejemplo, si usa la biblioteca de .NET MSAL, realice una llamada a lo siguiente:

`var accessToken = (await client.AcquireTokenAsync(scopes)).AccessToken;`

>**Nota:** Este ejemplo debe utilizar los permisos con privilegios mínimos, como "User.Read". Sin embargo, el token de acceso que se muestre puede contener los permisos concedidos por el administrador del espacio empresarial para el espacio empresarial del usuario actual, como "User.Read.All" o "User.ReadWrite.All".

Azure AD muestra un token (cadena) que contiene su información de autenticación y los permisos que necesita la aplicación. Asigne este token al encabezado HTTP como un token portador, tal como se muestra en el siguiente ejemplo.

`request.Headers.Authorization = new AuthenticationHeaderValue("bearer", accessToken);`

Microsoft Graph validará la información que contenga este token y concederá o rechazará el acceso.

Para ver notificaciones incluidas en el token que se muestre, use la biblioteca "System.IdentityModel.Tokens.Jwt" de NuGet.

`JwtSecurityTokenHandler tokenHandler = new JwtSecurityTokenHandler();`</br>
`var securityToken = tokenHandler.ReadToken(accessToken) as JwtSecurityToken;`

La respuesta de Microsoft Graph contiene un encabezado llamado "client-request-id", que es un GUID. Si se rechaza el acceso, especifique este GUID cuando obtenga asistencia técnica en [Microsoft Tech Community](https://techcommunity.microsoft.com/t5/Microsoft-Graph-Security-API/ct-p/SecurityGraphAPI). De esta forma, podremos ayudarlo a investigar la causa de este error de autenticación.
