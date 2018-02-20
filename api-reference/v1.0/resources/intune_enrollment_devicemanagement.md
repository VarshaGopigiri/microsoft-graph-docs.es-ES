# <a name="devicemanagement-resource-type"></a>Tipo de recurso deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso deviceManagement representa las identidades de dispositivo de colección de un espacio empresarial que se han preconfigurado en Intune y los perfiles de inscripción que se pueden asignar a las identidades de dispositivos compatibles con la configuración de preinscripción.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceManagement](../api/intune_enrollment_devicemanagement_get.md)|[deviceManagement](../resources/intune_enrollment_devicemanagement.md)|Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_enrollment_devicemanagement.md).|
|[Actualizar deviceManagement](../api/intune_enrollment_devicemanagement_update.md)|[deviceManagement](../resources/intune_enrollment_devicemanagement.md)|Actualice las propiedades de un objeto [deviceManagement](../resources/intune_enrollment_devicemanagement.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El GUID para el objeto.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```



