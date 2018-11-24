# <a name="deviceinstallstate-resource-type"></a>Tipo de recurso deviceInstallState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del estado de la instalación para un dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceInstallStates](../api/intune_books_deviceinstallstate_list.md)|Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)|Enumere las propiedades y las relaciones de los objetos [deviceInstallState](../resources/intune_books_deviceinstallstate.md).|
|[Obtener deviceInstallState](../api/intune_books_deviceinstallstate_get.md)|[deviceInstallState](../resources/intune_books_deviceinstallstate.md)|Lea las propiedades y las relaciones del objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).|
|[Crear deviceInstallState](../api/intune_books_deviceinstallstate_create.md)|[deviceInstallState](../resources/intune_books_deviceinstallstate.md)|Cree un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).|
|[Eliminar deviceInstallState](../api/intune_books_deviceinstallstate_delete.md)|Ninguna|Elimina un [deviceInstallState](../resources/intune_books_deviceinstallstate.md).|
|[Actualizar deviceInstallState](../api/intune_books_deviceinstallstate_update.md)|[deviceInstallState](../resources/intune_books_deviceinstallstate.md)|Actualice las propiedades de un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|deviceName|cadena|Nombre del dispositivo.|
|deviceId|cadena|Id. del dispositivo|
|lastSyncDateTime|DateTimeOffset|Fecha y hora de la última sincronización.|
|installState|[installState](../resources/intune_books_installstate.md)|El estado de instalación del libro electrónico. Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.|
|errorCode|cadena|El código de error si hay errores de instalación.|
|osVersion|cadena|Versión del sistema operativo.|
|osDescription|cadena|Descripción del sistema operativo.|
|userName|cadena|Nombre de usuario del dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceInstallState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "id": "String (identifier)",
  "deviceName": "String",
  "deviceId": "String",
  "lastSyncDateTime": "String (timestamp)",
  "installState": "String",
  "errorCode": "String",
  "osVersion": "String",
  "osDescription": "String",
  "userName": "String"
}
```



