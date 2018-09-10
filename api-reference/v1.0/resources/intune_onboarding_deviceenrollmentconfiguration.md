# <a name="deviceenrollmentconfiguration-resource-type"></a>Tipo de recurso deviceEnrollmentConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceEnrollmentConfigurations](../api/intune_onboarding_deviceenrollmentconfiguration_list.md)|Colección [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md).|
|[Obtener deviceEnrollmentConfiguration](../api/intune_onboarding_deviceenrollmentconfiguration_get.md)|[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|Lea las propiedades y las relaciones del objeto [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md).|
|[Acción setPriority](../api/intune_onboarding_deviceenrollmentconfiguration_setpriority.md)|Ninguna|Todavía no documentado|
|[Acción assign](../api/intune_onboarding_deviceenrollmentconfiguration_assign.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Todavía no documentado|
|displayName|Cadena|Todavía no documentado|
|descripción|Cadena|Todavía no documentado|
|prioridad|Int32|Todavía no documentado|
|createdDateTime|DateTimeOffset|Todavía no documentado|
|lastModifiedDateTime|DateTimeOffset|Todavía no documentado|
|versión|Int32|Todavía no documentado|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|Asignaciones|Colección [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceEnrollmentConfiguration"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentConfiguration",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "priority": 1024,
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "version": 1024
}
```








