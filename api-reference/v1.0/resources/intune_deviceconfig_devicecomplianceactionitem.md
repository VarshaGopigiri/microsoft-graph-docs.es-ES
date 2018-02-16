# <a name="devicecomplianceactionitem-resource-type"></a>Tipo de recurso deviceComplianceActionItem

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de la acción programada
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceComplianceActionItems](../api/intune_deviceconfig_devicecomplianceactionitem_list.md)|Colección [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md)|Enumere las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).|
|[Obtener deviceComplianceActionItem](../api/intune_deviceconfig_devicecomplianceactionitem_get.md)|[deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md)|Lea las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).|
|[Crear deviceComplianceActionItem](../api/intune_deviceconfig_devicecomplianceactionitem_create.md)|[deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md)|Cree un objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).|
|[Eliminar deviceComplianceActionItem](../api/intune_deviceconfig_devicecomplianceactionitem_delete.md)|Ninguna|Elimina un [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).|
|[Actualizar deviceComplianceActionItem](../api/intune_deviceconfig_devicecomplianceactionitem_update.md)|[deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md)|Actualice las propiedades de un objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|gracePeriodHours|Int32|Número de horas de espera hasta que se aplica la acción. Valores válidos de 0 a 8760|
|actionType|cadena|Qué acción tomar. Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe` y `removeResourceAccessProfiles`.|
|notificationTemplateId|cadena|Qué plantilla de mensaje de notificación usar|
|notificationMessageCCList|Colección de cadenas|Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceActionItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
  "id": "String (identifier)",
  "gracePeriodHours": 1024,
  "actionType": "String",
  "notificationTemplateId": "String",
  "notificationMessageCCList": [
    "String"
  ]
}
```



