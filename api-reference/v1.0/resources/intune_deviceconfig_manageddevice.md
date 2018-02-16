# <a name="manageddevice-resource-type"></a>Tipo de recurso managedDevice

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Dispositivos administrados o inscritos previamente a través de Intune
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedDevices](../api/intune_deviceconfig_manageddevice_list.md)|Colección [managedDevice](../resources/intune_deviceconfig_manageddevice.md)|Enumere las propiedades y las relaciones de los objetos [managedDevice](../resources/intune_deviceconfig_manageddevice.md).|
|[Obtener managedDevice](../api/intune_deviceconfig_manageddevice_get.md)|[managedDevice](../resources/intune_deviceconfig_manageddevice.md)|Lea las propiedades y las relaciones del objeto [managedDevice](../resources/intune_deviceconfig_manageddevice.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Todavía no documentado|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceConfigurationStates|Colección [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md)|Estados de configuración del dispositivo para este dispositivo.|
|deviceCompliancePolicyStates|Colección [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md)|Estados de directivas de cumplimiento del dispositivo para este dispositivo.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDevice"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDevice",
  "id": "String (identifier)"
}
```



