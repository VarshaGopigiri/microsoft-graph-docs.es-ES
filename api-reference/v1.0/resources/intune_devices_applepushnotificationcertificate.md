# <a name="applepushnotificationcertificate-resource-type"></a>Tipo de recurso applePushNotificationCertificate

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Certificado de notificación de inserción de Apple.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener applePushNotificationCertificate](../api/intune_devices_applepushnotificationcertificate_get.md)|[applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md)|Lea las propiedades y las relaciones del objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).|
|[Actualizar applePushNotificationCertificate](../api/intune_devices_applepushnotificationcertificate_update.md)|[applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md)|Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).|
|[Función downloadApplePushNotificationCertificateSigningRequest](../api/intune_devices_applepushnotificationcertificate_downloadapplepushnotificationcertificatesigningrequest.md)|cadena|Descargar solicitud de firma de certificado de notificación de inserción de Apple|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Identificador único del certificado|
|appleIdentifier|cadena|Id. de Apple de la cuenta que se usó para crear el certificado push MDM.|
|topicIdentifier|cadena|Id. del tema|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación del certificado de notificación push de Apple.|
|expirationDateTime|DateTimeOffset|Fecha y hora de la expiración del certificado de notificación push de Apple.|
|certificado|cadena|Todavía no documentado|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.applePushNotificationCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.applePushNotificationCertificate",
  "id": "String (identifier)",
  "appleIdentifier": "String",
  "topicIdentifier": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "certificate": "String"
}
```



