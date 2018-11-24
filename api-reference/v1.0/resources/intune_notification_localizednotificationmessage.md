# <a name="localizednotificationmessage-resource-type"></a>Tipo de recurso localizedNotificationMessage

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El contenido de texto de una plantilla de mensaje de notificación para la configuración regional.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar localizedNotificationMessages](../api/intune_notification_localizednotificationmessage_list.md)|Colección [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md)|Enumere las propiedades y las relaciones de los objetos [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).|
|[Obtener localizedNotificationMessage](../api/intune_notification_localizednotificationmessage_get.md)|[localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md)|Lea las propiedades y las relaciones del objeto [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).|
|[Crear localizedNotificationMessage](../api/intune_notification_localizednotificationmessage_create.md)|[localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md)|Cree un objeto [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).|
|[Eliminar localizedNotificationMessage](../api/intune_notification_localizednotificationmessage_delete.md)|Ninguna|Elimina un [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).|
|[Actualizar localizedNotificationMessage](../api/intune_notification_localizednotificationmessage_update.md)|[localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md)|Actualice las propiedades de un objeto [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|configuración regional|cadena|La configuración regional para la que se destina este mensaje.|
|asunto|cadena|El asunto de la plantilla del mensaje.|
|messageTemplate|cadena|El contenido de la plantilla del mensaje.|
|isDefault|Booleano|Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma. Solo se puede establecer esta marca. Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.localizedNotificationMessage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "locale": "String",
  "subject": "String",
  "messageTemplate": "String",
  "isDefault": true
}
```



