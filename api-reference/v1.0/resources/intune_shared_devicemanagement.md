# <a name="devicemanagement-resource-type"></a>Tipo de recurso deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso deviceManagement representa un contenedor cuyo contenido varía según el flujo de trabajo, incluidos:

- Eventos de auditoría
- Términos y condiciones corporativos 
- Perfiles de inscripción corporativa
- Opciones de configuración de dispositivo
- Administración de dispositivos
- Protección de extremo
- Perfiles de inscripción
- Notificaciones
- Las directivas de incorporación, configuración y detalles
- Directivas de control de acceso basado en roles (RBAC)
- Socios de asistencia remota
- Socios de administración de extensión de telecomunicaciones
- Eventos de solución de problemas
- Resúmenes de Protección de la información de Windows

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceManagement](../api/intune_shared_devicemanagement_get.md)|[deviceManagement](../resources/intune_shared_devicemanagement.md)|Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).|
|[Actualizar deviceManagement](../api/intune_shared_devicemanagement_update.md)|[deviceManagement](../resources/intune_shared_devicemanagement.md)|Actualiza las propiedades de un objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).|
|**Incorporación**|
|[Función verifyWindowsEnrollmentAutoDiscovery](../api/intune_shared_devicemanagement_verifywindowsenrollmentautodiscovery.md)|Booleano|Todavía no documentado|
|**RBAC**|
|[Función getEffectivePermissions](../api/intune_shared_devicemanagement_geteffectivepermissions.md)|Colección o colección de cadenas [rolePermission](../resources/intune_rbac_rolepermission.md)|Recupera los permisos efectivos del usuario autenticado actualmente|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del dispositivo|
|**Configuración de dispositivos**|
|settings|[deviceManagementSettings](../resources/intune_deviceconfig_devicemanagementsettings.md)|Configuración de niveles de cuenta.|
|**Administración de dispositivos**|
|subscriptionState|Cadena|Estado de suscripción de administración de dispositivos móviles del espacio empresarial. Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked` y `lockedOut`.|
|**Incorporación**|
|intuneBrand|[intuneBrand](../resources/intune_onboarding_intunebrand.md)|intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|**Auditoría**|
|auditEvents|Colección [auditEvent](../resources/intune_auditing_auditevent.md)|Los eventos de auditoría|
|**Términos y condiciones corporativos**|
|termsAndConditions|Colección [termsAndConditions](../resources/intune_companyterms_termsandconditions.md)|Los términos y condiciones asociados a la administración de dispositivos de la empresa.|
|**Configuración de dispositivos**|
|deviceCompliancePolicies|Colección [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|Las directivas de cumplimiento de dispositivos.|
|deviceCompliancePolicyDeviceStateSummary|[deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md)|El resumen del estado de cumplimiento de dispositivos para esta cuenta.|
|deviceCompliancePolicySettingStateSummaries|Colección [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md)|Los estados de resumen de la configuración de directiva de cumplimiento para esta cuenta.|
|deviceConfigurationDeviceStateSummaries|[deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md)|El resumen de estado del dispositivo de la configuración de dispositivo para esta cuenta.|
|deviceConfigurations|Colección [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|Las configuraciones de dispositivos.|
|iosUpdateStatuses|Colección [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md)|Los estados de instalación de actualización del software de iOS para esta cuenta.|
|softwareUpdateStatusSummary|[softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md)|El resumen del estado de la actualización de software.|
|**Administración de dispositivos**|
|applePushNotificationCertificate|[applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md)|Certificado de notificación de inserción de Apple.|
|detectedApps|Colección [detectedApp](../resources/intune_devices_detectedapp.md)|La lista de aplicaciones detectadas asociadas a un dispositivo.|
|managedDeviceOverview|[managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md)|Resumen de dispositivos|
|managedDevices|Colección [managedDevice](../resources/intune_devices_manageddevice.md)|La lista de dispositivos administrados.|
|**Inscripción**|
|importedWindowsAutopilotDeviceIdentities|Colección [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md)|Colección de dispositivos importados de Windows Autopilot.|
|**Notificaciones**|
|notificationMessageTemplates|Colección [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md)|Las plantillas de mensajes de notificación.|
|**Incorporación**|
|conditionalAccessSettings|[onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|La configuración de acceso condicional local de Exchange. El acceso condicional local requiere que los dispositivos estén inscritos y sean compatibles para tener acceso al correo|
|deviceCategories|Colección [deviceCategory](../resources/intune_shared_devicecategory.md)|La lista de categorías de dispositivo con el espacio empresarial.|
|deviceEnrollmentConfigurations|Colección [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|La lista de configuraciones de la inscripción de dispositivos|
|deviceManagementPartners|Colección [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md)|La lista de partners de administración de dispositivos configurados por el espacio empresarial.|
|exchangeConnectors|Colección [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md)|La lista de conectores de Exchange configurados por el espacio empresarial.|
|mobileThreatDefenseConnectors|Colección [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|La lista de conectores de Mobile Threat Defense configurados por el espacio empresarial.|
|**RBAC**|
|resourceOperations|Colección [resourceOperation](../resources/intune_rbac_resourceoperation.md)|Las operaciones de recursos.|
|roleAssignments|Colección [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md)|Las asignaciones de roles.|
|roleDefinitions|Colección [roleDefinition](../resources/intune_rbac_roledefinition.md)|Las definiciones de roles.|
|**Asistencia remota**|
|remoteAssistancePartners|Colección [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md)|Los partners de asistencia remota.|
|**Gestión de gastos de telecomunicaciones**|
|telecomExpenseManagementPartners|Colección [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md)|El partner de administración de gastos de telecomunicaciones.|
|**Solución de problemas**|
|troubleshootingEvents|Colección [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)|La lista de eventos de solución de problemas del espacio empresarial.|
|**Protección de la información de Windows**|
|windowsInformationProtectionAppLearningSummaries|Colección [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md)|Los resúmenes de aprendizaje sobre las aplicaciones de Windows Information Protection|
|windowsInformationProtectionNetworkLearningSummaries|Colección [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md)|Los resúmenes de aprendizaje sobre la red de Windows Information Protection|


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)",
  "intuneBrand": {"@odata.type": "microsoft.graph.intuneBrand"},
  "subscriptionState": "String",
  "settings": {"@odata.type": "microsoft.graph.deviceManagementSettings"}
}
```



