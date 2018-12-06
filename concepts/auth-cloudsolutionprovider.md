---
title: Llamar a Microsoft Graph desde una aplicación del proveedor de soluciones en la nube
description: En este tema se describe cómo habilitar el acceso de la aplicación a datos de clientes administrados por el asociado a través de Microsoft Graph mediante el flujo de concesión del código de autorización o del flujo de credenciales de cliente de servicio a servicio.
ms.openlocfilehash: a14c610090a1232c72ec2fde4469dd1cd1d6f694
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092858"
---
# <a name="call-microsoft-graph-from-a-cloud-solution-provider-application"></a>Llamar a Microsoft Graph desde una aplicación del proveedor de soluciones en la nube

> **Nota:** Este tema **solo** se aplica a los desarrolladores de aplicaciones del proveedor de soluciones en la nube (CSP) de Microsoft. El programa del [Proveedor de soluciones en la nube (CSP) de Microsoft](https://partner.microsoft.com/es-ES/cloud-solution-provider) permite a los asociados de Microsoft revender y administrar Microsoft Online Services para los clientes.

En este tema se describe cómo habilitar el acceso de la aplicación a datos de clientes administrados por el asociado a través de Microsoft Graph mediante el [flujo de concesión del código de autorización](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-protocols-oauth-code) o del [flujo de credenciales de cliente de servicio a servicio](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service).

**Importante:** Solo se permite llamar a Microsoft Graph desde una aplicación CSP para los recursos de directorio (como **usuario**, **grupo**,**dispositivo**, **organización**) y recursos de [Intune](/graph/api/resources/intune-graph-overview?view=graph-rest-beta).

## <a name="what-is-a-partner-managed-application"></a>¿Qué es una aplicación administrada por el asociado?

El programa CSP permite a los asociados de Microsoft revender y administrar Microsoft Online Services (como Office 365, Microsoft Azure y CRM Online) para los clientes. La administración de los servicios de cliente se realiza a través de privilegios de administración delegados, lo que permite que los usuarios asociados designados (denominados "agentes") tengan acceso a los entornos de sus clientes y los configuren.

Además, como desarrollador asociado, puede compilar una **aplicación administrada por el asociado** para administrar los servicios de Microsoft de sus clientes. Las aplicaciones administradas por el asociado suelen denominarse aplicaciones *aceptadas previamente*, ya que se acepta previamente a todos los clientes de forma automática para las aplicaciones administradas por el asociado. Esto significa que cuando un usuario de uno de los inquilinos de cliente usa una de las aplicaciones administradas por el asociado, el usuario puede usarla sin que se le pida el consentimiento. Las aplicaciones administradas por el asociado también heredan los privilegios de administración delegados, por lo que los agentes asociados también pueden obtener acceso privilegiado a los clientes a través de la aplicación administrada por el asociado.

## <a name="how-to-set-up-a-partner-managed-application"></a>Cómo configurar una aplicación administrada por el asociado

Una aplicación se muestra como *administrada por el asociado* cuando se le han concedido permisos elevados para tener acceso a los datos de los clientes.

> **Nota:** Las aplicaciones administradas por el asociado *solo* pueden configurarse en los inquilinos del asociado, y con el fin de administrar los recursos del inquilino cliente, las aplicaciones administradas por el asociado **deben** configurarse como **aplicaciones multiinquilino**.

### <a name="register-and-configure-a-multi-tenant-app"></a>Registrar y configurar una aplicación multiinquilino

Aquí, los pasos iniciales necesarios son, en su mayoría, los mismos que se usan para registrar y configurar una aplicación multiinquilino:

1. [Registre la aplicación](https://docs.microsoft.com/es-ES/azure/active-directory/active-directory-app-registration) en su inquilino asociado a través del [Azure Portal](https://portal.azure.com). Para que una aplicación funcione como administrada por el asociado, debe estar configurada como [aplicación multiinquilino](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#update-registration-to-be-multi-tenant). Además, si la aplicación se implementa y se vende en varias regiones geográficas, deberá registrarla en cada una de esas regiones, tal como se describe <a href="#region">aquí</a>.
2. Configure la aplicación multiinquilino, de nuevo a través de Azure Portal, con los *permisos necesarios* mediante un enfoque de privilegios mínimos.

### <a name="pre-consent-your-app-for-all-your-customers"></a>Consentimiento previo de la aplicación para todos los clientes

Por último, conceda a la aplicación administrada por el asociado los permisos configurados para todos los clientes. Para hacerlo, agregue la entidad de servicio (**servicePrincipal**) que representa la aplicación en el grupo *Adminagents* del inquilino asociado mediante PowerShell V2 para Azure AD. Puede descargar e instalar PowerShell V2 para Azure AD desde [aquí](https://www.powershellgallery.com/packages/AzureAD).  Siga estos pasos para encontrar el grupo *Adminagents*, la **servicePrincipal** y agregarla al grupo.

1. Abra una sesión de PowerShell y conéctese al inquilino asociado. Para ello, escriba sus credenciales de administrador en la ventana de inicio de sesión.

    ```PowerShell
    Connect-AzureAd
    ```

2. Busque el grupo *Adminagents*.

    ```PowerShell
    $group = Get-AzureADGroup -Filter "displayName eq 'Adminagents'"
    ```

3. Busque la entidad de servicio que tenga el mismo *appId* que su aplicación.

    ```PowerShell
    $sp = Get-AzureADServicePrincipal -Filter "appId eq '{yourAppsAppId}'"
    ```

4. Por último, agregue la entidad de servicio al grupo *Adminagents*.

    ```PowerShell
    Add-AzureADGroupMember -ObjectId $group.ObjectId -RefObjectId $sp.ObjectId
    ```

## <a name="token-acquisition-flows"></a>Flujos de adquisición de tokens

Los flujos de adquisición de tokens para las aplicaciones administradas por el asociado ([flujo de concesión del código de autorización](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-protocols-oauth-code) y [flujo de credenciales de cliente de servicio a servicio](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service)) son iguales a los de las aplicaciones multiinquilino normales.

Además del acceso aceptado previamente a todos los inquilinos del cliente, las aplicaciones administradas por el asociado tienen una función adicional que permite que los agentes usen la aplicación para tener acceso a los datos de inquilino de los clientes (mediante privilegios de administración delegados). Conceptualmente funciona de la siguiente manera:

1. El agente inicia sesión en la aplicación con sus credenciales de usuario emitidas por el inquilino de asociado.
2. La aplicación solicita un token de acceso para el inquilino de cliente administrado por el asociado previsto.
3. La aplicación usa el token de acceso para llamar a Microsoft Graph.

Se trata de un estándar de [flujo para conceder el código de autorización](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-protocols-oauth-code), salvo que los agentes deben iniciar sesión con sus cuentas de socio. Para ver el aspecto que tendría, imagine que el inquilino de asociado es *partner.com* (que es el inquilino principal de los agentes) y uno de los clientes es *customer.com*:

1. [Adquiera un código de autorización:](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-protocols-oauth-code#request-an-authorization-code) La aplicación crea una solicitud para el punto de conexión ```/authorize``` y debe usar un **inquilino de cliente** (en nuestro ejemplo, ```customer.com```) para el inquilino de destino. Los agentes iniciarían sesión con su cuenta ```username@partner.com```.

    ```http
    GET https://login.microsoftonline.com/customer.com/oauth2/authorize
    ```

2. [Adquiera un token de acceso mediante el código de autorización:](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-protocols-oauth-code#use-the-authorization-code-to-request-an-access-token) La aplicación debe usar un **inquilino de cliente** como inquilino de destino (en nuestro ejemplo, ```customer.com```) al realizar la solicitud al punto de conexión ```token```:

    ```http
    POST https://login.microsoftonline.com/customer.com/oauth2/token
    ```

3. Ahora que tiene un token de acceso, llame a Microsoft Graph. Para ello, ponga el token de acceso en el encabezado de autorización HTTP:

    ```http
    GET https://graph.microsoft.com/beta/users
    Authorization: Bearer <token>
    ```

## <a name="register-your-app-in-the-regions-you-support"></a>Registrar la aplicación en las regiones admitidas
<a name="region"></a>

El compromiso con el cliente CSP está limitado actualmente a una sola región. Las aplicaciones administradas por el asociado conllevan la misma limitación. Esto significa que debe disponer de un inquilino independiente para cada región en la que venda. Por ejemplo, si la aplicación administrada por el asociado está registrada en un inquilino de los Estados Unidos pero el cliente está en la UE, la aplicación administrada por el asociado no funcionará.  Cada uno de los inquilinos de asociado regionales debe mantener su propio conjunto de aplicaciones administradas por el asociado para administrar a los clientes de la misma región. Esto podría requerir lógica adicional en la aplicación (antes del inicio de sesión) para obtener el nombre de usuario de inicio de sesión de los clientes, a fin de decidir qué identidad de la aplicación administrada por el asociado específica de la región se debe usar para dar servicio al usuario.

## <a name="calling-microsoft-graph-immediately-after-customer-creation"></a>Llamar a Microsoft Graph inmediatamente después de la creación del cliente

Cuando se crea un cliente mediante la [API Partner Center](https://partnercenter.microsoft.com/es-ES/partner/developer), se crea un inquilino de cliente. Además, también se crea una relación de asociado, que lo convierte a usted en asociado de registro para este nuevo inquilino de cliente. Esta relación de asociado puede tardar hasta tres minutos en propagarse al nuevo inquilino de cliente. Si la aplicación llama a Microsoft Graph justo después de la creación, es probable que reciba un error de acceso denegado. Es posible que experimente un retraso similar cuando un cliente existente acepte su invitación. Esto se debe a que la aceptación previa se basa en la relación de asociado presente en el inquilino de cliente.

Para evitar este problema, se recomienda que la aplicación de asociado espere **tres minutos** tras la creación del cliente antes de llamar a Azure AD para adquirir un token (a fin de llamar a Microsoft Graph). Esto debería abarcar la mayoría de los casos. Pero si al cabo de tres minutos sigue recibiendo un error de autorización, espere otros 60 segundos y vuelva a intentarlo.

> **Nota:** Durante el reintento, debe adquirir un nuevo token de acceso de Azure AD antes de llamar a Microsoft Graph.  No podrá llamar a Microsoft Graph con el token de acceso que ya tiene, ya que este es válido durante una hora y no contendrá las notificaciones del permiso aceptado previamente.
