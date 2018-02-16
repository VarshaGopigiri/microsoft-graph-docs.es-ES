# <a name="devicecompliancepolicystate-resource-type"></a>Tipo de recurso deviceCompliancePolicyState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estados de directivas de cumplimiento del dispositivo para un dispositivo determinado.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCompliancePolicyStates](../api/intune_deviceconfig_devicecompliancepolicystate_list.md)|Colección [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md)|Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md).|
|[Obtener deviceCompliancePolicyState](../api/intune_deviceconfig_devicecompliancepolicystate_get.md)|[deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md)|Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md).|
|[Crear deviceCompliancePolicyState](../api/intune_deviceconfig_devicecompliancepolicystate_create.md)|[deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md)|Cree un objeto [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md).|
|[Eliminar deviceCompliancePolicyState](../api/intune_deviceconfig_devicecompliancepolicystate_delete.md)|Ninguna|Elimina un [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md).|
|[Actualizar deviceCompliancePolicyState](../api/intune_deviceconfig_devicecompliancepolicystate_update.md)|[deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md)|Actualice las propiedades de un objeto [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|settingStates|Colección [deviceCompliancePolicySettingState](../resources/intune_deviceconfig_devicecompliancepolicysettingstate.md)|Todavía no documentado|
|displayName|cadena|El nombre de la directiva de este policyBase|
|versión|Int32|La versión de la directiva|
|platformType|cadena|Tipo de plataforma al que se aplica la directiva. Los valores posibles son: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `all`.|
|estado|cadena|Estado de cumplimiento de la directiva. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error` y `conflict`.|
|settingCount|Int32|Recuento del número de ajustes que contiene una directiva|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicyState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyState",
  "id": "String (identifier)",
  "settingStates": [
    {
      "@odata.type": "microsoft.graph.deviceCompliancePolicySettingState",
      "setting": "String",
      "settingName": "String",
      "instanceDisplayName": "String",
      "state": "String",
      "errorCode": 1024,
      "errorDescription": "String",
      "userId": "String",
      "userName": "String",
      "userEmail": "String",
      "userPrincipalName": "String",
      "sources": [
        {
          "@odata.type": "microsoft.graph.settingSource",
          "id": "String",
          "displayName": "String"
        }
      ],
      "currentValue": "String"
    }
  ],
  "displayName": "String",
  "version": 1024,
  "platformType": "String",
  "state": "String",
  "settingCount": 1024
}
```



