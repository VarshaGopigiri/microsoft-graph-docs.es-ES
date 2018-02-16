# <a name="deviceenrollmentwindowshelloforbusinessconfiguration-resource-type"></a>Tipo de recurso deviceEnrollmentWindowsHelloForBusinessConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado

Hereda de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceEnrollmentWindowsHelloForBusinessConfigurations](../api/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration_list.md)|Colección [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).|
|[Obtener deviceEnrollmentWindowsHelloForBusinessConfiguration](../api/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration_get.md)|[deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md)|Lea las propiedades y las relaciones del objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).|
|[Crear deviceEnrollmentWindowsHelloForBusinessConfiguration](../api/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration_create.md)|[deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md)|Cree un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).|
|[Eliminar deviceEnrollmentWindowsHelloForBusinessConfiguration](../api/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration_delete.md)|Ninguna|Elimina un [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).|
|[Actualizar deviceEnrollmentWindowsHelloForBusinessConfiguration](../api/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration_update.md)|[deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md)|Actualice las propiedades de un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|
|displayName|cadena|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|
|descripción|cadena|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|
|prioridad|Int32|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|
|createdDateTime|DateTimeOffset|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|
|versión|Int32|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|
|pinMinimumLength|Int32|Todavía no documentado|
|pinMaximumLength|Int32|Todavía no documentado|
|pinUppercaseCharactersUsage|cadena|Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.|
|pinLowercaseCharactersUsage|cadena|Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.|
|pinSpecialCharactersUsage|cadena|Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.|
|estado|cadena|Todavía no documentado Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|securityDeviceRequired|Booleano|Todavía no documentado|
|unlockWithBiometricsEnabled|Booleano|Todavía no documentado|
|remotePassportEnabled|Booleano|Todavía no documentado|
|pinPreviousBlockCount|Int32|Todavía no documentado|
|pinExpirationInDays|Int32|Todavía no documentado|
|enhancedBiometricsState|cadena|Todavía no documentado Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|Asignaciones|Colección [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo. Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "priority": 1024,
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "version": 1024,
  "pinMinimumLength": 1024,
  "pinMaximumLength": 1024,
  "pinUppercaseCharactersUsage": "String",
  "pinLowercaseCharactersUsage": "String",
  "pinSpecialCharactersUsage": "String",
  "state": "String",
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "remotePassportEnabled": true,
  "pinPreviousBlockCount": 1024,
  "pinExpirationInDays": 1024,
  "enhancedBiometricsState": "String"
}
```



