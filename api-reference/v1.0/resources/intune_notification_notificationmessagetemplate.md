# <a name="notificationmessagetemplate-resource-type"></a>Tipo de recurso notificationMessageTemplate

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Los mensajes de notificación son mensajes que se envían a los usuarios finales determinados como no compatibles con las directivas de cumplimiento definidas por el administrador. Los administradores eligen las notificaciones y las configuran en la consola de administración de Intune mediante la página de creación de directivas de cumplimiento en la sección "Acciones en caso de incumplimiento". Use el objeto notificationMessageTemplate para crear sus propias notificaciones personalizadas para que elijan los administradores al configurar las acciones en caso de incumplimiento.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar notificationMessageTemplates](../api/intune_notification_notificationmessagetemplate_list.md)|Colección [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md)|Enumere las propiedades y las relaciones de los objetos [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).|
|[Obtener notificationMessageTemplate](../api/intune_notification_notificationmessagetemplate_get.md)|[notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md)|Lea las propiedades y las relaciones del objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).|
|[Crear notificationMessageTemplate](../api/intune_notification_notificationmessagetemplate_create.md)|[notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md)|Cree un objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).|
|[Eliminar notificationMessageTemplate](../api/intune_notification_notificationmessagetemplate_delete.md)|Ninguno|Elimina un [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).|
|[Actualizar notificationMessageTemplate](../api/intune_notification_notificationmessagetemplate_update.md)|[notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md)|Actualice las propiedades de un objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).|
|[Acción sendTestMessage](../api/intune_notification_notificationmessagetemplate_sendtestmessage.md)|Ninguno|Envía un mensaje de prueba con la notificationMessageTemplate especificada en la configuración regional predeterminada|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|Cadena|Nombre para mostrar de la plantilla de mensajes de notificación.|
|defaultLocale|Cadena|La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.|
|brandingOptions|[notificationTemplateBrandingOptions](../resources/intune_notification_notificationtemplatebrandingoptions.md)|Las opciones de personalización de marca de la plantilla de mensaje. La personalización de marca está definida en la consola de administración de Intune. Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|localizedNotificationMessages|Colección [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md)|La lista de mensajes localizados para esta plantilla de mensajes de notificación.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.notificationMessageTemplate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "defaultLocale": "String",
  "brandingOptions": "String"
}
```



