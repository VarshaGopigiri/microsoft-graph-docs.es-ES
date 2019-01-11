---
title: Tipo de recurso deviceManagement
description: 'El recurso deviceManagement representa un contenedor cuyo contenido varía según el flujo de trabajo, incluidos:  '
localization_priority: Normal
ms.openlocfilehash: 72c8cde688e95d3ffda07e6e698e8fd5f0f08fc0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823250"
---
# <a name="devicemanagement-resource-type"></a>Tipo de recurso deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso deviceManagement representa un contenedor cuyo contenido varía según el flujo de trabajo, incluidos:  

- Configuración de Android for Work
- Eventos de auditoría
- Términos y condiciones corporativos 
- Perfiles de inscripción corporativo
- Opciones de configuración de dispositivo
- Administración de dispositivos
- SIM electrónica (ESIM)
- Barrera
- Notificaciones
- Obtener información detallada, la configuración y las directivas de incorporación
- Acceso remoto
- Socios de asistencia remota
- Directivas de acceso basado en roles (RBAC) de control
- Socios de administración de extensión de telecomunicaciones
- Solución de problemas de eventos
- Resúmenes de protección de la información de Windows

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceManagement](../api/intune-shared-devicemanagement-get.md)|Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).|
|[Actualizar deviceManagement](../api/intune-shared-devicemanagement-update.md)|Actualice las propiedades de un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).|
|**Configuración de dispositivos**|
|[acción enableLegacyPcManagement](../api/intune-shared-devicemanagement-enablelegacypcmanagement.md)|Ninguno|Todavía no documentado|
|**Administración de dispositivos**|
|[acción sendCustomNotificationToCompanyPortal](../api/intune-shared-devicemanagement-sendcustomnotificationtocompanyportal.md)|Ninguno|Todavía no documentado|
|**Incorporación de redes**|
|[Función verifyWindowsEnrollmentAutoDiscovery](../api/intune-shared-devicemanagement-verifywindowsenrollmentautodiscovery.md)|Booleano|Todavía no documentado|
|**Control de acceso basado en roles (RBAC)**|
|[Función getEffectivePermissions](../api/intune-shared-devicemanagement-geteffectivepermissions.md)|Colección [rolePermission](../resources/intune-rbac-rolepermission.md)|Recupera los permisos efectivos del usuario autenticado actualmente|
|[getRoleScopeTagsByIds (función)](../api/intune-shared-devicemanagement-getrolescopetagsbyids.md)|colección de [roleScopeTag](../resources/intune-rbac-rolescopetag.md)|Todavía no documentado|
|[getRoleScopeTagsByResource (función)](../api/intune-shared-devicemanagement-getrolescopetagsbyresource.md)|colección de [roleScopeTag](../resources/intune-rbac-rolescopetag.md)|Todavía no documentado|


## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único asociado con el dispositivo.|
|**Configuración de dispositivos**|
|intuneAccountId|Guid|Identificador de cuenta Intune para dado inquilino|
|legacyPcManangementEnabled|Booleano|La propiedad para habilitar no MDM administrados heredado administración de PC para esta cuenta. Esta propiedad es de sólo lectura.|
|maximumDepTokens|Int32|Número máximo de tokens DEP permitido por inquilino.|
|configuración|[deviceManagementSettings](../resources/intune-deviceconfig-devicemanagementsettings.md)|Configuración de niveles de cuenta.|
|**Administración de dispositivos**|
|accountMoveCompletionDateTime|DateTimeOffset|La fecha y la hora cuando mueven los datos de inquilinos entre scaleunits.|
|adminConsent|[adminConsent](../resources/intune-devices-adminconsent.md)|Información de consentimiento de administración.|
|deviceProtectionOverview|[deviceProtectionOverview](../resources/intune-devices-deviceprotectionoverview.md)|Información general de protección de dispositivos.|
|managedDeviceCleanupSettings|[managedDeviceCleanupSettings](../resources/intune-devices-manageddevicecleanupsettings.md)|Regla para dispositivos de limpieza|
|subscriptionState|[deviceManagementSubscriptionState](../resources/intune-devices-devicemanagementsubscriptionstate.md)|Estado de suscripción de administración de dispositivos móviles del espacio empresarial. Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked` y `lockedOut`.|
|suscripciones|[deviceManagementSubscriptions](../resources/intune-devices-devicemanagementsubscriptions.md)|Suscripción del inquilino. Los valores posibles son: `none`, `intune`, `office365`, `intunePremium`, `intune_EDU`, `intune_SMB`.|
|windowsMalwareOverview|[windowsMalwareOverview](../resources/intune-devices-windowsmalwareoverview.md)|Información general de malware para los dispositivos de windows.|
|**Incorporación de redes**|
|intuneBrand|[intuneBrand](../resources/intune-onboarding-intunebrand.md)|intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|:---|:---|:---|
|**Android para el trabajo**|
|androidDeviceOwnerEnrollmentProfiles|colección de [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md)|Entidades de perfil de inscripción de dispositivos Android propietario.|
|androidForWorkAppConfigurationSchemas|Colección [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md)|Entidades de esquema de configuración de la aplicación Android for Work.|
|androidForWorkEnrollmentProfiles|Colección [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|Entidades del perfil de inscripción de Android for Work|
|androidForWorkSettings|[androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md)|La entidad singleton de configuración de Android for Work.|
|androidManagedStoreAccountEnterpriseSettings|[androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md)|El singleton Android administrado almacenar entidad de configuración de empresa de cuenta.|
|androidManagedStoreAppConfigurationSchemas|colección de [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md)|Android aplicación configuración esquema las entidades de empresa.|
|**Auditoría**|
|auditEvents|Colección [auditEvent](../resources/intune-auditing-auditevent.md)|Los eventos de auditoría|
|**Términos de la compañía**|
|termsAndConditions|Colección [termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Los términos y condiciones asociados a la administración de dispositivos de la empresa.|
|**Inscripción corporativa**|
|enrollmentProfiles|colección de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|Los perfiles de inscripción.|
|importedAppleDeviceIdentities|colección de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|Las identidades de dispositivo importadas de Apple.|
|importedDeviceIdentities|colección de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|Las identidades de dispositivo importada.|
|**Configuración de dispositivos**|
|advancedThreatProtectionOnboardingStateSummary|[advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md)|El estado de resumen del estado de la incorporación de ATP para esta cuenta.|
|cartToClassAssociations|colección de [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md)|Carro para las asociaciones de clase.|
|deviceCompliancePolicies|Colección [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|Las directivas de cumplimiento de dispositivos.|
|deviceCompliancePolicyDeviceStateSummary|[deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md)|El resumen del estado de cumplimiento de dispositivos para esta cuenta.|
|deviceCompliancePolicySettingStateSummaries|Colección [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)|Los estados de resumen de la configuración de directiva de cumplimiento para esta cuenta.|
|deviceConfigurationConflictSummary|colección de [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md)|Resumen de las directivas de estado de conflicto para esta cuenta.|
|deviceConfigurationDeviceStateSummaries|[deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md)|El resumen de estado del dispositivo de la configuración de dispositivo para esta cuenta.|
|deviceConfigurationRestrictedAppsViolations|colección de [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md)|Infracciones de aplicaciones restringidos para esta cuenta.|
|deviceConfigurations|Colección [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|Las configuraciones de dispositivos.|
|deviceConfigurationUserStateSummaries|[deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md)|El dispositivo configuración estado del usuario resumen para esta cuenta.|
|iosUpdateStatuses|Colección [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md)|Los estados de instalación de actualización del software de iOS para esta cuenta.|
|ndesConnectors|colección de [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md)|La colección de conectores Ndes para esta cuenta.|
|softwareUpdateStatusSummary|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md)|El resumen del estado de la actualización de software.|
|**Administración de dispositivos**|
|applePushNotificationCertificate|[applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md)|Certificado de notificación de inserción de Apple.|
|dataSharingConsents|colección de [dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|Uso compartido de datos da su consentimiento.|
|detectedApps|Colección [detectedApp](../resources/intune-devices-detectedapp.md)|La lista de aplicaciones detectadas asociadas a un dispositivo.|
|deviceManagementScripts|colección de [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md)|La lista de secuencias de comandos de administración de dispositivo asociado con el inquilino.|
|managedDeviceOverview|[managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md)|Resumen de dispositivos|
|managedDevices|Colección [managedDevice](../resources/intune-devices-manageddevice.md)|La lista de dispositivos administrados.|
|remoteActionAudits|colección de [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md)|Auditorías de la lista de acción de dispositivo remoto con el inquilino.|
|windowsMalwareInformation|colección de [windowsMalwareInformation](../resources/intune-devices-windowsmalwareinformation.md)|La lista de malware afectado en el inquilino.|
|**Inscripción**|
|depOnboardingSettings|colección de [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md)|Este colecciones de varios tokens DEP por inquilino.|
|importedDeviceIdentities|colección de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)|Las identidades de dispositivo importada.|
|importedWindowsAutopilotDeviceIdentities|Colección [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md)|Colección de dispositivos importados de Windows Autopilot|
|importedWindowsAutopilotDeviceIdentityUploads|colección de [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md)|Colección de piloto automático de Windows para cargar los dispositivos.|
|windowsAutopilotDeploymentProfiles|colección de [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)|Perfiles de implementación piloto automático de Windows|
|windowsAutopilotDeviceIdentities|colección de [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md)|Las identidades de dispositivo de Windows piloto automático contenía la colección.|
|windowsAutopilotSettings|[windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md)|La configuración de la cuenta de Windows piloto automático.|
|**SIM incrustado**|
|embeddedSIMActivationCodePools|colección de [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md)|Incrustado grupos de código de activación SIM que creado por esta cuenta.|
|**Barrera**|
|managementConditions|colección de [managementCondition](../resources/intune-fencing-managementcondition.md)|Las condiciones de administración asociadas con la administración de dispositivos de la empresa.|
|managementConditionStatements|colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Las instrucciones de condición de administración asociadas con la administración de dispositivos de la empresa.|
|**Notificaciones**|
|notificationMessageTemplates|Colección [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md)|Las plantillas de mensajes de notificación.|
|**Incorporación de redes**|
|conditionalAccessSettings|[onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|La configuración de acceso condicional local de Exchange. El acceso condicional local requiere que los dispositivos estén inscritos y sean compatibles para tener acceso al correo|
|deviceCategories|Colección [deviceCategory](../resources/intune-shared-devicecategory.md)|La lista de categorías de dispositivo con el espacio empresarial.|
|deviceEnrollmentConfigurations|Colección [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|La lista de configuraciones de la inscripción de dispositivos|
|deviceManagementPartners|Colección [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md)|La lista de partners de administración de dispositivos configurados por el espacio empresarial.|
|exchangeConnectors|Colección [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md)|La lista de conectores de Exchange configurados por el espacio empresarial.|
|exchangeOnPremisesPolicies|colección de [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md)|La lista de directivas de Exchange en Premisis configurado por el inquilino.|
|exchangeOnPremisesPolicy|[deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md)|La directiva que controla el acceso de dispositivo móvil a Exchange local|
|mobileThreatDefenseConnectors|Colección [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md)|La lista de conectores de Mobile Threat Defense configurados por el espacio empresarial.|
|**Acceso remoto**|
|userPfxCertificates|colección de [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Colección de certificados PFX asociado con un usuario.|
|**Asistencia remota**|
|remoteAssistancePartners|Colección [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md)|Los partners de asistencia remota.|
|**Control de acceso basado en roles (RBAC)**|
|resourceOperations|Colección [resourceOperation](../resources/intune-rbac-resourceoperation.md)|Las operaciones de recursos.|
|roleAssignments|Colección [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md)|Las asignaciones de roles.|
|roleDefinitions|Colección [roleDefinition](../resources/intune-rbac-roledefinition.md)|Las definiciones de roles.|
|roleScopeTags|colección de [roleScopeTag](../resources/intune-rbac-rolescopetag.md)|Las etiquetas de ámbito de la función.|
|**Administración de gastos de telecomunicaciones (artículos)**|
|telecomExpenseManagementPartners|Colección [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md)|El partner de administración de gastos de telecomunicaciones.|
|**Solución de problemas**|
|troubleshootingEvents|Colección [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)|La lista de eventos de solución de problemas del espacio empresarial.|
|**Protección de la información de Windows**|
|intuneBrandingProfiles|colección de [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)|Intune perfiles dirigidos a grupos AAD de personalización de marca|
|windowsInformationProtectionAppLearningSummaries|Colección [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md)|Los resúmenes de aprendizaje sobre las aplicaciones de Windows Information Protection|
|windowsInformationProtectionNetworkLearningSummaries|Colección [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md)|Los resúmenes de aprendizaje sobre la red de Windows Information Protection|


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)",
  "subscriptionState": "String"
}
```



