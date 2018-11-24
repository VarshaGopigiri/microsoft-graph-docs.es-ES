# <a name="deviceconfigurationsettingstate-resource-type"></a>Tipo de recurso deviceConfigurationSettingState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de la configuración de dispositivos de un dispositivo determinado.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|ajustes|cadena|La configuración que se está notificando|
|settingName|cadena|Nombre descriptivo de la configuración de usuario o localizada que se está notificando|
|instanceDisplayName|cadena|Nombre de la instancia de configuración que se está notificando.|
|estado|[complianceStatus](../resources/intune_shared_compliancestatus.md)|El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|errorCode|Int64|Código de error de la configuración|
|errorDescription|Cadena|Descripción del error|
|userId|Cadena|UserId|
|userName|Cadena|UserName|
|userEmail|Cadena|UserEmail|
|userPrincipalName|String|UserPrincipalName.|
|orígenes|Colección [settingSource](../resources/intune_deviceconfig_settingsource.md)|Directivas colaboradoras|
|currentValue|Cadena|Valor actual de la configuración en el dispositivo|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceConfigurationSettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationSettingState",
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
```



