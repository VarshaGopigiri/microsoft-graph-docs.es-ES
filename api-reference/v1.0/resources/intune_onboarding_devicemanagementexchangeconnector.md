# <a name="devicemanagementexchangeconnector-resource-type"></a>Tipo de recurso deviceManagementExchangeConnector

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que representa una conexión a un entorno de Exchange.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceManagementExchangeConnectors](../api/intune_onboarding_devicemanagementexchangeconnector_list.md)|Colección [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md)|Enumere las propiedades y las relaciones de los objetos [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).|
|[Obtener deviceManagementExchangeConnector](../api/intune_onboarding_devicemanagementexchangeconnector_get.md)|[deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md)|Lea las propiedades y las relaciones del objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).|
|[Crear deviceManagementExchangeConnector](../api/intune_onboarding_devicemanagementexchangeconnector_create.md)|[deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md)|Cree un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).|
|[Eliminar deviceManagementExchangeConnector](../api/intune_onboarding_devicemanagementexchangeconnector_delete.md)|Ninguna|Elimina un [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).|
|[Actualizar deviceManagementExchangeConnector](../api/intune_onboarding_devicemanagementexchangeconnector_update.md)|[deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md)|Actualice las propiedades de un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).|
|[Acción sync](../api/intune_onboarding_devicemanagementexchangeconnector_sync.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Todavía no documentado|
|lastSyncDateTime|DateTimeOffset|Última hora de sincronización para Exchange Connector|
|status|[deviceManagementExchangeConnectorStatus](../resources/intune_onboarding_devicemanagementexchangeconnectorstatus.md)|Estado de Exchange Connector. Los valores posibles son: `none`, `connectionPending`, `connected` y `disconnected`.|
|primarySmtpAddress|Cadena|Dirección de correo electrónico que se usó para configurar el Exchange Connector de Service To Service.|
|serverName|Cadena|El nombre del servidor de Exchange.|
|connectorServerName|Cadena|El nombre del servidor que hospeda el Exchange Connector.|
|exchangeConnectorType|[deviceManagementExchangeConnectorType](../resources/intune_onboarding_devicemanagementexchangeconnectortype.md)|El tipo de Exchange Connector configurado. Los valores posibles son: `onPremises`, `hosted`, `serviceToService` y `dedicated`.|
|version|Cadena|La versión del ExchangeConnectorAgent|
|exchangeAlias|Cadena|Un alias asignado al servidor de Exchange|
|exchangeOrganization|Cadena|Organización de Exchange al servidor de Exchange|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceManagementExchangeConnector"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
  "id": "String (identifier)",
  "lastSyncDateTime": "String (timestamp)",
  "status": "String",
  "primarySmtpAddress": "String",
  "serverName": "String",
  "connectorServerName": "String",
  "exchangeConnectorType": "String",
  "version": "String",
  "exchangeAlias": "String",
  "exchangeOrganization": "String"
}
```



