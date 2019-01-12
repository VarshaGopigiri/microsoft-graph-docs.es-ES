---
title: tipo de recurso depIOSEnrollmentProfile
description: El recurso DepIOSEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP) específico para la configuración de iOS. Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 92a5e277f0356445ae1dd36c3a643d73624e2207
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985616"
---
# <a name="depiosenrollmentprofile-resource-type"></a>tipo de recurso depIOSEnrollmentProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso DepIOSEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP) específico para la configuración de iOS. Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.

Hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista depIOSEnrollmentProfiles](../api/intune-enrollment-depiosenrollmentprofile-list.md)|colección de [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md)|Propiedades de la lista y relaciones de los objetos [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .|
|[Obtener depIOSEnrollmentProfile](../api/intune-enrollment-depiosenrollmentprofile-get.md)|[depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md)|Leer las propiedades y las relaciones del objeto [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .|
|[Crear depIOSEnrollmentProfile](../api/intune-enrollment-depiosenrollmentprofile-create.md)|[depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md)|Crear un nuevo objeto [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .|
|[Eliminar depIOSEnrollmentProfile](../api/intune-enrollment-depiosenrollmentprofile-delete.md)|Ninguno|Elimina un [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md).|
|[Actualizar depIOSEnrollmentProfile](../api/intune-enrollment-depiosenrollmentprofile-update.md)|[depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md)|Actualizar las propiedades de un objeto [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|displayName|Cadena|Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|descripción|Cadena|Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|requiresUserAuthentication|Booleano|Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|configurationEndpointUrl|Cadena|Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|enableAuthenticationViaCompanyPortal|Booleano|Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa. Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|isDefault|Booleano|Indica si este es el perfil predeterminado heredado de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|supervisedModeEnabled|Booleano|Modo supervisado, True para habilitar, false en caso contrario. Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional. Se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|supportDepartment|Cadena|Información de departamento de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|passCodeDisabled|Booleano|Indica si el código de acceso del programa de instalación panel está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|isMandatory|Booleano|Indica si el perfil es obligatorio heredada de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|locationDisabled|Booleano|Indica si la ubicación de panel de servicio del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|supportPhoneNumber|Cadena|Número de teléfono de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|profileRemovalDisabled|Booleano|Indica si está deshabilitada la opción de eliminación de perfiles se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|restoreBlocked|Booleano|Indica si se bloquea el panel del programa de instalación de restauración se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|appleIdDisabled|Booleano|Indica si Apple panel de identificador del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|termsAndConditionsDisabled|Booleano|Indica si se deshabilita el panel del programa de instalación 'Términos y condiciones' se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|touchIdDisabled|Booleano|Indica si se deshabilita el panel de táctil identificador del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|applePayDisabled|Booleano|Indica si se deshabilita el panel de Apple pago del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|zoomDisabled|Booleano|Indica si se deshabilita el panel de zoom del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|siriDisabled|Booleano|Indica si se deshabilita el panel de siri el programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|diagnosticsDisabled|Booleano|Indica si el diagnóstico panel del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|iTunesPairingMode|[iTunesPairingMode](../resources/intune-enrollment-itunespairingmode.md)|Indica el modo de emparejamiento de iTunes. Los valores posibles son: `disallow`, `allow` y `requiresCertificate`.|
|managementCertificates|colección de [managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md)|Certificados de administración para Configurador de Apple|
|restoreFromAndroidDisabled|Booleano|Indica si está deshabilitado restaurar a partir de Android|
|awaitDeviceConfiguredConfirmation|Booleano|Indica si el dispositivo será necesario esperar confirmación configurado|
|sharedIPadMaximumUserCount|Int32|Especifica el número máximo de usuarios que pueden usar un iPad compartida. Solo se aplica en modo compartido iPad.|
|enableSharedIPad|Booleano|Esto indica si el dispositivo se se inscriben en un modo que permite los escenarios de usuario múltiple. Solo se aplica en iPad compartida.|
|companyPortalVppTokenId|Cadena|Si establece, indica qué token Vpp debe usarse para implementar el Portal de la empresa con licencias de dispositivo. 'enableAuthenticationViaCompanyPortal' debe establecerse en orden establecer esta propiedad.|
|enableSingleAppEnrollmentMode|Booleano|Indica el dispositivo para habilitar el modo de aplicación único y aplicar el bloqueo de la aplicación durante la inscripción. Valor predeterminado es false. 'enableAuthenticationViaCompanyPortal' y 'companyPortalVppTokenId' se deben establecer para que esta propiedad que se va a establecer.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.depIOSEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.depIOSEnrollmentProfile",
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
  "profileRemovalDisabled": true,
  "restoreBlocked": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true,
  "iTunesPairingMode": "String",
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "String",
      "certificate": "String"
    }
  ],
  "restoreFromAndroidDisabled": true,
  "awaitDeviceConfiguredConfirmation": true,
  "sharedIPadMaximumUserCount": 1024,
  "enableSharedIPad": true,
  "companyPortalVppTokenId": "String",
  "enableSingleAppEnrollmentMode": true
}
```





