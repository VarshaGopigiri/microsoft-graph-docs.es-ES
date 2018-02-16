# <a name="devicemanagement-resource-type"></a>Tipo de recurso deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceManagement](../api/intune_wip_devicemanagement_get.md)|[deviceManagement](../resources/intune_wip_devicemanagement.md)|Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_wip_devicemanagement.md).|
|[Actualizar deviceManagement](../api/intune_wip_devicemanagement_update.md)|[deviceManagement](../resources/intune_wip_devicemanagement.md)|Actualice las propiedades de un objeto [deviceManagement](../resources/intune_wip_devicemanagement.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Todavía no documentado|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|windowsInformationProtectionAppLearningSummaries|Colección [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md)|Los resúmenes de aprendizaje sobre las aplicaciones de Windows Information Protection|
|windowsInformationProtectionNetworkLearningSummaries|Colección [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md)|Los resúmenes de aprendizaje sobre la red de Windows Information Protection|

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



