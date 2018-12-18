---
title: tipo de recurso depEnrollmentBaseProfile
description: El recurso DepEnrollmentBaseProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP). Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.
author: tfitzmac
ms.openlocfilehash: 26335fd3d35494b815dd43531ad54b4796dc861c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308375"
---
# <a name="depenrollmentbaseprofile-resource-type"></a>tipo de recurso depEnrollmentBaseProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso DepEnrollmentBaseProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP). Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.

Hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista depEnrollmentBaseProfiles](../api/intune-enrollment-depenrollmentbaseprofile-list.md)|colección de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|Propiedades de la lista y relaciones de los objetos [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) .|
|[Obtener depEnrollmentBaseProfile](../api/intune-enrollment-depenrollmentbaseprofile-get.md)|[depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)|Leer las propiedades y las relaciones del objeto [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|displayName|String|Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|descripción|String|Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|requiresUserAuthentication|Boolean|Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|configurationEndpointUrl|String|Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|enableAuthenticationViaCompanyPortal|Boolean|Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa. Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|
|isDefault|Boolean|Indica si este es el perfil predeterminado|
|supervisedModeEnabled|Boolean|Modo supervisado, True para habilitar, false en caso contrario. Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.|
|supportDepartment|String|Información del departamento de soporte técnico|
|passCodeDisabled|Boolean|Indica si se deshabilita el panel de código de acceso del programa de instalación|
|isMandatory|Boolean|Indica si el perfil es obligatorio|
|locationDisabled|Boolean|Indica si se deshabilita el panel del programa de instalación del servicio de ubicación|
|supportPhoneNumber|String|Número de teléfono de soporte técnico|
|profileRemovalDisabled|Boolean|Indica si está deshabilitada la opción de eliminación de perfiles|
|restoreBlocked|Boolean|Indica si se bloquea el panel de restauración del programa de instalación|
|appleIdDisabled|Boolean|Indica si se deshabilita el panel de Apple identificador del programa de instalación|
|termsAndConditionsDisabled|Boolean|Indica si el panel del programa de instalación 'Términos y condiciones' está deshabilitado|
|touchIdDisabled|Boolean|Indica si se deshabilita el panel de táctil identificador del programa de instalación|
|applePayDisabled|Boolean|Indica si se deshabilita el panel de Apple pago del programa de instalación|
|zoomDisabled|Boolean|Indica si se deshabilita el panel de zoom del programa de instalación|
|siriDisabled|Boolean|Indica si se deshabilita el panel de siri el programa de instalación|
|diagnosticsDisabled|Boolean|Indica si se deshabilita el panel de diagnóstico del programa de instalación|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.depEnrollmentBaseProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.depEnrollmentBaseProfile",
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
  "diagnosticsDisabled": true
}
```





