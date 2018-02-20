# <a name="deviceappmanagement-resource-type"></a>Tipo de recurso deviceAppManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad de singleton de administración de aplicaciones de dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceAppManagement](../api/intune_mam_deviceappmanagement_get.md)|[deviceAppManagement](../resources/intune_mam_deviceappmanagement.md)|Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_mam_deviceappmanagement.md).|
|[Actualizar deviceAppManagement](../api/intune_mam_deviceappmanagement_update.md)|[deviceAppManagement](../resources/intune_mam_deviceappmanagement.md)|Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_mam_deviceappmanagement.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managedAppPolicies|Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|Directivas de aplicaciones administradas.|
|iosManagedAppProtections|Colección [iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md)|Directivas de aplicaciones administradas de iOS.|
|androidManagedAppProtections|Colección [androidManagedAppProtection](../resources/intune_mam_androidmanagedappprotection.md)|Directivas de aplicaciones administradas de Android.|
|defaultManagedAppProtections|Colección [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md)|Directivas de aplicaciones administradas predeterminadas.|
|targetedManagedAppConfigurations|Colección [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md)|Configuraciones de aplicaciones administradas dirigidas.|
|mdmWindowsInformationProtectionPolicies|Colección [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md)|Windows Information Protection para las aplicaciones que se ejecutan en dispositivos inscritos en MDM.|
|windowsInformationProtectionPolicies|Colección [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md)|Windows Information Protection para las aplicaciones que se ejecutan en dispositivos no inscritos en MDM.|
|managedAppRegistrations|Colección [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|Los registros de aplicaciones administradas.|
|managedAppStatuses|Colección [managedAppStatus](../resources/intune_mam_managedappstatus.md)|Los estados de aplicaciones administradas.|

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
  "id": "String (identifier)"
}
```



