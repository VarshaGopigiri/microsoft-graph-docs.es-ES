---
title: tipo de recurso depMacOSEnrollmentProfile
description: El recurso DepMacOSEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP) específico para la configuración de Mac OS. Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.
author: tfitzmac
ms.openlocfilehash: 138acbdbdc8325a15d6532b836c9c8da9b1363de
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346091"
---
# <a name="depmacosenrollmentprofile-resource-type"></a>tipo de recurso depMacOSEnrollmentProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso DepMacOSEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP) específico para la configuración de Mac OS. Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.

Hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista depMacOSEnrollmentProfiles](../api/intune-enrollment-depmacosenrollmentprofile-list.md)|colección de [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md)|Propiedades de la lista y relaciones de los objetos [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) .|
|[Obtener depMacOSEnrollmentProfile](../api/intune-enrollment-depmacosenrollmentprofile-get.md)|[depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md)|Leer las propiedades y las relaciones del objeto [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) .|
|[Crear depMacOSEnrollmentProfile](../api/intune-enrollment-depmacosenrollmentprofile-create.md)|[depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md)|Crear un nuevo objeto [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) .|
|[Eliminar depMacOSEnrollmentProfile](../api/intune-enrollment-depmacosenrollmentprofile-delete.md)|Ninguno|Elimina un [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md).|
|[Actualizar depMacOSEnrollmentProfile](../api/intune-enrollment-depmacosenrollmentprofile-update.md)|[depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md)|Actualizar las propiedades de un objeto [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|displayName|String|Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|descripción|String|Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|requiresUserAuthentication|Boolean|Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|configurationEndpointUrl|String|Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|enableAuthenticationViaCompanyPortal|Boolean|Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa. Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|isDefault|Boolean|Indica si este es el perfil predeterminado heredado de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|supervisedModeEnabled|Boolean|Modo supervisado, True para habilitar, false en caso contrario. Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional. Se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|supportDepartment|String|Información de departamento de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|passCodeDisabled|Boolean|Indica si el código de acceso del programa de instalación panel está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|isMandatory|Boolean|Indica si el perfil es obligatorio heredada de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|locationDisabled|Boolean|Indica si la ubicación de panel de servicio del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|supportPhoneNumber|String|Número de teléfono de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|profileRemovalDisabled|Boolean|Indica si está deshabilitada la opción de eliminación de perfiles se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|restoreBlocked|Boolean|Indica si se bloquea el panel del programa de instalación de restauración se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|appleIdDisabled|Boolean|Indica si Apple panel de identificador del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|termsAndConditionsDisabled|Boolean|Indica si se deshabilita el panel del programa de instalación 'Términos y condiciones' se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|touchIdDisabled|Boolean|Indica si se deshabilita el panel de táctil identificador del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|applePayDisabled|Boolean|Indica si se deshabilita el panel de Apple pago del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|zoomDisabled|Boolean|Indica si se deshabilita el panel de zoom del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|siriDisabled|Boolean|Indica si se deshabilita el panel de siri el programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|diagnosticsDisabled|Boolean|Indica si el diagnóstico panel del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|
|registrationDisabled|Boolean|Indica si el registro está deshabilitado|
|fileVaultDisabled|Boolean|Indica si está deshabilitada la cámara de archivo|
|iCloudDiagnosticsDisabled|Boolean|Indica si se deshabilita la pantalla de análisis iCloud|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.depMacOSEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.depMacOSEnrollmentProfile",
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
  "registrationDisabled": true,
  "fileVaultDisabled": true,
  "iCloudDiagnosticsDisabled": true
}
```





