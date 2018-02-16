# <a name="reportroot-resource-type"></a>Tipo de recurso reportRoot

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso que representa una instancia del historial de informes.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener reportRoot](../api/intune_deviceconfig_reportroot_get.md)|[reportRoot](../resources/intune_deviceconfig_reportroot.md)|Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune_deviceconfig_reportroot.md).|
|[Actualizar reportRoot](../api/intune_deviceconfig_reportroot_update.md)|[reportRoot](../resources/intune_deviceconfig_reportroot.md)|Actualice las propiedades de un objeto [reportRoot](../resources/intune_deviceconfig_reportroot.md).|
|[Función deviceConfigurationUserActivity](../api/intune_deviceconfig_reportroot_deviceconfigurationuseractivity.md)|[report](../resources/intune_deviceconfig_report.md)|Metadatos para el informe de actividad de usuario de configuración de dispositivo|
|[Función deviceConfigurationDeviceActivity](../api/intune_deviceconfig_reportroot_deviceconfigurationdeviceactivity.md)|[report](../resources/intune_deviceconfig_report.md)|Metadatos para el informe de actividad de dispositivo de configuración de dispositivo|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|El identificador único de esta entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.reportRoot"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "String (identifier)"
}
```



