---
title: Actualizar windowsIdentityProtectionConfiguration
description: Actualizar las propiedades de un objeto windowsIdentityProtectionConfiguration.
author: tfitzmac
ms.openlocfilehash: 4131672de21560311ee1c2c1f8c1eb930a3de255
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326897"
---
# <a name="update-windowsidentityprotectionconfiguration"></a>Actualizar windowsIdentityProtectionConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Boolean|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|enhancedAntiSpoofingForFacialFeaturesEnabled|Boolean|Valor booleano que se usa para permitir mejorada contra la suplantación de reconocimiento de característica faciales acerca de la autenticación de Windows Hola cara.|
|pinMinimumLength|Int32|Valor entero que establece el número mínimo de caracteres necesarios para el Windows Hello de PIN de negocio. Los valores válidos son de 4 a 127 inclusive y menor o igual que el valor establecido para el PIN máximo. Valores válidos 4 a 127|
|pinMaximumLength|Int32|Valor entero que establece el número máximo de caracteres permitidos para el trabajo PIN. Los valores válidos son de 4 a 127 inclusive y mayor o igual que el valor establecido para el PIN mínimo. Valores válidos 4 a 127|
|pinUppercaseCharactersUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Este valor configura el uso de caracteres en mayúsculas en el Windows Hello para profesionales PIN. Los valores posibles son: `blocked`, `required` y `allowed`.|
|pinLowercaseCharactersUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Este valor configura el uso de caracteres en minúsculas en el Windows Hello para profesionales PIN. Los valores posibles son: `blocked`, `required` y `allowed`.|
|pinSpecialCharactersUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Controla la capacidad de usar caracteres especiales en el Windows Hello para profesionales PIN. Los valores posibles son: `blocked`, `required` y `allowed`.|
|pinExpirationInDays|Int32|Valor entero especifica el período (en días) que se puede usar un NIP antes de que el sistema requiere que el usuario que la cambie. Los valores válidos son 0 a 730 inclusive. Valores válidos de 0 a 730.|
|pinPreviousBlockCount|Int32|Controla la capacidad para impedir que los usuarios utilicen más allá de los PIN. Esto se debe establecer entre 0 y 50, ambos inclusive, y el PIN del usuario actual se incluye en ese número. Si se establece en 0, anterior no se almacenan los PIN. No se conserva el historial de PIN a través de un PIN restablecer. Valores válidos de 0 a 50.|
|pinRecoveryEnabled|Boolean|Valor booleano que permite a un usuario cambiar su PIN mediante el Windows Hello para servicio de recuperación de PIN de negocio.|
|securityDeviceRequired|Booleano|Controla si se debe requerir un módulo de plataforma segura (TPM) para aprovisionamiento Windows Hello para la empresa. Un TPM proporciona una ventaja de seguridad adicional en que los datos almacenados en él no se puede usar en otros dispositivos. Si se establece en False, todos los dispositivos pueden aprovisionar Windows Hello para la empresa, incluso si no hay un TPM utilizable.|
|unlockWithBiometricsEnabled|Booleano|Controla el uso de gestos biométricas, como cara y de huella digital, como una alternativa a la Windows Hola de PIN de negocio.  Si se establece en False, biométricas gestos no se permite. Los usuarios aún deben configurar un PIN como una copia de seguridad en caso de errores.|
|useCertificatesForOnPremisesAuthEnabled|Boolean|Valor booleano que permite Windows Hello para la empresa a usar certificados para autenticar los recursos locales.|
|windowsHelloForBusinessBlocked|Boolean|Valor booleano que bloquea Windows Hello para la empresa como un método para iniciar sesión en Windows.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 761

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enhancedAntiSpoofingForFacialFeaturesEnabled": true,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "pinExpirationInDays": 3,
  "pinPreviousBlockCount": 5,
  "pinRecoveryEnabled": true,
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "useCertificatesForOnPremisesAuthEnabled": true,
  "windowsHelloForBusinessBlocked": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 946

{
  "@odata.type": "#microsoft.graph.windowsIdentityProtectionConfiguration",
  "id": "b2e64303-4303-b2e6-0343-e6b20343e6b2",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enhancedAntiSpoofingForFacialFeaturesEnabled": true,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "pinExpirationInDays": 3,
  "pinPreviousBlockCount": 5,
  "pinRecoveryEnabled": true,
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "useCertificatesForOnPremisesAuthEnabled": true,
  "windowsHelloForBusinessBlocked": true
}
```





