# <a name="devicecategory-resource-type"></a>Tipo de recurso deviceCategory

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceCategory](../api/intune_devices_devicecategory_get.md)|[deviceCategory](../resources/intune_devices_devicecategory.md)|Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune_devices_devicecategory.md).|
|[Actualizar deviceCategory](../api/intune_devices_devicecategory_update.md)|[deviceCategory](../resources/intune_devices_devicecategory.md)|Actualice las propiedades de un objeto [deviceCategory](../resources/intune_devices_devicecategory.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|El identificador único de la categoría de dispositivo. Solo lectura.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)"
}
```



