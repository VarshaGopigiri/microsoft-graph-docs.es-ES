# <a name="deviceappmanagement-resource-type"></a>Tipo de recurso deviceAppManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de aplicaciones de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceAppManagement](../api/intune_onboarding_deviceappmanagement_get.md)|[deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md)|Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md).|
|[Actualizar deviceAppManagement](../api/intune_onboarding_deviceappmanagement_update.md)|[deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md)|Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md).|
|[Acción syncMicrosoftStoreForBusinessApps](../api/intune_onboarding_deviceappmanagement_syncmicrosoftstoreforbusinessapps.md)|Ninguna|Sincroniza la cuenta de Intune con Microsoft Store para Empresas|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Todavía no documentado|
|microsoftStoreForBusinessLastSuccessfulSyncDateTime|DateTimeOffset|La última vez que se sincronizaron correctamente las aplicaciones de Microsoft Store para Empresas en la cuenta.|
|isEnabledForMicrosoftStoreForBusiness|Booleano|Si la cuenta está habilitada para la sincronización de aplicaciones de Microsoft Store para Empresas.|
|microsoftStoreForBusinessLanguage|cadena|La información local que se usa para sincronizar las aplicaciones de Microsoft Store para Empresas. Referencias culturales que son específicas de un país o región. Los nombres de dichas referencias culturales siguen RFC 4646 (Windows Vista y versiones posteriores). El formato es <languagecode2>-<country/regioncode2>, donde <languagecode2> es un código de dos letras en minúsculas proveniente de ISO 639-1 y <country/regioncode2> es un código de dos letras en mayúsculas derivado de ISO 3166. Por ejemplo, en-US para inglés (Estados Unidos) es una referencia cultural específica.|
|microsoftStoreForBusinessLastCompletedApplicationSyncTime|DateTimeOffset|La última vez que se completó una sincronización de aplicaciones desde Microsoft Store para Empresas.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAppManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "String (identifier)",
  "microsoftStoreForBusinessLastSuccessfulSyncDateTime": "String (timestamp)",
  "isEnabledForMicrosoftStoreForBusiness": true,
  "microsoftStoreForBusinessLanguage": "String",
  "microsoftStoreForBusinessLastCompletedApplicationSyncTime": "String (timestamp)"
}
```



