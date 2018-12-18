---
title: tipo de recurso depOnboardingSetting
description: El depOnboardingSetting representa una instancia del servicio de Apple DEP que se va a onboarded a Intune. La instancia de servicio onboarded administra la utiliza para sincronizar datos entre Apple y Intune un Token de Apple.
author: tfitzmac
ms.openlocfilehash: ac38b1716dd156c95fda9cee8fb76a9f75921b0f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341163"
---
# <a name="deponboardingsetting-resource-type"></a>tipo de recurso depOnboardingSetting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El depOnboardingSetting representa una instancia del servicio de Apple DEP que se va a onboarded a Intune. La instancia de servicio onboarded administra la utiliza para sincronizar datos entre Apple y Intune un Token de Apple.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista depOnboardingSettings](../api/intune-enrollment-deponboardingsetting-list.md)|colección de [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md)|Propiedades de la lista y relaciones de los objetos [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .|
|[Obtener depOnboardingSetting](../api/intune-enrollment-deponboardingsetting-get.md)|[depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md)|Leer las propiedades y las relaciones del objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .|
|[Crear depOnboardingSetting](../api/intune-enrollment-deponboardingsetting-create.md)|[depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md)|Crear un nuevo objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .|
|[Eliminar depOnboardingSetting](../api/intune-enrollment-deponboardingsetting-delete.md)|Ninguno|Elimina un [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md).|
|[Actualizar depOnboardingSetting](../api/intune-enrollment-deponboardingsetting-update.md)|[depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md)|Actualizar las propiedades de un objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .|
|[getEncryptionPublicKey (función)](../api/intune-enrollment-deponboardingsetting-getencryptionpublickey.md)|String|Obtener una clave pública se utiliza para cifrar el programa de inscripción de dispositivos de Apple símbolo (token)|
|[acción uploadDepToken](../api/intune-enrollment-deponboardingsetting-uploaddeptoken.md)|Ninguno|Carga un nuevo token de programa de inscripción de dispositivo|
|[acción syncWithAppleDeviceEnrollmentProgram](../api/intune-enrollment-deponboardingsetting-syncwithappledeviceenrollmentprogram.md)|Ninguno|Sincroniza entre Intune y programa de inscripción de dispositivos de Apple|
|[acción shareForSchoolDataSyncService](../api/intune-enrollment-deponboardingsetting-shareforschooldatasyncservice.md)|Ninguno|Todavía no documentado|
|[acción unshareForSchoolDataSyncService](../api/intune-enrollment-deponboardingsetting-unshareforschooldatasyncservice.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|UUID para el objeto|
|appleIdentifier|String|El identificador de Apple se utiliza para obtener el token actual.|
|tokenExpirationDateTime|DateTimeOffset|Cuando caduca el token.|
|lastModifiedDateTime|DateTimeOffset|Cuando el servicio fue onboarded.|
|lastSuccessfulSyncDateTime|DateTimeOffset|Cuando el syned último servicio con Intune|
|lastSyncTriggeredDateTime|DateTimeOffset|Cuando Intune solicitada por última vez una sincronización.|
|shareTokenWithSchoolDataSyncService|Boolean|Si el símbolo (token) de la característica Dep compartir está habilitada o no con el servicio de sincronización de datos de School.|
|lastSyncErrorCode|Int32|Código de error que informa Apple durante la última sincronización de la característica dep.|
|TokenType en|[depTokenType](../resources/intune-enrollment-deptokentype.md)|Obtiene o establece el tipo de símbolo (token) de la característica Dep. Los valores posibles son: `none`, `dep` y `appleSchoolManager`.|
|tokenName|String|Nombre descriptivo para la característica Dep símbolo (token)|
|syncedDeviceCount|Int32|Obtiene sincronizado recuento de dispositivo|
|defaultProfileDisplayName|String|Obtiene sincronizado recuento de dispositivo|
|dataSharingConsentGranted|Boolean|Concede de consentimiento para uso compartido con Apple Dep servicio de datos|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|defaultIosEnrollmentProfile|[depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md)|De forma predeterminada iOS perfil de inscripción|
|defaultMacOsEnrollmentProfile|[depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md)|Perfil predeterminado de inscripción Mac OS|
|enrollmentProfiles|colección de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|Los perfiles de inscripción.|
|importedAppleDeviceIdentities|colección de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|Las identidades de dispositivo importadas de Apple.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.depOnboardingSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.depOnboardingSetting",
  "id": "String (identifier)",
  "appleIdentifier": "String",
  "tokenExpirationDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "lastSuccessfulSyncDateTime": "String (timestamp)",
  "lastSyncTriggeredDateTime": "String (timestamp)",
  "shareTokenWithSchoolDataSyncService": true,
  "lastSyncErrorCode": 1024,
  "tokenType": "String",
  "tokenName": "String",
  "syncedDeviceCount": 1024,
  "defaultProfileDisplayName": "String",
  "dataSharingConsentGranted": true
}
```





