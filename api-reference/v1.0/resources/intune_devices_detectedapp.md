# <a name="detectedapp-resource-type"></a>Tipo de recurso detectedApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una aplicación administrada o no administrada que está instalada en un dispositivo administrado. Las aplicaciones no administradas solo aparecerán para los dispositivos marcados como propiedad de la empresa.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar detectedApps](../api/intune_devices_detectedapp_list.md)|Colección [detectedApp](../resources/intune_devices_detectedapp.md)|Enumere las propiedades y las relaciones de los objetos [detectedApp](../resources/intune_devices_detectedapp.md).|
|[Obtener detectedApp](../api/intune_devices_detectedapp_get.md)|[detectedApp](../resources/intune_devices_detectedapp.md)|Lea las propiedades y las relaciones del objeto [detectedApp](../resources/intune_devices_detectedapp.md).|
|[Crear detectedApp](../api/intune_devices_detectedapp_create.md)|[detectedApp](../resources/intune_devices_detectedapp.md)|Cree un objeto [detectedApp](../resources/intune_devices_detectedapp.md).|
|[Eliminar detectedApp](../api/intune_devices_detectedapp_delete.md)|Ninguna|Elimina un [detectedApp](../resources/intune_devices_detectedapp.md).|
|[Actualizar detectedApp](../api/intune_devices_detectedapp_update.md)|[detectedApp](../resources/intune_devices_detectedapp.md)|Actualice las propiedades de un objeto [detectedApp](../resources/intune_devices_detectedapp.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El identificador único de la aplicación detectada. Intune lo genera automáticamente en el momento en que se crea la aplicación. Solo lectura.|
|displayName|Cadena|Nombre de la aplicación detectada. Solo lectura|
|versión|Cadena|Versión de la aplicación detectada. Solo lectura|
|sizeInByte|Int64|Tamaño en bytes de la aplicación detectada. Solo lectura|
|deviceCount|Int32|El número de dispositivos que han instalado esta aplicación.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managedDevices|Colección [managedDevice](../resources/intune_devices_manageddevice.md)|Los dispositivos que tienen instalada la aplicación detectada|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.detectedApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.detectedApp",
  "id": "String (identifier)",
  "displayName": "String",
  "version": "String",
  "sizeInByte": 1024,
  "deviceCount": 1024
}
```



