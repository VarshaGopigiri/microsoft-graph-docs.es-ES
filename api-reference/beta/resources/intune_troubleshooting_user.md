# <a name="user-resource-type"></a>Tipo de recurso del usuario

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar usuarios](../api/intune_troubleshooting_user_list.md)|Colección [user](../resources/intune_troubleshooting_user.md)|Enumere las propiedades y las relaciones de los objetos [user](../resources/intune_troubleshooting_user.md).|
|[Obtener user](../api/intune_troubleshooting_user_get.md)|[user](../resources/intune_troubleshooting_user.md)|Lea las propiedades y las relaciones del objeto [user](../resources/intune_troubleshooting_user.md).|
|[Crear user](../api/intune_troubleshooting_user_create.md)|[user](../resources/intune_troubleshooting_user.md)|Cree un objeto [user](../resources/intune_troubleshooting_user.md).|
|[Eliminar user](../api/intune_troubleshooting_user_delete.md)|Ninguna|Elimina un [user](../resources/intune_troubleshooting_user.md).|
|[Actualizar user](../api/intune_troubleshooting_user_update.md)|[user](../resources/intune_troubleshooting_user.md)|Actualice las propiedades de un objeto [user](../resources/intune_troubleshooting_user.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del usuario|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceManagementTroubleshootingEvents|Colección [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)|La lista de eventos de solución de problemas para este usuario.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.user"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.user",
  "id": "String (identifier)"
}
```



