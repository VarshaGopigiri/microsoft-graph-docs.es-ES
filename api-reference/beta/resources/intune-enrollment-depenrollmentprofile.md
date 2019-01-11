---
title: tipo de recurso depEnrollmentProfile
description: El recurso depEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP). Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: da2bd0415abfeefb6e7a330663ed51cb9e5de271
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849087"
---
# <a name="depenrollmentprofile-resource-type"></a>tipo de recurso depEnrollmentProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso depEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP). Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.

Hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista depEnrollmentProfiles](../api/intune-enrollment-depenrollmentprofile-list.md)|colección de [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md)|Propiedades de la lista y relaciones de los objetos [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .|
|[Obtener depEnrollmentProfile](../api/intune-enrollment-depenrollmentprofile-get.md)|[depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md)|Leer las propiedades y las relaciones del objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .|
|[Crear depEnrollmentProfile](../api/intune-enrollment-depenrollmentprofile-create.md)|[depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md)|Crear un nuevo objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .|
|[Eliminar depEnrollmentProfile](../api/intune-enrollment-depenrollmentprofile-delete.md)|Ninguno|Elimina un [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md).|
|[Actualizar depEnrollmentProfile](../api/intune-enrollment-depenrollmentprofile-update.md)|[depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md)|Actualizar las propiedades de un objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|displayName|Cadena|Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|descripción|Cadena|Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|requiresUserAuthentication|Booleano|Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|configurationEndpointUrl|Cadena|Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|enableAuthenticationViaCompanyPortal|Booleano|Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa. Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|isDefault|Booleano|Indica si este es el perfil predeterminado|
|supervisedModeEnabled|Booleano|Modo supervisado, True para habilitar, false en caso contrario. Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.|
|supportDepartment|Cadena|Información del departamento de soporte técnico|
|passCodeDisabled|Booleano|Indica si se deshabilita el panel de código de acceso del programa de instalación|
|isMandatory|Booleano|Indica si el perfil es obligatorio|
|locationDisabled|Booleano|Indica si se deshabilita el panel del programa de instalación del servicio de ubicación|
|supportPhoneNumber|Cadena|Número de teléfono de soporte técnico|
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

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.depEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.depEnrollmentProfile",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "String",
  "enableAuthenticationViaCompanyPortal": true,
  "isDefault": true,
  "supervisedModeEnabled": true,
  "supportDepartment": "String",
  "passCodeDisabled": true,
  "isMandatory": true,
  "locationDisabled": true,
  "supportPhoneNumber": "String",
  "iTunesPairingMode": "String",
  "profileRemovalDisabled": true,
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "String",
      "certificate": "String"
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
  "sharedIPadMaximumUserCount": 1024,
  "enableSharedIPad": true
}
```





