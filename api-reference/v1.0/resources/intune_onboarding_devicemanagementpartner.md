# <a name="devicemanagementpartner-resource-type"></a>Tipo de recurso deviceManagementPartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que representa una conexión a un partner de administración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceManagementPartners](../api/intune_onboarding_devicemanagementpartner_list.md)|Colección [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md)|Enumere las propiedades y las relaciones de los objetos [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).|
|[Obtener deviceManagementPartner](../api/intune_onboarding_devicemanagementpartner_get.md)|[deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md)|Lea las propiedades y las relaciones del objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).|
|[Crear deviceManagementPartner](../api/intune_onboarding_devicemanagementpartner_create.md)|[deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md)|Cree un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).|
|[Eliminar deviceManagementPartner](../api/intune_onboarding_devicemanagementpartner_delete.md)|Ninguna|Elimina un [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).|
|[Actualizar deviceManagementPartner](../api/intune_onboarding_devicemanagementpartner_update.md)|[deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md)|Actualice las propiedades de un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Todavía no documentado|
|lastHeartbeatDateTime|DateTimeOffset|Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos|
|partnerState|[deviceManagementPartnerTenantState](../resources/intune_onboarding_devicemanagementpartnertenantstate.md)|Estado de partner de este espacio empresarial. Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected` y `unresponsive`.|
|partnerAppType|[deviceManagementPartnerAppType](../resources/intune_onboarding_devicemanagementpartnerapptype.md)|Tipo de aplicación de partner. Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.|
|singleTenantAppId|Cadena|Identificador de aplicación de espacio empresarial único de partner|
|displayName|Cadena|Nombre para mostrar del partner|
|isConfigured|Booleano|Si el partner de administración de dispositivos está configurado o no|
|whenPartnerDevicesWillBeRemovedDateTime|DateTimeOffset|Fecha y hora en UTC de cuándo se quitará PartnerDevices|
|whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime|DateTimeOffset|Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementPartner"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "id": "String (identifier)",
  "lastHeartbeatDateTime": "String (timestamp)",
  "partnerState": "String",
  "partnerAppType": "String",
  "singleTenantAppId": "String",
  "displayName": "String",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "String (timestamp)",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "String (timestamp)"
}
```








