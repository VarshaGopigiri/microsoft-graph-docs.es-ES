# <a name="windowsinformationprotectionapplearningsummary-resource-type"></a>Tipo de recurso windowsInformationProtectionAppLearningSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad del resumen de aprendizaje de aplicación de Windows Information Protection.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsInformationProtectionAppLearningSummaries](../api/intune_wip_windowsinformationprotectionapplearningsummary_list.md)|Colección [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md)|Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).|
|[Obtener windowsInformationProtectionAppLearningSummary](../api/intune_wip_windowsinformationprotectionapplearningsummary_get.md)|[windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md)|Lea las propiedades y las relaciones del objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).|
|[Crear windowsInformationProtectionAppLearningSummary](../api/intune_wip_windowsinformationprotectionapplearningsummary_create.md)|[windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md)|Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).|
|[Eliminar windowsInformationProtectionAppLearningSummary](../api/intune_wip_windowsinformationprotectionapplearningsummary_delete.md)|Ninguna|Elimina un [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).|
|[Actualizar windowsInformationProtectionAppLearningSummary](../api/intune_wip_windowsinformationprotectionapplearningsummary_update.md)|[windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md)|Actualice las propiedades de un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Identificador único para WindowsInformationProtectionAppLearningSummary.|
|applicationName|cadena|Nombre de la aplicación|
|applicationType|cadena|Tipo de aplicación Los valores posibles son: `universal` y `desktop`.|
|deviceCount|Int32|Recuento de dispositivos|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtectionAppLearningSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "id": "String (identifier)",
  "applicationName": "String",
  "applicationType": "String",
  "deviceCount": 1024
}
```



