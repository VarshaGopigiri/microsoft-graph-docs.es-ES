---
title: Crear depEnrollmentProfile
description: Crear un nuevo objeto depEnrollmentProfile.
ms.openlocfilehash: 52a099afe1322aa07f893190ebf7cc50ecde7a06
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085762"
---
# <a name="create-depenrollmentprofile"></a>Crear depEnrollmentProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un nuevo objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementServiceConfig.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto depEnrollmentProfile.

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el depEnrollmentProfile.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|displayName|String|Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|descripción|String|Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|requiresUserAuthentication|Booleano|Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|configurationEndpointUrl|String|Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|enableAuthenticationViaCompanyPortal|Booleano|Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa. Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|isDefault|Booleano|Indica si este es el perfil predeterminado|
|supervisedModeEnabled|Booleano|Modo supervisado, True para habilitar, false en caso contrario. Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.|
|supportDepartment|String|Información del departamento de soporte técnico|
|passCodeDisabled|Booleano|Indica si se deshabilita el panel de código de acceso del programa de instalación|
|isMandatory|Booleano|Indica si el perfil es obligatorio|
|locationDisabled|Booleano|Indica si se deshabilita el panel del programa de instalación del servicio de ubicación|
|supportPhoneNumber|String|Número de teléfono de soporte técnico|
|iTunesPairingMode|[iTunesPairingMode](../resources/intune-enrollment-itunespairingmode.md)|Indica el modo de emparejamiento de iTunes. Los valores posibles son: `disallow`, `allow` y `requiresCertificate`.|
|profileRemovalDisabled|Booleano|Indica si está deshabilitada la opción de eliminación de perfiles|
|managementCertificates|colección de [managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md)|Certificados de administración para Configurador de Apple|
|restoreBlocked|Booleano|Indica si se bloquea el panel de restauración del programa de instalación|
|restoreFromAndroidDisabled|Booleano|Indica si está deshabilitado restaurar a partir de Android|
|appleIdDisabled|Booleano|Indica si se deshabilita el panel de Apple identificador del programa de instalación|
|termsAndConditionsDisabled|Booleano|Indica si el panel del programa de instalación 'Términos y condiciones' está deshabilitado|
|touchIdDisabled|Booleano|Indica si se deshabilita el panel de táctil identificador del programa de instalación|
|applePayDisabled|Booleano|Indica si se deshabilita el panel de Apple pago del programa de instalación|
|zoomDisabled|Booleano|Indica si se deshabilita el panel de zoom del programa de instalación|
|siriDisabled|Booleano|Indica si se deshabilita el panel de siri el programa de instalación|
|diagnosticsDisabled|Booleano|Indica si se deshabilita el panel de diagnóstico del programa de instalación|
|macOSRegistrationDisabled|Booleano|Indica si se deshabilita el registro de Mac OS|
|macOSFileVaultDisabled|Booleano|Indica si está deshabilitada la cámara de archivo Mac OS|
|awaitDeviceConfiguredConfirmation|Booleano|Indica si el dispositivo será necesario esperar confirmación configurado|
|sharedIPadMaximumUserCount|Int32|Especifica el número máximo de usuarios que pueden usar un iPad compartida. Solo se aplica en modo compartido iPad.|
|enableSharedIPad|Booleano|Esto indica si el dispositivo se se inscriben en un modo que permite los escenarios de usuario múltiple. Solo se aplica en iPad compartida.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
Content-type: application/json
Content-length: 1290

{
  "@odata.type": "#microsoft.graph.depEnrollmentProfile",
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true,
  "isDefault": true,
  "supervisedModeEnabled": true,
  "supportDepartment": "Support Department value",
  "passCodeDisabled": true,
  "isMandatory": true,
  "locationDisabled": true,
  "supportPhoneNumber": "Support Phone Number value",
  "iTunesPairingMode": "allow",
  "profileRemovalDisabled": true,
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "Thumbprint value",
      "certificate": "Certificate value"
    }
  ],
  "restoreBlocked": true,
  "restoreFromAndroidDisabled": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true,
  "macOSRegistrationDisabled": true,
  "macOSFileVaultDisabled": true,
  "awaitDeviceConfiguredConfirmation": true,
  "sharedIPadMaximumUserCount": 10,
  "enableSharedIPad": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1339

{
  "@odata.type": "#microsoft.graph.depEnrollmentProfile",
  "id": "3d4534f7-34f7-3d45-f734-453df734453d",
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true,
  "isDefault": true,
  "supervisedModeEnabled": true,
  "supportDepartment": "Support Department value",
  "passCodeDisabled": true,
  "isMandatory": true,
  "locationDisabled": true,
  "supportPhoneNumber": "Support Phone Number value",
  "iTunesPairingMode": "allow",
  "profileRemovalDisabled": true,
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "Thumbprint value",
      "certificate": "Certificate value"
    }
  ],
  "restoreBlocked": true,
  "restoreFromAndroidDisabled": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true,
  "macOSRegistrationDisabled": true,
  "macOSFileVaultDisabled": true,
  "awaitDeviceConfiguredConfirmation": true,
  "sharedIPadMaximumUserCount": 10,
  "enableSharedIPad": true
}
```





