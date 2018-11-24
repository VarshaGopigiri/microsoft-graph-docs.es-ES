# <a name="deviceappmanagement-resource-type"></a>Tipo de recurso deviceAppManagement

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de aplicaciones de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceAppManagement](../api/intune_shared_deviceappmanagement_get.md)|Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md).|
|[Actualizar deviceAppManagement](../api/intune_shared_deviceappmanagement_update.md)|Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md).|
|**Incorporación de redes**|
|[Acción syncMicrosoftStoreForBusinessApps](../api/intune_shared_deviceappmanagement_syncmicrosoftstoreforbusinessapps.md)|Ninguna|Sincroniza la cuenta de Intune con Microsoft Store para Empresas|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|**Incorporación de redes**|
|isEnabledForMicrosoftStoreForBusiness|Booleano|Indica si la cuenta está habilitada para la sincronización de aplicaciones de Microsoft Store para Empresas.|
|microsoftStoreForBusinessLanguage|String|Información local que se usa para sincronizar las aplicaciones de Microsoft Store para Empresas. Referencias culturales que son específicas de un país o región. Los nombres de dichas referencias culturales siguen RFC 4646 (Windows Vista y versiones posteriores). El formato es <languagecode2>-<country/regioncode2>, donde <languagecode2> es un código de dos letras en minúsculas proveniente de ISO 639-1 y <country/regioncode2> es un código de dos letras en mayúsculas derivado de ISO 3166. Por ejemplo, en-US para inglés (Estados Unidos) es una referencia cultural específica.|
|microsoftStoreForBusinessLastCompletedApplicationSyncTime|DateTimeOffset|La última vez que se completó una sincronización de aplicaciones desde Microsoft Store para Empresas.|
|microsoftStoreForBusinessLastSuccessfulSyncDateTime|DateTimeOffset|Última vez que se sincronizaron correctamente las aplicaciones de Microsoft Store para Empresas en la cuenta.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|**Aplicaciones**|
|mobileAppCategories|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|Las categorías de las aplicaciones para móviles.|
|mobileAppConfigurations|Colección [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|La configuración de aplicaciones móviles para dispositivo administrado.|
|mobileApps|Colección [mobileApp](../resources/intune_apps_mobileapp.md)|Las aplicaciones móviles.|
|**Libros**|
|managedEBooks|Colección [managedEBook](../resources/intune_books_managedebook.md)|El libro electrónico Managed.|
|**Administración de aplicaciones móviles (MAM)**|
|androidManagedAppProtections|Colección [androidManagedAppProtection](../resources/intune_mam_androidmanagedappprotection.md)|Directivas de aplicaciones administradas de Android.|
|defaultManagedAppProtections|Colección [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md)|Directivas de aplicaciones administradas predeterminadas.|
|iosManagedAppProtections|Colección [iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md)|Directivas de aplicaciones administradas de iOS.|
|managedAppPolicies|Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|Directivas de aplicaciones administradas.|
|managedAppRegistrations|Colección [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|Los registros de aplicaciones administradas.|
|managedAppStatuses|Colección [managedAppStatus](../resources/intune_mam_managedappstatus.md)|Los estados de aplicaciones administradas.|
|mdmWindowsInformationProtectionPolicies|Colección [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md)|Windows Information Protection para las aplicaciones que se ejecutan en dispositivos inscritos en MDM.|
|targetedManagedAppConfigurations|Colección [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md)|Configuraciones de aplicaciones administradas dirigidas.|
|windowsInformationProtectionPolicies|Colección [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md)|Windows Information Protection para las aplicaciones que se ejecutan en dispositivos no inscritos en MDM.|
|**Incorporación de redes**|
|vppTokens|Colección [vppToken](../resources/intune_onboarding_vpptoken.md)|Enumera los token Vpp para esta organización.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.  Tenga en cuenta que esto es sólo un ejemplo; las respuestas de consultas a las consultas real contendrá las propiedades adecuadas para el contexto.  
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
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



