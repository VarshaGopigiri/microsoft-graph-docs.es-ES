# <a name="deviceconfigurationstate-resource-type"></a>Tipo de recurso deviceConfigurationState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de configuración de dispositivos para un dispositivo determinado.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurationStates](../api/intune_deviceconfig_deviceconfigurationstate_list.md)|Colección [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).|
|[Obtener deviceConfigurationState](../api/intune_deviceconfig_deviceconfigurationstate_get.md)|[deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).|
|[Crear deviceConfigurationState](../api/intune_deviceconfig_deviceconfigurationstate_create.md)|[deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md)|Cree un objeto [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).|
|[Eliminar deviceConfigurationState](../api/intune_deviceconfig_deviceconfigurationstate_delete.md)|Ninguna|Elimina un [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).|
|[Actualizar deviceConfigurationState](../api/intune_deviceconfig_deviceconfigurationstate_update.md)|[deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md)|Actualice las propiedades de un objeto [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|settingStates|Colección [deviceConfigurationSettingState](../resources/intune_deviceconfig_deviceconfigurationsettingstate.md)|Todavía no documentado|
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
  "@odata.type": "microsoft.graph.deviceConfigurationState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationState",
  "id": "String (identifier)",
  "settingStates": [
    {
      "@odata.type": "microsoft.graph.deviceConfigurationSettingState",
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



