# <a name="mobilethreatdefenseconnector-resource-type"></a>Tipo de recurso mobileThreatDefenseConnector

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que representa una conexión a un partner de Mobile Threat Defense.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileThreatDefenseConnectors](../api/intune_onboarding_mobilethreatdefenseconnector_list.md)|Colección [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|Enumere las propiedades y las relaciones de los objetos [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).|
|[Obtener mobileThreatDefenseConnector](../api/intune_onboarding_mobilethreatdefenseconnector_get.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|Lea las propiedades y las relaciones del objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).|
|[Crear mobileThreatDefenseConnector](../api/intune_onboarding_mobilethreatdefenseconnector_create.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|Cree un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).|
|[Eliminar mobileThreatDefenseConnector](../api/intune_onboarding_mobilethreatdefenseconnector_delete.md)|Ninguna|Elimina un [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).|
|[Actualizar mobileThreatDefenseConnector](../api/intune_onboarding_mobilethreatdefenseconnector_update.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|Actualice las propiedades de un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Todavía no documentado|
|lastHeartbeatDateTime|DateTimeOffset|Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a MTP|
|partnerState|Cadena|Estado de partner de este espacio empresarial. Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.|
|androidEnabled|Booleano|Botón de activar o desactivar de Android|
|androidDeviceBlockedOnMissingPartnerData|Booleano|Para Android, Permitir que el administrador configure debe recibir datos del partner de sincronización de datos antes de que se considere compatible|
|iosDeviceBlockedOnMissingPartnerData|Booleano|Para iOS, Permitir que el administrador configure debe recibir datos del partner de sincronización de datos antes de que se considere compatible|
|partnerUnsupportedOsVersionBlocked|Booleano|Permite al administrador bloquear los dispositivos en las plataformas habilitadas que no cumplan los requisitos de versión mínima|
|iosEnabled|Booleano|Botón de activar o desactivar de iOS|
|partnerUnresponsivenessThresholdInDays|Int32|Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileThreatDefenseConnector"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "String (identifier)",
  "lastHeartbeatDateTime": "String (timestamp)",
  "partnerState": "String",
  "androidEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "iosEnabled": true,
  "partnerUnresponsivenessThresholdInDays": 1024
}
```



