# <a name="importedwindowsautopilotdeviceidentity-resource-type"></a>tipo de recurso importedWindowsAutopilotDeviceIdentity

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Dispositivos importados de Windows Autopilot.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar importedWindowsAutopilotDeviceIdentities](../api/intune_enrollment_importedwindowsautopilotdeviceidentity_list.md)|Colección [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md)|Lista de propiedades y relaciones de los objetos [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).|
|[Obtener importedWindowsAutopilotDeviceIdentity](../api/intune_enrollment_importedwindowsautopilotdeviceidentity_get.md)|[importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md)|Lee las propiedades y relaciones de los objetos [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).|
|[Crear importedWindowsAutopilotDeviceIdentity](../api/intune_enrollment_importedwindowsautopilotdeviceidentity_create.md)|[importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md)|Crea un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md) nuevo.|
|[Eliminar importedWindowsAutopilotDeviceIdentity](../api/intune_enrollment_importedwindowsautopilotdeviceidentity_delete.md)|Ninguno|Elimina una [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).|
|[Actualizar importedWindowsAutopilotDeviceIdentity](../api/intune_enrollment_importedwindowsautopilotdeviceidentity_update.md)|[importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md)|Actualiza las propiedades de un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El GUID para el objeto|
|orderIdentifier|Cadena|Id. de pedido del dispositivo Windows Autopilot.|
|serialNumber|Cadena|Número de serie del dispositivo Windows Autopilot.|
|productKey|Cadena|Clave de producto del dispositivo Windows Autopilot.|
|hardwareIdentifier|Binario|Blob de hardware del dispositivo Windows Autopilot.|
|estado|[importedWindowsAutopilotDeviceIdentityState](../resources/intune_enrollment_importedwindowsautopilotdeviceidentitystate.md)|Estado actual del dispositivo importado.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentity"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentity",
  "id": "String (identifier)",
  "orderIdentifier": "String",
  "serialNumber": "String",
  "productKey": "String",
  "hardwareIdentifier": "binary",
  "state": {
    "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
    "deviceImportStatus": "String",
    "deviceRegistrationId": "String",
    "deviceErrorCode": 1024,
    "deviceErrorName": "String"
  }
}
```


