# <a name="windowsinformationprotectionnetworklearningsummary-resource-type"></a>Tipo de recurso windowsInformationProtectionNetworkLearningSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad del resumen de aprendizaje sobre la red de Windows Information Protection.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsInformationProtectionNetworkLearningSummaries](../api/intune_wip_windowsinformationprotectionnetworklearningsummary_list.md)|Colección [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md)|Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md).|
|[Obtener windowsInformationProtectionNetworkLearningSummary](../api/intune_wip_windowsinformationprotectionnetworklearningsummary_get.md)|[windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md)|Lea las propiedades y las relaciones del objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md).|
|[Crear windowsInformationProtectionNetworkLearningSummary](../api/intune_wip_windowsinformationprotectionnetworklearningsummary_create.md)|[windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md)|Cree un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md).|
|[Eliminar windowsInformationProtectionNetworkLearningSummary](../api/intune_wip_windowsinformationprotectionnetworklearningsummary_delete.md)|Ninguna|Elimina un [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md).|
|[Actualizar windowsInformationProtectionNetworkLearningSummary](../api/intune_wip_windowsinformationprotectionnetworklearningsummary_update.md)|[windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md)|Actualice las propiedades de un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para WindowsInformationProtectionNetworkLearningSummary.|
|url|String|Dirección URL del sitio web|
|deviceCount|Int32|Recuento de dispositivos|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.windowsInformationProtectionNetworkLearningSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
  "id": "String (identifier)",
  "url": "String",
  "deviceCount": 1024
}
```



