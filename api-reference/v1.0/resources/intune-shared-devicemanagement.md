---
title: Tipo de recurso deviceManagement
description: 'El recurso deviceManagement representa un contenedor cuyo contenido varía según el flujo de trabajo, incluidos:  '
localization_priority: Normal
ms.openlocfilehash: e7517ac2c9560723c6c3c4dce2dc070b1ec96af3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822207"
---
# <a name="devicemanagement-resource-type"></a>Tipo de recurso deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso deviceManagement representa un contenedor cuyo contenido varía según el flujo de trabajo, incluidos:  

- Eventos de auditoría  
- Términos y condiciones corporativos   
- Opciones de configuración de dispositivo  
- Administración de dispositivos  
- Protección de extremo  
- Perfiles de inscripción  
- Notificaciones  
- Obtener información detallada, la configuración y las directivas de incorporación  
- Directivas de acceso basado en roles (RBAC) de control  
- Socios de asistencia remota  
- Socios de administración de extensión de telecomunicaciones  
- Solución de problemas de eventos  
- Resúmenes de protección de la información de Windows  

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceManagement](../api/intune-shared-devicemanagement-get.md)|[deviceManagement](../resources/intune-shared-devicemanagement.md)|Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).|
|[Actualizar deviceManagement](../api/intune-shared-devicemanagement-update.md)|[deviceManagement](../resources/intune-shared-devicemanagement.md)|Actualice las propiedades de un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).|
|**Incorporación de redes**|
|[Función verifyWindowsEnrollmentAutoDiscovery](../api/intune-shared-devicemanagement-verifywindowsenrollmentautodiscovery.md)|Booleano|Todavía no documentado|
|**RBAC**|
|[Función getEffectivePermissions](../api/intune-shared-devicemanagement-geteffectivepermissions.md)|colección de [rolePermission](../resources/intune-rbac-rolepermission.md) o cadena|Recupera los permisos efectivos del usuario autenticado actualmente|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del dispositivo.|
|**Configuración de dispositivos**|
|configuración|[deviceManagementSettings](../resources/intune-deviceconfig-devicemanagementsettings.md)|Configuración de niveles de cuenta.|
|**Administración de dispositivos**|
|subscriptionState|String|Estado de suscripción de administración de dispositivos móviles del espacio empresarial. Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked`, `lockedOut`.|
|**Incorporación de redes**|
|intuneBrand|[intuneBrand](../resources/intune-onboarding-intunebrand.md)|intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Description|
|:---|:---|:---|
|**Auditoría**|
|auditEvents|Colección [auditEvent](../resources/intune-auditing-auditevent.md)|Los eventos de auditoría|
|**Términos y condiciones corporativos**|
|termsAndConditions|Colección [termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Los términos y condiciones asociados a la administración de dispositivos de la empresa.|
|**Configuración de dispositivos**|
|deviceCompliancePolicies|Colección [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)|Las directivas de cumplimiento de dispositivos.|
|deviceCompliancePolicyDeviceStateSummary|[deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md)|El resumen del estado de cumplimiento de dispositivos para esta cuenta.|
|deviceCompliancePolicySettingStateSummaries|Colección [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)|Los estados de resumen de la configuración de directiva de cumplimiento para esta cuenta.|
|deviceConfigurationDeviceStateSummaries|[deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md)|El resumen de estado del dispositivo de la configuración de dispositivo para esta cuenta.|
|deviceConfigurations|Colección [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|Las configuraciones de dispositivos.|
|iosUpdateStatuses|Colección [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md)|Los estados de instalación de actualización del software de iOS para esta cuenta.|
|softwareUpdateStatusSummary|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md)|El resumen del estado de la actualización de software.|
|**Administración de dispositivos**|
|applePushNotificationCertificate|[applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md)|Certificado de notificación de inserción de Apple.|
|detectedApps|Colección [detectedApp](../resources/intune-devices-detectedapp.md)|La lista de aplicaciones detectadas asociadas a un dispositivo.|
|managedDeviceOverview|[managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md)|Resumen de dispositivos|
|managedDevices|Colección [managedDevice](../resources/intune-devices-manageddevice.md)|La lista de dispositivos administrados.|
|**Inscripción**|
|importedWindowsAutopilotDeviceIdentities|Colección [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md)|Colección de dispositivos importados de Windows Autopilot|
|importedWindowsAutopilotDeviceIdentityUploads|colección de [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md)|Colección de piloto automático de Windows para cargar los dispositivos.|
|**Notificaciones**|
|notificationMessageTemplates|Colección [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md)|Las plantillas de mensajes de notificación.|
|**Incorporación de redes**|
|conditionalAccessSettings|[onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|La configuración de acceso condicional local de Exchange. El acceso condicional local requiere que los dispositivos estén inscritos y sean compatibles para tener acceso al correo|
|deviceCategories|Colección [deviceCategory](../resources/intune-shared-devicecategory.md)|La lista de categorías de dispositivo con el espacio empresarial.|
|deviceEnrollmentConfigurations|Colección [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|La lista de configuraciones de la inscripción de dispositivos|
|deviceManagementPartners|Colección [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md)|La lista de partners de administración de dispositivos configurados por el espacio empresarial.|
|exchangeConnectors|Colección [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md)|La lista de conectores de Exchange configurados por el espacio empresarial.|
|mobileThreatDefenseConnectors|Colección [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md)|La lista de conectores de Mobile Threat Defense configurados por el espacio empresarial.|
|**RBAC**|
|resourceOperations|Colección [resourceOperation](../resources/intune-rbac-resourceoperation.md)|Las operaciones de recursos.|
|roleAssignments|Colección [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md)|Las asignaciones de roles.|
|roleDefinitions|Colección [roleDefinition](../resources/intune-rbac-roledefinition.md)|Las definiciones de roles.|
|**Asistencia remota**|
|remoteAssistancePartners|Colección [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md)|Los partners de asistencia remota.|
|**Administración de gastos de telecomunicaciones**|
|telecomExpenseManagementPartners|Colección [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md)|El partner de administración de gastos de telecomunicaciones.|
|**Solución de problemas**|
|troubleshootingEvents|Colección [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)|La lista de eventos de solución de problemas del espacio empresarial.|
|**Protección de la información de Windows**|
|windowsInformationProtectionAppLearningSummaries|Colección [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md)|Los resúmenes de aprendizaje sobre las aplicaciones de Windows Information Protection|
|windowsInformationProtectionNetworkLearningSummaries|Colección [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md)|Los resúmenes de aprendizaje sobre la red de Windows Information Protection|


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



