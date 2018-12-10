---
title: Registro de cambios para Microsoft Graph
description: Este registro de cambios abarca las modificaciones de Microsoft Graph, incluidas las API de Microsoft Graph del punto de conexión beta y v1.0.
ms.openlocfilehash: 6f42282844fd0dbed5c5df2ffdda86fd7eb559b5
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27191217"
---
# <a name="changelog-for-microsoft-graph"></a>Registro de cambios de Microsoft Graph

Este registro de cambios abarca las modificaciones de Microsoft Graph, incluidas las API de Microsoft Graph del punto de conexión beta y v1.0.

Para obtener más información sobre problemas conocidos con las API de Microsoft Graph, vea [Problemas conocidos](known-issues.md).

## <a name="december-2018"></a>Diciembre de 2018

### <a name="directory-apis"></a>API de directorio

| Tipo de cambio | Versión                                    | Descripción                              |
| :---------- | :----------------------------------------- | :--------------------------------------- |
| Adición    | Beta | Se agregó la propiedad `createdDateTime` al recurso [organización](/graph/api/resources/organization?view=graph-rest-beta).|
| Adición | v1.0 | Se agregó el método `memberOf` para obtener la [pertenencia](/graph/api/device-list-memberOf?view=graph-rest-1.0) directa de un [dispositivo](/graph/api/resources/device?view=graph-rest-1.0). Se ha agregado este método para obtener la lista de pertenencias incluyendo las pertenencias anidadas.|

### <a name="privileged-identity-management-apis"></a>API de Privileged Identity Management

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | beta | Se agregó la propiedad `registeredRoot` a la entidad [governanceResource](/graph/api/resources/governanceresource?view=graph-rest-beta).|
| Cambio | beta | Se cambió el nombre de la propiedad `onboardDateTime` de la entidad [governanceResource](/graph/api/resources/governanceresource?view=graph-rest-beta) a `registeredDateTime`.|
| Adición | beta | Se agregó una nueva acción [register resource](/graph/api/governanceresource-register?view=graph-rest-beta).|
| Eliminación | beta | Se eliminó la propiedad `isPermanent` en la entidad [governanceRoleAssignment](/graph/api/resources/governanceroleassignment?view=graph-rest-beta).|
| Eliminación | beta | Se eliminó la propiedad `roleAssignmentStartDateTime` en la entidad [governanceRoleAssignmentRequest](/graph/api/resources/governanceroleassignmentrequest?view=graph-rest-beta).|
| Eliminación | beta | Se eliminó la propiedad `roleAssignmentEndDateTime` en la entidad [governanceRoleAssignmentRequest](/graph/api/resources/governanceroleassignmentrequest?view=graph-rest-beta).|


## <a name="november-2018"></a>Noviembre de 2018

### <a name="data-policy-operations-api"></a>La API de operaciones de política de datos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | beta        | Se ha agregado una nueva **progress** a [dataPolicyOperation](/graph/api/resources/dataPolicyOperation?view=graph-rest-beta) Especifica el progreso de una operación.

### <a name="microsoft-teams-apis"></a>Las API de Microsoft Teams

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Adición |v1.0| Agregado el nuevo tipo de recurso [team](/graph/api/resources/team?view=graph-rest-1.0).|
|Adición |v1.0| Agregado el nuevo tipo de recurso [channel](/graph/api/resources/channel?view=graph-rest-1.0).|
|Adición |v1.0| Agregado el nuevo tipo de recurso [teamsApp](/graph/api/resources/teamsapp?view=graph-rest-1.0).|
|Adición |v1.0| Agregado el nuevo tipo de recurso [teamsAppDefinition](/graph/api/resources/teamsappdefinition?view=graph-rest-1.0).|
|Adición |v1.0| Agregado el nuevo tipo de recurso [teamsAppInstallation](/graph/api/resources/teamsappinstallation?view=graph-rest-1.0).|
|Adición |v1.0| Agregado el nuevo tipo de recurso [teamsAsyncOperation](/graph/api/resources/teamsasyncoperation?view=graph-rest-1.0). |
|Adición |v1.0| Agregado el nuevo tipo complejo [teamGuestSettings](/graph/api/resources/teamguestsettings?view=graph-rest-1.0). |
|Adición |v1.0| Agregado el nuevo tipo complejo [teamMemberSettings](/graph/api/resources/teammembersettings?view=graph-rest-1.0). |
|Adición |v1.0| Agregado el nuevo tipo complejo [teamMessagingSettings](/graph/api/resources/teammessagingsettings?view=graph-rest-1.0). |
|Adición |v1.0| Agregado el nuevo tipo complejo [teamFunSettings](/graph/api/resources/teamfunsettings?view=graph-rest-1.0). |
|Adición |v1.0| Se añadió la nueva acción [Clonar equipo](/graph/api/team-clone?view=graph-rest-1.0). |
|Adición |v1.0| Se añadió la nueva acción [Archivar equipo](/graph/api/team-archive?view=graph-rest-1.0).|
|Adición |v1.0| Se añadió la nueva acción [Desarchivar equipo](/graph/api/team-unarchive?view=graph-rest-1.0). |
|Adición         | Beta          | Se agregó la compatibilidad con permisos de aplicación a [clonar equipo](/graph/api/team-clone?view=graph-rest-beta). |
|Adición |beta| Se introdujo [/teams/{id}/installedApps](/graph/api/resources/teamsappinstallation?view=graph-rest-beta), que sustituirá a /teams/{id}/apps con algunas diferencias en la carga. |
|Adición |beta| Se añadió [/appCatalogs/teamsApps/{id}/appDefinition](/graph/api/resources/teamsappdefinition?view=graph-rest-beta), que reemplazará la propiedad de versión en [/appCatalogs/teamsApps/{id}](/graph/api/resources/teamsapp?view=graph-rest-beta). |
|Cambio   |beta| Se cambió el nombre del tipo de [/appCatalogs/teamsApps](/graph/api/resources/teamsapp?view=graph-rest-beta) de teamsCatalogApp a teamsApp. |
|Cambio   |beta| Se cambió el nombre del tipo de la propiedad distributionMethod en [/appCatalogs/teamsApps](/graph/api/resources/teamsapp?view=graph-rest-beta) de teamsCatalogAppDistributionMethod a teamsAppDistributionMethod  |
|Eliminación |beta| Se ha cambiado el nombre de teamsCatalogAppDistributionMethod a teamsAppDistributionMethod  |
|Adición |beta| Se introdujo [/teams/{id}/installedApps](/graph/api/resources/teamsappinstallation?view=graph-rest-beta), que sustituirá a /teams/{id}/apps con algunas diferencias en la carga. |
|Adición |beta| Se agregó la propiedad displayName a [teamsTab](/graph/api/resources/teamstab?view=graph-rest-beta) |
|Adición |beta| Se agregó la propiedad messageId a [teamsTab](/graph/api/resources/teamstab?view=graph-rest-beta) |
|Adición |beta| Se agregó la propiedad teamsApp a [teamsTab](/graph/api/resources/teamstab?view=graph-rest-beta) |
|Adición |beta| Agregado el nuevo tipo de recurso [teamsAppInstallation](/graph/api/resources/teamsappinstallation?view=graph-rest-beta).|
|Adición |beta| Agregado el nuevo tipo de recurso [teamsApp](/graph/api/resources/teamsapp?view=graph-rest-beta).|
|Adición |beta| Agregado el nuevo tipo de recurso [teamsAppDefinition](/graph/api/resources/teamsappdefinition?view=graph-rest-beta).|
|Adición |beta| Se ha añadido el nuevo tipo de enumeración hiddenMembership a teamVisibilityType.|
|Adición |beta| Se ha añadido el nuevo tipo de enumeración createTeam a teamsAsyncOperationType.|
|Adición |beta| Se añadió el nuevo miembro de enumeración teamsAppDistributionMethod.|
|Adición |beta| Se añadió la nueva acción de actualización de aplicación en [/teams/{id}/installedApps](/graph/api/resources/teamsappinstallation?view=graph-rest-beta). |

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | v1.0 | Se agregó la acción [forceDelete](/graph/api/domain-forcedelete?view=graph-rest-1.0) a [domains](/graph/api/resources/domain?view=graph-rest-1.0).|
| Adición | beta | Se agregó el nuevo método transitiveMembers en [groups](/graph/api/group-list-transitivemembers?view=graph-rest-beta). Este método devuelve una lista plana de miembros incluyendo los miembros anidados.|
| Adición | beta | Se agregó el nuevo método transitiveMemberOf en [usuarios](/graph/api/user-list-transitivemembersof?view=graph-rest-beta), [grupos](/graph/api/group-list-transitivemembersof?view=graph-rest-beta), [dispositivos](/graph/api/device-list-transitivemembersof?view=graph-rest-beta) y [entidades de servicio](/graph/api/serviceprincipal-list-transitivemembersof?view=graph-rest-beta).|
| Adición | beta | Se agregó el método memberOf para obtener la [pertenencia](/graph/api/device-list-members?view=graph-rest-beta) directa de un dispositivo. Se ha agregado este método para obtener la lista de pertenencias incluyendo las pertenencias anidadas.|
| Adición | beta | Se agregaron nuevas propiedades a [users](/graph/api/resources/user?view=graph-rest-beta): **faxNumber**, **onPremisesDistinguishedName** y **otherMails**.|
| Adición | beta | Se agregó la propiedad **forceChangePasswordNextSignInWithMfa** al tipo complejo [passwordProfile](/graph/api/resources/passwordprofile?view=graph-rest-beta).|

### <a name="reports-apis"></a>API de informes

| Tipo de cambio | Versión                                    | Descripción                              |
| :---------- | :----------------------------------------- | :--------------------------------------- |
| Adición    | Versión beta en Microsoft Graph China gestionado por 21Vianet | Se agregaron las API siguientes:<br>[getEmailActivityUserDetail](/graph/api/reportroot-getemailactivityuserdetail?view=graph-rest-beta)<br>[getEmailActivityCounts](/graph/api/reportroot-getemailactivitycounts?view=graph-rest-beta)<br>[getEmailActivityUserCounts](/graph/api/reportroot-getemailactivityusercounts?view=graph-rest-beta)<br>[getEmailAppUsageUserDetail](/graph/api/reportroot-getemailappusageuserdetail?view=graph-rest-beta)<br>[getEmailAppUsageAppsUserCounts](/graph/api/reportroot-getemailappusageappsusercounts?view=graph-rest-beta)<br>[getEmailAppUsageUserCounts](/graph/api/reportroot-getemailappusageusercounts?view=graph-rest-beta)<br>[getEmailAppUsageVersionsUserCounts](/graph/api/reportroot-getemailappusageversionsusercounts?view=graph-rest-beta)<br>[getMailboxUsageDetail](/graph/api/reportroot-getmailboxusagedetail?view=graph-rest-beta)<br>[getMailboxUsageMailboxCounts](/graph/api/reportroot-getmailboxusagemailboxcounts?view=graph-rest-beta)<br>[getMailboxUsageQuotaStatusMailboxCounts](/graph/api/reportroot-getmailboxusagequotastatusmailboxcounts?view=graph-rest-beta)<br>[getMailboxUsageStorage](/graph/api/reportroot-getmailboxusagestorage?view=graph-rest-beta)<br>[getOffice365ActivationsUserDetail](/graph/api/reportroot-getoffice365activationsuserdetail?view=graph-rest-beta)<br>[getOffice365ActivationCounts](/graph/api/reportroot-getoffice365activationcounts?view=graph-rest-beta)<br>[getOffice365ActivationsUserCounts](/graph/api/reportroot-getoffice365activationsusercounts?view=graph-rest-beta)<br>[getOffice365ActiveUserDetail](/graph/api/reportroot-getoffice365activeuserdetail?view=graph-rest-beta)<br>[getOffice365ActiveUserCounts](/graph/api/reportroot-getoffice365activeusercounts?view=graph-rest-beta)<br>[getOffice365ServicesUserCounts](/graph/api/reportroot-getoffice365servicesusercounts?view=graph-rest-beta)<br>[getOffice365GroupsActivityDetail](/graph/api/reportroot-getoffice365groupsactivitydetail?view=graph-rest-beta)<br> [getOffice365GroupsActivityCounts](/graph/api/reportroot-getoffice365groupsactivitycounts?view=graph-rest-beta)<br>[getOffice365GroupsActivityGroupCounts](/graph/api/reportroot-getoffice365groupsactivitygroupcounts?view=graph-rest-beta)<br>[getOffice365GroupsActivityStorage](/graph/api/reportroot-getoffice365groupsactivitystorage?view=graph-rest-beta)<br>[getOffice365GroupsActivityFileCounts](/graph/api/reportroot-getoffice365groupsactivityfilecounts?view=graph-rest-beta)<br>[getOneDriveActivityUserDetail](/graph/api/reportroot-getonedriveactivityuserdetail?view=graph-rest-beta)<br>[getOneDriveActivityUserCounts](/graph/api/reportroot-getonedriveactivityusercounts?view=graph-rest-beta)<br>[getOneDriveActivityFileCounts](/graph/api/reportroot-getonedriveactivityfilecounts?view=graph-rest-beta)<br>[getOneDriveUsageAccountDetail](/graph/api/reportroot-getonedriveusageaccountdetail?view=graph-rest-beta)<br>[getOneDriveUsageAccountCounts](/graph/api/reportroot-getonedriveusageaccountcounts?view=graph-rest-beta)<br>[getOneDriveUsageFileCounts](/graph/api/reportroot-getonedriveusagefilecounts?view=graph-rest-beta)<br>[getOneDriveUsageStorage](/graph/api/reportroot-getonedriveusagestorage?view=graph-rest-beta)<br>[getSharePointActivityUserDetail](/graph/api/reportroot-getsharepointactivityuserdetail?view=graph-rest-beta)<br>[getSharePointActivityFileCounts](/graph/api/reportroot-getsharepointactivityfilecounts?view=graph-rest-beta)<br>[getSharePointActivityUserCounts](/graph/api/reportroot-getsharepointactivityusercounts?view=graph-rest-beta)<br>[getSharePointActivityPages](/graph/api/reportroot-getsharepointactivitypages?view=graph-rest-beta)<br>[getSharePointSiteUsageDetail](/graph/api/reportroot-getsharepointsiteusagedetail?view=graph-rest-beta)<br>[getSharePointSiteUsageFileCounts](/graph/api/reportroot-getsharepointsiteusagefilecounts?view=graph-rest-beta)<br>[getSharePointSiteUsageSiteCounts](/graph/api/reportroot-getsharepointsiteusagesitecounts?view=graph-rest-beta)<br>[getSharePointSiteUsageStorage](/graph/api/reportroot-getsharepointsiteusagestorage?view=graph-rest-beta)<br>[getSharePointSiteUsagePages](/graph/api/reportroot-getsharepointsiteusagepages?view=graph-rest-beta)<br>[getSkypeForBusinessActivityUserDetail](/graph/api/reportroot-getskypeforbusinessactivityuserdetail?view=graph-rest-beta)<br>[getSkypeForBusinessActivityCounts](/graph/api/reportroot-getskypeforbusinessactivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessActivityUserCounts](/graph/api/reportroot-getskypeforbusinessactivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessDeviceUsageUserDetail](/graph/api/reportroot-getskypeforbusinessdeviceusageuserdetail?view=graph-rest-beta)<br>[getSkypeForBusinessDeviceUsageDistributionUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusagedistributionusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessDeviceUsageUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusageusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessOrganizerActivityCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessOrganizerActivityUserCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessOrganizerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityminutecounts?view=graph-rest-beta)<br>[getSkypeForBusinessParticipantActivityCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessParticipantActivityUserCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessParticipantActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityminutecounts?view=graph-rest-beta)<br>[getSkypeForBusinessPeerToPeerActivityCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessPeerToPeerActivityUserCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessPeerToPeerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityminutecounts?view=graph-rest-beta). |

### <a name="directory-apis"></a>API de directorio
| Tipo de cambio | Versión                                    | Descripción                              |
| :---------- | :----------------------------------------- | :--------------------------------------- |
| Adición    | Beta | Se agregaron las propiedades 'externalUserState' y 'externalUserStateChangeDateTime' al objeto [user](/graph/api/resources/user?view=graph-rest-beta).|

## <a name="october-2018"></a>Octubre de 2018

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | beta | Se agregó el nuevo método transitiveMembers en [groups](/graph/api/group-list-transitivemembers?view=graph-rest-beta). Este método devuelve una lista plana de miembros incluyendo los miembros anidados.|
| Adición | beta | Se agregó el nuevo método transitiveMemberOf en [usuarios](/graph/api/user-list-transitivemembersof?view=graph-rest-beta), [grupos](/graph/api/group-list-transitivemembersof?view=graph-rest-beta), [dispositivos](/graph/api/device-list-transitivemembersof?view=graph-rest-beta) y [entidades de servicio](/graph/api/serviceprincipal-list-transitivemembersof?view=graph-rest-beta).|
| Adición | beta | Se agregó el método memberOf para obtener la [pertenencia](/graph/api/device-list-members?view=graph-rest-beta) directa de un dispositivo. Se ha agregado este método para obtener la lista de pertenencias incluyendo las pertenencias anidadas.|
| Adición | beta | Se agregaron nuevas propiedades a [users](/graph/api/resources/user?view=graph-rest-beta): **faxNumber**, **onPremisesDistinguishedName** y **otherMails**.|

### <a name="riskyusers-apis"></a>API de RiskyUsers

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Adición |beta| Se añadió [la API riskyUsers](/graph/api/resources/riskyuser?view=graph-rest-beta), que representa los usuarios de Azure AD que están en peligro, detectados por Azure AD Identity Protection. |


### <a name="signin-apis"></a>API de inicio de sesión

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Cambio   |beta| Se cambió el nombre de la propiedad `conditionalAccessPolicies` a `appliedConditionalAccessPolicy`.|
|Adición |beta| Se introdujeron propiedades de riesgo adicionales en la [API de inicio de sesión](/graph/api/resources/signin?view=graph-rest-beta), incluyendo `riskDetail`, `riskLevelAggregated`, `riskLevelDuringSignIn`, `riskEventTypes` y `riskState`.|
|Adición |beta| Se introdujeron propiedades de inicio de sesión adicionales en la [API de inicio de sesión](/graph/api/resources/signin?view=graph-rest-beta), incluyendo `authenticationProcessingDetails`, `originalRequestID`, `isInteractive`, `tokenIssuerName`, `tokenIssuerType`, `correlationId` y `processingTimeinMilliseconds`.|
|Eliminación   |beta| Se eliminó la propiedad `isRisky`.|

## <a name="october-2018"></a>Octubre de 2018

### <a name="delta-query"></a>Consulta delta

| **Tipo de cambio** | **Versión** | **Descripción**                  |
|:------------|:--------|:-----------------------------------------|
| Adición    | Beta   | Se agregó la capacidad [consulta delta](delta-query-overview.md) para [directoryObject](/graph/api/directoryobject-delta?view=graph-rest-beta) |
| Cambio      | V1.0 y beta  | Comportamiento alternativo para devolver propiedades cambiadas solo en respuesta JSON para [usuarios](/graph/api/user-delta?view=graph-rest-1.0) y [grupos](/graph/api/group-delta?view=graph-rest-1.0). |
| Adición    | v1.0   | Se agregó la función [delta](/graph/api/directoryrole-delta?view=graph-rest-1.0) para [directoryRole](/graph/api/resources/directoryrole?view=graph-rest-1.0) para admitir [control de cambios mediante consulta delta](delta-query-overview.md). |

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | Beta | Se agregó la propiedad **licenseAssignmentStates** a la entidad [User](/graph/api/resources/user?view=graph-rest-beta) para [Licencias basadas en grupos](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).|
| Adición | Beta | Se agregó el recurso **licenseAssignmentState** para [Licencias basadas en grupos](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).|
| Adición | Beta | Se agregaron las propiedades **assignedLicenses**, **licenseProcessingState**, **hasMembersWithLicenseErrors** y **membersWithLicenseErrors** a la entidad [Group](/graph/api/resources/group?view=graph-rest-beta) para [Licencias basadas en grupos](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).|

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Se agregó la propiedad **tenantLockdownRequireNetworkDuringOutOfBoxExperience** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-1.0)|
|Adición|v1.0|Se agregó la propiedad **v12_0** al tipo complejo [iosMinimumOperatingSystem](/graph/api/resources/intune-apps-iosminimumoperatingsystem?view=graph-rest-1.0)|
|Adición|beta|Se agregó la propiedad **lastReportAggregationDateTime** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta)|
|Adición|beta|Nuevas entidades agregadas:<br/>[intuneBrandingProfile](/graph/api/resources/intune-wip-intunebrandingprofile?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos complejos agregados:<br/>[deviceAndAppManagementAssignedRoleIds](/graph/api/resources/intune-rbac-deviceandappmanagementassignedroleids?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos de enumeración agregados:<br/>[applicationGuardEnabledOptions](/graph/api/resources/intune-deviceconfig-applicationguardenabledoptions?view=graph-rest-beta)<br/>[autoRestartNotificationDismissalMethod](/graph/api/resources/intune-deviceconfig-autorestartnotificationdismissalmethod?view=graph-rest-beta)<br/>[meteredConnectionLimitType](/graph/api/resources/intune-deviceconfig-meteredconnectionlimittype?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la acción [enableLegacyPcManagement](/graph/api/intune-deviceconfig-devicemanagement-enablelegacypcmanagement?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [extendFeatureUpdatesPause](/graph/api/intune-deviceconfig-windowsupdateforbusinessconfiguration-extendfeatureupdatespause?view=graph-rest-beta) en [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [extendQualityUpdatesPause](/graph/api/intune-deviceconfig-windowsupdateforbusinessconfiguration-extendqualityupdatespause?view=graph-rest-beta) en [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [unassignUserFromDevice](/graph/api/intune-enrollment-windowsautopilotdeviceidentity-unassignuserfromdevice?view=graph-rest-beta) en [windowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-windowsautopilotdeviceidentity?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [getAssignedRoleIdsForLoggedInUser](/graph/api/intune-rbac-devicemanagement-getassignedroleidsforloggedinuser?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [getManagedDevicesWithAppFailures](/graph/api/intune-troubleshooting-user-getmanageddeviceswithappfailures?view=graph-rest-beta) en [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [managedDeviceEnrollmentAbandonmentSummary](/graph/api/intune-troubleshooting-reportroot-manageddeviceenrollmentabandonmentsummary?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [managedDeviceEnrollmentAbandonmentDetails](/graph/api/intune-troubleshooting-reportroot-manageddeviceenrollmentabandonmentdetails?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta) |
|Eliminación|beta|Se eliminó la propiedad **subjectAlternativeNameType** de la entidad [androidForWorkCertificateProfileBase](/graph/api/resources/intune-deviceconfig-androidforworkcertificateprofilebase?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **subjectAlternativeNameType** a la entidad [androidForWorkPkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkpkcscertificateprofile?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **certificateStore**, **customSubjectAlternativeNames** y **subjectAlternativeNameType** a la entidad [androidForWorkScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkscepcertificateprofile?view=graph-rest-beta)|
|Eliminación|beta|Se eliminó la propiedad **subjectAlternativeNameType** de la entidad [androidWorkProfileCertificateProfileBase](/graph/api/resources/intune-deviceconfig-androidworkprofilecertificateprofilebase?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **subjectAlternativeNameType** a la entidad [androidWorkProfilePkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-androidworkprofilepkcscertificateprofile?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **certificateStore**, **customSubjectAlternativeNames** y **subjectAlternativeNameType** a la entidad [androidWorkProfileScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidworkprofilescepcertificateprofile?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **legacyPcManangementEnabled** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta)|
|Eliminación|beta|Se eliminó la propiedad **pinRequiredOnLaunchInsteadOfBiometric** de la entidad [managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **roleScopeTagIds** a la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **applicationGuardEnabledOptions** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **selectedMobileAppIds** a la entidad [windows10EnrollmentCompletionPageConfiguration](/graph/api/resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **engagedRestartDeadlineInDays**, **engagedRestartSnoozeScheduleInDays**, **engagedRestartTransitionScheduleInDays**, **autoRestartNotificationDismissal**, **scheduleRestartWarningInHours** y **scheduleImminentRestartWarningInMinutes** a la entidad [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **preSharedKey** y **meteredConnectionLimit** a la entidad [windowsWifiConfiguration](/graph/api/resources/intune-deviceconfig-windowswificonfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad de navegación **intuneBrandingProfiles** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **v6_0**, **v7_0**, **v7_1**, **v8_0**, **v8_1** y **v9_0** al tipo complejo [androidMinimumOperatingSystem](/graph/api/resources/intune-apps-androidminimumoperatingsystem?view=graph-rest-beta) complex type|
|Adición|beta|Se agregó la propiedad **v12_0** al tipo complejo [iosMinimumOperatingSystem](/graph/api/resources/intune-apps-iosminimumoperatingsystem?view=graph-rest-beta)|
|Eliminación|beta|Se eliminó la propiedad **runAsLoggedOnUser** del tipo complejo [win32LobAppPowerShellScriptDetection](/graph/api/resources/intune-apps-win32lobapppowershellscriptdetection?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **lastUpdateDateTime** al tipo complejo [osVersionCount](/graph/api/resources/intune-devices-osversioncount?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **lastUpdateDateTime** al tipo complejo [windowsMalwareCategoryCount](/graph/api/resources/intune-devices-windowsmalwarecategorycount?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **lastUpdateDateTime** al tipo complejo [windowsMalwareExecutionStateCount](/graph/api/resources/intune-devices-windowsmalwareexecutionstatecount?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **lastUpdateDateTime** al tipo complejo [windowsMalwareNameCount](/graph/api/resources/intune-devices-windowsmalwarenamecount?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **lastUpdateDateTime** al tipo complejo [windowsMalwareStateCount](/graph/api/resources/intune-devices-windowsmalwarestatecount?view=graph-rest-beta)|

### <a name="privileged-identity-management-apis"></a>API de Privileged Identity Management

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Cambio | beta | Se cambió la entidad [privilegedapproval](/graph/api/resources/privilegedapproval?view=graph-rest-beta).|
| Adición | beta | Se ha agregado la entidad [privilegedroleassignmentrequest](/graph/api/resources/privilegedroleassignmentrequest?view=graph-rest-beta), así como los métodos y las acciones siguientes:<br> [List](/graph/api/privilegedroleassignmentrequest-list?view=graph-rest-beta) <br> [Create](/graph/api/privilegedroleassignmentrequest-post?view=graph-rest-beta) <br> [Cancel](/graph/api/privilegedroleassignmentrequest-cancel?view=graph-rest-beta) <br> [My](/graph/api/privilegedroleassignmentrequest-my?view=graph-rest-beta) |
| Adición | beta | Se agregó [Update](/graph/api/privilegedrolesettings-update?view=graph-rest-beta) para [privilegedRoleSettings](/graph/api/resources/privilegedrolesettings?view=graph-rest-beta)|
| Eliminación |beta| Quedó en desuso [Active una asignación de roles automáticamente.](/graph/api/privilegedrole_selfactivate?view=graph-rest-beta)|

### <a name="microsoft-teams-apis"></a>API de Microsoft Teams

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a las API de [archivar equipo](/graph/api/team-archive?view=graph-rest-beta) y [desarchivar equipo](/graph/api/team-unarchive?view=graph-rest-beta).|

### <a name="outlook-contacts"></a>Contactos de Outlook

| **Tipo de cambio** | **Versión** | **Description**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Eliminación         | v1.0        | Esto es una corrección de la documentación: se eliminó la propiedad **flag** del tema de entidad [contact](/graph/api/resources/contact?view=graph-rest-1.0). La propiedad nunca estuvo disponible en la entidad **contact**.|

### <a name="reports-apis"></a>API de informes
| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Adición    | v1.0    | Se agregó la propiedad **Site ID** a [getSharePointSiteUsageDetail](/graph/api/reportroot-getsharepointsiteusagedetail?view=graph-rest-1.0). |

## <a name="september-2018"></a>Septiembre de 2018

### <a name="calls-and-online-meetings-api"></a>API de reuniones en línea y llamadas

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | El recurso [application](/graph/api/resources/application?view=graph-rest-beta) se actualizó para agregar una colección de llamadas. |
| Cambio          | Beta        | El recurso [operation](/graph/api/resources/operation?view=graph-rest-beta) se actualizó para admitir API de reuniones y llamadas de larga duración. |
| Adición        | Beta        | Se agrego el recurso [call](/graph/api/resources/call?view=graph-rest-beta) para administrar llamadas de audio y vídeo (al principio, en Microsoft Teams), incluidas las API de [crear llamadas](/graph/api/application-post-calls?view=graph-rest-beta), [Recuperar una llamada](/graph/api/call-get?view=graph-rest-beta), [eliminar (colgar) una llamada](/graph/api/call-delete?view=graph-rest-beta), [responder a una llamada](/graph/api/call-answer?view=graph-rest-beta), [rechazar una llamada](/graph/api/call-reject?view=graph-rest-beta), [redirigir una llamada](/graph/api/call-redirect?view=graph-rest-beta) y [ transferir una llamada](/graph/api/call-transfer?view=graph-rest-beta). También hemos agregado API para admitir [escenarios IVR](/graph/api/resources/calls-api-ivr-overview?view=graph-rest-beta): [reproducir un mensaje](/graph/api/call-playprompt?view=graph-rest-beta), [grabar una llamada](/graph/api/call-record?view=graph-rest-beta), [cancelar el procesamiento de datos multimedia](/graph/api/call-cancelmediaprocessing?view=graph-rest-beta) y [suscribirse a las notificaciones de marcación por tono](/graph/api/call-subscribetotone?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó el recurso [participant](/graph/api/resources/call?view=graph-rest-beta) y las API para la administración de llamadas de audio o vídeo y reuniones, incluyendo [recuperar un objeto participante](/graph/api/participant-get?view=graph-rest-beta), [configurar la mezcla de audio para un participante](/graph/api/participant-configuremixer?view=graph-rest-beta), silenciar a [uno](/graph/api/participant-mute?view=graph-rest-beta) o [todos](/graph/api/participant-muteall?view=graph-rest-beta) los participantes, [recuperar una lista de los participantes](/graph/api/call-list-participants?view=graph-rest-beta) en una llamada o reunión e [invitar a participantes](/graph/api/participant-invite?view=graph-rest-beta) a una llamada o reunión. |
| Adición        | Beta        | Se agregaron las API para que las aplicaciones puedan administrar y participar en llamadas y reuniones, incluida la capacidad de [compartir contenido](/graph/api/call-changescreensharingrole?view=graph-rest-beta), [desactivar y reactivar su audio](/graph/api/call-unmute?view=graph-rest-beta) y [actualizar los metadatos asociados con una llamada](/graph/api/call-updatemetadata?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó el recurso [grupo de enrutamiento de audio](/graph/api/resources/audioroutinggroup?view=graph-rest-beta) y API para administrar las rutas de audio privadas entre los participantes en una conversación con varios participantes, incluyendo [crear de grupos de enrutamiento de audio](/graph/api/call-post-audioroutinggroups?view=graph-rest-beta), [ recuperar una lista de ellos](/graph/api/audioroutinggroup-get?view=graph-rest-beta), [actualizarlos](/graph/api/audioroutinggroup-update?view=graph-rest-beta) y [eliminarlos](/graph/api/audioroutinggroup-delete?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó el recurso [reunión en línea](/graph/api/resources/audioroutinggroup?view=graph-rest-beta) y API para administrar las reuniones en línea de Microsoft Teams. El principio, hay una única API para reuniones en línea, para [recuperar un objeto de la reunión en línea](/graph/api/onlinemeeting-get?view=graph-rest-beta). También se ha agregado un recurso relacionado para la [información de audioconferencia](/graph/api/resources/audioconferencing?view=graph-rest-beta) asociada a una reunión (por ejemplo, dirección URL de acceso telefónico, contraseñas y números de teléfono). |
| Adición        | Beta        | Muchas de las API de llamadas y reuniones toman su tiempo, por lo que se agregaron recursos para estas operaciones de larga duración: [operaciones específicas de llamadas](/graph/api/resources/commsoperation?view=graph-rest-beta), [reproducción de indicaciones de audio](/graph/api/resources/playpromptoperation?view=graph-rest-beta) y [ grabación](/graph/api/resources/recordoperation?view=graph-rest-beta).  |

### <a name="dynamics-365-business-central-api"></a>API de Dynamics 365 Business Central

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | Beta          | Se agregaron AP de finanzas para Dynamics 365 Business Central. Para obtener más información, consulte la [referencia de la API de finanzas](/graph/api/resources/dynamics-graph-reference?view=graph-rest-beta)

### <a name="microsoft-graph-data-connect"></a>Conexión a los datos de Microsoft Graph

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Adición         | No aplicable| Se introdujo la posibilidad de obtener acceso a datos de Office 365 de forma masiva. Para obtener más información, vea [Conexión de datos de Microsoft Graph (versión preliminar)](data-connect-overview.md).|

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-apps-manageddevicemobileappconfiguration-assign?view=graph-rest-1.0) a [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-1.0) |
|Adición|beta|Nuevas entidades agregadas:<br/>[officeClientConfiguration](/graph/api/resources/intune-cirrus-officeclientconfiguration?view=graph-rest-beta)<br/>[officeClientConfigurationAssignment](/graph/api/resources/intune-cirrus-officeclientconfigurationassignment?view=graph-rest-beta)<br/>[officeConfiguration](/graph/api/resources/intune-cirrus-officeconfiguration?view=graph-rest-beta)<br/>[windowsOfficeClientConfiguration](/graph/api/resources/intune-cirrus-windowsofficeclientconfiguration?view=graph-rest-beta)<br/>[windowsOfficeClientSecurityConfiguration](/graph/api/resources/intune-cirrus-windowsofficeclientsecurityconfiguration?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos complejos agregados:<br/>[officeClientCheckinStatus](/graph/api/resources/intune-cirrus-officeclientcheckinstatus?view=graph-rest-beta)<br/>[officeConfigurationAssignmentTarget](/graph/api/resources/intune-cirrus-officeconfigurationassignmenttarget?view=graph-rest-beta)<br/>[officeConfigurationGroupAssignmentTarget](/graph/api/resources/intune-cirrus-officeconfigurationgroupassignmenttarget?view=graph-rest-beta)<br/>[officeUserCheckinSummary](/graph/api/resources/intune-cirrus-officeusercheckinsummary?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la acción [assign](/graph/api/intune-cirrus-officeclientconfiguration-assign?view=graph-rest-beta) en [officeClientConfiguration](/graph/api/resources/intune-cirrus-officeclientconfiguration?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción **updatePrioritie** en [officeClientConfiguration](/graph/api/resources/intune-cirrus-officeclientconfiguration?view=graph-rest-beta) collection |
|Adición|beta|Nuevas entidades agregadas:<br/>[deviceConfigurationConflictSummary](/graph/api/resources/intune-deviceconfig-deviceconfigurationconflictsummary?view=graph-rest-beta)<br/>[importedWindowsAutopilotDeviceIdentityUpload](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload?view=graph-rest-beta)<br/>[win32LobApp](/graph/api/resources/intune-apps-win32lobapp?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos complejos agregados:<br/>[deviceConfigurationTargetedUserAndDevice](/graph/api/resources/intune-deviceconfig-deviceconfigurationtargeteduseranddevice?view=graph-rest-beta)<br/>[win32LobAppDetection](/graph/api/resources/intune-apps-win32lobappdetection?view=graph-rest-beta)<br/>[win32LobAppFileSystemDetection](/graph/api/resources/intune-apps-win32lobappfilesystemdetection?view=graph-rest-beta)<br/>[win32LobAppInstallExperience](/graph/api/resources/intune-apps-win32lobappinstallexperience?view=graph-rest-beta)<br/>[win32LobAppMsiInformation](/graph/api/resources/intune-apps-win32lobappmsiinformation?view=graph-rest-beta)<br/>[win32LobAppPowerShellScriptDetection](/graph/api/resources/intune-apps-win32lobapppowershellscriptdetection?view=graph-rest-beta)<br/>[win32LobAppProductCodeDetection](/graph/api/resources/intune-apps-win32lobappproductcodedetection?view=graph-rest-beta)<br/>[win32LobAppRegistryDetection](/graph/api/resources/intune-apps-win32lobappregistrydetection?view=graph-rest-beta)<br/>[win32LobAppReturnCode](/graph/api/resources/intune-apps-win32lobappreturncode?view=graph-rest-beta)<br/>[windows10AppsForceUpdateSchedule](/graph/api/resources/intune-deviceconfig-windows10appsforceupdateschedule?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos de enumeración agregados:<br/>[administratorConfiguredDeviceComplianceState](/graph/api/resources/intune-deviceconfig-administratorconfigureddevicecompliancestate?view=graph-rest-beta)<br/>[importedWindowsAutopilotDeviceIdentityUploadStatus](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentityuploadstatus?view=graph-rest-beta)<br/>[microsoftStoreForBusinessPortalSelectionOptions](/graph/api/resources/intune-onboarding-microsoftstoreforbusinessportalselectionoptions?view=graph-rest-beta)<br/>[win32LobAppDetectionOperator](/graph/api/resources/intune-apps-win32lobappdetectionoperator?view=graph-rest-beta)<br/>[win32LobAppFileSystemDetectionType](/graph/api/resources/intune-apps-win32lobappfilesystemdetectiontype?view=graph-rest-beta)<br/>[win32LobAppMsiPackageType](/graph/api/resources/intune-apps-win32lobappmsipackagetype?view=graph-rest-beta)<br/>[win32LobAppRegistryDetectionType](/graph/api/resources/intune-apps-win32lobappregistrydetectiontype?view=graph-rest-beta)<br/>[win32LobAppReturnCodeType](/graph/api/resources/intune-apps-win32lobappreturncodetype?view=graph-rest-beta)<br/>[windows10AppsUpdateRecurrence](/graph/api/resources/intune-deviceconfig-windows10appsupdaterecurrence?view=graph-rest-beta)<br/>[windowsAppStartLayoutTileSize](/graph/api/resources/intune-deviceconfig-windowsappstartlayouttilesize?view=graph-rest-beta)<br/>[windowsAutopilotProfileAssignmentDetailedStatus](/graph/api/resources/intune-enrollment-windowsautopilotprofileassignmentdetailedstatus?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la acción **overrideComplianceState** en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción **getTargetedUsersAndDevices** en [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta) collection |
|Adición|beta|Se agregó la función [autopilotDeviceStream](/graph/api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-autopilotdevicestream?view=graph-rest-beta) en [importedWindowsAutopilotDeviceIdentityUpload](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload?view=graph-rest-beta) |
|Adición|beta|Se agregó la propiedad **restrictedApps** a la entidad [androidCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidcompliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **tokenCreationDateTime** a la entidad [androidDeviceOwnerEnrollmentProfile](/graph/api/resources/intune-androidforwork-androiddeviceownerenrollmentprofile?view=graph-rest-beta)|
|Eliminación|beta|Se eliminó la propiedad **restrictedApps** de la entidad [androidForWorkCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidforworkcompliancepolicy?view=graph-rest-beta)|
|Eliminación|beta|Se eliminó la propiedad **restrictedApps** de la entidad [androidWorkProfileCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidworkprofilecompliancepolicy?view=graph-rest-beta)|
|Cambio|beta|Se cambiaron las propiedades siguientes en la entidad [appleVpnConfiguration](/graph/api/resources/intune-deviceconfig-applevpnconfiguration?view=graph-rest-beta):<br/>**enablePerApp** de requerido a opcional<br/>|
|Adición|beta|Se agregaron las propiedades **disableProtectionOfManagedOutboundOpenInData** y **protectInboundDataFromUnknownSources** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **microsoftStoreForBusinessPortalSelection** a la entidad [deviceAppManagement](/graph/api/resources/intune-shared-deviceappmanagement?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **passcodeMinutesOfInactivityBeforeScreenTimeout** a la entidad [iosCompliancePolicy](/graph/api/resources/intune-deviceconfig-ioscompliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **useOAuth** a la entidad [iosEasEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-ioseasemailprofileconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **kioskModeBlockVolumeButtons**, **classroomForceRequestPermissionToLeaveClasses**, **keychainBlockCloudSync**, **pkiBlockOTAUpdates**, **privacyForceLimitAdTracking**, **enterpriseBookBlockBackup**, **enterpriseBookBlockMetadataSync**, **airPrintBlocked**, **airPrintBlockCredentialsStorage**, **airPrintForceTrustedTLS**, **airPrintBlockiBeaconDiscovery**, **blockSystemAppRemoval** y **vpnBlockCreation** a la entidad [iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **disableProtectionOfManagedOutboundOpenInData** y **protectInboundDataFromUnknownSources** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **gatekeeperAllowedAppSource** a la entidad [macOSCompliancePolicy](/graph/api/resources/intune-deviceconfig-macoscompliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **keychainBlockCloudSync**, **airPrintBlocked**, **airPrintForceTrustedTLS** y **airPrintBlockiBeaconDiscovery** a la entidad [macOSGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-macosgeneraldeviceconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **deviceModel** y **deviceManufacturer** a la entidad [managedAppRegistration](/graph/api/resources/intune-mam-managedappregistration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **enabledForScopeValidation** a la entidad [resourceOperation](/graph/api/resources/intune-rbac-resourceoperation?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **claimTokenManagementFromExternalMdm** a la entidad [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **windows10AppsForceUpdateSchedule** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **deploymentProfileAssignmentDetailedStatus** a la entidad [windowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-windowsautopilotdeviceidentity?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades de navegación **deviceConfigurationConflictSummary** y **importedWindowsAutopilotDeviceIdentityUploads** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad de navegación **intendedDeploymentProfile** a la entidad [windowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-windowsautopilotdeviceidentity?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **startLayoutTileSize** y **name** al tipo complejo [windowsKioskAppBase](/graph/api/resources/intune-deviceconfig-windowskioskappbase?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **desktopApplicationId** y **desktopApplicationLinkPath** al tipo complejo [windowsKioskDesktopApp](/graph/api/resources/intune-deviceconfig-windowskioskdesktopapp?view=graph-rest-beta)|
|Eliminación|beta|Se eliminó la propiedad **name** del tipo complejo [windowsKioskDesktopApp](/graph/api/resources/intune-deviceconfig-windowskioskdesktopapp?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **disallowDesktopApps** al tipo complejo [windowsKioskMultipleApps](/graph/api/resources/intune-deviceconfig-windowskioskmultipleapps?view=graph-rest-beta)|
|Cambio|beta|Se cambiaron las propiedades siguientes en el tipo complejo [windowsKioskMultipleApps](/graph/api/resources/intune-deviceconfig-windowskioskmultipleapps?view=graph-rest-beta):<br/>**startMenuLayoutXml** de requerido a opcional<br/>|
|Adición|beta|Se agregaron las propiedades **v10_1607**, **v10_1703**, **v10_1709** y **v10_1803** al tipo complejo [windowsMinimumOperatingSystem](/graph/api/resources/intune-apps-windowsminimumoperatingsystem?view=graph-rest-beta)|
|Adición|beta|Se agregó el miembro **paloAltoGlobalProtect** al tipo de enumeración [androidWorkProfileVpnConnectionType](/graph/api/resources/intune-deviceconfig-androidworkprofilevpnconnectiontype?view=graph-rest-beta).|
|Adición|beta|Se agregó el miembro **remoteLock** al tipo de enumeración [deviceComplianceActionType](/graph/api/resources/intune-deviceconfig-devicecomplianceactiontype?view=graph-rest-beta)|


### <a name="microsoft-teams-apis"></a>API de Microsoft Teams

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Adición|beta|Se agregó la API para [pestañas](/graph/api/resources/teamstab?view=graph-rest-beta).|
|Adición|beta|Se agregó la API para [publicar aplicaciones para su organización](/graph/api/resources/teamsapp?view=graph-rest-beta).|
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a [GET /teams/{id}](/graph/api/team-get?view=graph-rest-beta). |
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a [GET /teams/{id}/channels](/graph/api/group-list-channels?view=graph-rest-beta). |
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a [GET /teams/{id}/channels/{id}](/graph/api/channel-get?view=graph-rest-beta). |
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a [PUT /groups/{id}/team](/graph/api/team-put-teams?view=graph-rest-beta). |
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a [PATCH /teams/{id}](/graph/api/team-update?view=graph-rest-beta). |
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a [Crear canal](/graph/api/channel-post?view=graph-rest-beta), [Actualizar canal](/graph/api/channel-patch?view=graph-rest-beta) y [Eliminar canal](/graph/api/channel-delete?view=graph-rest-beta). |
|Eliminación|beta| Se eliminó la propiedad isBlocks y se agregó installedState de [teamsApp](/graph/api/resources/teamsapp?view=graph-rest-beta).|
|Cambio| beta | El nombre de la propiedad de contexto en [teamsApp](/graph/api/resources/teamsapp?view=graph-rest-beta) ha cambiado a distributionMethod.|

### <a name="outlook-mail"></a>Correo de Outlook

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | La propiedad **internetMessageHeaders** de la entidad [message](/graph/api/resources/message?view=graph-rest-1.0) ahora se puede escribir en la creación del mensaje. |


### <a name="project-rome-notifications-api"></a>API de notificaciones del Proyecto Rome

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición          | Beta        | Se agregó el tipo de recurso [notification](/graph/api/resources/projectrome-notification?view=graph-rest-beta). |
| Adición          | Beta        | Se agregó la API [crear y publicar notificaciones] (/graph/api/projectrome_notification_post?view=graph-rest-beta).|

### <a name="security-apis"></a>API de seguridad

| **Tipo de cambio** | **Versión** | **Descripción**              |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta       | Se han agregado las API de puntuación segura a las [API para seguridad](/graph/api/resources/securescore-api-overview?view=graph-rest-beta), incluidos los siguientes recursos y operaciones:<br/>[secureScores](/graph/api/resources/securescores?view=graph-rest-beta) (y entidades relacionadas)<br/>[Lista secureScores](/graph/api/securescores-list?view=graph-rest-beta)<br/>[secureScoreControlProfiles](/graph/api/resources/securescorecontrolprofiles?view=graph-rest-beta)<br/>[Lista secureScoreControlProfiles](/graph/api/securescorecontrolprofiles-list?view=graph-rest-beta)<br/>[Actualizar secureScoreControlProfiles](/graph/api/securescorecontrolprofiles-update?view=graph-rest-beta)


### <a name="onedrive-and-sharepoint-apis"></a>API de SharePoint y OneDrive

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la acción **deferCommit** argument to the [createUploadSession](/graph/api/driveitem-createuploadsession?view=graph-rest-beta) en [driveItem](/graph/api/resources/driveitem?view=graph-rest-beta)|
| Adición        | Beta        | Se agregó el tipo complejo [storagePlanInformation](/graph/api/resources/storageplaninformation?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **storagePlanInformation** al tipo complejo [quota](/graph/api/resources/quota?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **following** navigation a la entidad [drive](/graph/api/resources/drive?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la acción [follow](/graph/api/driveitem-follow?view=graph-rest-beta) en [driveItem](/graph/api/resources/driveitem?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la API [dejar de seguir](/graph/api/driveitem-unfollow?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **hasPassword** a la entidad [permission](/graph/api/resources/permission?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **preventsDownload** al tipo complejo [sharingLink](/graph/api/resources/sharinglink?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad de navegación **permission** a la entidad [sharedDriveItem](/graph/api/resources/shareddriveitem?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **geolocation** a la entidad [columnDefinition](/graph/api/resources/columndefinition?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó el tipo complejo [geolocationColumn](/graph/api/resources/geolocationcolumn?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **analytics** a la entidad [driveItem](/graph/api/resources/driveitem?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **analytics** a la entidad [site](/graph/api/resources/site?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **analytics** a la entidad [listItem](/graph/api/resources/listitem?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función **getActivitiesByInterval** en la entidad [driveItem](/graph/api/resources/driveitem?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función **getActivitiesByInterval** en la entidad [site](/graph/api/resources/site?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función **getActivitiesByInterval** en la entidad [listItem](/graph/api/resources/listitem?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la entidad [itemAnalytics](/graph/api/resources/itemanalytics?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la entidad [itemActivityStat](/graph/api/resources/itemactivity?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó el tipo complejo [itemActionStat](/graph/api/resources/itemactionstat?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó el tipo complejo [accessAction](/graph/api/resources/accessaction?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó el tipo complejo [incompleteData](/graph/api/resources/incompletedata?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **access** al tipo complejo [itemActivity](/graph/api/resources/itemactivity?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la propiedad **location** al tipo complejo [itemActivity](/graph/api/resources/itemactivity?view=graph-rest-beta) |
| Adición        | v1.0        | Se agregó la acción **preview** a la entidad [driveItem](/graph/api/resources/driveitem?view=graph-rest-1.0) |
| Adición        | v1.0        | Se agregó el tipo complejo [itemPreviewInfo](/graph/api/resources/itempreviewinfo?view=graph-rest-1.0) |

## <a name="august-2018"></a>Agosto de 2018

### <a name="delta-query"></a>Consulta delta

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la capacidad [consulta delta](delta-query-overview.md) para las entidades siguientes en Azure AD:<br/>[application](/graph/api/application-delta?view=graph-rest-beta)<br/>[directoryRole](/graph/api/directoryrole-delta?view=graph-rest-beta)<br/>[servicePrincipal](/graph/api/serviceprincipal-delta?view=graph-rest-beta) |

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | v1.0 | Se agregó la propiedad isMultipleDataLocationsForServicesEnabled al recurso [Organization](/graph/api/resources/organization?view=graph-rest-beta) que permite a las aplicaciones comprobar que el inquilino está habilitado para funciones multigeográficas. Se agregó la propiedad preferredDataLocation a los recursos [user](/graph/api/resources/user?view=graph-rest-beta) y [group](/graph/api/resources/group?view=graph-rest-beta) que permiten la configuración de una ubicación de datos preferida para un usuario y grupo.|
| Adición | v1.0 | Se agregó la propiedad [onPremisesProvisioningErrors](/graph/api/resources/onpremisesprovisioningerror?view=graph-rest-1.0) a las entidades [User](/graph/api/resources/user?view=graph-rest-1.0) y [Group](/graph/api/resources/group?view=graph-rest-1.0) que representa los errores de sincronización de directorio al sincronizar directorios locales con Azure Active Directory al usar el producto de sincronización de Microsoft (incluidos Azure AD Connect, DirSync y el conector MIM +).|
| Adición | v1.0 | Se agregó la propiedad  [onPremisesExtensionAttributes](/graph/api/resources/onpremisesextensionattributes?view=graph-rest-1.0) a la entidad [User](/graph/api/resources/user?view=graph-rest-1.0) que contiene quince propiedades de atributo de extensión personalizada. Para un usuario con onPremisesSyncEnabled, este conjunto de propiedades se usa como patrón en Active Directory local y se sincroniza con Azure AD, es de solo lectura. Para un usuario de solo nube (donde onPremisesSyncEnabled es false), estas propiedades pueden establecerse durante la creación o la actualización.|
|Adición|v1.0|Se agregaron las propiedades **onPremisesDomainName**, **onPremisesSamAccountName** y **onPremisesUserPrincipalName** a la entidad [User](/graph/api/resources/user?view=graph-rest-1.0)|

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Nuevas entidades agregadas:<br/>[androidWorkProfileCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidworkprofilecompliancepolicy?view=graph-rest-1.0)<br/>[androidWorkProfileCustomConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilecustomconfiguration?view=graph-rest-1.0)<br/>[androidWorkProfileGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Se han agregado nuevos tipos de enumeración:<br/>[androidWorkProfileCrossProfileDataSharingType](/graph/api/resources/intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype?view=graph-rest-1.0)<br/>[androidWorkProfileDefaultAppPermissionPolicyType](/graph/api/resources/intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype?view=graph-rest-1.0)<br/>[androidWorkProfileRequiredPasswordType](/graph/api/resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Se agregó la función [managedDeviceEnrollmentFailureDetails](/graph/api/intune-shared-reportroot-manageddeviceenrollmentfailuredetails?view=graph-rest-1.0) en [reportRoot](/graph/api/resources/intune-shared-reportroot?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la función [managedDeviceEnrollmentTopFailures](/graph/api/intune-shared-reportroot-manageddeviceenrollmenttopfailures?view=graph-rest-1.0) en [reportRoot](/graph/api/resources/intune-shared-reportroot?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la propiedad **kioskModeBuiltInAppId** a la entidad [iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-1.0)|
|Adición|v1.0|Se agregó el miembro **notAssigned** al tipo de enumeración [complianceStatus](/graph/api/resources/intune-shared-compliancestatus?view=graph-rest-1.0)|
|Adición|v1.0|Se agregó el miembro **pushNotification** al tipo de enumeración [deviceComplianceActionType](/graph/api/resources/intune-deviceconfig-devicecomplianceactiontype?view=graph-rest-1.0)|
|Adición|v1.0|Se agregó el miembro **userAbandonment** al tipo de enumeración [deviceEnrollmentFailureReason](/graph/api/resources/intune-troubleshooting-deviceenrollmentfailurereason?view=graph-rest-1.0)|
|Adición|v1.0|Se agregaron los miembros **compromised** y **misconfigured** al tipo de enumeración [managedDevicePartnerReportedHealthState](/graph/api/resources/intune-devices-manageddevicepartnerreportedhealthstate?view=graph-rest-1.0)|
|Adición|v1.0|Se agregó el miembro **assignedToExternalMDM** al tipo de enumeración [vppTokenState](/graph/api/resources/intune-onboarding-vpptokenstate?view=graph-rest-1.0)|
||
|Adición|beta|Nuevas entidades agregadas:<br/>[advancedThreatProtectionOnboardingDeviceSettingState](/graph/api/resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate?view=graph-rest-beta)<br/>[advancedThreatProtectionOnboardingStateSummary](/graph/api/resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary?view=graph-rest-beta)<br/>[depEnrollmentBaseProfile](/graph/api/resources/intune-enrollment-depenrollmentbaseprofile?view=graph-rest-beta)<br/>[depEnrollmentProfile](/graph/api/resources/intune-enrollment-depenrollmentprofile?view=graph-rest-beta)<br/>[depIOSEnrollmentProfile](/graph/api/resources/intune-enrollment-depiosenrollmentprofile?view=graph-rest-beta)<br/>[depMacOSEnrollmentProfile](/graph/api/resources/intune-enrollment-depmacosenrollmentprofile?view=graph-rest-beta)<br/>[enrollmentProfile](/graph/api/resources/intune-enrollment-enrollmentprofile?view=graph-rest-beta)<br/>[importedAppleDeviceIdentity](/graph/api/resources/intune-enrollment-importedappledeviceidentity?view=graph-rest-beta)<br/>[importedAppleDeviceIdentityResult](/graph/api/resources/intune-enrollment-importedappledeviceidentityresult?view=graph-rest-beta)<br/>[importedWindowsAutopilotDeviceIdentityUpload](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload?view=graph-rest-beta)<br/>[roleScopeTag](/graph/api/resources/intune-rbac-rolescopetag?view=graph-rest-beta)<br/>[windowsIdentityProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windowsidentityprotectionconfiguration?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos complejos agregados:<br/>[configurationManagerClientHealthState](/graph/api/resources/intune-devices-configurationmanagerclienthealthstate?view=graph-rest-beta)<br/>[customSubjectAlternativeName](/graph/api/resources/intune-deviceconfig-customsubjectalternativename?view=graph-rest-beta)<br/>[deviceManagementUserRightsLocalUserOrGroup](/graph/api/resources/intune-deviceconfig-devicemanagementuserrightslocaluserorgroup?view=graph-rest-beta)<br/>[deviceManagementUserRightsSetting](/graph/api/resources/intune-deviceconfig-devicemanagementuserrightssetting?view=graph-rest-beta)<br/>[managementCertificateWithThumbprint](/graph/api/resources/intune-enrollment-managementcertificatewiththumbprint?view=graph-rest-beta)<br/>[mobileAppSupportedDeviceType](/graph/api/resources/intune-troubleshooting-mobileappsupporteddevicetype?view=graph-rest-beta)<br/>[osVersionCount](/graph/api/resources/intune-devices-osversioncount?view=graph-rest-beta)<br/>[windowsMalwareCategoryCount](/graph/api/resources/intune-devices-windowsmalwarecategorycount?view=graph-rest-beta)<br/>[windowsMalwareExecutionStateCount](/graph/api/resources/intune-devices-windowsmalwareexecutionstatecount?view=graph-rest-beta)<br/>[windowsMalwareNameCount](/graph/api/resources/intune-devices-windowsmalwarenamecount?view=graph-rest-beta)<br/>[windowsMalwareOverview](/graph/api/resources/intune-devices-windowsmalwareoverview?view=graph-rest-beta)<br/>[windowsMalwareStateCount](/graph/api/resources/intune-devices-windowsmalwarestatecount?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos de enumeración agregados:<br/>[configurationManagerClientState](/graph/api/resources/intune-devices-configurationmanagerclientstate?view=graph-rest-beta)<br/>[depTokenType](/graph/api/resources/intune-enrollment-deptokentype?view=graph-rest-beta)<br/>[discoverySource](/graph/api/resources/intune-enrollment-discoverysource?view=graph-rest-beta)<br/>[importedWindowsAutopilotDeviceIdentityUploadStatus](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentityuploadstatus?view=graph-rest-beta)<br/>[iTunesPairingMode](/graph/api/resources/intune-enrollment-itunespairingmode?view=graph-rest-beta)<br/>[lanManagerAuthenticationLevel](/graph/api/resources/intune-deviceconfig-lanmanagerauthenticationlevel?view=graph-rest-beta)<br/>[localSecurityOptionsMinimumSessionSecurity](/graph/api/resources/intune-deviceconfig-localsecurityoptionsminimumsessionsecurity?view=graph-rest-beta)<br/>[resultantAppStateDetail](/graph/api/resources/intune-apps-resultantappstatedetail?view=graph-rest-beta)<br/>[vpnProviderType](/graph/api/resources/intune-deviceconfig-vpnprovidertype?view=graph-rest-beta)<br/>[windowsMalwareThreatState](/graph/api/resources/intune-devices-windowsmalwarethreatstate?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la acción [uploadDepToken](/graph/api/intune-enrollment-deponboardingsetting-uploaddeptoken?view=graph-rest-beta) en [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [syncWithAppleDeviceEnrollmentProgram](/graph/api/intune-enrollment-deponboardingsetting-syncwithappledeviceenrollmentprogram?view=graph-rest-beta) en [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [setDefaultProfile](/graph/api/intune-enrollment-enrollmentprofile-setdefaultprofile?view=graph-rest-beta) en [enrollmentProfile](/graph/api/resources/intune-enrollment-enrollmentprofile?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción **importAppleDeviceIdentityList** en la colección [importedAppleDeviceIdentity](/graph/api/resources/intune-enrollment-importedappledeviceidentity?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [updateDeviceProfileAssignment](/graph/api/intune-enrollment-enrollmentprofile-updatedeviceprofileassignment?view=graph-rest-beta) en [enrollmentProfile](/graph/api/resources/intune-enrollment-enrollmentprofile?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [shareForSchoolDataSyncService](/graph/api/intune-enrollment-deponboardingsetting-shareforschooldatasyncservice?view=graph-rest-beta) en [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [unshareForSchoolDataSyncService](/graph/api/intune-enrollment-deponboardingsetting-unshareforschooldatasyncservice?view=graph-rest-beta) en [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta) |
|Adición|beta|Se agregó la acción [assignUserToDevice](/graph/api/intune-enrollment-windowsautopilotdeviceidentity-assignusertodevice?view=graph-rest-beta) en [windowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-windowsautopilotdeviceidentity?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [getRoleScopeTagsByResource](/graph/api/intune-rbac-devicemanagement-getrolescopetagsbyresource?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [getRoleScopeTagsByIds](/graph/api/intune-rbac-devicemanagement-getrolescopetagsbyids?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [getEncryptionPublicKey](/graph/api/intune-enrollment-deponboardingsetting-getencryptionpublickey?view=graph-rest-beta) en [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [exportMobileConfig](/graph/api/intune-enrollment-enrollmentprofile-exportmobileconfig?view=graph-rest-beta) en [enrollmentProfile](/graph/api/resources/intune-enrollment-enrollmentprofile?view=graph-rest-beta) |
|Adición|beta|Se agregó la función [autopilotDeviceStream](/graph/api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-autopilotdevicestream?view=graph-rest-beta) en [importedWindowsAutopilotDeviceIdentityUpload](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload?view=graph-rest-beta) |
|Eliminación|beta|Se quitó la colección **uploadDepToken** |
|Eliminación|beta|Se quitó la acción **syncWithAppleDeviceEnrollmentProgram** de la colección [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta) |
|Eliminación|beta|Se eliminó la función **getEncryptionPublicKey** en la colección [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta) |
|Adición|beta|Se agregó la propiedad **restrictedApps** a la entidad [androidForWorkCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidforworkcompliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **vpnAlwaysOnPackageIdentifier** y **vpnEnableAlwaysOnLockdownMode** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta)|
|Eliminación|beta|Se eliminó la propiedad **packageName** de la entidad [androidForWorkMobileAppConfiguration](/graph/api/resources/intune-apps-androidforworkmobileappconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **restrictedApps** a la entidad [androidWorkProfileCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidworkprofilecompliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **vpnAlwaysOnPackageIdentifier** y **vpnEnableAlwaysOnLockdownMode** a la entidad [androidWorkProfileGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **optInToDeviceIdSharing** a la entidad [appleVpnConfiguration](/graph/api/resources/intune-deviceconfig-applevpnconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **tokenType**, **tokenName**, **syncedDeviceCount**, **defaultProfileDisplayName** y **dataSharingConsentGranted** a la entidad [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **roleScopeTagIds** a la entidad [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **roleScopeTagIds** y **supportsScopeTags** a la entidad [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **windowsMalwareOverview** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta)|
|Cambio|beta|Se cambiaron las propiedades siguientes en la entidad [iosCertificateProfileBase](/graph/api/resources/intune-deviceconfig-ioscertificateprofilebase?view=graph-rest-beta):<br/>**subjectAlternativeNameType** ha pasado de obligatoria a opcional.<br/>|
|Adición|beta|Se agregó la propiedad **restrictedApps** a la entidad [iosCompliancePolicy](/graph/api/resources/intune-deviceconfig-ioscompliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **certificateStore** y **customSubjectAlternativeNames** a la entidad [iosScepCertificateProfile](/graph/api/resources/intune-deviceconfig-iosscepcertificateprofile?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **enforcedSoftwareUpdateDelayInDays** a la entidad [iosUpdateConfiguration](/graph/api/resources/intune-deviceconfig-iosupdateconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **providerType**, **userDomain**, **strictEnforcement**, **cloudName** y **excludeList** a la entidad [iosVpnConfiguration](/graph/api/resources/intune-deviceconfig-iosvpnconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **safariBlockAutofill**, **cameraBlocked**, **iTunesBlockMusicService**, **spotlightBlockInternetResults**, **keyboardBlockDictation**, **definitionLookupBlocked**, **appleWatchBlockAutoUnlock**, **iTunesBlockFileSharing**, **iCloudBlockDocumentSync**, **iCloudBlockMail**, **iCloudBlockAddressBook**, **iCloudBlockCalendar**, **iCloudBlockReminders**, **iCloudBlockBookmarks**, **iCloudBlockNotes**, **airDropBlocked**, **passwordBlockModification** y **passwordBlockFingerprintUnlock** a la entidad [macOSGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-macosgeneraldeviceconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **roleScopeTagIds**, **windowsActiveMalwareCount**, **windowsRemediatedMalwareCount**, **notes** y **configurationManagerClientHealthState** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **installStateDetail** a la entidad [mobileAppInstallStatus](/graph/api/resources/intune-apps-mobileappinstallstatus?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **roleScopeTagIds** a la entidad [notificationMessageTemplate](/graph/api/resources/intune-notification-notificationmessagetemplate?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **targetVersion** y **updateVersion** a la entidad [officeSuiteApp](/graph/api/resources/intune-apps-officesuiteapp?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **resource** a la entidad [resourceOperation](/graph/api/resources/intune-rbac-resourceoperation?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **localStorage**, **setPowerPolicies** y **signInOnResume** a la entidad [sharedPCConfiguration](/graph/api/resources/intune-deviceconfig-sharedpcconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **configurationManagerComplianceRequired** a la entidad [windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **userRightsAccessCredentialManagerAsTrustedCaller**, **userRightsAllowAccessFromNetwork**, **userRightsBlockAccessFromNetwork**, **userRightsActAsPartOfTheOperatingSystem**, **userRightsLocalLogOn**, **userRightsBackupData**, **userRightsChangeSystemTime**, **userRightsCreateGlobalObjects**, **userRightsCreatePageFile**, **userRightsCreatePermanentSharedObjects**, **userRightsCreateSymbolicLinks**, **userRightsCreateToken**, **userRightsDebugPrograms**, **userRightsRemoteDesktopServicesLogOn**, **userRightsDelegation**, **userRightsGenerateSecurityAudits**, **userRightsImpersonateClient**, **userRightsIncreaseSchedulingPriority**, **userRightsLoadUnloadDrivers**, **userRightsLockMemory**, **userRightsManageAuditingAndSecurityLogs**, **userRightsManageVolumes**, **userRightsModifyFirmwareEnvironment**, **userRightsModifyObjectLabels**, **userRightsProfileSingleProcess**, **userRightsRemoteShutdown**, **userRightsRestoreData**, **userRightsTakeOwnership**, **userRightsRegisterProcessAsService**, **localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedClients**, **localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedServers**, **lanManagerAuthenticationLevel** y **lanManagerWorkstationEnableInsecureGuestLogons** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **passwordMinimumAgeInDays**, **tenantLockdownRequireNetworkDuringOutOfBoxExperience** y **dataProtectionBlockDirectMemoryAccess** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **extendedKeyUsages** a la entidad [windows10PkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-windows10pkcscertificateprofile?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **enableDnsRegistration** y **dnsSuffixes** a la entidad [windows10VpnConfiguration](/graph/api/resources/intune-deviceconfig-windows10vpnconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **customSubjectAlternativeNames** a la entidad [windows81CertificateProfileBase](/graph/api/resources/intune-deviceconfig-windows81certificateprofilebase?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **extractHardwareHash** y **deviceNameTemplate** a la entidad [windowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-windowsautopilotdeploymentprofile?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **addressableUserName** y **userPrincipalName** a la entidad [windowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-windowsautopilotdeviceidentity?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **threatState** a la entidad [windowsDeviceMalwareState](/graph/api/resources/intune-devices-windowsdevicemalwarestate?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades **qualityUpdatesPauseStartDateTime**, **featureUpdatesPauseStartDateTime**, **featureUpdatesRollbackWindowInDays**, **qualityUpdatesWillBeRolledBack**, **featureUpdatesWillBeRolledBack**, **qualityUpdatesRollbackStartDateTime** y **featureUpdatesRollbackStartDateTime** a la entidad [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **trustedServerCertificateNames** a la entidad [windowsWifiEnterpriseEAPConfiguration](/graph/api/resources/intune-deviceconfig-windowswifienterpriseeapconfiguration?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades de navegación **defaultIosEnrollmentProfile**, **defaultMacOsEnrollmentProfile**, **enrollmentProfiles** y **importedAppleDeviceIdentities** a la entidad [depOnboardingSetting](/graph/api/resources/intune-enrollment-deponboardingsetting?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad de navegación **roleScopeTags** a la entidad [deviceAndAppManagementRoleAssignment](/graph/api/resources/intune-rbac-deviceandappmanagementroleassignment?view=graph-rest-beta)|
|Adición|beta|Se agregaron las propiedades de navegación **advancedThreatProtectionOnboardingStateSummary**, **roleScopeTags** y **importedWindowsAutopilotDeviceIdentityUploads** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **supportedDeviceTypes** al tipo complejo [mobileAppIntentAndStateDetail](/graph/api/resources/intune-troubleshooting-mobileappintentandstatedetail?view=graph-rest-beta)|
|Adición|beta|Se agregó la propiedad **hideEscapeLink** al tipo complejo [outOfBoxExperienceSettings](/graph/api/resources/intune-enrollment-outofboxexperiencesettings?view=graph-rest-beta)|
|Adición|beta|Se agregaron los miembros **zscalerPrivateAccess**, **f5Access2018**, **citrixSso** y **paloAltoGlobalProtectV2** al tipo de enumeración [appleVpnConnectionType](/graph/api/resources/intune-deviceconfig-applevpnconnectiontype?view=graph-rest-beta)|
|Adición|beta|Se agregó el miembro **userAbandonment** al tipo de enumeración [deviceEnrollmentFailureReason](/graph/api/resources/intune-troubleshooting-deviceenrollmentfailurereason?view=graph-rest-beta)|
|Adición|beta|Se agregó el miembro **blocked** al tipo de enumeración [enrollmentState](/graph/api/resources/intune-enrollment-enrollmentstate?view=graph-rest-beta)|
|Adición|beta|Se agregó el miembro **microsoft365ManagedMdm** al tipo de enumeración [managementAgentType](/graph/api/resources/intune-devices-managementagenttype?view=graph-rest-beta)|
|Adición|beta|Se agregó el miembro **domainNameService** al tipo de enumeración [subjectAlternativeNameType](/graph/api/resources/intune-deviceconfig-subjectalternativenametype?view=graph-rest-beta)|
|Adición|beta|Se agregaron los miembros **wpa2Personal** y **wpa2Enterprise** al tipo de enumeración [wiFiSecurityType](/graph/api/resources/intune-deviceconfig-wifisecuritytype?view=graph-rest-beta)|
|Adición|beta|Se agregaron los miembros **enterpriseUnwantedSoftware**, **ransom** y **hipsRule** al tipo de enumeración [windowsMalwareCategory](/graph/api/resources/intune-devices-windowsmalwarecategory?view=graph-rest-beta)|

### <a name="outlook-calendar"></a>Calendario de Outlook

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | Beta | Se agregaron la acción [getSchedule](/graph/api/calendar-getschedule?view=graph-rest-beta) y los tipos complejos [freeBusyError](/graph/api/resources/freebusyerror?view=graph-rest-beta), [scheduleInformation](/graph/api/resources/scheduleinformation?view=graph-rest-beta) y [scheduleItem](/graph/api/resources/scheduleitem?view=graph-rest-beta) para admitir los tipos complejos [obtener la información de disponibilidad de los usuarios, listas de distribución y recursos para un determinado período de tiempo](outlook-get-free-busy-schedule.md). |

### <a name="outlook-mail"></a>Correo de Outlook

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0        | Se agregó la compatibilidad con la acción [getMailTips](/graph/api/user-getmailtips?view=graph-rest-1.0) para obtener las sugerencias de correo electrónico para destinatarios específicos. Se agregaron los siguientes recursos: [automaticRepliesMailTips](/graph/api/resources/automaticrepliesmailtips?view=graph-rest-1.0), [mailTips](/graph/api/resources/mailtips?view=graph-rest-1.0) y [mailTipsError](/graph/api/resources/mailtipserror?view=graph-rest-1.0). |

### <a name="reports-apis"></a>API de informes
| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Adición    | v1.0    | Se agregó la propiedad **Activated On Shared Computer** a [getoffice365activationsuserdetail](/graph/api/reportroot-getoffice365activationsuserdetail?view=graph-rest-1.0). |
| Adición    | v1.0    | Se agregó la propiedad **Shared Computer Activation** a [getoffice365activationsusercounts](/graph/api/reportroot-getoffice365activationsusercounts?view=graph-rest-1.0). |

### <a name="security-apis"></a>API de seguridad

| **Tipo de cambio** | **Versión** | **Descripción**              |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | beta       | Se agregaron las propiedades **activityGroupName**, **cloudAppStates**, **confidence** y **registryKeyStates** a [alert](/graph/api/resources/alert?view=graph-rest-beta ). |
|Eliminación|beta| Se quitaron las propiedades **activityGroupStates**, **applicationStates**, **malwareWasRunning**, **riskScore** y **type** de [alert](/graph/api/resources/alert?view=graph-rest-beta ). |
|Cambio|beta| Se cambió el tipo **comments** de una `String` a una `String collection` y se cambió el tipo **severity** de una `String` a una enumeración [alertSeverity](/graph/api/resources/alertseverityenumtype?view=graph-rest-beta) en [alert](/graph/api/resources/alert?view=graph-rest-beta). |
| Adición        | beta       | Se agregaron los siguientes tipos de recursos: <br/> [cloudAppSecurityState](/graph/api/resources/cloudappsecuritystate?view=graph-rest-beta) <br/> [fileHash](/graph/api/resources/filehash?view=graph-rest-beta) <br/> [registryKeyState](/graph/api/resources/registrykeystate?view=graph-rest-beta) |
|Eliminación|beta| Se quitaron los siguientes tipos de recursos: <br/> **activityGroupState**  <br/> **applicationSecurityState** |
| Adición        | beta       | Se agregaron las siguientes enumeraciones: <br/> [alertSeverity](/graph/api/resources/alertseverityenumtype?view=graph-rest-beta) <br/> [connectionDirection](/graph/api/resources/connectiondirectionenumtype?view=graph-rest-beta) <br/> [connectionStatus](/graph/api/resources/connectionstatusenumtype?view=graph-rest-beta) <br/> [emailRole](/graph/api/resources/emailroleenumtype?view=graph-rest-beta) <br/> [fileHashType](/graph/api/resources/filehashtypeenumtype?view=graph-rest-beta) <br/> [registryHive](/graph/api/resources/registryhiveenumtype?view=graph-rest-beta)  <br/> [registryOperation](/graph/api/resources/registryoperationenumtype?view=graph-rest-beta) <br/> [registryValueType](/graph/api/resources/registryvaluetypeenumtype?view=graph-rest-beta)|
|Eliminación|beta| Se han quitado los siguientes tipos de enumeración: <br/> **alertType** <br/> **applicationPermissionsRequired** |
| Adición        | beta       | Se agregó la propiedad **fileHash** a [fileSecurityState](/graph/api/resources/filesecuritystate?view=graph-rest-beta ).|
|Eliminación|beta| Se quitaron las propiedades **authenticodeHash256** y **sha256** de [fileSecurityState](/graph/api/resources/filesecuritystate?view=graph-rest-beta). |
| Adición | beta | Se agregó la propiedad **os** a [hostSecurityState](/graph/api/resources/hostsecuritystate?view=graph-rest-beta).|
| Adición | beta | Se agregaron las propiedades **category**, **family** y **wasRunning** a [malwareState](/graph/api/resources/malwarestate?view=graph-rest-beta).|
|Eliminación|beta| Se quitó la propiedad **aliases** de [malwareState](/graph/api/resources/malwarestate?view=graph-rest-beta). |
|Cambio|beta| Se movió la propiedad **malwareWasRunning** de [alert](/graph/api/resources/alert?view=graph-rest-beta ) a [malwareState](/graph/api/resources/malwarestate?view=graph-rest-beta) y se cambió su nombre a **wasRunning**. |
| Adición        | beta       | Se agregaron las propiedades **applicationName**, **destinationDomain**, **direction**, **domainRegisteredDateTime**, **localDnsName**, **natDestinationAddress**, **natDestinationPort**, **natSourceAddress**, **natSourcePort**, **riskScore**, **status** y **urlParameters** a [networkConnection](/graph/api/resources/networkconnection?view=graph-rest-beta ).|
|Cambio|beta| Se cambió la propiedad **uri** a **destinationUrl** en [networkConnection](/graph/api/resources/networkconnection?view=graph-rest-beta ). |
| Adición        | beta       | Se agregó la propiedad **fileHash** a [process](/graph/api/resources/process?view=graph-rest-beta ).|
|Eliminación|beta| Se quitaron las propiedades **authenticodeHash256** y **sha256** de [process](/graph/api/resources/process?view=graph-rest-beta ). |
| Adición        | beta       | Se agregaron las propiedades **aadUserId**, **emailRole**, **isVpn** y **logonIp** a [userSecurityState](/graph/api/resources/usersecuritystate?view=graph-rest-beta).|
|Cambio|beta| Se cambió la propiedad **logonIpAddress** a **logonIp** en [userSecurityState](/graph/api/resources/usersecuritystate?view=graph-rest-beta). |
| Adición        | beta       | Se agregó la propiedad **wasRunning** a [vulnerabilityState](/graph/api/resources/vulnerabilitystate?view=graph-rest-beta).|
|Eliminación|beta| Se quitó la propiedad **name** de [vulnerabilityState](/graph/api/resources/vulnerabilitystate?view=graph-rest-beta). |

## <a name="july-2018"></a>Julio de 2018

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Cambio|beta|Se actualizó el recurso [chatmessage](/graph/api/resources/chatmessage?view=graph-rest-beta)|
|Adición|beta|Se actualizó el tipo de recurso [Datos adjuntos de chat](/graph/api/resources/chatattachment?view=graph-rest-beta)|
|Adición|beta|Se actualizó el tipo de recurso [Mención de chat](/graph/api/resources/chatattachment?view=graph-rest-beta)|
|Adición|beta|Se actualizó el tipo de recurso [Reacción de chat](/graph/api/resources/chatattachment?view=graph-rest-beta)|
|Adición|beta|Se agregó la [API Obtener todos los mensajes del canal](/graph/api/channel-list-messages?view=graph-rest-beta) |
|Adición|beta|Se agregó la [API Obtener mensaje del canal](/graph/api/channel-get-message?view=graph-rest-beta) |
|Adición|beta|Se agregó la [API Obtener todas las respuestas de mensaje](/graph/api/channel-list-messagereplies?view=graph-rest-beta) |
|Adición|beta|Se agregó la [API Obtener respuesta a un mensaje](/graph/api/channel-get-messagereply?view=graph-rest-beta) |

### <a name="synchronization-apis"></a>API de sincronización

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | Beta | Se agregó la propiedad **progress** a [sychronizationStatus](/graph/api/resources/synchronization-synchronizationstatus?view=graph-rest-beta) para permitir a los clientes supervisar el progreso de un trabajo de sincronización.|

### <a name="application-and-serviceprincipal-api-changes"></a>Cambios en la API servicePrincipal y en aplicaciones

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Las API [application](/graph/api/resources/application?view=graph-rest-beta) y [servicePrincipal](/graph/api/resources/serviceprincipal?view=graph-rest-beta) se actualizarán en la versión preliminar (beta). El primer conjunto de cambios se aplicará el 16 de julio de 2018. Entre los cambios se incluyen la reestructuración y el cambio de nombre de propiedades. La mayoría de las propiedades existentes no estarán disponibles hasta que se completen los cambios. Se agregarán nuevas propiedades. Los cambios se publicarán en versión preliminar (beta) antes de publicarse la versión 1.0. |

### <a name="microsoft-teams-apis"></a>API de Microsoft Teams
| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Adición|beta|Se agregó la compatibilidad con permisos de aplicación a [/users/{id}/joinedTeams](/graph/api/user-list-joinedteams?view=graph-rest-beta) |
|Adición|beta|Se agregó la [API Obtener todos los mensajes del canal](/graph/api/channel-list-messages?view=graph-rest-beta) |
|Adición|beta|Se agregó la [API Obtener mensaje del canal](/graph/api/channel-get-message?view=graph-rest-beta) |
|Adición|beta|Se agregó la [API Obtener todas las respuestas de mensaje](/graph/api/channel-list-messagereplies?view=graph-rest-beta) |
|Adición|beta|Se agregó la [API Obtener respuesta a un mensaje](/graph/api/channel-get-messagereply?view=graph-rest-beta) |
|Adición|beta|Se actualizó el tipo de recurso [Datos adjuntos de chat](/graph/api/resources/chatattachment?view=graph-rest-beta)|
|Adición|beta|Se actualizó el tipo de recurso [Mención de chat](/graph/api/resources/chatattachment?view=graph-rest-beta)|
|Adición|beta|Se actualizó el tipo de recurso [Reacción de chat](/graph/api/resources/chatattachment?view=graph-rest-beta)|
|Cambio|beta|Se actualizó el recurso [chatmessage](/graph/api/resources/chatmessage?view=graph-rest-beta))|
|Eliminación|beta|Quitar ELIMINAR /grupos/{id}/grupo/canales/{id}, use ELIMINAR /equipos/{id}/canales/{id} en su lugar. |
|Eliminación|beta|Quitar OBTENER /grupos/{id}/grupo/canales/{id}, use OBTENER /equipos/{id}/canales/{id} en su lugar. |
|Eliminación|beta|Quitar REVISIÓN /grupos/{id}/grupo/canales/{id}, use REVISIÓN /equipos/{id}/canales/{id} en su lugar. |
|Eliminación|beta|Quitar PUBLICAR /grupos/{id}/grupo/canales/{id}/hilos de chat, use PUBLICAR /equipos/{id}/canales/{id}/hilos de chat en su lugar. |
|Eliminación|beta|Quitar OBTENER /grupos/{id}/grupo/canales, use OBTENER /equipos/{id}/canales en su lugar. |
|Eliminación|beta|Quitar ELIMINAR /grupos/{id}/canales/{id}, use ELIMINAR /equipos/{id}/canales/{id} en su lugar. |
|Eliminación|beta|Quitar OBTENER /grupos/{id}/canales/{id}, use OBTENER /equipos/{id}/canales/{id} en su lugar. |
|Eliminación|beta|Quitar REVISIÓN /grupos/{id}/canales/{id}, use REVISIÓN /equipos/{id}/canales/{id} en su lugar. |
|Eliminación|beta|Quitar PUBLICAR /grupos/{id}/canales/{id}/hilos de chat, use PUBLICAR /equipos/{id}/canales/{id}/hilos de chat en su lugar. |
|Eliminación|beta|Quitar OBTENER /grupos/{id}/canales, use OBTENER /equipos/{id}/canales en su lugar. |
|Eliminación|beta|Quitar PUBLICAR /grupos/{id}/equipo/canales, use PUBLICAR /equipos/{id}/canales en su lugar. |
|Eliminación|beta|Quitar OBTENER /grupos/{id}/equipo, use OBTENER /equipos/{id} en su lugar. |
|Eliminación|beta|Se quitó PATCH /groups/{id}/team, use PATCH /teams/{id} en su lugar. |
|Adición|beta|Agrega la API para [lista de todos los equipos de la organización](teams-list-all-teams.md). |

### <a name="outlook-contacts"></a>Contactos de Outlook
| **Tipo de cambio** | **Versión**   | **Descripción**                          |
|:--------------- |:------------- |:---------------------------------------- |
|Adición |Beta | Agregar el tipo complejo [typedEmailAddress](/graph/api/resources/typedemailaddress?view=graph-rest-beta). |
|Cambio | Beta | Cambiar el tipo de la propiedad **emailAddresses** de [contact](/graph/api/resources/contact?view=graph-rest-beta) para que sea una colección de instancias **typedEmailAddress**.|

### <a name="webhooks"></a>Webhooks
| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Cambio importante | Beta y v1.0 | Para los [webhooks](/graph/api/resources/webhooks?view=graph-rest-1.0), [se redujo la duración máxima de la fecha de expiración de la suscripción](/graph/api/resources/subscription?view=graph-rest-1.0#maximum-length-of-subscription-per-resource-type) para elementos de la raíz de la unidad a 3 días. |


## <a name="june-2018"></a>Junio de 2018

### <a name="identity-and-access-apis"></a>API de identidad y acceso

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | beta | Se agregó la característica [acceder a revisiones](/graph/api/resources/accessreviews-root?view=graph-rest-beta) en [Azure AD](/graph/api/resources/azure-ad-overview?view=graph-rest-beta). |

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | Todo | Nuevos permisos de aplicación, _Application.ReadWrite.All_ y _Application.ReadWrite.OwnedBy_, que permiten que una aplicación cliente cree, lea, actualice y elimine aplicaciones y entidades de seguridad tal y como se describe en el [tema sobre permisos](permissions-reference.md#application-resource-permissions). |
| Adición | v1.0 | Se agregaron las propiedades **ageGroup**, **legalAgeGroupClassification** y **ConsentRequiredForMinor** al recurso [user](/graph/api/resources/user?view=graph-rest-1.0)

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Se ha agregado la propiedad **connectorServerName** a la entidad [deviceManagementExchangeConnector](/graph/api/resources/intune-onboarding-devicemanagementexchangeconnector?view=graph-rest-1.0).|
|Adición|v1.0|Se han agregado las propiedades **firewallEnabled**, **firewallBlockAllIncoming** y **firewallEnableStealthMode** a la entidad [macOSCompliancePolicy](/graph/api/resources/intune-deviceconfig-macoscompliancepolicy?view=graph-rest-1.0).|
|Adición|v1.0|Se ha agregado el miembro **unknown** al tipo de enumeración [iosUpdatesInstallStatus](/graph/api/resources/intune-deviceconfig-iosupdatesinstallstatus?view=graph-rest-1.0).|
|Adición|beta|Nuevas entidades agregadas:<br/>[androidDeviceOwnerWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androiddeviceownerwificonfiguration?view=graph-rest-beta)<br/>[iosVppAppAssignedDeviceLicense](/graph/api/resources/intune-apps-iosvppappassigneddevicelicense?view=graph-rest-beta)<br/>[iosVppAppAssignedLicense](/graph/api/resources/intune-apps-iosvppappassignedlicense?view=graph-rest-beta)<br/>[iosVppAppAssignedUserLicense](/graph/api/resources/intune-apps-iosvppappassigneduserlicense?view=graph-rest-beta)<br/>[managedDeviceMobileAppConfigurationState](/graph/api/resources/intune-deviceconfig-manageddevicemobileappconfigurationstate?view=graph-rest-beta)<br/>[userPFXCertificate](/graph/api/resources/intune-raimportcerts-userpfxcertificate?view=graph-rest-beta)<br/>[vppTokenLicenseSummary](/graph/api/resources/intune-onboarding-vpptokenlicensesummary?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos complejos agregados:<br/>[iosVppAppRevokeLicensesActionResult](/graph/api/resources/intune-apps-iosvppapprevokelicensesactionresult?view=graph-rest-beta)<br/>|
|Adición|beta|Se han agregado nuevos tipos de enumeración:<br/>[androidDeviceOwnerSystemUpdateInstallType](/graph/api/resources/intune-deviceconfig-androiddeviceownersystemupdateinstalltype?view=graph-rest-beta)<br/>[androidDeviceOwnerWiFiSecurityType](/graph/api/resources/intune-deviceconfig-androiddeviceownerwifisecuritytype?view=graph-rest-beta)<br/>[userPfxIntendedPurpose](/graph/api/resources/intune-raimportcerts-userpfxintendedpurpose?view=graph-rest-beta)<br/>[userPfxPaddingScheme](/graph/api/resources/intune-raimportcerts-userpfxpaddingscheme?view=graph-rest-beta)<br/>|
|Adición|beta|Se ha agregado la acción [createGooglePlayWebToken](/graph/api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-creategoogleplaywebtoken?view=graph-rest-beta) en [androidManagedStoreAccountEnterpriseSettings](/graph/api/resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la acción [revokeAllLicenses](/graph/api/intune-apps-iosvppapp-revokealllicenses?view=graph-rest-beta) en [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la acción [revokeUserLicense](/graph/api/intune-apps-iosvppapp-revokeuserlicense?view=graph-rest-beta) en [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la acción [revokeDeviceLicense](/graph/api/intune-apps-iosvppapp-revokedevicelicense?view=graph-rest-beta) en [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la acción [sendCustomNotificationToCompanyPortal](/graph/api/intune-shared-devicemanagement-sendcustomnotificationtocompanyportal?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la función **getLicensesForApp** en la colección [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta). |
|Eliminación|beta|Se han quitado los siguientes tipos de enumeración:<br/>**windowsUpdateInsiderBuildControl**<br/>|
|Adición|beta|Se han agregado las propiedades **systemUpdateWindowStartMinutesAfterMidnight**, **systemUpdateWindowEndMinutesAfterMidnight** y **systemUpdateInstallType** a la entidad [androidDeviceOwnerGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration?view=graph-rest-beta).|
|Cambio|beta|Se cambió el tipo de las propiedades siguientes en la entidad [androidDeviceOwnerGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration?view=graph-rest-beta):<br/>**passwordMinutesOfInactivityBeforeScreenTimeout** de Int64 a Int32<br/>|
|Adición|beta|Se ha agregado la propiedad **customKeyValueData** a la entidad [androidForWorkVpnConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkvpnconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **customKeyValueData** a la entidad [androidVpnConfiguration](/graph/api/resources/intune-deviceconfig-androidvpnconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **customKeyValueData** a la entidad [androidWorkProfileVpnConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilevpnconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **customKeyValueData** a la entidad [appleVpnConfiguration](/graph/api/resources/intune-deviceconfig-applevpnconfiguration?view=graph-rest-beta)|
|Adición|beta|Se han agregado las propiedades **userId** y **userPrincipalName** a la entidad [deviceCompliancePolicyState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicystate?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **userId** y **userPrincipalName** a la entidad [deviceConfigurationState](/graph/api/resources/intune-deviceconfig-deviceconfigurationstate?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **connectorServerName** a la entidad [deviceManagementExchangeConnector](/graph/api/resources/intune-onboarding-devicemanagementexchangeconnector?view=graph-rest-beta).|
|Eliminación|beta|Se ha quitado la propiedad **settingXml** de la entidad [iosMobileAppConfiguration](/graph/api/resources/intune-apps-iosmobileappconfiguration?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **vppTokenId** y **revokeLicenseActionResults** a la entidad [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **firewallEnabled**, **firewallBlockAllIncoming** y **firewallEnableStealthMode** a la entidad [macOSCompliancePolicy](/graph/api/resources/intune-deviceconfig-macoscompliancepolicy?view=graph-rest-beta).|
|Eliminación|beta|Se ha quitado la propiedad **remoteAssistanceSessionErrorString** de la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **antivirusRequired** y **antiSpywareRequired** a la entidad [windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **defenderOfficeAppsOtherProcessInjection**, **defenderOfficeAppsExecutableContentCreationOrLaunch**, **defenderOfficeAppsLaunchChildProcess**, **defenderOfficeMacroCodeAllowWin32Imports**, **defenderScriptObfuscatedMacroCode**, **defenderScriptDownloadedPayloadExecution**, **defenderProcessCreation**, **defenderUntrustedUSBProcess**, **defenderUntrustedExecutable** y **defenderEmailContentExecution** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **searchDisableLocation**, **inkWorkspaceAccessState**, **defenderPotentiallyUnwantedAppActionSetting** y **defenderCloudExtendedTimeoutInSeconds** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **updatesMinimumAutoInstallClassification** a la entidad [windows81GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows81generalconfiguration?view=graph-rest-beta).|
|Eliminación|beta|Se ha quitado la propiedad **previewBuildSetting** de la entidad [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad de navegación **userPfxCertificates** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad de navegación **assignedLicenses** a la entidad [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad de navegación **managedDeviceMobileAppConfigurationStates** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **websiteList** al tipo complejo [iosWebContentFilterSpecificWebsitesAccess](/graph/api/resources/intune-deviceconfig-ioswebcontentfilterspecificwebsitesaccess?view=graph-rest-beta).|
|Adición|beta|Se ha agregado el miembro **androidWorkProfile** al tipo de enumeración [devicePlatformType](/graph/api/resources/intune-deviceconfig-deviceplatformtype?view=graph-rest-beta).|
|Adición|beta|Se ha agregado el miembro **notConfigured** al tipo de enumeración [editionUpgradeLicenseType](/graph/api/resources/intune-deviceconfig-editionupgradelicensetype?view=graph-rest-beta).|
|Adición|beta|Se ha agregado el miembro **unknown** al tipo de enumeración [iosUpdatesInstallStatus](/graph/api/resources/intune-deviceconfig-iosupdatesinstallstatus?view=graph-rest-beta).|
|Adición|beta|Se ha agregado el miembro **userRequestedInstall** al tipo de enumeración [mobileAppActionType](/graph/api/resources/intune-troubleshooting-mobileappactiontype?view=graph-rest-beta).|
|Adición|beta|Se ha agregado el miembro **notConfigured** al tipo de enumeración [windows10EditionType](/graph/api/resources/intune-deviceconfig-windows10editiontype?view=graph-rest-beta).

### <a name="microsoft-teams-apis"></a>API de Microsoft Teams
| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
|Adición         | Beta          | Se han agregado las API [archive](/graph/api/team-archive?view=graph-rest-beta) y [unarchive](/graph/api/team-unarchive?view=graph-rest-beta) de equipo.|
|Adición         | Beta          | Se ha agregado la operación [clone](/graph/api/team-clone?view=graph-rest-beta) de equipo. |
|Adición         | Beta          | Se han agregado las API para agregar y quitar [apps](/graph/api/resources/teamsapp?view=graph-rest-beta) en equipos. |
|Cambio|Beta|Se ha actualizado la ruta de acceso a la entidad [team](/graph/api/resources/team?view=graph-rest-beta).|
|Cambio|Beta|Se ha actualizado la ruta de acceso a la entidad [channel](/graph/api/resources/channel?view=graph-rest-beta).|


### <a name="privileged-identity-management-apis"></a>API de Privileged Identity Management

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición | beta | Se ha agregado la entidad [privilegedAccess](/graph/api/resources/privilegedaccess?view=graph-rest-beta).|
| Adición | beta | Se ha agregado la entidad [governanceResource](/graph/api/resources/governanceresource?view=graph-rest-beta), así como los métodos y las acciones siguientes: <br> [List](/graph/api/governanceresource-list?view=graph-rest-beta) <br> [Get](/graph/api/governanceresource-get?view=graph-rest-beta)<br>|
| Adición | beta | Se ha agregado la entidad [governanceSubject](/graph/api/resources/governancesubject?view=graph-rest-beta).|
| Adición | beta | Se ha agregado la entidad [governanceRoleDefinition](/graph/api/resources/governanceroledefinition?view=graph-rest-beta), así como los métodos y las acciones siguientes:<br> [List](/graph/api/governanceroledefinition-list?view=graph-rest-beta) <br> [Get](/graph/api/governanceroledefinition-get?view=graph-rest-beta) |
| Adición | beta | Se ha agregado la entidad [governanceRoleAssignment](/graph/api/resources/governanceroleassignment?view=graph-rest-beta), así como los métodos y las acciones siguientes:<br> [List](/graph/api/governanceroleassignment-list?view=graph-rest-beta) <br> [Get](/graph/api/governanceroleassignment-get?view=graph-rest-beta) <br> [Export](/graph/api/governanceroleassignment-export?view=graph-rest-beta) |
| Adición | beta | Se ha agregado la entidad [governanceRoleAssignmentRequest](/graph/api/resources/governanceroleassignmentrequest?view=graph-rest-beta), así como los métodos y las acciones siguientes:<br> [List](/graph/api/governanceroleassignmentrequest-list?view=graph-rest-beta) <br> [Get](/graph/api/governanceroleassignmentrequest-get?view=graph-rest-beta) <br> [Create](/graph/api/governanceroleassignmentrequest-post?view=graph-rest-beta) <br> [Cancel](/graph/api/governanceroleassignmentrequest-cancel?view=graph-rest-beta) <br> [Update](/graph/api/governanceroleassignmentrequest-update?view=graph-rest-beta) |
| Adición | beta | Se ha agregado la entidad [governanceRoleSetting](/graph/api/resources/governancerolesetting?view=graph-rest-beta), así como los métodos y las acciones siguientes:<br> [List](/graph/api/governancerolesetting-list?view=graph-rest-beta) <br> [Get](/graph/api/governancerolesetting-get?view=graph-rest-beta) <br> [Update](/graph/api/governancerolesetting-update?view=graph-rest-beta) |
| Adición | beta | Se han agregado los tipos complejos siguientes: <br> [governancePermission](/graph/api/resources/governancepermission?view=graph-rest-beta) <br> [governanceRoleAssignmentRequestStatus](/graph/api/resources/governanceroleassignmentrequeststatus?view=graph-rest-beta) <br> [governanceRuleSetting](/graph/api/resources/governancerulesetting?view=graph-rest-beta) <br> [governanceSchedule](/graph/api/resources/governanceschedule?view=graph-rest-beta)|

### <a name="security-apis"></a>API de seguridad

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | beta        | Se han agregado nuevos tipos de enumeración:<br/>[alertFeedback](/graph/api/resources/alertfeedbackenumtype?view=graph-rest-beta)<br/>[alertStatus](/graph/api/resources/alertstatusenumtype?view=graph-rest-beta)<br/>[alertType](/graph/api/resources/alerttypeenumtype?view=graph-rest-beta)<br/>[applicationPermissionsRequired](/graph/api/resources/applicationpermissionsrequiredenumtype?view=graph-rest-beta)<br/>[logonType](/graph/api/resources/logontypeenumtype?view=graph-rest-beta)<br/>[processIntegrityLevel](/graph/api/resources/processintegritylevelenumtype?view=graph-rest-beta)<br/>[securityNetworkProtocol](/graph/api/resources/securitynetworkprotocolenumtype?view=graph-rest-beta)<br/>[userAccountSecurityType](/graph/api/resources/useraccountsecuritytypeenumtype?view=graph-rest-beta)<br/>

## <a name="may-2018"></a>Mayo de 2018

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0        | Se ha agregado la acción [Mostrar lista de elementos eliminados que pertenecen a un usuario](/graph/api/directory-deleteditems-user-owned?view=graph-rest-1.0) al recurso [directorio (elementos eliminados)](/graph/api/resources/directory?view=graph-rest-1.0). |
| Adición | beta | Se agregó la función [getUserOwnedObjects](/graph/api/directory-deleteditems-user-owned?view=graph-rest-beta) al recurso [directory](/graph/api/resources/directory?view=graph-rest-beta) para mostrar una lista de los grupos eliminados que pertenecen a un usuario determinado. |

### <a name="education-api"></a>API para el ámbito educativo

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Cambio          | versión 1.0 y beta | El ámbito **Members.Read.Hidden** se requiere para leer o actualizar la colección **Members** de una entidad [educationClass](/graph/api/resources/educationclass?view=graph-rest-1.0) con tokens solo de aplicación. |
|Cambio           |Beta           |Se han actualizado los valores posibles del tipo **educationSubmissionStatus** en la propiedad del estado de [educationsubmission](/graph/api/resources/educationsubmission?view=graph-rest-beta).|
|Cambio           |Beta           |Se agregó el tipo complejo **educationAssignmentIndividualRecipient** a la propiedad assignTo de [educationAssignment](/graph/api/resources/educationassignment?view=graph-rest-beta).|
|Cambio           |Beta           |Se agregaron las propiedades **unsubmittedBy**, **unsubmittedDate**, **returnedBy** y **returnedDate** de [educationSubmission](/graph/api/resources/educationsubmission?view=graph-rest-beta).|
|Adición         |Beta           |Se agregaron las acciones [return](/graph/api/educationsubmission-return?view=graph-rest-beta) y [unsubmit](/graph/api/educationsubmission-unsubmit?view=graph-rest-beta) a [educationSubmission](/graph/api/resources/educationsubmission?view=graph-rest-beta).|
|Cambio           |Beta           |Se quitaron las acciones release y recall de [educationSubmission](/graph/api/resources/educationsubmission?view=graph-rest-beta).|

### <a name="groups"></a>Grupos

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0 y beta | Se agregó la propiedad **importance** a la entidad [post](/graph/api/resources/post?view=graph-rest-1.0). |

### <a name="microsoft-bookings-api"></a>API de Microsoft Bookings

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | Beta          | Se agregó la entidad [bookingBusiness](/graph/api/resources/bookingbusiness?view=graph-rest-beta) y las siguientes acciones y métodos CRUD: <br> [Lista](/graph/api/bookingbusiness-list?view=graph-rest-beta) <br> [Crear](/graph/api/bookingbusiness-post-bookingbusinesses?view=graph-rest-beta) <br> [Obtener](/graph/api/bookingbusiness-get?view=graph-rest-beta) <br> [Actualizar](/graph/api/bookingbusiness-update?view=graph-rest-beta) <br> [Eliminar](/graph/api/bookingbusiness-delete?view=graph-rest-beta) <br> [Publicar](/graph/api/bookingbusiness-publish?view=graph-rest-beta) <br> [Cancelar la publicación](/graph/api/bookingbusiness-unpublish?view=graph-rest-beta). <br> Obtenga más información sobre la integración con la [API de Microsoft Bookings](booking-concept-overview.md). |
| Adición        | Beta          | Se agregó la entidad [bookingAppointment](/graph/api/resources/bookingappointment?view=graph-rest-beta) y las siguientes acciones y métodos CRUD: <br> [Lista](/graph/api/bookingbusiness-list-appointments?view=graph-rest-beta) <br> [Crear](/graph/api/bookingbusiness-post-appointments?view=graph-rest-beta) <br> [Obtener](/graph/api/bookingappointment-get?view=graph-rest-beta) <br> [Actualizar](/graph/api/bookingappointment-update?view=graph-rest-beta) <br> [Eliminar](/graph/api/bookingappointment-delete?view=graph-rest-beta) <br> [Cancelar](/graph/api/bookingappointment-cancel?view=graph-rest-beta). |
| Adición        | Beta          | Se agregó la entidad [bookingCurrency](/graph/api/resources/bookingcurrency?view=graph-rest-beta) y los métodos siguientes: <br> [Lista](/graph/api/bookingcurrency-list?view=graph-rest-beta) <br> [Obtener](/graph/api/bookingcurrency-get?view=graph-rest-beta). |
| Adición        | Beta          | Se agregó la entidad [bookingCustomer](/graph/api/resources/bookingcustomer?view=graph-rest-beta) y los siguientes métodos CRUD: <br> [Lista](/graph/api/bookingbusiness-list-customers?view=graph-rest-beta) <br> [Crear](/graph/api/bookingbusiness-post-customers?view=graph-rest-beta) <br> [Obtener](/graph/api/bookingcustomer-get?view=graph-rest-beta) <br> [Actualizar](/graph/api/bookingcustomer-update?view=graph-rest-beta) <br> [Eliminar](/graph/api/bookingcustomer-delete?view=graph-rest-beta).|
| Adición        | Beta          | Se agregó la entidad [bookingService](/graph/api/resources/bookingservice?view=graph-rest-beta) y los siguientes métodos CRUD: <br> [Lista](/graph/api/bookingbusiness-list-services?view=graph-rest-beta) <br> [Crear](/graph/api/bookingbusiness-post-services?view=graph-rest-beta) <br> [Obtener](/graph/api/bookingservice-get?view=graph-rest-beta) <br> [Actualizar](/graph/api/bookingservice-update?view=graph-rest-beta) <br> [Eliminar](/graph/api/bookingservice-delete?view=graph-rest-beta).|
| Adición        | Beta          | Se agregó la entidad [bookingStaffMember](/graph/api/resources/bookingstaffmember?view=graph-rest-beta) y los siguientes métodos CRUD: <br> [Lista](/graph/api/bookingbusiness-list-staffmembers?view=graph-rest-beta) <br> [Crear](/graph/api/bookingbusiness-post-staffmembers?view=graph-rest-beta) <br> [Obtener](/graph/api/bookingstaffmember-get?view=graph-rest-beta) <br> [Actualizar](/graph/api/bookingstaffmember-update?view=graph-rest-beta) <br> [Eliminar](/graph/api/bookingstaffmember-delete?view=graph-rest-beta).|
| Adición        | Beta          | Se agregaron los tipos complejos siguientes: <br> [bookingNamedEntity](/graph/api/resources/bookingnamedentity?view=graph-rest-beta) <br> [bookingPerson](/graph/api/resources/bookingperson?view=graph-rest-beta) <br> [bookingReminder](/graph/api/resources/bookingreminder?view=graph-rest-beta) <br> [bookingWorkHours](/graph/api/resources/bookingworkhours?view=graph-rest-beta) <br> [bookingWorkTimeSlot](/graph/api/resources/bookingworktimeslot?view=graph-rest-beta).|

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|beta|Nuevas entidades agregadas:<br/>[androidWorkProfileCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidworkprofilecompliancepolicy?view=graph-rest-beta)<br/>[easEmailProfileConfigurationBase](/graph/api/resources/intune-deviceconfig-easemailprofileconfigurationbase?view=graph-rest-beta)<br/>[mobileAppIntentAndState](/graph/api/resources/intune-troubleshooting-mobileappintentandstate?view=graph-rest-beta)<br/>[mobileAppTroubleshootingEvent](/graph/api/resources/intune-troubleshooting-mobileapptroubleshootingevent?view=graph-rest-beta)<br/>[unsupportedDeviceConfiguration](/graph/api/resources/intune-deviceconfig-unsupporteddeviceconfiguration?view=graph-rest-beta)<br/>[windowsKioskConfiguration](/graph/api/resources/intune-deviceconfig-windowskioskconfiguration?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos complejos agregados:<br/>[managedDeviceCleanupSettings](/graph/api/resources/intune-devices-manageddevicecleanupsettings?view=graph-rest-beta)<br/>[mobileAppIntentAndStateDetail](/graph/api/resources/intune-troubleshooting-mobileappintentandstatedetail?view=graph-rest-beta)<br/>[mobileAppTroubleshootingAppPolicyCreationHistory](/graph/api/resources/intune-troubleshooting-mobileapptroubleshootingapppolicycreationhistory?view=graph-rest-beta)<br/>[mobileAppTroubleshootingAppStateHistory](/graph/api/resources/intune-troubleshooting-mobileapptroubleshootingappstatehistory?view=graph-rest-beta)<br/>[mobileAppTroubleshootingAppTargetHistory](/graph/api/resources/intune-troubleshooting-mobileapptroubleshootingapptargethistory?view=graph-rest-beta)<br/>[mobileAppTroubleshootingAppUpdateHistory](/graph/api/resources/intune-troubleshooting-mobileapptroubleshootingappupdatehistory?view=graph-rest-beta)<br/>[mobileAppTroubleshootingDeviceCheckinHistory](/graph/api/resources/intune-troubleshooting-mobileapptroubleshootingdevicecheckinhistory?view=graph-rest-beta)<br/>[mobileAppTroubleshootingHistoryItem](/graph/api/resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem?view=graph-rest-beta)<br/>[unsupportedDeviceConfigurationDetail](/graph/api/resources/intune-deviceconfig-unsupporteddeviceconfigurationdetail?view=graph-rest-beta)<br/>**windowsAutoPilotEnrollmentSettings**<br/>[windowsKioskActiveDirectoryGroup](/graph/api/resources/intune-deviceconfig-windowskioskactivedirectorygroup?view=graph-rest-beta)<br/>[windowsKioskAppBase](/graph/api/resources/intune-deviceconfig-windowskioskappbase?view=graph-rest-beta)<br/>[windowsKioskAppConfiguration](/graph/api/resources/intune-deviceconfig-windowskioskappconfiguration?view=graph-rest-beta)<br/>[windowsKioskAutologon](/graph/api/resources/intune-deviceconfig-windowskioskautologon?view=graph-rest-beta)<br/>[windowsKioskAzureADGroup](/graph/api/resources/intune-deviceconfig-windowskioskazureadgroup?view=graph-rest-beta)<br/>[windowsKioskAzureADUser](/graph/api/resources/intune-deviceconfig-windowskioskazureaduser?view=graph-rest-beta)<br/>[windowsKioskDesktopApp](/graph/api/resources/intune-deviceconfig-windowskioskdesktopapp?view=graph-rest-beta)<br/>[windowsKioskLocalGroup](/graph/api/resources/intune-deviceconfig-windowskiosklocalgroup?view=graph-rest-beta)<br/>[windowsKioskLocalUser](/graph/api/resources/intune-deviceconfig-windowskiosklocaluser?view=graph-rest-beta)<br/>[windowsKioskMultipleApps](/graph/api/resources/intune-deviceconfig-windowskioskmultipleapps?view=graph-rest-beta)<br/>[windowsKioskProfile](/graph/api/resources/intune-deviceconfig-windowskioskprofile?view=graph-rest-beta)<br/>[windowsKioskSingleUWPApp](/graph/api/resources/intune-deviceconfig-windowskiosksingleuwpapp?view=graph-rest-beta)<br/>[windowsKioskUser](/graph/api/resources/intune-deviceconfig-windowskioskuser?view=graph-rest-beta)<br/>[windowsKioskUWPApp](/graph/api/resources/intune-deviceconfig-windowskioskuwpapp?view=graph-rest-beta)<br/>[windowsKioskVisitor](/graph/api/resources/intune-deviceconfig-windowskioskvisitor?view=graph-rest-beta)<br/>|
|Adición|beta|Nuevos tipos de enumeración agregados:<br/>[defenderScheduleScanDay](/graph/api/resources/intune-deviceconfig-defenderschedulescanday?view=graph-rest-beta)<br/>[defenderSubmitSamplesConsentType](/graph/api/resources/intune-deviceconfig-defendersubmitsamplesconsenttype?view=graph-rest-beta)<br/>[domainNameSource](/graph/api/resources/intune-deviceconfig-domainnamesource?view=graph-rest-beta)<br/>[localSecurityOptionsSmartCardRemovalBehaviorType](/graph/api/resources/intune-deviceconfig-localsecurityoptionssmartcardremovalbehaviortype?view=graph-rest-beta)<br/>[mobileAppActionType](/graph/api/resources/intune-troubleshooting-mobileappactiontype?view=graph-rest-beta)<br/>[mobileAppIntent](/graph/api/resources/intune-troubleshooting-mobileappintent?view=graph-rest-beta)<br/>[roleAssignmentScopeType](/graph/api/resources/intune-rbac-roleassignmentscopetype?view=graph-rest-beta)<br/>[usernameSource](/graph/api/resources/intune-deviceconfig-usernamesource?view=graph-rest-beta)<br/>[windowsDeviceUsageType](/graph/api/resources/intune-enrollment-windowsdeviceusagetype?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la acción [setDeviceName](/graph/api/intune-devices-manageddevice-setdevicename?view=graph-rest-beta)<br/>a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
|Eliminación|beta|Se quitaron las entidades siguientes:<br/>**depEnrollmentProfile**<br/>**enrollmentProfile**<br/>**importedAppleDeviceIdentity**<br/>**importedAppleDeviceIdentityResult**<br/>|
|Eliminación|beta|Se quitaron los tipos complejos siguientes:<br/>**managementCertificateWithThumbprint**<br/>|
|Eliminación|beta|Se quitaron los siguientes tipos de enumeración:<br/>**depTokenType**<br/>**discoverySource**<br/>**iTunesPairingMode**<br/>|
|Eliminación|beta|Se quitó la acción importAppleDeviceIdentityList de la colección [importedAppleDeviceIdentity](/graph/api/resources/intune-corpenrollment-importedappledeviceidentity?view=graph-rest-beta). |
|Eliminación|beta|Se quitó la acción [updateDeviceProfileAssignment](/graph/api/intune-corpenrollment-enrollmentprofile-updatedeviceprofileassignment?view=graph-rest-beta) de [enrollmentProfile](/graph/api/resources/intune-corpenrollment-enrollmentprofile?view=graph-rest-beta). |
|Eliminación|beta|Se agregó la acción setDefaultProfile a [enrollmentProfile](/graph/api/resources/intune-corpenrollment-enrollmentprofile?view=graph-rest-beta). |
|Eliminación|beta|Se agregó la acción shareForSchoolDataSyncService a [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta). |
|Eliminación|beta|Se agregó la acción unshareForSchoolDataSyncService a [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta). |
|Eliminación|beta|Se eliminó la función exportMobileConfig](/graph/api/intune_corpenrollment_enrollmentprofile_exportmobileconfig?view=graph-rest-beta) en [enrollmentProfile](/graph/api/resources/intune-corpenrollment-enrollmentprofile?view=graph-rest-beta) |
|Adición|beta|Se agregaron las propiedades **userDomainNameSource** y **customDomainName** a la entidad [androidEasEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-androideasemailprofileconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **workProfileBlockCamera** y **workProfileBlockCrossProfileContactsSearch** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **workProfileBlockCamera** y **workProfileBlockCrossProfileContactsSearch** a la entidad [androidWorkProfileGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **thirdPartyKeyboardsBlocked** y **filterOpenInToOnlyManagedApps** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **conflictCount** a la entidad [deviceComplianceUserOverview](/graph/api/resources/intune-deviceconfig-devicecomplianceuseroverview?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **conflictCount** a la entidad [deviceConfigurationUserOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationuseroverview?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **managedDeviceCleanupSettings** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta).|
|Eliminación|beta|Se quitó la propiedad **usernameSource** de la entidad [iosEasEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-ioseasemailprofileconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **thirdPartyKeyboardsBlocked** y **filterOpenInToOnlyManagedApps** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **ignoreVersionDetection** a la entidad [macOSLobApp](/graph/api/resources/intune-apps-macoslobapp?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **pinRequiredOnLaunchInsteadOfBiometric** y **pinRequiredInsteadOfBiometricTimeout** a la entidad [managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **autopilotEnrolled**, **requireUserEnrollmentApproval**, **iccid** y **udid** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Eliminación|beta|Se quitó la propiedad **isAutopilotEnrolled** de la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **notApplicablePlatformCount** y **conflictCount** a la entidad [managedDeviceMobileAppConfigurationDeviceSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicesummary?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **conflictCount** a la entidad [managedDeviceMobileAppConfigurationUserSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationusersummary?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **scopeType** a la entidad [roleAssignment](/graph/api/resources/intune-rbac-roleassignment?view=graph-rest-beta).|
|Eliminación|beta|Se quitó la propiedad **usernameSource** de la entidad [windows10EasEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-windows10easemailprofileconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **localSecurityOptionsDisableClientDigitallySignCommunicationsIfServerAgrees**, **localSecurityOptionsClientSendUnencryptedPasswordToThirdPartySMBServers**, **localSecurityOptionsDisableServerDigitallySignCommunicationsAlways**, **localSecurityOptionsDisableServerDigitallySignCommunicationsIfClientAgrees**, **localSecurityOptionsRestrictAnonymousAccessToNamedPipesAndShares**, **localSecurityOptionsDoNotAllowAnonymousEnumerationOfSAMAccounts**, **localSecurityOptionsAllowAnonymousEnumerationOfSAMAccountsAndShares**, **localSecurityOptionsDoNotStoreLANManagerHashValueOnNextPasswordChange** y **localSecurityOptionsSmartCardRemovalBehavior** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **showInstallationProgress**, **blockDeviceSetupRetryByUser**, **allowDeviceResetOnInstallFailure**, **allowLogCollectionOnInstallFailure**, **customErrorMessage**, **installProgressTimeoutInMinutes** y **allowDeviceUseOnInstallFailure** a la entidad [windows10EnrollmentCompletionPageConfiguration](/graph/api/resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration?view=graph-rest-beta).|
|Eliminación|beta|Se quitaron las propiedades **title**, **bodyText**, **moreInfoUrl** y **moreInfoText** de la entidad [windows10EnrollmentCompletionPageConfiguration](/graph/api/resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **defenderBlockOnAccessProtection**, **defenderScheduleScanDay** y **defenderSubmitSamplesConsentType** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **language** y **enrollmentSettings** a la entidad [windowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-windowsautopilotdeploymentprofile?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **useDeviceContext** a la entidad [windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-beta).|
|Eliminación|beta|Se quitó la propiedad **usernameSource** de la entidad [windowsPhoneEASEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration?view=graph-rest-beta).|
|Eliminación|beta|Se quitó la propiedad de navegación **localActions** de la entidad [yroidCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidcompliancepolicy?view=graph-rest-beta).|
|Eliminación|beta|Se quitaron las propiedades de navegación **enrollmentProfiles** y **importedAppleDeviceIdentities** de la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad de navegación **mobileAppIntentAndStates** y **mobileAppTroubleshootingEvents** a la entidad [user](/graph/api/resources/intune-shared-user?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **deviceUsageType** y **skipKeyboardSelectionPage** al tipo complejo [outOfBoxExperienceSettings](/graph/api/resources/intune-enrollment-outofboxexperiencesettings?view=graph-rest-beta).|
|Eliminación|beta|Se quitó el miembro **paloAltoGlobalProtect** del tipo de enumeración [yroidForWorkVpnConnectionType](/graph/api/resources/intune-deviceconfig-androidforworkvpnconnectiontype?view=graph-rest-beta).|
|Adición|beta|Se agregaron los miembros **samAccountName** y **primarySmtpAddress** al tipo de enumeración [yroidUsernameSource](/graph/api/resources/intune-deviceconfig-androidusernamesource?view=graph-rest-beta).|
|Eliminación|beta|Se quitó el miembro **paloAltoGlobalProtect** del tipo de enumeración [yroidVpnConnectionType](/graph/api/resources/intune-deviceconfig-androidvpnconnectiontype?view=graph-rest-beta).|
|Adición|beta|Se agregó el miembro **paloAltoGlobalProtect** al tipo de enumeración [windows10VpnConnectionType](/graph/api/resources/intune-deviceconfig-windows10vpnconnectiontype?view=graph-rest-beta).|

### <a name="insights-api"></a>API de Insights

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | Beta          | Se agregó la entidad [settings](/graph/api/resources/user-settings?view=graph-rest-beta) y los siguientes métodos CRUD: <br> [Obtener](/graph/api/user-get-settings?view=graph-rest-beta) <br> [Actualizar](/graph/api/user-update-settings?view=graph-rest-beta) |

### <a name="azure-ad-apis"></a>API de Azure AD

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Cambio           | Beta          | Se ha cambiado el nombre de la propiedad **creatorUserId** de la entidad [subscription](/graph/api/resources/subscription?view=graph-rest-beta) a **creatorId** para reflejar mejor su significado. |

## <a name="april-2018"></a>Abril de 2018

### <a name="audit-log-api"></a>API de registros de auditoría

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Se agregaron las entidades [directoryAudit](/graph/api/resources/directoryaudit?view=graph-rest-beta) y [signIn](/graph/api/resources/signin?view=graph-rest-beta) para admitir la nueva API de registros de auditoría. |
|Adición|Beta|Se agregaron los recursos siguientes para admitir la API de registros de auditoría: [appIndentity](/graph/api/resources/appidentity?view=graph-rest-beta), [auditActivityInitiator](/graph/api/resources/auditactivityinitiator?view=graph-rest-beta), [conditionalAccessPolicy](/graph/api/resources/conditionalaccesspolicy?view=graph-rest-beta), [deviceDetail](/graph/api/resources/devicedetail?view=graph-rest-beta), [mfaDetail](/graph/api/resources/mfadetail?view=graph-rest-beta), [modifiedProperty](/graph/api/resources/modifiedproperty?view=graph-rest-beta), [signinLocation](/graph/api/resources/signinlocation?view=graph-rest-beta), [signinStatus](/graph/api/resources/signinstatus?view=graph-rest-beta), [targetResource](/graph/api/resources/targetresource?view=graph-rest-beta), [targetResourceApp](/graph/api/resources/targetresourceapp?view=graph-rest-beta), [targetResourceDevice](/graph/api/resources/targetresourcedevice?view=graph-rest-beta), [targetResourceDirectory](/graph/api/resources/targetresourcedirectory?view=graph-rest-beta), [targetResourceGroup](/graph/api/resources/targetresourcegroup?view=graph-rest-beta), [targetResourceOther](/graph/api/resources/targetresourceother?view=graph-rest-beta), [targetResourcePolicy](/graph/api/resources/targetresourcepolicy?view=graph-rest-beta), [targetResourceRole](/graph/api/resources/targetresourcerole?view=graph-rest-beta), [targetResourceServicePrincipal](/graph/api/resources/targetresourceserviceprincipal?view=graph-rest-beta), [targetResourceUser](/graph/api/resources/targetresourceuser?view=graph-rest-beta), [userIdentity](/graph/api/resources/useridentity?view=graph-rest-beta) |

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se ha agregado el tipo complejo **privacyProfile** a la entidad [organization](/graph/api/resources/organization?view=graph-rest-1.0). |
| Adición        | v1.0        | Se agregaron los tipos complejos **legalAgeGroup, ageGroup y consentProvidedForMinor** a la entidad [user](/graph/api/resources/user?view=graph-rest-1.0). |
| Adición        | v1.0        | Se agregó la compatibilidad de grupos y usuarios a las suscripciones de notificación de [webhooks](/graph/api/resources/webhooks?view=graph-rest-1.0). |
| Adición        | beta        | Se agregó la acción [Mostrar lista de elementos eliminados que pertenecen a un usuario](/graph/api/directory-deleteditems-user-owned?view=graph-rest-beta) al recurso [directorio (elementos eliminados)](/graph/api/resources/directory?view=graph-rest-beta). |

### <a name="education-apis"></a>API para el ámbito educativo

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Cambio|Beta|Se ha agregado la propiedad reportableIdentifier a [educationsynchronizationerror](/graph/api/resources/educationsynchronizationerror?view=graph-rest-beta).|
|Cambio|Beta|Se han actualizado las opciones de respuesta para la API [uploadUrl](/graph/api/educationsynchronizationprofile-uploadurl?view=graph-rest-beta).|
|Cambio|Beta|Se ha actualizado el texto de descripción del tipo de recurso [educationSynchronizationError](/graph/api/resources/educationsynchronizationerror?view=graph-rest-beta).|
|Cambio|Beta|Se actualizó el texto de descripción de la API [Obtener errores de sincronización](/graph/api/educationsynchronizationerrors-get?view=graph-rest-beta).|


### <a name="microsoft-intune-apis"></a>API de Microsoft Intune
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Se agregaron nuevas entidades:<br/>[managedDeviceMobileAppConfigurationDeviceStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicestatus?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Se agregaron nuevos tipos de enumeración:<br/>[managedDeviceOwnerType](/graph/api/resources/intune-devices-manageddeviceownertype?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Se agregó la propiedad **managedDeviceOwnerType** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0).|
|Adición|v1.0|Se agregó la propiedad de navegación **deviceStatuses** a la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-1.0).|
|Adición|v1.0|Se agregó el miembro **androidWorkProfile** al tipo de enumeración [policyPlatformType](/graph/api/resources/intune-deviceconfig-policyplatformtype?view=graph-rest-1.0).|
|Adición|beta|Se agregaron nuevas entidades:<br/>[androidWorkProfileCertificateProfileBase](/graph/api/resources/intune-deviceconfig-androidworkprofilecertificateprofilebase?view=graph-rest-beta)<br/>[androidWorkProfileCustomConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilecustomconfiguration?view=graph-rest-beta)<br/>[androidWorkProfileEasEmailProfileBase](/graph/api/resources/intune-deviceconfig-androidworkprofileeasemailprofilebase?view=graph-rest-beta)<br/>[androidWorkProfileEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration?view=graph-rest-beta)<br/>[androidWorkProfileGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration?view=graph-rest-beta)<br/>[androidWorkProfileGmailEasConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilegmaileasconfiguration?view=graph-rest-beta)<br/>[androidWorkProfileNineWorkEasConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration?view=graph-rest-beta)<br/>[androidWorkProfilePkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-androidworkprofilepkcscertificateprofile?view=graph-rest-beta)<br/>[androidWorkProfileScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidworkprofilescepcertificateprofile?view=graph-rest-beta)<br/>[androidWorkProfileTrustedRootCertificate](/graph/api/resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate?view=graph-rest-beta)<br/>[androidWorkProfileVpnConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilevpnconfiguration?view=graph-rest-beta)<br/>[androidWorkProfileWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidworkprofilewificonfiguration?view=graph-rest-beta)<br/>[restrictedAppsViolation](/graph/api/resources/intune-deviceconfig-restrictedappsviolation?view=graph-rest-beta)<br/>[windowsAutopilotDeploymentProfileAssignment](/graph/api/resources/intune-enrollment-windowsautopilotdeploymentprofileassignment?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregaron nuevos tipos complejos:<br/>[managedDeviceModelsAndManufacturers](/graph/api/resources/intune-devices-manageddevicemodelsandmanufacturers?view=graph-rest-beta)<br/>[managedDeviceReportedApp](/graph/api/resources/intune-devices-manageddevicereportedapp?view=graph-rest-beta)<br/>[windowsEnrollmentStatusScreenSettings](/graph/api/resources/intune-enrollment-windowsenrollmentstatusscreensettings?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregaron nuevos tipos de enumeración:<br/>[androidWorkProfileCrossProfileDataSharingType](/graph/api/resources/intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype?view=graph-rest-beta)<br/>[androidWorkProfileDefaultAppPermissionPolicyType](/graph/api/resources/intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype?view=graph-rest-beta)<br/>[androidWorkProfileRequiredPasswordType](/graph/api/resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype?view=graph-rest-beta)<br/>[androidWorkProfileVpnConnectionType](/graph/api/resources/intune-deviceconfig-androidworkprofilevpnconnectiontype?view=graph-rest-beta)<br/>[bitLockerRecoveryInformationType](/graph/api/resources/intune-deviceconfig-bitlockerrecoveryinformationtype?view=graph-rest-beta)<br/>[localSecurityOptionsInformationShownOnLockScreenType](/graph/api/resources/intune-deviceconfig-localsecurityoptionsinformationshownonlockscreentype?view=graph-rest-beta)<br/>[managedAppRemediationAction](/graph/api/resources/intune-mam-managedappremediationaction?view=graph-rest-beta)<br/>[managedDeviceOwnerType](/graph/api/resources/intune-devices-manageddeviceownertype?view=graph-rest-beta)<br/>[restrictedAppsState](/graph/api/resources/intune-deviceconfig-restrictedappsstate?view=graph-rest-beta)<br/>[windows10VpnProfileTarget](/graph/api/resources/intune-deviceconfig-windows10vpnprofiletarget?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la acción [playLostModeSound](/graph/api/intune-devices-manageddevice-playlostmodesound?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
|Eliminación|beta|Se quitaron los siguientes tipos de enumeración:<br/>**bitLockerRecoveryinformationType**<br/>**windowsUpdateRestartMode**<br/>|
|Adición|beta|Se agregaron las propiedades **workProfileBlockScreenCapture** y **workProfileBlockCrossProfileCallerId** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **minimumWipePatchVersion**, **allowedAndroidDeviceManufacturers** y **appActionIfAndroidDeviceManufacturerNotAllowed** a la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **minimumWipeSdkVersion**, **minimumWipePatchVersion**, **allowedIosDeviceModels**, **appActionIfIosDeviceModelNotAllowed**, **allowedAndroidDeviceManufacturers** y **appActionIfAndroidDeviceManufacturerNotAllowed** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **notApplicablePlatformCount** y **conflictCount** a la entidad [deviceComplianceDeviceOverview](/graph/api/resources/intune-deviceconfig-devicecompliancedeviceoverview?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **notApplicablePlatformCount** y **conflictCount** a la entidad [deviceConfigurationDeviceOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationdeviceoverview?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **accountMoveCompletionDateTime** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **minimumWipeSdkVersion**, **allowedIosDeviceModels** y **appActionIfIosDeviceModelNotAllowed** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **minimumWipeOsVersion**, **minimumWipeAppVersion**, **appActionIfDeviceComplianceRequired** y **appActionIfMaximumPinRetriesExceeded** a la entidad [managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **managedDeviceOwnerType**, **preferMdmOverGroupPolicyAppliedDateTime**, **isAutopilotEnrolled** y **requestUserEnrollmentApproval** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **managedDeviceModelsAndManufacturers** a la entidad [managedDeviceOverview](/graph/api/resources/intune-devices-manageddeviceoverview?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **localSecurityOptionsMachineInactivityLimitInMinutes**, **localSecurityOptionsAllowRemoteCallsToSecurityAccountsManagerHelperBool**, **localSecurityOptionsInformationShownOnLockScreen**, **defenderSecurityCenterDisableAccountUI**, **defenderSecurityCenterDisableHardwareUI**, **defenderSecurityCenterDisableRansomwareUI**, **defenderSecurityCenterDisableSecureBootUI** y **defenderSecurityCenterDisableTroubleshootingUI** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **printerNames**, **printerDefaultName**, **printerBlockAddition** y **searchBlockWebResults** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregaron las propiedades **profileTarget**, **enableAlwaysOn** y **enableDeviceTunnel** a la entidad [windows10VpnConfiguration](/graph/api/resources/intune-deviceconfig-windows10vpnconfiguration?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **enrollmentStatusScreenSettings** a la entidad [windowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-windowsautopilotdeploymentprofile?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad de navegación **deviceConfigurationRestrictedAppsViolations** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad de navegación **assignments** a la entidad [windowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-windowsautopilotdeploymentprofile?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad de navegación **networkAccessConfigurations** a la entidad [windowsDomainJoinConfiguration](/graph/api/resources/intune-deviceconfig-windowsdomainjoinconfiguration?view=graph-rest-beta).|
|Eliminación|beta|Se quitó la propiedad **permissions** del tipo complejo [auditActor](/graph/api/resources/intune-auditing-auditactor?view=graph-rest-beta).|
|Cambio|beta|Se cambió el tipo de las propiedades siguientes en el tipo complejo [bitLockerRecoveryOptions](/graph/api/resources/intune-deviceconfig-bitlockerrecoveryoptions?view=graph-rest-beta):<br/>**recoveryInformationToStore** de [bitLockerRecoveryinformationType](/graph/api/resources/intune-deviceconfig-bitlockerrecoveryinformationtype?view=graph-rest-beta) a [bitLockerRecoveryInformationType](/graph/api/resources/intune-deviceconfig-bitlockerrecoveryinformationtype?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la propiedad **deviceInactivityBeforeRetirementInDay** al tipo complejo [deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad **landingPageCustomizedImage** al tipo complejo [intuneBrand](/graph/api/resources/intune-onboarding-intunebrand?view=graph-rest-beta).|
|Eliminación|beta|Se agregó la propiedad **ipAddressOrFqdn** al tipo complejo [vpnServer](/graph/api/resources/intune-deviceconfig-vpnserver?view=graph-rest-beta)|
|Eliminación|beta|Se quitó la propiedad **restartMode** al tipo complejo [windowsUpdateScheduledInstall](/graph/api/resources/intune-deviceconfig-windowsupdatescheduledinstall?view=graph-rest-beta)|
|Adición|beta|Se agregó el miembro **paloAltoGlobalProtect** al tipo de enumeración [androidForWorkVpnConnectionType](/graph/api/resources/intune-deviceconfig-androidforworkvpnconnectiontype?view=graph-rest-beta).|
|Adición|beta|Se agregó el miembro **paloAltoGlobalProtect** al tipo de enumeración [androidVpnConnectionType](/graph/api/resources/intune-deviceconfig-androidvpnconnectiontype?view=graph-rest-beta).|
|Adición|beta|Se agregó el miembro **paloAltoGlobalProtect** al tipo de enumeración [appleVpnConnectionType](/graph/api/resources/intune-deviceconfig-applevpnconnectiontype?view=graph-rest-beta).|
|Adición|beta|Se agregó el miembro **androidWorkProfile** al tipo de enumeración [policyPlatformType](/graph/api/resources/intune-deviceconfig-policyplatformtype?view=graph-rest-beta).|

### <a name="outlook-calendar"></a>Calendario de Outlook

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0          | Se ha agregado la propiedad **locations** a la entidad [event](/graph/api/resources/event?view=graph-rest-1.0) para admitir la organización de un evento al que puedan asistir asistentes de más de una ubicación. |
| Adición        | v1.0          | Se ha agregado la propiedad **locationType** al tipo complejo [ubication](/graph/api/resources/location?view=graph-rest-1.0). |
| Adición        | v1.0          | Se han agregado las propiedades **uniqueId** y **uniqueIdType** al tipo complejo [location](/graph/api/resources/location?view=graph-rest-1.0). Estas propiedades son solo para uso interno en este momento. |


### <a name="outlook-contacts"></a>Contactos de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0          | Se ha agregado la propiedad **flag** a la entidad [contact](/graph/api/resources/contact?view=graph-rest-1.0). Se ha agregado el tipo complejo [followupFlag](/graph/api/resources/followupflag?view=graph-rest-1.0) compartido.|


### <a name="outlook-mail"></a>Correo de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0          | Se ha agregado la propiedad **flag** a la entidad [message](/graph/api/resources/message?view=graph-rest-1.0). Se ha agregado el tipo complejo [followupFlag](/graph/api/resources/followupflag?view=graph-rest-1.0) compartido.|
| Adición        | v1.0        | Se ha agregado la propiedad **internetMessageHeaders** a la entidad [message](/graph/api/resources/message?view=graph-rest-1.0). |
| Adición        | v1.0        | Se ha agregado el tipo complejo [internetMessageHeader](/graph/api/resources/internetmessageheader?view=graph-rest-1.0). |
| Adición        | v1.0        | Se ha agregado la propiedad de navegación **messageRules** a la entidad [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0). **messageRules** es una colección de instancias de [messageRule](/graph/api/resources/messagerule?view=graph-rest-1.0). |
| Adición        | v1.0        | Se ha agregado la entidad [messageRule](/graph/api/resources/messagerule?view=graph-rest-1.0) y los tipos complejos [messageRuleActions](/graph/api/resources/messageruleactions?view=graph-rest-1.0), [messageRulePredicates](/graph/api/resources/messagerulepredicates?view=graph-rest-1.0) y [sizeRange](/graph/api/resources/sizerange?view=graph-rest-1.0). |
| Adición        | v1.0        | Se han agregado las siguientes operaciones CRUD para reglas de mensaje: [crear](/graph/api/mailfolder-post-messagerules?view=graph-rest-1.0), [enumerar](/graph/api/mailfolder-list-messagerules?view=graph-rest-1.0), [obtener](/graph/api/messagerule-get?view=graph-rest-1.0), [actualizar](/graph/api/messagerule-update?view=graph-rest-1.0) y [eliminar](/graph/api/messagerule-delete?view=graph-rest-1.0). |
| Adición | Beta | Se ha agregado [mailSearchFolder](/graph/api/resources/mailsearchfolder?view=graph-rest-beta). |
| Adición | Beta | Se han agregado las siguientes API para la carpeta de búsqueda correo: [crear](/graph/api/mailsearchfolder-post?view=graph-rest-beta), [actualizar](/graph/api/mailsearchfolder-update?view=graph-rest-beta). |
| Cambio | Beta | Se ha agregado compatibilidad con la carpeta de búsqueda correo para [eliminar mailFolder](/graph/api/mailfolder-delete?view=graph-rest-beta), [obtener mailFolder](/graph/api/mailfolder-get?view=graph-rest-beta) y [enumerar carpetas secundarias](/graph/api/mailfolder-list-childfolders?view=graph-rest-beta). |


### <a name="outlook-user-choices"></a>Opciones de usuario de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se ha agregado la nueva propiedad de navegación **masterCategories** a la entidad [outlookUser](/graph/api/resources/outlookuser?view=graph-rest-1.0). **masterCategories** es una colección de objetos [outlookCategory](/graph/api/resources/outlookcategory?view=graph-rest-1.0). |
| Adición        | v1.0        | Se ha agregado la entidad [outlookCategory](/graph/api/resources/outlookcategory?view=graph-rest-1.0). |
| Adición        | v1.0        | Se han agregado las siguientes operaciones CRUD para [outlookCategory](/graph/api/resources/outlookcategory?view=graph-rest-1.0): [crear](/graph/api/outlookuser-post-mastercategories?view=graph-rest-1.0), [obtener](/graph/api/outlookcategory-get?view=graph-rest-1.0), [actualizar](/graph/api/outlookcategory-update?view=graph-rest-1.0) y [eliminar](/graph/api/outlookcategory-delete?view=graph-rest-1.0). |
| Adición        | v1.0        | Se ha agregado la nueva función [supportedLanguages](/graph/api/outlookuser-supportedlanguages?view=graph-rest-1.0) a la entidad [outlookUser](/graph/api/resources/outlookuser?view=graph-rest-1.0). |
| Adición        | v1.0        | Se ha agregado la nueva función [supportedTimeZones](/graph/api/outlookuser-supportedtimezones?view=graph-rest-1.0) a la entidad [outlookUser](/graph/api/resources/outlookuser?view=graph-rest-1.0). |
|Adición | v1.0 | Se ha agregado la nueva propiedad **workingHours** a [mailboxSettings](/graph/api/resources/mailboxsettings?view=graph-rest-1.0). Vea [tipo de recurso workingHours](/graph/api/resources/workinghours?view=graph-rest-1.0) para obtener información sobre los casos de uso compatibles.|
|Adición | v1.0 | Se han agregado los nuevos tipos complejos siguientes: <br> [workingHours](/graph/api/resources/workinghours?view=graph-rest-1.0) <br> [timeZoneBase](/graph/api/resources/timezonebase?view=graph-rest-1.0) <br> [customTimeZone](/graph/api/resources/customtimezone?view=graph-rest-1.0) <br> [standardTimeZoneOffset](/graph/api/resources/standardtimezoneoffset?view=graph-rest-1.0) <br> [daylightTimeZoneOffset](/graph/api/resources/daylighttimezoneoffset?view=graph-rest-1.0)|


### <a name="microsoft-teams"></a>Microsoft Teams

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Se agregó la nueva entidad [teamMemberSettings](/graph/api/resources/teammembersettings?view=graph-rest-beta).|
|Adición|Beta|Se agregó la nueva entidad [teamGuestSettings](/graph/api/resources/teamguestsettings?view=graph-rest-beta).|
|Adición|Beta|Se agregó la nueva entidad [teamMessagingSettings](/graph/api/resources/teammessagingsettings?view=graph-rest-beta).|
|Adición|Beta|Se agregó la nueva entidad [teamFunSettings](/graph/api/resources/teamfunsettings?view=graph-rest-beta).|
|Adición|Beta|Se agregó la nueva operación [eliminar canal](/graph/api/channel-delete?view=graph-rest-beta).|
|Adición|Beta|Se ha agregado la nueva operación [aplicar revisión en canal](/graph/api/channel-patch?view=graph-rest-beta).|
|Adición|Beta|Se ha agregado la nueva propiedad webUrl al recurso [team](/graph/api/resources/team?view=graph-rest-beta).|
|Cambio|Beta|Se actualizó la ruta a la entidad [channel](/graph/api/resources/channel?view=graph-rest-beta).|


### <a name="project-rome-apis"></a>API del proyecto Rome

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición | v1.0 | Se ha agregado la [API Obtener actividades recientes](/graph/api/projectrome-get-recent-activities?view=graph-rest-1.0). |
| Adición | v1.0 | Se ha agregado la [API Obtener actividades](/graph/api/projectrome-get-activities?view=graph-rest-1.0). |
| Adición | v1.0 | Se agregó [Upsert Activity](/graph/api/projectrome-put-activity?view=graph-rest-1.0). |
| Adición | v1.0 | Se agregó [Upsert HistoryItem](/graph/api/projectrome-put-historyitem?view=graph-rest-1.0). |
| Adición | v1.0 | Se agregó [Delete Activity](/graph/api/projectrome-delete-activity?view=graph-rest-1.0). |
| Adición | v1.0 | Se agregó [Upsert HistoryItem](/graph/api/projectrome-delete-historyitem?view=graph-rest-1.0). |
| Adición | v1.0 | Se agregó [activity](/graph/api/resources/projectrome-activity?view=graph-rest-1.0). |
| Adición | v.10 | Se agregó [historyItem](/graph/api/resources/projectrome-historyitem?view=graph-rest-1.0). |
| Adición | v1.0 | Se agregó [visualInfo](/graph/api/resources/projectrome-visualinfo?view=graph-rest-1.0). |
| Adición | v1.0 | Se agregó [imageInfo](/graph/api/resources/projectrome-imageinfo?view=graph-rest-1.0). |
| Adición | v.10 | Se agregó [información general sobre el proyecto Rome](/graph/api/resources/project-rome-overview?view=graph-rest-1.0). |
| Cambio | Beta | Se agregó la documentación exhaustiva sobre la inserción en la [actividad Upsert](/graph/api/projectrome-put-activity?view=graph-rest-beta). |

### <a name="reports-apis"></a>API de informes
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|beta| Se ha agregado compatibilidad con acceso delegado. |
|Adición|v1.0| Se ha agregado compatibilidad con acceso delegado. |

### <a name="security-apis"></a>API de seguridad

| **Tipo de cambio** | **Versión** | **Descripción**              |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta       | Se ha agregado la [API para seguridad](/graph/api/resources/security-api-overview?view=graph-rest-beta), incluidos los siguientes recursos y operaciones:<br/>[alert](/graph/api/resources/alert?view=graph-rest-beta) (y entidades relacionadas)<br/>[Get alert](/graph/api/alert-get?view=graph-rest-beta)<br/>[List alerts](/graph/api/alert-list?view=graph-rest-beta)<br/>[Update alert](/graph/api/alert-update?view=graph-rest-beta)<br/><br/>Se ha incluido la siguiente documentación complementaria:<br/>[Errores](/graph/api/resources/security-error-codes?view=graph-rest-beta)<br/>[Integración con un SIEM](security-siemintegration.md)


## <a name="march-2018"></a>Marzo de 2018

### <a name="data-policy-operations"></a>Operaciones de directiva de datos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | beta        | Se agregó la nueva entidad [dataPolicyOperation](/graph/api/resources/datapolicyoperation?view=graph-rest-beta). Representa una operación de directiva de datos enviados con fines de seguimiento.
| Adición        | beta        | Se agregó la acción [exportPersonalData](/graph/api/user-exportpersonaldata?view=graph-rest-beta) en [users](/graph/api/resources/users?view=graph-rest-beta). Esta acción envía una solicitud de operación de directiva de datos para exportar datos personales de un usuario almacenados por Microsoft. |

### <a name="activityfeedservice-apis"></a>API de ActivityFeedService

| **Tipo de cambio** | **Versión** | **Descripción**              |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta       | Se ha agregado la [API Obtener actividades recientes](/graph/api/projectrome-get-recent-activities?view=graph-rest-beta). |
| Adición        | Beta       | Se ha agregado la [API Obtener actividades](/graph/api/projectrome-get-activities?view=graph-rest-beta). |
| Cambio | Beta | Se ha agregado el permiso UserActivity.ReadWrite.CreatedByApp a [Upsert Activity](/graph/api/projectrome-put-activity?view=graph-rest-beta). |
| Cambio | Beta | Se ha agregado el permiso UserActivity.ReadWrite.CreatedByApp a [Upsert HistoryItem](/graph/api/projectrome-put-historyitem?view=graph-rest-beta). |
| Cambio | Beta | Se ha agregado el permiso UserActivity.ReadWrite.CreatedByApp a [Delete Activity](/graph/api/projectrome-delete-activity?view=graph-rest-beta). |
| Cambio | Beta | Se ha agregado el permiso UserActivity.ReadWrite.CreatedByApp a [Upsert HistoryItem](/graph/api/projectrome-delete-historyitem?view=graph-rest-beta). |
| Cambio | Beta | Se ha agregado la propiedad **status** a [activity](/graph/api/resources/projectrome-activity?view=graph-rest-beta). |
| Cambio | Beta | Se ha agregado la propiedad de navegación **activity** a [historyItem](/graph/api/resources/projectrome-historyitem?view=graph-rest-beta). |
| Cambio | Beta | Se han agregado nuevas API a [Información general sobre Project Rome](/graph/api/resources/project-rome-overview?view=graph-rest-beta). |

### <a name="azure-ad-apis"></a>API de Azure AD

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Cambio|beta|Se han agregado las propiedades **applicationID** y **creatorUserID** al recurso [subscription](/graph/api/resources/subscription?view=graph-rest-beta). |
|Cambio|beta|Se ha agregado la operación [list](/graph/api/subscription-list?view=graph-rest-beta) a la entidad [subscription](/graph/api/resources/subscription?view=graph-rest-beta). |


### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se ha agregado el tipo complejo **onPremisesExtensionAttributes** a la entidad [user](/graph/api/resources/user?view=graph-rest-beta). Contiene los atributos 1-15 de extensión de AD local. |
| Adición        | Beta        | Se ha agregado el tipo complejo **privacyProfile** a la entidad [organization](/graph/api/resources/organization?view=graph-rest-beta). |
| Adición        | v1.0        | Se agregó compatibilidad con [la restauración de usuarios y grupos, y su eliminación permanente](/graph/api/resources/directory?view=graph-rest-1.0). |

### <a name="excel-apis"></a>API de Excel

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
|Cambio|v1.0|Se agregó la propiedad **legacyId** a la entidad [Tabla de Excel](/graph/api/resources/table?view=graph-rest-1.0). Esta contendrá el identificador de valor numérico (tipo de datos String) que quedará constante para una tabla de Excel determinada. Se proporciona como metadatos adicionales si la aplicación dependía del identificador heredado usado en aplicaciones cliente de Excel anteriores. Nota: Las propiedades `id` y `legacyId` deben tratarse como un valor de cadena opaco y no se deberían analizar para ningún otro tipo de la aplicación. |

### <a name="reports-apis"></a>API de informes

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
|Adición|beta|Agregada la propiedad **Id. del sitio** a la entidad [sharePointSiteUsageDetail](/graph/api/resources/sharepointsiteusagedetail?view=graph-rest-beta).|

### <a name="group-lifecycle-policy"></a>Directiva de ciclo de vida del grupo

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó [groupLifecyclePolicy](/graph/api/resources/grouplifecyclepolicy?view=graph-rest-1.0). |
| Adición        | versión 1.0        | Se agregaron las siguientes API para la directiva de ciclo de vida del grupo: [Crear](/graph/api/grouplifecyclepolicy-post-grouplifecyclepolicies?view=graph-rest-1.0), [Enumerar](/graph/api/grouplifecyclepolicy-list?view=graph-rest-1.0), [Obtener](/graph/api/grouplifecyclepolicy-get?view=graph-rest-1.0), [Actualizar](/graph/api/grouplifecyclepolicy-update?view=graph-rest-1.0), [Eliminar](/graph/api/grouplifecyclepolicy-delete?view=graph-rest-1.0), [Agregar grupo](/graph/api/grouplifecyclepolicy-addgroup?view=graph-rest-1.0), [Quitar grupo ](/graph/api/grouplifecyclepolicy-removegroup?view=graph-rest-1.0) |
| Adición        | v1.0        | Se agregó la función [List groupLifecylePolicies](/graph/api/group-list-grouplifecyclepolicies?view=graph-rest-1.0) al [grupo](/graph/api/resources/group?view=graph-rest-1.0). |
| Cambio | v1.0 | Se ha agregado la propiedad renewedDateTime y [renew](/graph/api/group-renew?view=graph-rest-1.0) a [group](/graph/api/resources/group?view=graph-rest-1.0). |

### <a name="terms-of-use"></a>Términos de uso

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se han agregado los recursos [agreement](/graph/api/resources/agreement?view=graph-rest-beta) y [agreementAcceptance](/graph/api/resources/agreementacceptance?view=graph-rest-beta). |
| Adición        | Beta        | Se ha agregado las siguientes API para [agreement](/graph/api/resources/agreement?view=graph-rest-beta): [Crear](/graph/api/greement-post-agreements?view=graph-rest-beta), [Enumerar](/graph/api/agreement-list?view=graph-rest-beta), [Obtener](/graph/api/agreement-get?view=graph-rest-beta), [Actualizar](/graph/api/agreement-update?view=graph-rest-beta), [Eliminar](/graph/api/agreement-delete?view=graph-rest-beta). |
| Adición        | Beta        | Se han agregado las relaciones [agreementAcceptance](/graph/api/resources/agreementacceptance?view=graph-rest-beta) al recurso [user](/graph/api/resources/user?view=graph-rest-beta). |

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Se han agregado nuevas entidades:<br/>[iosMobileAppConfiguration](/graph/api/resources/intune-apps-iosmobileappconfiguration?view=graph-rest-1.0)<br/>[vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Se han agregado nuevos tipos complejos:<br/>[appConfigurationSettingItem](/graph/api/resources/intune-apps-appconfigurationsettingitem?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Se ha agregado la acción [syncLicenses](/graph/api/intune-onboarding-vpptoken-synclicenses?view=graph-rest-1.0) en [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-1.0). |
|Adición|v1.0|Se ha agregado la propiedad de navegación **vppTokens** a la entidad [deviceAppManagement](/graph/api/resources/intune-shared-deviceappmanagement?view=graph-rest-1.0).|
|Adición|beta|Se ha agregado la propiedad **managementCertificateExpirationDate** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **enhancedJailBreak** al tipo complejo [deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-beta)|
|Adición|beta|Se han agregado nuevas entidades:<br/>[androidDeviceOwnerEnrollmentProfile](/graph/api/resources/intune-androidforwork-androiddeviceownerenrollmentprofile?view=graph-rest-beta)<br/>[androidDeviceOwnerGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration?view=graph-rest-beta)<br/>[androidManagedStoreAccountEnterpriseSettings](/graph/api/resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings?view=graph-rest-beta)<br/>[androidManagedStoreAppConfigurationSchema](/graph/api/resources/intune-androidforwork-androidmanagedstoreappconfigurationschema?view=graph-rest-beta)<br/>[dataSharingConsent](/graph/api/resources/intune-devices-datasharingconsent?view=graph-rest-beta)<br/>[deviceConfigurationUserStateSummary](/graph/api/resources/intune-deviceconfig-deviceconfigurationuserstatesummary?view=graph-rest-beta)<br/>[macOSEndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-macosendpointprotectionconfiguration?view=graph-rest-beta)<br/>[macOSImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-macosimportedpfxcertificateprofile?view=graph-rest-beta)<br/>[macOSLobApp](/graph/api/resources/intune-apps-macoslobapp?view=graph-rest-beta)<br/>[managedEBookCategory](/graph/api/resources/intune-books-managedebookcategory?view=graph-rest-beta)<br/>[microsoftStoreForBusinessContainedApp](/graph/api/resources/intune-apps-microsoftstoreforbusinesscontainedapp?view=graph-rest-beta)<br/>[mobileContainedApp](/graph/api/resources/intune-apps-mobilecontainedapp?view=graph-rest-beta)<br/>[windowsUniversalAppXContainedApp](/graph/api/resources/intune-apps-windowsuniversalappxcontainedapp?view=graph-rest-beta)<br/>|
|Adición|beta|Se han agregado nuevos tipos complejos:<br/>[androidManagedStoreAppConfigurationSchemaItem](/graph/api/resources/intune-androidforwork-androidmanagedstoreappconfigurationschemaitem?view=graph-rest-beta)<br/>[deviceAndAppManagementData](/graph/api/resources/intune-onboarding-deviceandappmanagementdata?view=graph-rest-beta)<br/>[loggedOnUser](/graph/api/resources/intune-devices-loggedonuser?view=graph-rest-beta)<br/>[macOSFirewallApplication](/graph/api/resources/intune-deviceconfig-macosfirewallapplication?view=graph-rest-beta)<br/>[macOSLobChildApp](/graph/api/resources/intune-apps-macoslobchildapp?view=graph-rest-beta)<br/>[macOSMinimumOperatingSystem](/graph/api/resources/intune-apps-macosminimumoperatingsystem?view=graph-rest-beta)<br/>[windowsAppXAppAssignmentSettings](/graph/api/resources/intune-apps-windowsappxappassignmentsettings?view=graph-rest-beta)<br/>[windowsUniversalAppXAppAssignmentSettings](/graph/api/resources/intune-apps-windowsuniversalappxappassignmentsettings?view=graph-rest-beta)<br/>|
|Adición|beta|Se ha agregado la acción [requestSignupUrl](/graph/api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-requestsignupurl?view=graph-rest-beta) en [androidManagedStoreAccountEnterpriseSettings](/graph/api/resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la acción [completeSignup](/graph/api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-completesignup?view=graph-rest-beta) en [androidManagedStoreAccountEnterpriseSettings](/graph/api/resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings?view=graph-rest-beta) |
|Adición|beta|Se ha agregado la acción [syncApps](/graph/api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-syncapps?view=graph-rest-beta) en [androidManagedStoreAccountEnterpriseSettings](/graph/api/resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings?view=graph-rest-beta) |
|Adición|beta|Se ha agregado la acción [unbind](/graph/api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-unbind?view=graph-rest-beta) en [androidManagedStoreAccountEnterpriseSettings](/graph/api/resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings?view=graph-rest-beta) |
|Adición|beta|Se ha agregado la acción [revokeToken](/graph/api/intune-androidforwork-androiddeviceownerenrollmentprofile-revoketoken?view=graph-rest-beta) en [androidDeviceOwnerEnrollmentProfile](/graph/api/resources/intune-androidforwork-androiddeviceownerenrollmentprofile?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la acción [createToken](/graph/api/intune-androidforwork-androiddeviceownerenrollmentprofile-createtoken?view=graph-rest-beta) en [androidDeviceOwnerEnrollmentProfile](/graph/api/resources/intune-androidforwork-androiddeviceownerenrollmentprofile?view=graph-rest-beta) |
|Adición|beta|Se ha agregado la acción [assign](/graph/api/intune-apps-manageddevicemobileappconfiguration-assign?view=graph-rest-beta) en [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta) |
|Adición|beta|Se ha agregado la acción [consentToDataSharing](/graph/api/intune-devices-datasharingconsent-consenttodatasharing?view=graph-rest-beta) en [dataSharingConsent](/graph/api/resources/intune-devices-datasharingconsent?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la función [getLoggedOnManagedDevices](/graph/api/intune-devices-user-getloggedonmanageddevices?view=graph-rest-beta) en [user](/graph/api/resources/intune-shared-user?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la función [exportDeviceAndAppManagementData](/graph/api/intune-onboarding-user-exportdeviceandappmanagementdata?view=graph-rest-beta) en [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la función [exportDeviceAndAppManagementData](/graph/api/intune-onboarding-user-exportdeviceandappmanagementdata?view=graph-rest-beta) en [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta). |
|Eliminación|beta|Se quitaron las entidades siguientes:<br/>**appleVolumePurchaseProgramToken**<br/>**mdmAppConfigGroupAssignment**<br/>**windows10KioskConfiguration**<br/>|
|Eliminación|beta|Se ha quitado la acción [assign](/graph/api/intune-apps-manageddevicemobileappconfiguration-assign?view=graph-rest-beta) en [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta). |
|Eliminación|beta|Se ha quitado la acción [syncApps](/graph/api/intune-onboarding-applevolumepurchaseprogramtoken-syncapps?view=graph-rest-beta) en [appleVolumePurchaseProgramToken](/graph/api/resources/intune-onboarding-applevolumepurchaseprogramtoken?view=graph-rest-beta). |
|Adición|beta|Se ha agregado la propiedad **workProfileBluetoothEnableContactSharing** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **intendedPurpose** a la entidad [androidForWorkImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **intendedPurpose** a la entidad [androidImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-androidimportedpfxcertificateprofile?view=graph-rest-beta)|
|Adición|beta|Se ha agregado la propiedad **intendedPurpose** a la entidad [iosImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-iosimportedpfxcertificateprofile?view=graph-rest-beta)|
|Adición|beta|Se ha agregado la propiedad **encodedSettingXml** a la entidad [iosMobileAppConfiguration](/graph/api/resources/intune-apps-iosmobileappconfiguration?view=graph-rest-beta)|
|Adición|beta|Se han agregado las propiedades **managedDeviceId** y **azureADDeviceId** a la entidad [managedAppRegistration](/graph/api/resources/intune-mam-managedappregistration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **usersLoggedOn** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Eliminación|beta|Se ha quitado la propiedad **lastLoggedOnUserId** de la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **lastModifiedDateTime** a la entidad [managedDeviceOverview](/graph/api/resources/intune-devices-manageddeviceoverview?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **isDependency** a la entidad [mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **windowsEnabled**, **macEnabled**, **windowsDeviceBlockedOnMissingPartnerData** y **macDeviceBlockedOnMissingPartnerData** a la entidad [mobileThreatDefenseConnector](/graph/api/resources/intune-onboarding-mobilethreatdefenseconnector?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **shouldUninstallOlderVersionsOfOffice** a la entidad [officeSuiteApp](/graph/api/resources/intune-apps-officesuiteapp?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **dataSharingConsentGranted** a la entidad [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **localSecurityOptionsBlockRemoteLogonWithBlankPassword**, **localSecurityOptionsAdministratorAccountName**, **localSecurityOptionsEnableGuestAccount**, **localSecurityOptionsGuestAccountName**, **localSecurityOptionsAllowUndockWithoutHavingToLogon**, **localSecurityOptionsBlockUsersInstallingPrinterDrivers**, **localSecurityOptionsBlockRemoteOpticalDriveAccess**, **localSecurityOptionsFormatAndEjectOfRemovableMediaAllowedUser**, **localSecurityOptionsMachineInactivityLimit**, **localSecurityOptionsDoNotRequireCtrlAltDel**, **localSecurityOptionsInformationDisplayedOnLockScreen**, **localSecurityOptionsHideLastSignedInUser**, **localSecurityOptionsHideUsernameAtSignIn**, **localSecurityOptionsLogOnMessageTitle**, **localSecurityOptionsLogOnMessageText**, **localSecurityOptionsAllowPKU2UAuthenticationRequests**, **localSecurityOptionsAllowRemoteCallsToSecurityAccountsManager**, **localSecurityOptionsClearVirtualMemoryPageFile**, **localSecurityOptionsAllowSystemToBeShutDownWithoutHavingToLogOn**, **localSecurityOptionsAllowUIAccessApplicationElevation**, **localSecurityOptionsVirtualizeFileAndRegistryWriteFailuresToPerUserLocations**, **localSecurityOptionsOnlyElevateSignedExecutables**, **localSecurityOptionsAdministratorElevationPromptBehavior**, **localSecurityOptionsStandardUserElevationPromptBehavior**, **localSecurityOptionsSwitchToSecureDesktopWhenPromptingForElevation**, **localSecurityOptionsDetectApplicationInstallationsAndPromptForElevation**, **localSecurityOptionsAllowUIAccessApplicationsForSecureLocations**, **localSecurityOptionsUseAdminApprovalMode**, **localSecurityOptionsUseAdminApprovalModeForAdministrators**, **deviceGuardLocalSystemAuthorityCredentialGuardSettings**, **deviceGuardEnableVirtualizationBasedSecurity** y **deviceGuardEnableSecureBootWithDMA** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta).|
|Eliminación|beta|Se ha quitado la propiedad **defenderPasswordProtectedEmailContentExecutionType** de la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **intendedPurpose** a la entidad [windows10ImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-windows10importedpfxcertificateprofile?view=graph-rest-beta).|
|Eliminación|beta|Se han quitado las propiedades **printerNames**, **defaultPrinterName** y **blockAddingNewPrinter** de la entidad [windows10SecureAssessmentConfiguration](/graph/api/resources/intune-deviceconfig-windows10secureassessmentconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **certificateStore** a la entidad [windows81SCEPCertificateProfile](/graph/api/resources/intune-deviceconfig-windows81scepcertificateprofile?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **purchaseOrderIdentifier** a la entidad [windowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-windowsautopilotdeviceidentity?view=graph-rest-beta).|
|Cambio|beta|Se cambiaron las propiedades siguientes en la entidad [windowsCertificateProfileBase](/graph/api/resources/intune-deviceconfig-windowscertificateprofilebase?view=graph-rest-beta):<br/>**subjectAlternativeNameType** ha pasado de obligatoria a opcional.<br/>|
|Adición|beta|Se han agregado las propiedades **advancedThreatProtectionOnboardingFilename** y **advancedThreatProtectionOffboardingFilename** a la entidad [windowsDefenderAdvancedThreatProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad **intendedPurpose** a la entidad [windowsPhone81ImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-windowsphone81importedpfxcertificateprofile?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades **skipChecksBeforeRestart** y **updateWeeks** a la entidad [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad de navegación **managedEBookCategories** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta).|
|Adición|beta|Se han agregado las propiedades de navegación **androidManagedStoreAccountEnterpriseSettings**, **androidManagedStoreAppConfigurationSchemas**, **androidDeviceOwnerEnrollmentProfiles**, **dataSharingConsents** y **deviceConfigurationUserStateSummaries** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta).|
|Eliminación|beta|Se ha quitado la propiedad de navegación **deviceSetupConfigurations** de la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta).|
|Eliminación|beta|Se ha quitado la propiedad de navegación **groupAssignments** de la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad de navegación **categories** a la entidad [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad de navegación **containedApps** a la entidad [microsoftStoreForBusinessApp](/graph/api/resources/intune-apps-microsoftstoreforbusinessapp?view=graph-rest-beta).|
|Adición|beta|Se ha agregado la propiedad de navegación **containedApps** a la entidad [mobileAppContent](/graph/api/resources/intune-apps-mobileappcontent?view=graph-rest-beta).|
|Adición|beta|Se agregó la propiedad de navegación **committedContainedApps** a la entidad [windowsUniversalAppX](/graph/api/resources/intune-apps-windowsuniversalappx?view=graph-rest-beta).|

### <a name="onedrive"></a>OneDrive
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Se agregaron nuevas entidades:<br/>[baseItemVersion](/graph/api/resources/baseitemversion?view=graph-rest-1.0)<br/>[driveItemVersion](/graph/api/resources/driveitemversion?view=graph-rest-1.0)<br/>[listItemVersion](/graph/api/resources/listitemversion?view=graph-rest-1.0)<br/> |
|Adición|v1.0|Se agregaron nuevos tipos complejos:<br/>[publicationFacet](/graph/api/resources/publicationfacet?view=graph-rest-1.0)<br/> |
|Adición|v1.0|Se agregó la propiedad <b>publication</b> a la entidad [driveItem](/graph/api/resources/driveitem?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la propiedad de navegación <b>versions</b> a la entidad [driveItem](/graph/api/resources/driveitem?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la propiedad de navegación <b>versions</b> a la entidad [listItem](/graph/api/resources/listitem?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la propiedad <b>root</b> a la entidad [siteCollection](/graph/api/resources/sitecollection?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [restoreVersion](/graph/api/driveitemversion-restore?view=graph-rest-1.0) a la entidad [driveItemVersion](/graph/api/resources/driveitemversion?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [restoreVersion](/graph/api/listitemversion-restore?view=graph-rest-1.0) a la entidad [listItemVersion](/graph/api/resources/listitemversion?view=graph-rest-1.0). |


### <a name="onedrive"></a>OneDrive
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|beta|Se agregó un nuevo tipo complejo:<br/>[itemPreviewInfo](/graph/api/resources/itempreviewinfo?view=graph-rest-beta)<br/> |
|Adición|beta|Se agregó la propiedad <b>name</b> al tipo complejo [contentTypeInfo](/graph/api/resources/contenttypeinfo?view=graph-rest-beta). |
|Adición|beta|Se agregó la propiedad <b>objectType</b> al tipo complejo [deleteAction](/graph/api/resources/deleteaction?view=graph-rest-beta). |
|Adición|beta|Se agregó la propiedad <b>newName</b> al tipo complejo [renameAction](/graph/api/resources/renameaction?view=graph-rest-beta). |
|Adición|beta|Se agregó la propiedad <b>tenantId</b> al tipo complejo [sharepointIds](/graph/api/resources/renameaction?view=graph-rest-beta). |
|Adición|beta|Se agregó la propiedad <b>lastRecordedDateTime</b> al tipo complejo [itemActivityTimeSet](/graph/api/resources/itemactivitytimeset?view=graph-rest-beta). |
|Adición|beta|Se agregó la acción [preview](/graph/api/driveitem-preview?view=graph-rest-beta) a la entidad [driveItem](/graph/api/resources/driveitem?view=graph-rest-beta). |


## <a name="february-2018"></a>Febrero de 2018

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|beta|Se agregaron nuevas entidades:<br/>[androidForWorkImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile?view=graph-rest-beta)<br/>[androidImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-androidimportedpfxcertificateprofile?view=graph-rest-beta)<br/>[importedWindowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentity?view=graph-rest-beta)<br/>[iosImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-iosimportedpfxcertificateprofile?view=graph-rest-beta)<br/>[windows10ImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-windows10importedpfxcertificateprofile?view=graph-rest-beta)<br/>[windows10KioskConfiguration](/graph/api/resources/intune-deviceconfig-windows10kioskconfiguration?view=graph-rest-beta)<br/>[windowsPhone81ImportedPFXCertificateProfile](/graph/api/resources/intune-deviceconfig-windowsphone81importedpfxcertificateprofile?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregaron nuevos tipos complejos:<br/>[importedWindowsAutopilotDeviceIdentityState](/graph/api/resources/intune-enrollment-importedwindowsautopilotdeviceidentitystate?view=graph-rest-beta)<br/>|
|Adición|beta|Se agregó la función [managedDeviceEnrollmentFailureDetails](/graph/api/intune-troubleshooting-reportroot-manageddeviceenrollmentfailuredetails?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta). |
|Adición|beta|Se agregó la función [managedDeviceEnrollmentFailureDetails](/graph/api/intune-troubleshooting-reportroot-manageddeviceenrollmentfailuredetails?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta). |
|Adición|beta|Se agregó la función [managedDeviceEnrollmentFailureTrends](/graph/api/intune-troubleshooting-reportroot-manageddeviceenrollmentfailuretrends?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta). |
|Adición|beta|Se agregó la función [managedDeviceEnrollmentTopFailures](/graph/api/intune-troubleshooting-reportroot-manageddeviceenrollmenttopfailures?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta). |
|Adición|beta|Se agregó la función [managedDeviceEnrollmentTopFailures](/graph/api/intune-troubleshooting-reportroot-manageddeviceenrollmenttopfailures?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta). |
|Cambio|beta|Se agregaron las propiedades **requireAppVerify**, **requireSafetyNetAttestationBasicIntegrity**, **requireSafetyNetAttestationCertifiedDevice**, **requireGooglePlayServices**, **requireUpToDateSecurityProviders** y **requireCompanyPortalAppIntegrity** a la entidad [androidCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidcompliancepolicy?view=graph-rest-beta).|
|Cambio|beta|Se agregaron las propiedades **requireAppVerify**, **requireSafetyNetAttestationBasicIntegrity**, **requireSafetyNetAttestationCertifiedDevice**, **requireGooglePlayServices**, **requireUpToDateSecurityProviders** y **requireCompanyPortalAppIntegrity** a la entidad [androidForWorkCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidforworkcompliancepolicy?view=graph-rest-beta).|
|Cambio|beta|Se quitaron las propiedades **name**, **modifiedDateTime**, **totalEnrollmentCount** y **qrCode** de la entidad [androidForWorkEnrollmentProfile](/graph/api/resources/intune-androidforwork-androidforworkenrollmentprofile?view=graph-rest-beta).|
|Cambio|beta|Se quitaron las propiedades **nonEapAuthenticationMethodForEapTtls**, **nonEapAuthenticationMethodForPeap** y **enableOuterIdentityPrivacy** de la entidad [androidForWorkEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkenterprisewificonfiguration?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **workProfileBlockAddingAccounts** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta).|
|Cambio|beta|Se agregaron las propiedades **blockCrossProfileCopyPaste** y **requireAppVerify** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **deviceOwnerManagementEnabled** a la entidad [androidForWorkSettings](/graph/api/resources/intune-androidforwork-androidforworksettings?view=graph-rest-beta).|
|Cambio|beta|Se quitó la propiedad **requireAppVerify** de la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **exemptedAppPackages** a la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta).|
|Cambio|beta|Se agregan las propiedades **exemptedAppProtocols** y **exemptedAppPackages** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **exemptedAppProtocols** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **lastLoggedOnUserId** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **isFrameworkFile** a la entidad [mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **targetedAppManagementLevels** a la entidad [targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-beta).|
|Cambio|beta|Se agregan las propiedades **localSecurityOptionsBlockMicrosoftAccounts**, **localSecurityOptionsEnableAdministratorAccount**, **defenderPreventCredentialStealingType**, **defenderProcessCreationType**, **defenderUntrustedUSBProcessType**, **defenderUntrustedExecutableType**, **defenderPasswordProtectedEmailContentExecutionType**, **defenderAdvancedRansomewareProtectionType** y **applicationGuardAllowFileSaveOnHost** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta).|
|Cambio|beta|Se agregan las propiedades **edgeFavoritesListLocation** y **edgeBlockEditFavorites** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta).|
|Cambio|beta|Se agregan las propiedades **printerNames**, **defaultPrinterName** y **blockAddingNewPrinter** a la entidad [windows10SecureAssessmentConfiguration](/graph/api/resources/intune-deviceconfig-windows10secureassessmentconfiguration?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad de navegación **importedWindowsAutopilotDeviceIdentities** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta).|
|Cambio|beta|Se agregó la propiedad **shareAPNSData** al tipo complejo [adminConsent](/graph/api/resources/intune-devices-adminconsent?view=graph-rest-beta).|
|Cambio|beta|Se quitó la propiedad **collectFullIOSAppInventory** del tipo complejo [adminConsent](/graph/api/resources/intune-devices-adminconsent?view=graph-rest-beta).|
|Cambio|beta|Se quitó la propiedad **deviceUsageType** del tipo complejo [outOfBoxExperienceSettings](/graph/api/resources/intune-enrollment-outofboxexperiencesettings?view=graph-rest-beta).|


### <a name="planner-apis"></a>API de Planner

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Nuevos tipos complejos agregados:<br/>[plannerPlanContext](/graph/api/resources/plannerplancontext?view=graph-rest-beta)<br/>[plannerPlanContextDetails](/graph/api/resources/plannerplancontextdetails?view=graph-rest-beta)<br/>[plannerPlanContextCollection](/graph/api/resources/plannerplancontextcollection?view=graph-rest-beta)<br/>[plannerPlanContextDetailsCollection](/graph/api/resources/plannerplancontextdetailscollection?view=graph-rest-beta)<br/>[plannerFavoritePlanReference](/graph/api/resources/plannerfavoriteplanreference?view=graph-rest-beta)<br/>[plannerRecentPlanReference](/graph/api/resources/plannerrecentplanreference?view=graph-rest-beta)<br/>[plannerFavoritePlanReferenceCollection](/graph/api/resources/plannerfavoriteplanreferencecollection?view=graph-rest-beta)<br/>[plannerRecentPlanReferenceCollection](/graph/api/resources/plannerrecentplanreferencecollection?view=graph-rest-beta)|
|Adición|Beta|Se agregaron las propiedades `favoritePlanReferences` y `recentPlanReferences` a la entidad [plannerUser](/graph/api/resources/planneruser?view=graph-rest-beta). |
|Adición|Beta|Se agregaron las propiedades de navegación `favoritePlans` y `recentPlans` a la entidad [plannerUser](/graph/api/resources/planneruser?view=graph-rest-beta). |
|Adición|Beta|Se agregó la propiedad `contexts` a la entidad [plannerPlan](/graph/api/resources/plannerplan?view=graph-rest-beta). |
|Adición|Beta|Se agregó la propiedad `contextDetails` a la entidad [plannerPlanDetails](/graph/api/resources/plannerplandetails?view=graph-rest-beta). |
|Adición|Beta|Se agregó una [consulta delta](/graph/api/planneruser-list-delta?view=graph-rest-beta) de Planner. |

### <a name="reports-apis"></a>API de informes
| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Adición    | Beta    | Se agregó la propiedad **activatedOnSharedComputer** a la entidad [userActivationCounts](/graph/api/resources/useractivationcounts?view=graph-rest-beta).|
| Adición    | Beta    | Se agregó la propiedad **sharedComputerActivation** a la entidad [office365ActivationsUserCounts](/graph/api/resources/office365activationsusercounts?view=graph-rest-beta).|

## <a name="january-2018"></a>Enero de 2018

### <a name="json-batching"></a>Procesamiento por lotes JSON

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Se agregó compatibilidad con el [procesamiento por lotes JSON](json-batching.md). Límite de solicitudes internas establecido en 20.|
|Cambio|Beta|Se aumentó el límite de solicitudes internas del [procesamiento por lotes JSON](json-batching.md) de 5 a 20.|

### <a name="education-apis"></a>API para el ámbito educativo

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Se han agregado propiedades de navegación adicionales y se ha mejorado la compatibilidad de filtrado con [API de listas](/graph/api/resources/education-overview?view=graph-rest-beta).|

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|v1.0|Nuevas entidades agregadas:<br/>[androidCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidcompliancepolicy?view=graph-rest-1.0)<br/>[androidCustomConfiguration](/graph/api/resources/intune-deviceconfig-androidcustomconfiguration?view=graph-rest-1.0)<br/>[androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-1.0)<br/>[androidLobApp](/graph/api/resources/intune-apps-androidlobapp?view=graph-rest-1.0)<br/>[androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-1.0)<br/>[androidManagedAppRegistration](/graph/api/resources/intune-mam-androidmanagedappregistration?view=graph-rest-1.0)<br/>[androidStoreApp](/graph/api/resources/intune-apps-androidstoreapp?view=graph-rest-1.0)<br/>[appleDeviceFeaturesConfigurationBase](/graph/api/resources/intune-deviceconfig-appledevicefeaturesconfigurationbase?view=graph-rest-1.0)<br/>[applePushNotificationCertificate](/graph/api/resources/intune-devices-applepushnotificationcertificate?view=graph-rest-1.0)<br/>[defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-1.0)<br/>[detectedApp](/graph/api/resources/intune-devices-detectedapp?view=graph-rest-1.0)<br/>[deviceAndAppManagementRoleAssignment](/graph/api/resources/intune-rbac-deviceandappmanagementroleassignment?view=graph-rest-1.0)<br/>[deviceAndAppManagementRoleDefinition](/graph/api/resources/intune-rbac-deviceandappmanagementroledefinition?view=graph-rest-1.0)<br/>[deviceAppManagement](/graph/api/resources/intune-shared-deviceappmanagement?view=graph-rest-1.0)<br/>[deviceCategory](/graph/api/resources/intune-shared-devicecategory?view=graph-rest-1.0)<br/>[deviceComplianceActionItem](/graph/api/resources/intune-deviceconfig-devicecomplianceactionitem?view=graph-rest-1.0)<br/>[deviceComplianceDeviceOverview](/graph/api/resources/intune-deviceconfig-devicecompliancedeviceoverview?view=graph-rest-1.0)<br/>[deviceComplianceDeviceStatus](/graph/api/resources/intune-deviceconfig-devicecompliancedevicestatus?view=graph-rest-1.0)<br/>[deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-1.0)<br/>[deviceCompliancePolicyAssignment](/graph/api/resources/intune-deviceconfig-devicecompliancepolicyassignment?view=graph-rest-1.0)<br/>[deviceCompliancePolicyDeviceStateSummary](/graph/api/resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary?view=graph-rest-1.0)<br/>[deviceCompliancePolicySettingStateSummary](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary?view=graph-rest-1.0)<br/>[deviceCompliancePolicyState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicystate?view=graph-rest-1.0)<br/>[deviceComplianceScheduledActionForRule](/graph/api/resources/intune-deviceconfig-devicecompliancescheduledactionforrule?view=graph-rest-1.0)<br/>[deviceComplianceSettingState](/graph/api/resources/intune-deviceconfig-devicecompliancesettingstate?view=graph-rest-1.0)<br/>[deviceComplianceUserOverview](/graph/api/resources/intune-deviceconfig-devicecomplianceuseroverview?view=graph-rest-1.0)<br/>[deviceComplianceUserStatus](/graph/api/resources/intune-deviceconfig-devicecomplianceuserstatus?view=graph-rest-1.0)<br/>[deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-1.0)<br/>[deviceConfigurationAssignment](/graph/api/resources/intune-deviceconfig-deviceconfigurationassignment?view=graph-rest-1.0)<br/>[deviceConfigurationDeviceOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationdeviceoverview?view=graph-rest-1.0)<br/>[deviceConfigurationDeviceStateSummary](/graph/api/resources/intune-deviceconfig-deviceconfigurationdevicestatesummary?view=graph-rest-1.0)<br/>[deviceConfigurationDeviceStatus](/graph/api/resources/intune-deviceconfig-deviceconfigurationdevicestatus?view=graph-rest-1.0)<br/>[deviceConfigurationState](/graph/api/resources/intune-deviceconfig-deviceconfigurationstate?view=graph-rest-1.0)<br/>[deviceConfigurationUserOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationuseroverview?view=graph-rest-1.0)<br/>[deviceConfigurationUserStatus](/graph/api/resources/intune-deviceconfig-deviceconfigurationuserstatus?view=graph-rest-1.0)<br/>[deviceEnrollmentConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentconfiguration?view=graph-rest-1.0)<br/>[deviceEnrollmentLimitConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentlimitconfiguration?view=graph-rest-1.0)<br/>[deviceEnrollmentPlatformRestrictionsConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration?view=graph-rest-1.0)<br/>[deviceEnrollmentWindowsHelloForBusinessConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration?view=graph-rest-1.0)<br/>[deviceInstallState](/graph/api/resources/intune-books-deviceinstallstate?view=graph-rest-1.0)<br/>[deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-1.0)<br/>[deviceManagementExchangeConnector](/graph/api/resources/intune-onboarding-devicemanagementexchangeconnector?view=graph-rest-1.0)<br/>[deviceManagementPartner](/graph/api/resources/intune-onboarding-devicemanagementpartner?view=graph-rest-1.0)<br/>[deviceManagementTroubleshootingEvent](/graph/api/resources/intune-troubleshooting-devicemanagementtroubleshootingevent?view=graph-rest-1.0)<br/>[eBookInstallSummary](/graph/api/resources/intune-books-ebookinstallsummary?view=graph-rest-1.0)<br/>[editionUpgradeConfiguration](/graph/api/resources/intune-deviceconfig-editionupgradeconfiguration?view=graph-rest-1.0)<br/>[enrollmentConfigurationAssignment](/graph/api/resources/intune-onboarding-enrollmentconfigurationassignment?view=graph-rest-1.0)<br/>[enrollmentTroubleshootingEvent](/graph/api/resources/intune-troubleshooting-enrollmenttroubleshootingevent?view=graph-rest-1.0)<br/>[iosCertificateProfile](/graph/api/resources/intune-deviceconfig-ioscertificateprofile?view=graph-rest-1.0)<br/>[iosCompliancePolicy](/graph/api/resources/intune-deviceconfig-ioscompliancepolicy?view=graph-rest-1.0)<br/>[iosCustomConfiguration](/graph/api/resources/intune-deviceconfig-ioscustomconfiguration?view=graph-rest-1.0)<br/>[iosDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-iosdevicefeaturesconfiguration?view=graph-rest-1.0)<br/>[iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-1.0)<br/>[iosLobApp](/graph/api/resources/intune-apps-ioslobapp?view=graph-rest-1.0)<br/>[iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-1.0)<br/>[iosManagedAppRegistration](/graph/api/resources/intune-mam-iosmanagedappregistration?view=graph-rest-1.0)<br/>[iosStoreApp](/graph/api/resources/intune-apps-iosstoreapp?view=graph-rest-1.0)<br/>[iosUpdateConfiguration](/graph/api/resources/intune-deviceconfig-iosupdateconfiguration?view=graph-rest-1.0)<br/>[iosUpdateDeviceStatus](/graph/api/resources/intune-deviceconfig-iosupdatedevicestatus?view=graph-rest-1.0)<br/>[iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-1.0)<br/>[iosVppEBook](/graph/api/resources/intune-books-iosvppebook?view=graph-rest-1.0)<br/>[iosVppEBookAssignment](/graph/api/resources/intune-books-iosvppebookassignment?view=graph-rest-1.0)<br/>[localizedNotificationMessage](/graph/api/resources/intune-notification-localizednotificationmessage?view=graph-rest-1.0)<br/>[macOSCompliancePolicy](/graph/api/resources/intune-deviceconfig-macoscompliancepolicy?view=graph-rest-1.0)<br/>[macOSCustomConfiguration](/graph/api/resources/intune-deviceconfig-macoscustomconfiguration?view=graph-rest-1.0)<br/>[macOSDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-macosdevicefeaturesconfiguration?view=graph-rest-1.0)<br/>[macOSGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-macosgeneraldeviceconfiguration?view=graph-rest-1.0)<br/>[macOSOfficeSuiteApp](/graph/api/resources/intune-apps-macosofficesuiteapp?view=graph-rest-1.0)<br/>[managedAndroidLobApp](/graph/api/resources/intune-apps-managedandroidlobapp?view=graph-rest-1.0)<br/>[managedAndroidStoreApp](/graph/api/resources/intune-apps-managedandroidstoreapp?view=graph-rest-1.0)<br/>[managedApp](/graph/api/resources/intune-apps-managedapp?view=graph-rest-1.0)<br/>[managedAppConfiguration](/graph/api/resources/intune-mam-managedappconfiguration?view=graph-rest-1.0)<br/>[managedAppOperation](/graph/api/resources/intune-mam-managedappoperation?view=graph-rest-1.0)<br/>[managedAppPolicy](/graph/api/resources/intune-mam-managedapppolicy?view=graph-rest-1.0)<br/>[managedAppPolicyDeploymentSummary](/graph/api/resources/intune-mam-managedapppolicydeploymentsummary?view=graph-rest-1.0)<br/>[managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-1.0)<br/>[managedAppRegistration](/graph/api/resources/intune-mam-managedappregistration?view=graph-rest-1.0)<br/>[managedAppStatus](/graph/api/resources/intune-mam-managedappstatus?view=graph-rest-1.0)<br/>[managedAppStatusRaw](/graph/api/resources/intune-mam-managedappstatusraw?view=graph-rest-1.0)<br/>[managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0)<br/>[managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-1.0)<br/>[managedDeviceMobileAppConfigurationAssignment](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationassignment?view=graph-rest-1.0)<br/>[managedDeviceMobileAppConfigurationDeviceSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicesummary?view=graph-rest-1.0)<br/>[managedDeviceMobileAppConfigurationUserStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationuserstatus?view=graph-rest-1.0)<br/>[managedDeviceMobileAppConfigurationUserSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationusersummary?view=graph-rest-1.0)<br/>[managedDeviceOverview](/graph/api/resources/intune-devices-manageddeviceoverview?view=graph-rest-1.0)<br/>[managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-1.0)<br/>[managedEBookAssignment](/graph/api/resources/intune-books-managedebookassignment?view=graph-rest-1.0)<br/>[managedIOSLobApp](/graph/api/resources/intune-apps-managedioslobapp?view=graph-rest-1.0)<br/>[managedIOSStoreApp](/graph/api/resources/intune-apps-managediosstoreapp?view=graph-rest-1.0)<br/>[managedMobileApp](/graph/api/resources/intune-mam-managedmobileapp?view=graph-rest-1.0)<br/>[managedMobileLobApp](/graph/api/resources/intune-apps-managedmobilelobapp?view=graph-rest-1.0)<br/>[mdmWindowsInformationProtectionPolicy](/graph/api/resources/intune-mam?view=graph-rest-1.0mwindowsinformationprotectionpolicy)<br/>[microsoftStoreForBusinessApp](/graph/api/resources/intune-apps-microsoftstoreforbusinessapp?view=graph-rest-1.0)<br/>[mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-1.0)<br/>[mobileAppAssignment](/graph/api/resources/intune-apps-mobileappassignment?view=graph-rest-1.0)<br/>[mobileAppCategory](/graph/api/resources/intune-apps-mobileappcategory?view=graph-rest-1.0)<br/>[mobileAppContent](/graph/api/resources/intune-apps-mobileappcontent?view=graph-rest-1.0)<br/>[mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-1.0)<br/>[mobileLobApp](/graph/api/resources/intune-apps-mobilelobapp?view=graph-rest-1.0)<br/>[mobileThreatDefenseConnector](/graph/api/resources/intune-onboarding-mobilethreatdefenseconnector?view=graph-rest-1.0)<br/>[notificationMessageTemplate](/graph/api/resources/intune-notification-notificationmessagetemplate?view=graph-rest-1.0)<br/>[onPremisesConditionalAccessSettings](/graph/api/resources/intune-onboarding-onpremisesconditionalaccesssettings?view=graph-rest-1.0)<br/>[remoteAssistancePartner](/graph/api/resources/intune-remoteassistance-remoteassistancepartner?view=graph-rest-1.0)<br/>[resourceOperation](/graph/api/resources/intune-rbac-resourceoperation?view=graph-rest-1.0)<br/>[roleAssignment](/graph/api/resources/intune-rbac-roleassignment?view=graph-rest-1.0)<br/>[roleDefinition](/graph/api/resources/intune-rbac-roledefinition?view=graph-rest-1.0)<br/>[settingStateDeviceSummary](/graph/api/resources/intune-deviceconfig-settingstatedevicesummary?view=graph-rest-1.0)<br/>[sharedPCConfiguration](/graph/api/resources/intune-deviceconfig-sharedpcconfiguration?view=graph-rest-1.0)<br/>[softwareUpdateStatusSummary](/graph/api/resources/intune-deviceconfig-softwareupdatestatussummary?view=graph-rest-1.0)<br/>[targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-1.0)<br/>targetedManagedAppPolicyAssignment<br/>[targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-1.0)<br/>[telecomExpenseManagementPartner](/graph/api/resources/intune-tem-telecomexpensemanagementpartner?view=graph-rest-1.0)<br/>[termsAndConditions](/graph/api/resources/intune-companyterms-termsandconditions?view=graph-rest-1.0)<br/>[termsAndConditionsAcceptanceStatus](/graph/api/resources/intune-companyterms-termsandconditionsacceptancestatus?view=graph-rest-1.0)<br/>[termsAndConditionsAssignment](/graph/api/resources/intune-companyterms-termsandconditionsassignment?view=graph-rest-1.0)<br/>[userInstallStateSummary](/graph/api/resources/intune-books-userinstallstatesummary?view=graph-rest-1.0)<br/>[webApp](/graph/api/resources/intune-apps-webapp?view=graph-rest-1.0)<br/>[windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-1.0)<br/>[windows10CustomConfiguration](/graph/api/resources/intune-deviceconfig-windows10customconfiguration?view=graph-rest-1.0)<br/>[windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-1.0)<br/>[windows10EnterpriseModernAppManagementConfiguration](/graph/api/resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration?view=graph-rest-1.0)<br/>[windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-1.0)<br/>[windows10MobileCompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10mobilecompliancepolicy?view=graph-rest-1.0)<br/>[windows10SecureAssessmentConfiguration](/graph/api/resources/intune-deviceconfig-windows10secureassessmentconfiguration?view=graph-rest-1.0)<br/>[windows10TeamGeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10teamgeneralconfiguration?view=graph-rest-1.0)<br/>[windows81CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows81compliancepolicy?view=graph-rest-1.0)<br/>[windows81GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows81generalconfiguration?view=graph-rest-1.0)<br/>[windowsDefenderAdvancedThreatProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration?view=graph-rest-1.0)<br/>[windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-1.0)<br/>[windowsInformationProtectionAppLearningSummary](/graph/api/resources/intune-wip-windowsinformationprotectionapplearningsummary?view=graph-rest-1.0)<br/>[windowsInformationProtectionAppLockerFile](/graph/api/resources/intune-mam-windowsinformationprotectionapplockerfile?view=graph-rest-1.0)<br/>[windowsInformationProtectionNetworkLearningSummary](/graph/api/resources/intune-wip-windowsinformationprotectionnetworklearningsummary?view=graph-rest-1.0)<br/>[windowsInformationProtectionPolicy](/graph/api/resources/intune-mam-windowsinformationprotectionpolicy?view=graph-rest-1.0)<br/>[windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-1.0)<br/>[windowsPhone81CompliancePolicy](/graph/api/resources/intune-deviceconfig-windowsphone81compliancepolicy?view=graph-rest-1.0)<br/>[windowsPhone81CustomConfiguration](/graph/api/resources/intune-deviceconfig-windowsphone81customconfiguration?view=graph-rest-1.0)<br/>[windowsPhone81GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windowsphone81generalconfiguration?view=graph-rest-1.0)<br/>[windowsUniversalAppX](/graph/api/resources/intune-apps-windowsuniversalappx?view=graph-rest-1.0)<br/>[windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Nuevos tipos complejos agregados:<br/>[allDevicesAssignmentTarget](/graph/api/resources/intune-shared-alldevicesassignmenttarget?view=graph-rest-1.0)<br/>[allLicensedUsersAssignmentTarget](/graph/api/resources/intune-shared-alllicensedusersassignmenttarget?view=graph-rest-1.0)<br/>[androidMinimumOperatingSystem](/graph/api/resources/intune-apps-androidminimumoperatingsystem?view=graph-rest-1.0)<br/>[androidMobileAppIdentifier](/graph/api/resources/intune-mam-androidmobileappidentifier?view=graph-rest-1.0)<br/>[appListItem](/graph/api/resources/intune-deviceconfig-applistitem?view=graph-rest-1.0)<br/>[bitLockerRemovableDrivePolicy](/graph/api/resources/intune-deviceconfig-bitlockerremovabledrivepolicy?view=graph-rest-1.0)<br/>[configurationManagerClientEnabledFeatures](/graph/api/resources/intune-devices-configurationmanagerclientenabledfeatures?view=graph-rest-1.0)<br/>[defenderDetectedMalwareActions](/graph/api/resources/intune-deviceconfig-defenderdetectedmalwareactions?view=graph-rest-1.0)<br/>[deleteUserFromSharedAppleDeviceActionResult](/graph/api/resources/intune-devices-deleteuserfromsharedappledeviceactionresult?view=graph-rest-1.0)<br/>[deviceActionResult](/graph/api/resources/intune-devices-deviceactionresult?view=graph-rest-1.0)<br/>[deviceAndAppManagementAssignmentTarget](/graph/api/resources/intune-shared-deviceandappmanagementassignmenttarget?view=graph-rest-1.0)<br/>[deviceCompliancePolicySettingState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstate?view=graph-rest-1.0)<br/>[deviceConfigurationSettingState](/graph/api/resources/intune-deviceconfig-deviceconfigurationsettingstate?view=graph-rest-1.0)<br/>[deviceEnrollmentPlatformRestriction](/graph/api/resources/intune-onboarding-deviceenrollmentplatformrestriction?view=graph-rest-1.0)<br/>[deviceExchangeAccessStateSummary](/graph/api/resources/intune-devices-deviceexchangeaccessstatesummary?view=graph-rest-1.0)<br/>[deviceGeoLocation](/graph/api/resources/intune-devices-devicegeolocation?view=graph-rest-1.0)<br/>[deviceHealthAttestationState](/graph/api/resources/intune-devices-devicehealthattestationstate?view=graph-rest-1.0)<br/>[deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-1.0)<br/>[deviceOperatingSystemSummary](/graph/api/resources/intune-devices-deviceoperatingsystemsummary?view=graph-rest-1.0)<br/>[edgeSearchEngine](/graph/api/resources/intune-deviceconfig-edgesearchengine?view=graph-rest-1.0)<br/>[edgeSearchEngineBase](/graph/api/resources/intune-deviceconfig-edgesearchenginebase?view=graph-rest-1.0)<br/>[edgeSearchEngineCustom](/graph/api/resources/intune-deviceconfig-edgesearchenginecustom?view=graph-rest-1.0)<br/>[exclusionGroupAssignmentTarget](/graph/api/resources/intune-shared-exclusiongroupassignmenttarget?view=graph-rest-1.0)<br/>[fileEncryptionInfo](/graph/api/resources/intune-apps-fileencryptioninfo?view=graph-rest-1.0)<br/>[groupAssignmentTarget](/graph/api/resources/intune-shared-groupassignmenttarget?view=graph-rest-1.0)<br/>[intuneBrand](/graph/api/resources/intune-onboarding-intunebrand?view=graph-rest-1.0)<br/>[iosDeviceType](/graph/api/resources/intune-apps-iosdevicetype?view=graph-rest-1.0)<br/>[iosHomeScreenApp](/graph/api/resources/intune-deviceconfig-ioshomescreenapp?view=graph-rest-1.0)<br/>[iosHomeScreenFolder](/graph/api/resources/intune-deviceconfig-ioshomescreenfolder?view=graph-rest-1.0)<br/>[iosHomeScreenFolderPage](/graph/api/resources/intune-deviceconfig-ioshomescreenfolderpage?view=graph-rest-1.0)<br/>[iosHomeScreenItem](/graph/api/resources/intune-deviceconfig-ioshomescreenitem?view=graph-rest-1.0)<br/>[iosHomeScreenPage](/graph/api/resources/intune-deviceconfig-ioshomescreenpage?view=graph-rest-1.0)<br/>[iosLobAppAssignmentSettings](/graph/api/resources/intune-apps-ioslobappassignmentsettings?view=graph-rest-1.0)<br/>[iosMinimumOperatingSystem](/graph/api/resources/intune-apps-iosminimumoperatingsystem?view=graph-rest-1.0)<br/>[iosMobileAppIdentifier](/graph/api/resources/intune-mam-iosmobileappidentifier?view=graph-rest-1.0)<br/>[iosNetworkUsageRule](/graph/api/resources/intune-deviceconfig-iosnetworkusagerule?view=graph-rest-1.0)<br/>[iosNotificationSettings](/graph/api/resources/intune-deviceconfig-iosnotificationsettings?view=graph-rest-1.0)<br/>[iosStoreAppAssignmentSettings](/graph/api/resources/intune-apps-iosstoreappassignmentsettings?view=graph-rest-1.0)<br/>[iosVppAppAssignmentSettings](/graph/api/resources/intune-apps-iosvppappassignmentsettings?view=graph-rest-1.0)<br/>[ipRange](/graph/api/resources/intune-mam-iprange?view=graph-rest-1.0)<br/>[iPv4Range](/graph/api/resources/intune-mam-ipv4range?view=graph-rest-1.0)<br/>[iPv6Range](/graph/api/resources/intune-mam-ipv6range?view=graph-rest-1.0)<br/>[keyValuePair](/graph/api/resources/intune-androidforwork-keyvaluepair?view=graph-rest-1.0)<br/>[locateDeviceActionResult](/graph/api/resources/intune-devices-locatedeviceactionresult?view=graph-rest-1.0)<br/>[managedAppDiagnosticStatus](/graph/api/resources/intune-mam-managedappdiagnosticstatus?view=graph-rest-1.0)<br/>[managedAppPolicyDeploymentSummaryPerApp](/graph/api/resources/intune-mam-managedapppolicydeploymentsummaryperapp?view=graph-rest-1.0)<br/>[mediaContentRatingAustralia](/graph/api/resources/intune-deviceconfig-mediacontentratingaustralia?view=graph-rest-1.0)<br/>[mediaContentRatingCanada](/graph/api/resources/intune-deviceconfig-mediacontentratingcanada?view=graph-rest-1.0)<br/>[mediaContentRatingFrance](/graph/api/resources/intune-deviceconfig-mediacontentratingfrance?view=graph-rest-1.0)<br/>[mediaContentRatingGermany](/graph/api/resources/intune-deviceconfig-mediacontentratinggermany?view=graph-rest-1.0)<br/>[mediaContentRatingIreland](/graph/api/resources/intune-deviceconfig-mediacontentratingireland?view=graph-rest-1.0)<br/>[mediaContentRatingJapan](/graph/api/resources/intune-deviceconfig-mediacontentratingjapan?view=graph-rest-1.0)<br/>[mediaContentRatingNewZealand](/graph/api/resources/intune-deviceconfig-mediacontentratingnewzealand?view=graph-rest-1.0)<br/>[mediaContentRatingUnitedKingdom](/graph/api/resources/intune-deviceconfig-mediacontentratingunitedkingdom?view=graph-rest-1.0)<br/>[mediaContentRatingUnitedStates](/graph/api/resources/intune-deviceconfig-mediacontentratingunitedstates?view=graph-rest-1.0)<br/>[microsoftStoreForBusinessAppAssignmentSettings](/graph/api/resources/intune-apps-microsoftstoreforbusinessappassignmentsettings?view=graph-rest-1.0)<br/>[mimeContent](/graph/api/resources/intune-shared-mimecontent?view=graph-rest-1.0)<br/>[mobileAppAssignmentSettings](/graph/api/resources/intune-apps-mobileappassignmentsettings?view=graph-rest-1.0)<br/>[mobileAppIdentifier](/graph/api/resources/intune-mam-mobileappidentifier?view=graph-rest-1.0)<br/>[omaSetting](/graph/api/resources/intune-deviceconfig-omasetting?view=graph-rest-1.0)<br/>[omaSettingBase64](/graph/api/resources/intune-deviceconfig-omasettingbase64?view=graph-rest-1.0)<br/>[omaSettingBoolean](/graph/api/resources/intune-deviceconfig-omasettingboolean?view=graph-rest-1.0)<br/>[omaSettingDateTime](/graph/api/resources/intune-deviceconfig-omasettingdatetime?view=graph-rest-1.0)<br/>[omaSettingFloatingPoint](/graph/api/resources/intune-deviceconfig-omasettingfloatingpoint?view=graph-rest-1.0)<br/>[omaSettingInteger](/graph/api/resources/intune-deviceconfig-omasettinginteger?view=graph-rest-1.0)<br/>[omaSettingString](/graph/api/resources/intune-deviceconfig-omasettingstring?view=graph-rest-1.0)<br/>[omaSettingStringXml](/graph/api/resources/intune-deviceconfig-omasettingstringxml?view=graph-rest-1.0)<br/>[proxiedDomain](/graph/api/resources/intune-mam-proxieddomain?view=graph-rest-1.0)<br/>[remoteLockActionResult](/graph/api/resources/intune-devices-remotelockactionresult?view=graph-rest-1.0)<br/>[resetPasscodeActionResult](/graph/api/resources/intune-devices-resetpasscodeactionresult?view=graph-rest-1.0)<br/>[resourceAction](/graph/api/resources/intune-rbac-resourceaction?view=graph-rest-1.0)<br/>[rgbColor](/graph/api/resources/intune-onboarding-rgbcolor?view=graph-rest-1.0)<br/>[rolePermission](/graph/api/resources/intune-rbac-rolepermission?view=graph-rest-1.0)<br/>[settingSource](/graph/api/resources/intune-deviceconfig-settingsource?view=graph-rest-1.0)<br/>[sharedPCAccountManagerPolicy](/graph/api/resources/intune-deviceconfig-sharedpcaccountmanagerpolicy?view=graph-rest-1.0)<br/>[updateWindowsDeviceAccountActionParameter](/graph/api/resources/intune-devices-updatewindowsdeviceaccountactionparameter?view=graph-rest-1.0)<br/>[vppLicensingType](/graph/api/resources/intune-apps-vpplicensingtype?view=graph-rest-1.0)<br/>[windows10NetworkProxyServer](/graph/api/resources/intune-deviceconfig-windows10networkproxyserver?view=graph-rest-1.0)<br/>[windowsDefenderScanActionResult](/graph/api/resources/intune-devices-windowsdefenderscanactionresult?view=graph-rest-1.0)<br/>[windowsDeviceAccount](/graph/api/resources/intune-devices-windowsdeviceaccount?view=graph-rest-1.0)<br/>[windowsDeviceADAccount](/graph/api/resources/intune-devices-windowsdeviceadaccount?view=graph-rest-1.0)<br/>[windowsDeviceAzureADAccount](/graph/api/resources/intune-devices-windowsdeviceazureadaccount?view=graph-rest-1.0)<br/>[windowsFirewallNetworkProfile](/graph/api/resources/intune-deviceconfig-windowsfirewallnetworkprofile?view=graph-rest-1.0)<br/>[windowsInformationProtectionApp](/graph/api/resources/intune-mam-windowsinformationprotectionapp?view=graph-rest-1.0)<br/>[windowsInformationProtectionDataRecoveryCertificate](/graph/api/resources/intune-mam-windowsinformationprotectiondatarecoverycertificate?view=graph-rest-1.0)<br/>[windowsInformationProtectionDesktopApp](/graph/api/resources/intune-mam-windowsinformationprotectiondesktopapp?view=graph-rest-1.0)<br/>[windowsInformationProtectionIPRangeCollection](/graph/api/resources/intune-mam-windowsinformationprotectioniprangecollection?view=graph-rest-1.0)<br/>[windowsInformationProtectionProxiedDomainCollection](/graph/api/resources/intune-mam-windowsinformationprotectionproxieddomaincollection?view=graph-rest-1.0)<br/>[windowsInformationProtectionResourceCollection](/graph/api/resources/intune-mam-windowsinformationprotectionresourcecollection?view=graph-rest-1.0)<br/>[windowsInformationProtectionStoreApp](/graph/api/resources/intune-mam-windowsinformationprotectionstoreapp?view=graph-rest-1.0)<br/>[windowsMinimumOperatingSystem](/graph/api/resources/intune-apps-windowsminimumoperatingsystem?view=graph-rest-1.0)<br/>[windowsUpdateActiveHoursInstall](/graph/api/resources/intune-deviceconfig-windowsupdateactivehoursinstall?view=graph-rest-1.0)<br/>[windowsUpdateInstallScheduleType](/graph/api/resources/intune-deviceconfig-windowsupdateinstallscheduletype?view=graph-rest-1.0)<br/>[windowsUpdateScheduledInstall](/graph/api/resources/intune-deviceconfig-windowsupdatescheduledinstall?view=graph-rest-1.0)<br/>|
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-apps-mobileapp-assign?view=graph-rest-1.0) a [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [commit](/graph/api/intune-apps-mobileappcontentfile-commit?view=graph-rest-1.0) a [mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [renewUpload](/graph/api/intune-apps-mobileappcontentfile-renewupload?view=graph-rest-1.0) a [mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [retire](/graph/api/intune-devices-manageddevice-retire?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [wipe](/graph/api/intune-devices-manageddevice-wipe?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [resetPasscode](/graph/api/intune-devices-manageddevice-resetpasscode?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [remoteLock](/graph/api/intune-devices-manageddevice-remotelock?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [requestRemoteAssistance](/graph/api/intune-devices-manageddevice-requestremoteassistance?view=graph-rest-1.0) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [disableLostMode](/graph/api/intune-devices-manageddevice-disablelostmode?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [locateDevice](/graph/api/intune-devices-manageddevice-locatedevice?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [bypassActivationLock](/graph/api/intune-devices-manageddevice-bypassactivationlock?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [rebootNow](/graph/api/intune-devices-manageddevice-rebootnow?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [shutDown](/graph/api/intune-devices-manageddevice-shutdown?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [recoverPasscode](/graph/api/intune-devices-manageddevice-recoverpasscode?view=graph-rest-1.0) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [cleanWindowsDevice](/graph/api/intune-devices-manageddevice-cleanwindowsdevice?view=graph-rest-1.0) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [logoutSharedAppleDeviceActiveUser](/graph/api/intune-devices-manageddevice-logoutsharedappledeviceactiveuser?view=graph-rest-1.0) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [deleteUserFromSharedAppleDevice](/graph/api/intune-devices-manageddevice-deleteuserfromsharedappledevice?view=graph-rest-1.0) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [syncDevice](/graph/api/intune-devices-manageddevice-syncdevice?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [windowsDefenderScan](/graph/api/intune-devices-manageddevice-windowsdefenderscan?view=graph-rest-1.0) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [windowsDefenderUpdateSignatures](/graph/api/intune-devices-manageddevice-windowsdefenderupdatesignatures?view=graph-rest-1.0) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [updateWindowsDeviceAccount](/graph/api/intune-devices-manageddevice-updatewindowsdeviceaccount?view=graph-rest-1.0) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [removeAllDevicesFromManagement](/graph/api/intune-devices-user-removealldevicesfrommanagement?view=graph-rest-1.0) a [user](/graph/api/resources/intune-shared-user?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-deviceconfig-deviceconfiguration-assign?view=graph-rest-1.0) a [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-deviceconfig-devicecompliancepolicy-assign?view=graph-rest-1.0) a [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [scheduleActionsForRules](/graph/api/intune-deviceconfig-devicecompliancepolicy-scheduleactionsforrules?view=graph-rest-1.0) a [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [setMobileDeviceManagementAuthority](/graph/api/intune-onboarding-organization-setmobiledevicemanagementauthority?view=graph-rest-1.0) a [organization](/graph/api/resources/intune-onboarding-organization?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [syncMicrosoftStoreForBusinessApps](/graph/api/intune-onboarding-deviceappmanagement-syncmicrosoftstoreforbusinessapps?view=graph-rest-1.0) a [deviceAppManagement](/graph/api/resources/intune-shared-deviceappmanagement?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [sync](/graph/api/intune-onboarding-devicemanagementexchangeconnector-sync?view=graph-rest-1.0) a [deviceManagementExchangeConnector](/graph/api/resources/intune-onboarding-devicemanagementexchangeconnector?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [setPriority](/graph/api/intune-onboarding-deviceenrollmentconfiguration-setpriority?view=graph-rest-1.0) en [deviceEnrollmentConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentconfiguration?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [asignar](/graph/api/intune-onboarding-deviceenrollmentconfiguration-assign?view=graph-rest-1.0) en [deviceEnrollmentConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentconfiguration?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-mam-targetedmanagedappprotection-assign?view=graph-rest-1.0) a [targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-mam-targetedmanagedappconfiguration-assign?view=graph-rest-1.0) a [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-mam-windowsinformationprotection-assign?view=graph-rest-1.0) a [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [targetApps](/graph/api/intune-mam-managedapppolicy-targetapps?view=graph-rest-1.0) a [managedAppPolicy](/graph/api/resources/intune-mam-managedapppolicy?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [targetApps](/graph/api/intune-mam-managedappprotection-targetapps?view=graph-rest-1.0) a [managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [targetApps](/graph/api/intune-mam-targetedmanagedappconfiguration-targetapps?view=graph-rest-1.0) a [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [wipeManagedAppRegistrationsByDeviceTag](/graph/api/intune-mam-user-wipemanagedappregistrationsbydevicetag?view=graph-rest-1.0) a [user](/graph/api/resources/intune-shared-user?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [sendTestMessage](/graph/api/intune-notification-notificationmessagetemplate-sendtestmessage?view=graph-rest-1.0) a [notificationMessageTemplate](/graph/api/resources/intune-notification-notificationmessagetemplate?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la acción [assign](/graph/api/intune-books-managedebook-assign?view=graph-rest-1.0) a [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [beginOnboarding](/graph/api/intune-remoteassistance-remoteassistancepartner-beginonboarding?view=graph-rest-1.0) a [remoteAssistancePartner](/graph/api/resources/intune-remoteassistance-remoteassistancepartner?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la acción [disconnect](/graph/api/intune-remoteassistance-remoteassistancepartner-disconnect?view=graph-rest-1.0) a [remoteAssistancePartner](/graph/api/resources/intune-remoteassistance-remoteassistancepartner?view=graph-rest-1.0). |
|Adición|v1.0|Se agregó la función [downloadApplePushNotificationCertificateSigningRequest](/graph/api/intune-devices-applepushnotificationcertificate-downloadapplepushnotificationcertificatesigningrequest?view=graph-rest-1.0) en [applePushNotificationCertificate](/graph/api/resources/intune-devices-applepushnotificationcertificate?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la función [deviceConfigurationUserActivity](/graph/api/intune-deviceconfig-reportroot-deviceconfigurationuseractivity?view=graph-rest-1.0) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la función [deviceConfigurationDeviceActivity](/graph/api/intune-deviceconfig-reportroot-deviceconfigurationdeviceactivity?view=graph-rest-1.0) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la función [verifyWindowsEnrollmentAutoDiscovery](/graph/api/intune-onboarding-devicemanagement-verifywindowsenrollmentautodiscovery?view=graph-rest-1.0) en [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la función **getUserIdsWithFlaggedAppRegistration** a la colección [managedAppRegistration](/graph/api/resources/intune-mam-managedappregistration?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la función [getManagedAppDiagnosticStatuses](/graph/api/intune-mam-user-getmanagedappdiagnosticstatuses?view=graph-rest-1.0) a [user](/graph/api/resources/intune-shared-user?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la función [getManagedAppPolicies](/graph/api/intune-mam-user-getmanagedapppolicies?view=graph-rest-1.0) a [user](/graph/api/resources/intune-shared-user?view=graph-rest-1.0) |
|Adición|v1.0|Se agregó la función [getEffectivePermissions](/graph/api/intune-rbac-devicemanagement-geteffectivepermissions?view=graph-rest-1.0) en [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-1.0). |
|Cambio|v1.0|Se agregó la propiedad **mobileDeviceManagementAuthority** a la entidad [organization](/graph/api/resources/intune-onboarding-organization?view=graph-rest-1.0)|
|Cambio|v1.0|Se agregó la propiedad **deviceEnrollmentLimit** a la entidad [user](/graph/api/resources/intune-shared-user?view=graph-rest-1.0)|
|Cambio|v1.0|Se agregaron las propiedades de navegación **managedDevices**, **managedAppRegistrations** y **deviceManagementTroubleshootingEvents** a la entidad [user](/graph/api/resources/intune-shared-user?view=graph-rest-1.0)|
|||
|Adición|Beta|Nuevas entidades agregadas:<br/>[deviceManagementScriptAssignment](/graph/api/resources/intune-devices-devicemanagementscriptassignment?view=graph-rest-beta)<br/>[iosCertificateProfile](/graph/api/resources/intune-deviceconfig-ioscertificateprofile?view=graph-rest-beta)<br/>[windowsInformationProtectionNetworkLearningSummary](/graph/api/resources/intune-wip-windowsinformationprotectionnetworklearningsummary?view=graph-rest-beta)<br/>|
|Adición|Beta|Nuevos tipos complejos agregados:<br/>[revokeAppleVppLicensesActionResult](/graph/api/resources/intune-devices-revokeapplevpplicensesactionresult?view=graph-rest-beta)<br/>[vppTokenRevokeLicensesActionResult](/graph/api/resources/intune-onboarding-vpptokenrevokelicensesactionresult?view=graph-rest-beta)<br/>|
|Adición|Beta|Se agregó la acción [revokeToken](/graph/api/intune-androidforwork-androidforworkenrollmentprofile-revoketoken?view=graph-rest-beta) a [androidForWorkEnrollmentProfile](/graph/api/resources/intune-androidforwork-androidforworkenrollmentprofile?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-apps-mobileapp-assign?view=graph-rest-beta) a [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-devices-devicemanagementscript-assign?view=graph-rest-beta) en [deviceManagementScript](/graph/api/resources/intune-devices-devicemanagementscript?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [revokeAppleVppLicenses](/graph/api/intune-devices-manageddevice-revokeapplevpplicenses?view=graph-rest-beta) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-deviceconfig-devicecompliancepolicy-assign?view=graph-rest-beta) a [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [revokeLicenses](/graph/api/intune-onboarding-vpptoken-revokelicenses?view=graph-rest-beta) a [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [wipeManagedAppRegistrationsByDeviceTag](/graph/api/intune-mam-user-wipemanagedappregistrationsbydevicetag?view=graph-rest-beta) a [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta) |
|Adición|Beta|Se ha agregado la acción [assign](/graph/api/intune-books-managedebook-assign?view=graph-rest-beta) a [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta). |
|Adición|Beta|Se agregó la función [getEffectiveDeviceEnrollmentConfigurations](/graph/api/intune-onboarding-user-geteffectivedeviceenrollmentconfigurations?view=graph-rest-beta) a [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta) |
|Eliminación|Beta|Se quitaron las entidades siguientes:<br/>**appReportingOverviewStatus**<br/>**complianceSettingStateSummary**<br/>**deviceConfigurationUserStateSummary**<br/>**eBookGroupAssignment**<br/>**eBookVppGroupAssignment**<br/>**mobileAppGroupAssignment**<br/>**mobileAppVppGroupAssignment**<br/>|
|Eliminación|Beta|Se quitaron los tipos complejos siguientes:<br/>**androidForWorkAppConfigurationExample**<br/>**androidForWorkAppConfigurationExampleJson**<br/>**appInstallationFailure**<br/>**appsComplianceListItem**<br/>**defaultDeviceEnrollmentRestrictions**<br/>**defaultDeviceEnrollmentWindowsHelloForBusinessSettings**<br/>**deviceEnrollmentPlatformRestrictions**<br/>|
|Cambio|Beta|Se agregaron las propiedades **securityRequireVerifyApps**, **securityRequireSafetyNetAttestationBasicIntegrity**, **securityRequireSafetyNetAttestationCertifiedDevice**, ** securityRequireGooglePlayServices**, **securityRequireUpToDateSecurityProviders** y **securityRequireCompanyPortalAppIntegrity** a la entidad [androidCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidcompliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **packageId** a la entidad [androidForWorkApp](/graph/api/resources/intune-apps-androidforworkapp?view=graph-rest-beta)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [androidForWorkAppConfigurationSchema](/graph/api/resources/intune-androidforwork-androidforworkappconfigurationschema?view=graph-rest-beta):<br/>**exampleJson** de [androidForWorkAppConfigurationExample](/graph/api/resources/intune-androidforwork-androidforworkappconfigurationexample?view=graph-rest-beta) a Binario.<br/>|
|Cambio|Beta|Se agregaron las propiedades **securityRequireVerifyApps**, **securityRequireSafetyNetAttestationBasicIntegrity**, **securityRequireSafetyNetAttestationCertifiedDevice**, ** securityRequireGooglePlayServices**, **securityRequireUpToDateSecurityProviders** y **securityRequireCompanyPortalAppIntegrity** a la entidad [androidForWorkCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidforworkcompliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **displayName**, **lastModifiedDateTime**, **enrolledDeviceCount**, **qrCodeContent** y ** qrCodeImage** a la entidad [androidForWorkEnrollmentProfile](/graph/api/resources/intune-androidforwork-androidforworkenrollmentprofile?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **isTokenActive** de la entidad [androidForWorkEnrollmentProfile](/graph/api/resources/intune-androidforwork-androidforworkenrollmentprofile?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **innerAuthenticationProtocolForEapTtls**, **innerAuthenticationProtocolForPeap** y **outerIdentityPrivacyTemporaryValue** a la entidad [androidForWorkEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkenterprisewificonfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **workProfileBlockCrossProfileCopyPaste** y **securityRequireVerifyApps** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **securityRequireVerifyApps** a la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **packageId** e **identityVersion** a la entidad [androidLobApp](/graph/api/resources/intune-apps-androidlobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **packageId** a la entidad [androidStoreApp](/graph/api/resources/intune-apps-androidstoreapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **faceIdBlocked** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **members** a la entidad [deviceAndAppManagementRoleAssignment](/graph/api/resources/intune-rbac-deviceandappmanagementroleassignment?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **macOSRestriction** a la entidad [deviceEnrollmentPlatformRestrictionsConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **whenPartnerDevicesWillBeRemovedDateTime** y **whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime** a la entidad [deviceManagementPartner](/graph/api/resources/intune-onboarding-devicemanagementpartner?view=graph-rest-beta)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [deviceManagementScript](/graph/api/resources/intune-devices-devicemanagementscript?view=graph-rest-beta):<br/>**scriptContent** de cadena a Binario.<br/>|
|Cambio|Beta|Se agregó la propiedad **smimeEnablePerMessageSwitch** a la entidad [iosEasEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-ioseasemailprofileconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **identityVersion** a la entidad [iosLobApp](/graph/api/resources/intune-apps-ioslobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **faceIdBlocked** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **packageId** e **identityVersion** a la entidad [managedAndroidLobApp](/graph/api/resources/intune-apps-managedandroidlobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **azureADDeviceId** y **remoteAssistanceSessionErrorDetails** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **legacyAppConfiguration** de la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **identityVersion** a la entidad [managedIOSLobApp](/graph/api/resources/intune-apps-managedioslobapp?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **identityVersion** de la entidad [managedMobileLobApp](/graph/api/resources/intune-apps-managedmobilelobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **publishingState** a la entidad [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **installState** a la entidad [mobileAppInstallStatus](/graph/api/resources/intune-apps-mobileappinstallstatus?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **identityVersion** de la entidad [mobileLobApp](/graph/api/resources/intune-apps-mobilelobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **allowPartnerToCollectIOSApplicationMetadata** a la entidad [mobileThreatDefenseConnector](/graph/api/resources/intune-onboarding-mobilethreatdefenseconnector?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **members** de la entidad [roleAssignment](/graph/api/resources/intune-rbac-roleassignment?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **lastModifiedDateTime** a la entidad [termsAndConditions](/graph/api/resources/intune-companyterms-termsandconditions?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades**deviceThreatProtectionEnabled** y **deviceThreatProtectionRequiredSecurityLevel** a la entidad [windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-beta)|
|Cambio|Beta|Se eliminó la propiedad **minimumUpdateAutoInstallClassification** de la entidad [windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **privacyBlockPublishUserActivities** y **privacyBlockActivityFeed** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **configurationAccountType** a la entidad [windows10SecureAssessmentConfiguration](/graph/api/resources/intune-deviceconfig-windows10secureassessmentconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **trustedNetworkDomains** de la entidad [windows10VpnConfiguration](/graph/api/resources/intune-deviceconfig-windows10vpnconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se eliminó la propiedad **minimumUpdateAutoInstallClassification** de la entidad [windows81CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows81compliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **identityVersion** a la entidad [windowsAppX](/graph/api/resources/intune-apps-windowsappx?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **daysWithoutContactBeforeUnenroll** a la entidad [windowsInformationProtectionPolicy](/graph/api/resources/intune-mam-windowsinformationprotectionpolicy?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **identityVersion** a la entidad [windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **identityVersion** a la entidad [windowsPhone81AppX](/graph/api/resources/intune-apps-windowsphone81appx?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **identityVersion** a la entidad [windowsPhoneXAP](/graph/api/resources/intune-apps-windowsphonexap?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **identityVersion** a la entidad [windowsUniversalAppX](/graph/api/resources/intune-apps-windowsuniversalappx?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **domainJoinConfiguration** a la entidad [activeDirectoryWindowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-activedirectorywindowsautopilotdeploymentprofile?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad de navegación **notificationMessageTemplate** de la entidad [deviceComplianceActionItem](/graph/api/resources/intune-deviceconfig-devicecomplianceactionitem?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad de navegación **groupAssignments** de la entidad [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **windowsInformationProtectionNetworkLearningSummaries** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad de navegación **deviceConfigurationUserStateSummaries** de la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta).|
|Cambio|Beta|Se cambió el tipo de las siguientes propiedades en la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta):<br/>**roleAssignments** de la colección [roleAssignment](/graph/api/resources/intune-rbac-roleassignment?view=graph-rest-beta) a la colección [deviceAndAppManagementRoleAssignment](/graph/api/resources/intune-rbac-deviceandappmanagementroleassignment?view=graph-rest-beta)<br/>|
|Cambio|Beta|Se agregó la propiedad de navegación **assignments** a la entidad [deviceManagementScript](/graph/api/resources/intune-devices-devicemanagementscript?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **smimeEncryptionCertificate** a la entidad [iosEasEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-ioseasemailprofileconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [iosEasEmailProfileConfiguration](/graph/api/resources/intune-deviceconfig-ioseasemailprofileconfiguration?view=graph-rest-beta):<br/>**smimeSigningCertificate** de [iosCertificateProfileBase](/graph/api/resources/intune-deviceconfig-ioscertificateprofilebase?view=graph-rest-beta) a [iosCertificateProfile](/graph/api/resources/intune-deviceconfig-ioscertificateprofile?view=graph-rest-beta)<br/>|
|Cambio|Beta|Se quitó la propiedad de navegación **vppToken** de la entidad [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad de navegación **groupAssignments** de la entidad [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad de navegación **groupAssignments** de la entidad [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta)|
|Cambio|Beta|Se quitaron las propiedades de navegación **depOnboardingSettings** y **appleVolumePurchaseProgramTokens** de la entidad [organization](/graph/api/resources/intune-onboarding-organization?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **deviceEnrollmentConfigurations** a la entidad [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta)|
|Cambio|Beta|Se quitaron las propiedades **windowsCommercialId** y **windowsCommercialIdLastModifiedTime** del tipo complejo [deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **showDisplayNameNextToLogo** al tipo complejo [intuneBrand](/graph/api/resources/intune-onboarding-intunebrand?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **deviceUsageType** al tipo complejo [outOfBoxExperienceSettings](/graph/api/resources/intune-enrollment-outofboxexperiencesettings?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **supportsUserLicensing** y **supportsDeviceLicensing** al tipo complejo [vppLicensingType](/graph/api/resources/intune-apps-vpplicensingtype?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **actionMessage** del tipo complejo [vppTokenActionResult](/graph/api/resources/intune-onboarding-vpptokenactionresult?view=graph-rest-beta).|

### <a name="reports-apis"></a>API de informes
| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Adición    | v1.0    | Se agregaron las API siguientes:<br>[getTeamsUserActivityUserDetail](/graph/api/reportroot-getteamsuseractivityuserdetail?view=graph-rest-1.0)<br>[getTeamsUserActivityCounts](/graph/api/reportroot-getteamsuseractivitycounts?view=graph-rest-1.0)<br>[getTeamsUserActivityUserCounts](/graph/api/reportroot-getteamsuseractivityusercounts?view=graph-rest-1.0)<br>[getTeamsDeviceUsageUserDetail](/graph/api/reportroot-getteamsdeviceusageuserdetail?view=graph-rest-1.0)<br>[getTeamsDeviceUsageUserCounts](/graph/api/reportroot-getteamsdeviceusageusercounts?view=graph-rest-1.0)<br>[getTeamsDeviceUsageDistributionUserCounts](/graph/api/reportroot-getteamsdeviceusagedistributionusercounts?view=graph-rest-1.0) |

## <a name="december-2017"></a>Diciembre de 2017

### <a name="delta-query"></a>Consulta delta

| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Cambio      | v1.0    | Se agregó la función opcional de filtrado de consultas a [usuarios](/graph/api/user-delta?view=graph-rest-1.0) y [grupos](/graph/api/group-delta?view=graph-rest-1.0). |

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Se agregaron nuevas entidades:<br/>[androidForWorkEnrollmentProfile](/graph/api/resources/intune-androidforwork-androidforworkenrollmentprofile?view=graph-rest-beta)<br/>[deviceAndAppManagementRoleAssignment](/graph/api/resources/intune-rbac-deviceandappmanagementroleassignment?view=graph-rest-beta)<br/>[deviceAndAppManagementRoleDefinition](/graph/api/resources/intune-rbac-deviceandappmanagementroledefinition?view=graph-rest-beta)<br/>[macOSLobApp](/graph/api/resources/intune-apps-macoslobapp?view=graph-rest-beta)<br/>|
|Adición|Beta|Se agregaron nuevos tipos complejos:<br/>[resourceAction](/graph/api/resources/intune-rbac-resourceaction?view=graph-rest-beta)<br/>[updateWindowsDeviceAccountActionParameter](/graph/api/resources/intune-devices-updatewindowsdeviceaccountactionparameter?view=graph-rest-beta)<br/>[vppTokenActionResult](/graph/api/resources/intune-onboarding-vpptokenactionresult?view=graph-rest-beta)<br/>[windowsDeviceAADAccount](/graph/api/resources/intune-devices-windowsdeviceaadaccount?view=graph-rest-beta)<br/>[windowsDeviceAccount](/graph/api/resources/intune-devices-windowsdeviceaccount?view=graph-rest-beta)<br/>[windowsDeviceADAccount](/graph/api/resources/intune-devices-windowsdeviceadaccount?view=graph-rest-beta)<br/>|
|Adición|Beta|Se agregó la acción [revokeTokens](/graph/api/intune-androidforwork-androidforworkenrollmentprofile-revoketokens?view=graph-rest-beta) a [androidForWorkEnrollmentProfile](/graph/api/resources/intune-androidforwork-androidforworkenrollmentprofile?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [createToken](/graph/api/intune-androidforwork-androidforworkenrollmentprofile-createtoken?view=graph-rest-beta) a [androidForWorkEnrollmentProfile](/graph/api/resources/intune-androidforwork-androidforworkenrollmentprofile?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [wipe](/graph/api/intune-devices-manageddevice-wipe?view=graph-rest-beta) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [updateWindowsDeviceAccount](/graph/api/intune-devices-manageddevice-updatewindowsdeviceaccount?view=graph-rest-beta) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [revokeLicenses](/graph/api/intune-onboarding-vpptoken-revokelicenses?view=graph-rest-beta) a [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta). |
|Adición|Beta|Se agregó la función [getDevicePasscode](/graph/api/intune-deviceconfig-devicecompliancepolicy-getdevicepasscode?view=graph-rest-beta) a la colección [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta). |
|Adición|Beta|Se agregó la función [getEffectivePermissions](/graph/api/intune-rbac-devicemanagement-geteffectivepermissions?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta). |
|Eliminación|Beta|Se quitaron las entidades siguientes:<br/>**windowsStoreForBusinessApp**<br/>|
|Eliminación|Beta|Se quitaron los tipos complejos siguientes:<br/>**windowsStoreForBusinessAppAssignmentSettings**<br/>|
|Cambio|Beta|Se agregó la propiedad **dateAndTimeBlockChanges** a la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad **enableAuthenticationViaCompanyPortal** de la entidad [depEnrollmentProfile](/graph/api/resources/intune-corpenrollment-depenrollmentprofile?view=graph-rest-beta)|
|Cambio|Beta|Se quitaron las propiedades **windowsStoreForBusinessLastSuccessfulSyncDateTime**, **isEnabledForWindowsStoreForBusiness**, **windowsStoreForBusinessLanguage** y **windowsStoreForBusinessLastCompletedApplicationSyncTime** de la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **maximumDepTokens** y **intuneAccountId** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **enableAuthenticationViaCompanyPortal** a la entidad [enrollmentProfile](/graph/api/resources/intune-corpenrollment-enrollmentprofile?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **managedDeviceName** y **partnerReportedThreatState** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **installProgressDisplayLevel** a la entidad [officeSuiteApp](/graph/api/resources/intune-apps-officesuiteapp?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **resourceScopes** a la entidad [roleAssignment](/graph/api/resources/intune-rbac-roleassignment?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **rolePermissions** y **isBuiltIn** a la entidad [roleDefinition](/graph/api/resources/intune-rbac-roledefinition?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **tokenActionResults** a la entidad [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **minimumUpdateAutoInstallClassification** a la entidad [windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **defenderSecurityCenterDisableAppBrowserUI**, **defenderSecurityCenterDisableFamilyUI**, **defenderSecurityCenterDisableHealthUI**, **defenderSecurityCenterDisableNetworkUI**, **defenderSecurityCenterDisableVirusUI**, **defenderSecurityCenterOrganizationDisplayName**, **defenderSecurityCenterHelpEmail**, **defenderSecurityCenterHelpPhone**, **defenderSecurityCenterHelpURL**, **defenderSecurityCenterNotificationsFromApp**, **defenderSecurityCenterITContactDisplay** y **applicationGuardAllowVirtualGPU** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **enableAutomaticRedeployment** y **authenticationAllowFIDODevice** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **trustedNetworkDomains** a la entidad [windows10VpnConfiguration](/graph/api/resources/intune-deviceconfig-windows10vpnconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **minimumUpdateAutoInstallClassification** a la entidad [windows81CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows81compliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad de navegación **androidForWorkEnrollmentProfiles** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **healthAttestationSupportedStatus** al tipo complejo [deviceHealthAttestationState](/graph/api/resources/intune-devices-devicehealthattestationstate?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **tpmSpecificationVersion**, **operatingSystemEdition**, **deviceFullQualifiedDomainName**, **deviceGuardVirtualizationBasedSecurityHardwareRequirementState**, **deviceGuardVirtualizationBasedSecurityState** y **deviceGuardLocalSystemAuthorityCredentialGuardState** al tipo complejo [hardwareInformation](/graph/api/resources/intune-devices-hardwareinformation?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **vpnConfigurationId** al tipo complejo [iosVppAppAssignmentSettings](/graph/api/resources/intune-apps-iosvppappassignmentsettings?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **resourceActions** al tipo complejo [rolePermission](/graph/api/resources/intune-rbac-rolepermission?view=graph-rest-beta).|

### <a name="reports-apis"></a>API de informes
| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Adición    | v1.0    | Se agregaron las API siguientes:<br>[getEmailActivityUserDetail](/graph/api/reportroot-getemailactivityuserdetail?view=graph-rest-1.0)<br>[getEmailActivityCounts](/graph/api/reportroot-getemailactivitycounts?view=graph-rest-1.0)<br>[getEmailActivityUserCounts](/graph/api/reportroot-getemailactivityusercounts?view=graph-rest-1.0)<br>[getEmailAppUsageUserDetail](/graph/api/reportroot-getemailappusageuserdetail?view=graph-rest-1.0)<br>[getEmailAppUsageAppsUserCounts](/graph/api/reportroot-getemailappusageappsusercounts?view=graph-rest-1.0)<br>[getEmailAppUsageUserCounts](/graph/api/reportroot-getemailappusageusercounts?view=graph-rest-1.0)<br>[getEmailAppUsageVersionsUserCounts](/graph/api/reportroot-getemailappusageversionsusercounts?view=graph-rest-1.0)<br>[getMailboxUsageDetail](/graph/api/reportroot-getmailboxusagedetail?view=graph-rest-1.0)<br>[getMailboxUsageMailboxCounts](/graph/api/reportroot-getmailboxusagemailboxcounts?view=graph-rest-1.0)<br>[getMailboxUsageQuotaStatusMailboxCounts](/graph/api/reportroot-getmailboxusagequotastatusmailboxcounts?view=graph-rest-1.0)<br>[getMailboxUsageStorage](/graph/api/reportroot-getmailboxusagestorage?view=graph-rest-1.0)<br>[getOffice365ActivationsUserDetail](/graph/api/reportroot-getoffice365activationsuserdetail?view=graph-rest-1.0)<br>[getOffice365ActivationCounts](/graph/api/reportroot-getoffice365activationcounts?view=graph-rest-1.0)<br>[getOffice365ActivationsUserCounts](/graph/api/reportroot-getoffice365activationsusercounts?view=graph-rest-1.0)<br>[getOffice365ActiveUserDetail](/graph/api/reportroot-getoffice365activeuserdetail?view=graph-rest-1.0)<br>[getOffice365ActiveUserCounts](/graph/api/reportroot-getoffice365activeusercounts?view=graph-rest-1.0)<br>[getOffice365ServicesUserCounts](/graph/api/reportroot-getoffice365servicesusercounts?view=graph-rest-1.0)<br>[getOffice365GroupsActivityDetail](/graph/api/reportroot-getoffice365groupsactivitydetail?view=graph-rest-1.0)<br> [getOffice365GroupsActivityCounts](/graph/api/reportroot-getoffice365groupsactivitycounts?view=graph-rest-1.0)<br>[getOffice365GroupsActivityGroupCounts](/graph/api/reportroot-getoffice365groupsactivitygroupcounts?view=graph-rest-1.0)<br>[getOffice365GroupsActivityStorage](/graph/api/reportroot-getoffice365groupsactivitystorage?view=graph-rest-1.0)<br>[getOffice365GroupsActivityFileCounts](/graph/api/reportroot-getoffice365groupsactivityfilecounts?view=graph-rest-1.0)<br>[getOneDriveActivityUserDetail](/graph/api/reportroot-getonedriveactivityuserdetail?view=graph-rest-1.0)<br>[getOneDriveActivityUserCounts](/graph/api/reportroot-getonedriveactivityusercounts?view=graph-rest-1.0)<br>[getOneDriveActivityFileCounts](/graph/api/reportroot-getonedriveactivityfilecounts?view=graph-rest-1.0)<br>[getOneDriveUsageAccountDetail](/graph/api/reportroot-getonedriveusageaccountdetail?view=graph-rest-1.0)<br>[getOneDriveUsageAccountCounts](/graph/api/reportroot-getonedriveusageaccountcounts?view=graph-rest-1.0)<br>[getOneDriveUsageFileCounts](/graph/api/reportroot-getonedriveusagefilecounts?view=graph-rest-1.0)<br>[getOneDriveUsageStorage](/graph/api/reportroot-getonedriveusagestorage?view=graph-rest-1.0)<br>[getSharePointActivityUserDetail](/graph/api/reportroot-getsharepointactivityuserdetail?view=graph-rest-1.0)<br>[getSharePointActivityFileCounts](/graph/api/reportroot-getsharepointactivityfilecounts?view=graph-rest-1.0)<br>[getSharePointActivityUserCounts](/graph/api/reportroot-getsharepointactivityusercounts?view=graph-rest-1.0)<br>[getSharePointActivityPages](/graph/api/reportroot-getsharepointactivitypages?view=graph-rest-1.0)<br>[getSharePointSiteUsageDetail](/graph/api/reportroot-getsharepointsiteusagedetail?view=graph-rest-1.0)<br>[getSharePointSiteUsageFileCounts](/graph/api/reportroot-getsharepointsiteusagefilecounts?view=graph-rest-1.0)<br>[getSharePointSiteUsageSiteCounts](/graph/api/reportroot-getsharepointsiteusagesitecounts?view=graph-rest-1.0)<br>[getSharePointSiteUsageStorage](/graph/api/reportroot-getsharepointsiteusagestorage?view=graph-rest-1.0)<br>[getSharePointSiteUsagePages](/graph/api/reportroot-getsharepointsiteusagepages?view=graph-rest-1.0)<br>[getSkypeForBusinessActivityUserDetail](/graph/api/reportroot-getskypeforbusinessactivityuserdetail?view=graph-rest-1.0)<br>[getSkypeForBusinessActivityCounts](/graph/api/reportroot-getskypeforbusinessactivitycounts?view=graph-rest-1.0)<br>[getSkypeForBusinessActivityUserCounts](/graph/api/reportroot-getskypeforbusinessactivityusercounts?view=graph-rest-1.0)<br>[getSkypeForBusinessDeviceUsageUserDetail](/graph/api/reportroot-getskypeforbusinessdeviceusageuserdetail?view=graph-rest-1.0)<br>[getSkypeForBusinessDeviceUsageDistributionUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusagedistributionusercounts?view=graph-rest-1.0)<br>[getSkypeForBusinessDeviceUsageUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusageusercounts?view=graph-rest-1.0)<br>[getSkypeForBusinessOrganizerActivityCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivitycounts?view=graph-rest-1.0)<br>[getSkypeForBusinessOrganizerActivityUserCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityusercounts?view=graph-rest-1.0)<br>[getSkypeForBusinessOrganizerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityminutecounts?view=graph-rest-1.0)<br>[getSkypeForBusinessParticipantActivityCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivitycounts?view=graph-rest-1.0)<br>[getSkypeForBusinessParticipantActivityUserCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityusercounts?view=graph-rest-1.0)<br>[getSkypeForBusinessParticipantActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityminutecounts?view=graph-rest-1.0)<br>[getSkypeForBusinessPeerToPeerActivityCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivitycounts?view=graph-rest-1.0)<br>[getSkypeForBusinessPeerToPeerActivityUserCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityusercounts?view=graph-rest-1.0)<br>[getSkypeForBusinessPeerToPeerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityminutecounts?view=graph-rest-1.0)<br>[getYammerActivityUserDetail](/graph/api/reportroot-getyammeractivityuserdetail?view=graph-rest-1.0)<br>[getYammerActivityCounts](/graph/api/reportroot-getyammeractivitycounts?view=graph-rest-1.0)<br>[getYammerActivityUserCounts](/graph/api/reportroot-getyammeractivityusercounts?view=graph-rest-1.0)<br>[getYammerDeviceUsageUserDetail](/graph/api/reportroot-getyammerdeviceusageuserdetail?view=graph-rest-1.0)<br>[getYammerDeviceUsageDistributionUserCounts](/graph/api/reportroot-getyammerdeviceusagedistributionusercounts?view=graph-rest-1.0)<br>[getYammerDeviceUsageUserCounts](/graph/api/reportroot-getyammerdeviceusageusercounts?view=graph-rest-1.0)<br>[getYammerGroupsActivityDetail](/graph/api/reportroot-getyammergroupsactivitydetail?view=graph-rest-1.0)<br>[getYammerGroupsActivityGroupCounts](/graph/api/reportroot-getyammergroupsactivitygroupcounts?view=graph-rest-1.0)<br>[getYammerGroupsActivityCounts](/graph/api/reportroot-getyammergroupsactivitycounts?view=graph-rest-1.0).|
| Adición    | Beta    | Se agregaron las API siguientes:<br>[getTeamsUserActivityUserDetail](/graph/api/reportroot-getteamsuseractivityuserdetail?view=graph-rest-beta)<br>[getTeamsUserActivityCounts](/graph/api/reportroot-getteamsuseractivitycounts?view=graph-rest-beta)<br>[getTeamsUserActivityUserCounts](/graph/api/reportroot-getteamsuseractivityusercounts?view=graph-rest-beta)<br>[getTeamsDeviceUsageUserDetail](/graph/api/reportroot-getteamsdeviceusageuserdetail?view=graph-rest-beta)<br>[getTeamsDeviceUsageUserCounts](/graph/api/reportroot-getteamsdeviceusageusercounts?view=graph-rest-beta)<br>[getTeamsDeviceUsageDistributionUserCounts](/graph/api/reportroot-getteamsdeviceusagedistributionusercounts?view=graph-rest-beta) |

## <a name="november-2017"></a>Noviembre de 2017

### <a name="azure-ad-synchronization-apis"></a>API de sincronización de Azure AD

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Se agregó compatibilidad con la sincronización de identidades de Azure AD, incluidos los recursos siguientes:<br/>[Trabajo](/graph/api/resources/synchronization-synchronizationjob?view=graph-rest-beta)<br/>[Esquema](/graph/api/resources/synchronization-synchronizationschema?view=graph-rest-beta)<br/>[Plantilla](/graph/api/resources/synchronization-synchronizationtemplate?view=graph-rest-beta)<br/>Vea los temas de recursos para obtener información sobre los métodos disponibles.|

### <a name="education-apis"></a>API para el ámbito educativo

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Se agregó compatibilidad para escenarios del ámbito educativo, incluidos los recursos siguientes:<br/>[Centros educativos](/graph/api/resources/educationschool?view=graph-rest-beta)<br/>[Clases](/graph/api/resources/educationclass?view=graph-rest-beta)<br/>[Usuarios](/graph/api/resources/educationuser?view=graph-rest-beta)<br/>[Asignaciones](/graph/api/resources/educationassignment?view=graph-rest-beta)<br/>[Envíos](/graph/api/resources/educationsubmission?view=graph-rest-beta)<br/>Vea los temas de recursos para obtener información sobre los métodos disponibles.|

### <a name="microsoft-intune-apis"></a>API de Microsoft Intune
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Se agregaron nuevas entidades:<br/>[auditEvent](/graph/api/resources/intune-auditing-auditevent?view=graph-rest-beta)<br/>[deviceManagementTroubleshootingEvent](/graph/api/resources/intune-troubleshooting-devicemanagementtroubleshootingevent?view=graph-rest-beta)<br/>[deviceSetupConfiguration](/graph/api/resources/intune-deviceconfig-devicesetupconfiguration?view=graph-rest-beta)<br/>[enrollmentTroubleshootingEvent](/graph/api/resources/intune-troubleshooting-enrollmenttroubleshootingevent?view=graph-rest-beta)<br/>[macOSOfficeSuiteApp](/graph/api/resources/intune-apps-macosofficesuiteapp?view=graph-rest-beta)<br/>[microsoftStoreForBusinessApp](/graph/api/resources/intune-apps-microsoftstoreforbusinessapp?view=graph-rest-beta)<br/>[ndesConnector](/graph/api/resources/intune-deviceconfig-ndesconnector?view=graph-rest-beta)<br/>|
|Adición|Beta|Se agregaron nuevos tipos complejos:<br/>[auditActor](/graph/api/resources/intune-auditing-auditactor?view=graph-rest-beta)<br/>[auditProperty](/graph/api/resources/intune-auditing-auditproperty?view=graph-rest-beta)<br/>[auditResource](/graph/api/resources/intune-auditing-auditresource?view=graph-rest-beta)<br/>[bulkManagedDeviceActionResult](/graph/api/resources/intune-devices-bulkmanageddeviceactionresult?view=graph-rest-beta)<br/>[deviceProtectionOverview](/graph/api/resources/intune-devices-deviceprotectionoverview?view=graph-rest-beta)<br/>[microsoftStoreForBusinessAppAssignmentSettings](/graph/api/resources/intune-apps-microsoftstoreforbusinessappassignmentsettings?view=graph-rest-beta)<br/>[operatingSystemVersionRange](/graph/api/resources/intune-deviceconfig-operatingsystemversionrange?view=graph-rest-beta)<br/>[remoteLockActionResult](/graph/api/resources/intune-devices-remotelockactionresult?view=graph-rest-beta)<br/>|
|Adición|Beta|Se agregó la acción executeAction a la colección [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [wipe](/graph/api/intune-devices-manageddevice-wipe?view=graph-rest-beta) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [shutDown](/graph/api/intune-devices-manageddevice-shutdown?view=graph-rest-beta) a [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-deviceconfig-deviceconfiguration-assign?view=graph-rest-beta) a [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción [syncMicrosoftStoreForBusinessApps](/graph/api/intune-onboarding-deviceappmanagement-syncmicrosoftstoreforbusinessapps?view=graph-rest-beta) a [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción setDefaultProfile a [enrollmentProfile](/graph/api/resources/intune-corpenrollment-enrollmentprofile?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción shareForSchoolDataSyncService a [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta). |
|Adición|Beta|Se agregó la acción unshareForSchoolDataSyncService a [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta). |
|Adición|Beta|Se agregó la función getAuditCategories a la colección [auditEvent](/graph/api/resources/intune-auditing-auditevent?view=graph-rest-beta). |
|Adición|Beta|Se agregó la función getAuditActivityTypes a la colección [auditEvent](/graph/api/resources/intune-auditing-auditevent?view=graph-rest-beta). |
|Eliminación|Beta|Se quitaron las entidades siguientes:<br/>**mobileAppIdentifierDeployment**<br/>|
|Eliminación|Beta|Se quitaron los tipos complejos siguientes:<br/>**windowsInformationProtectionCloudResource**<br/>**windowsInformationProtectionCloudResourceCollection**<br/>|
|Cambio|Beta|Se cambiaron las propiedades siguientes en la entidad [androidDeviceComplianceLocalActionLockDeviceWithPasscode](/graph/api/resources/intune-deviceconfig-androiddevicecompliancelocalactionlockdevicewithpasscode?view=graph-rest-beta):<br/>**passcode**, de obligatorio a opcional.<br/>|
|Cambio|Beta|Se agregaron las propiedades **microsoftStoreForBusinessLastSuccessfulSyncDateTime**, **isEnabledForMicrosoftStoreForBusiness**, **microsoftStoreForBusinessLanguage** y **microsoftStoreForBusinessLastCompletedApplicationSyncTime** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **target** a la entidad [deviceConfigurationAssignment](/graph/api/resources/intune-deviceconfig-deviceconfigurationassignment?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **deviceProtectionOverview** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **exchangeAlias** y **exchangeOrganization** a la entidad [deviceManagementExchangeConnector](/graph/api/resources/intune-onboarding-devicemanagementexchangeconnector?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **appStoreUrl** y **minimumSupportedOperatingSystem** a la entidad [managedAndroidStoreApp](/graph/api/resources/intune-apps-managedandroidstoreapp?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **remoteAssistanceSessionErrorString** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **appStoreUrl**, **applicableDeviceType** y **minimumSupportedOperatingSystem** a la entidad [managedIOSStoreApp](/graph/api/resources/intune-apps-managediosstoreapp?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **notApplicableDeviceCount**, **pendingInstallDeviceCount**, **notApplicableUserCount** y **pendingInstallUserCount** a la entidad [mobileAppInstallSummary](/graph/api/resources/intune-apps-mobileappinstallsummary?view=graph-rest-beta).|
|Cambio|Beta|Se quitaron las propiedades **targetedSecurityGroupIds** y **targetedSecurityGroupsCount** de la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se quitaron las propiedades **targetedSecurityGroupsCount** y **targetedSecurityGroupIds** de la entidad [targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **validOperatingSystemBuildRanges** a la entidad [windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **activeFirewallRequired**, **uacRequired** y **validOperatingSystemBuildRanges** a la entidad [windows10MobileCompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10mobilecompliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **enableExpeditedTelemetryReporting** a la entidad [windowsDefenderAdvancedThreatProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se quitaron las propiedades **allowedApps**, **enterpriseCloudResources** y **targetedSecurityGroupIds** de la entidad [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **ignoreVersionDetection** a la entidad [windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad de navegación **mobileAppIdentifierDeployments** de la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad de navegación **mobileAppIdentifierDeployments** de la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad de navegación **assignments** a la entidad [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad de navegación **deviceConfiguration** de la entidad [deviceConfigurationAssignment](/graph/api/resources/intune-deviceconfig-deviceconfigurationassignment?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad de navegación **deviceConfiguration** a la entidad [deviceConfigurationGroupAssignment](/graph/api/resources/intune-deviceconfig-deviceconfigurationgroupassignment?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades de navegación **deviceSetupConfigurations**, **ndesConnectors**, **exchangeOnPremisesPolicies**, **conditionalAccessSettings**, **auditEvents** y **troubleshootingEvents** a la entidad [deviceManagement](/graph/api/resources/intune-androidforwork-devicemanagement?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad de navegación **mobileAppIdentifierDeployments** de la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta).|
|Cambio|Beta|Se ha agregado la propiedad de navegación **windowsProtectionState** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta).|
|Cambio|Beta|Se quitaron las propiedades de navegación **mobileAppIdentifierDeployments** y **targetedSecurityGroups** de la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad de navegación **targetedSecurityGroups** de la entidad [targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad de navegación **deviceManagementTroubleshootingEvents** a la entidad [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad de navegación **allowedAppLockerFiles** de la entidad [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta).|
|Cambio|Beta|Se quitó la propiedad de navegación **windowsProtectionState** de la entidad [windowsManagedDevice](/graph/api/resources/intune-devices-windowsmanageddevice?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **v11_0** al tipo complejo [iosMinimumOperatingSystem](/graph/api/resources/intune-apps-iosminimumoperatingsystem?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **denied** al tipo complejo [windowsInformationProtectionApp](/graph/api/resources/intune-mam-windowsinformationprotectionapp?view=graph-rest-beta).|

### <a name="reports-apis"></a>API de informes
| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Compatibilidad de JSON agregado con las siguientes API:<br>[getEmailActivityUserDetail](/graph/api/reportroot-getemailactivityuserdetail?view=graph-rest-beta)<br>[getEmailActivityCounts](/graph/api/reportroot-getemailactivitycounts?view=graph-rest-beta)<br>[getEmailActivityUserCounts](/graph/api/reportroot-getemailactivityusercounts?view=graph-rest-beta)<br>[getEmailAppUsageUserDetail](/graph/api/reportroot-getemailappusageuserdetail?view=graph-rest-beta)<br>[getEmailAppUsageAppsUserCounts](/graph/api/reportroot-getemailappusageappsusercounts?view=graph-rest-beta)<br>[getEmailAppUsageUserCounts](/graph/api/reportroot-getemailappusageusercounts?view=graph-rest-beta)<br>[getEmailAppUsageVersionsUserCounts](/graph/api/reportroot-getemailappusageversionsusercounts?view=graph-rest-beta)<br>[getMailboxUsageDetail](/graph/api/reportroot-getmailboxusagedetail?view=graph-rest-beta)<br>[getMailboxUsageMailboxCounts](/graph/api/reportroot-getmailboxusagemailboxcounts?view=graph-rest-beta)<br>[getMailboxUsageQuotaStatusMailboxCounts](/graph/api/reportroot-getmailboxusagequotastatusmailboxcounts?view=graph-rest-beta)<br>[getMailboxUsageStorage](/graph/api/reportroot-getmailboxusagestorage?view=graph-rest-beta)<br>[getOffice365ActivationsUserDetail](/graph/api/reportroot-getoffice365activationsuserdetail?view=graph-rest-beta)<br>[getOffice365ActivationCounts](/graph/api/reportroot-getoffice365activationcounts?view=graph-rest-beta)<br>[getOffice365ActivationsUserCounts](/graph/api/reportroot-getoffice365activationsusercounts?view=graph-rest-beta)<br>[getOffice365ActiveUserDetail](/graph/api/reportroot-getoffice365activeuserdetail?view=graph-rest-beta)<br>[getOffice365ActiveUserCounts](/graph/api/reportroot-getoffice365activeusercounts?view=graph-rest-beta)<br>[getOffice365ServicesUserCounts](/graph/api/reportroot-getoffice365servicesusercounts?view=graph-rest-beta)<br>[getOffice365GroupsActivityDetail](/graph/api/reportroot-getoffice365groupsactivitydetail?view=graph-rest-beta)<br> [getOffice365GroupsActivityCounts](/graph/api/reportroot-getoffice365groupsactivitycounts?view=graph-rest-beta)<br>[getOffice365GroupsActivityGroupCounts](/graph/api/reportroot-getoffice365groupsactivitygroupcounts?view=graph-rest-beta)<br>[getOffice365GroupsActivityStorage](/graph/api/reportroot-getoffice365groupsactivitystorage?view=graph-rest-beta)<br>[getOffice365GroupsActivityFileCounts](/graph/api/reportroot-getoffice365groupsactivityfilecounts?view=graph-rest-beta)<br>[getOneDriveActivityUserDetail](/graph/api/reportroot-getonedriveactivityuserdetail?view=graph-rest-beta)<br>[getOneDriveActivityUserCounts](/graph/api/reportroot-getonedriveactivityusercounts?view=graph-rest-beta)<br>[getOneDriveActivityFileCounts](/graph/api/reportroot-getonedriveactivityfilecounts?view=graph-rest-beta)<br>[getOneDriveUsageAccountDetail](/graph/api/reportroot-getonedriveusageaccountdetail?view=graph-rest-beta)<br>[getOneDriveUsageAccountCounts](/graph/api/reportroot-getonedriveusageaccountcounts?view=graph-rest-beta)<br>[getOneDriveUsageFileCounts](/graph/api/reportroot-getonedriveusagefilecounts?view=graph-rest-beta)<br>[getOneDriveUsageStorage](/graph/api/reportroot-getonedriveusagestorage?view=graph-rest-beta)<br>[getSharePointActivityUserDetail](/graph/api/reportroot-getsharepointactivityuserdetail?view=graph-rest-beta)<br>[getSharePointActivityFileCounts](/graph/api/reportroot-getsharepointactivityfilecounts?view=graph-rest-beta)<br>[getSharePointActivityUserCounts](/graph/api/reportroot-getsharepointactivityusercounts?view=graph-rest-beta)<br>[getSharePointActivityPages](/graph/api/reportroot-getsharepointactivitypages?view=graph-rest-beta)<br>[getSharePointSiteUsageDetail](/graph/api/reportroot-getsharepointsiteusagedetail?view=graph-rest-beta)<br>[getSharePointSiteUsageFileCounts](/graph/api/reportroot-getsharepointsiteusagefilecounts?view=graph-rest-beta)<br>[getSharePointSiteUsageSiteCounts](/graph/api/reportroot-getsharepointsiteusagesitecounts?view=graph-rest-beta)<br>[getSharePointSiteUsageStorage](/graph/api/reportroot-getsharepointsiteusagestorage?view=graph-rest-beta)<br>[getSharePointSiteUsagePages](/graph/api/reportroot-getsharepointsiteusagepages?view=graph-rest-beta)<br>[getSkypeForBusinessActivityUserDetail](/graph/api/reportroot-getskypeforbusinessactivityuserdetail?view=graph-rest-beta)<br>[getSkypeForBusinessActivityCounts](/graph/api/reportroot-getskypeforbusinessactivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessActivityUserCounts](/graph/api/reportroot-getskypeforbusinessactivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessDeviceUsageUserDetail](/graph/api/reportroot-getskypeforbusinessdeviceusageuserdetail?view=graph-rest-beta)<br>[getSkypeForBusinessDeviceUsageDistributionUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusagedistributionusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessDeviceUsageUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusageusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessOrganizerActivityCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessOrganizerActivityUserCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessOrganizerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityminutecounts?view=graph-rest-beta)<br>[getSkypeForBusinessParticipantActivityCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessParticipantActivityUserCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessParticipantActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityminutecounts?view=graph-rest-beta)<br>[getSkypeForBusinessPeerToPeerActivityCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivitycounts?view=graph-rest-beta)<br>[getSkypeForBusinessPeerToPeerActivityUserCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityusercounts?view=graph-rest-beta)<br>[getSkypeForBusinessPeerToPeerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityminutecounts?view=graph-rest-beta)<br>[getYammerActivityUserDetail](/graph/api/reportroot-getyammeractivityuserdetail?view=graph-rest-beta)<br>[getYammerActivityCounts](/graph/api/reportroot-getyammeractivitycounts?view=graph-rest-beta)<br>[getYammerActivityUserCounts](/graph/api/reportroot-getyammeractivityusercounts?view=graph-rest-beta)<br>[getYammerDeviceUsageUserDetail](/graph/api/reportroot-getyammerdeviceusageuserdetail?view=graph-rest-beta)<br>[getYammerDeviceUsageDistributionUserCounts](/graph/api/reportroot-getyammerdeviceusagedistributionusercounts?view=graph-rest-beta)<br>[getYammerDeviceUsageUserCounts](/graph/api/reportroot-getyammerdeviceusageusercounts?view=graph-rest-beta)<br>[getYammerGroupsActivityDetail](/graph/api/reportroot-getyammergroupsactivitydetail?view=graph-rest-beta)<br>[getYammerGroupsActivityGroupCounts](/graph/api/reportroot-getyammergroupsactivitygroupcounts?view=graph-rest-beta)<br>[getYammerGroupsActivityCounts](/graph/api/reportroot-getyammergroupsactivitycounts?view=graph-rest-beta). |

### <a name="webhooks"></a>Webhooks

| Tipo de cambio | Versión | Descripción                              |
|:------------|:--------|:-----------------------------------------|
| Cambio importante | Beta y v1.0 | Para los [webhooks](/graph/api/resources/webhooks?view=graph-rest-1.0), [se redujo la duración máxima de la fecha de expiración de la suscripción](/graph/api/resources/subscription?view=graph-rest-1.0#maximum-length-of-subscription-per-resource-type) para elementos de la raíz de la unidad. El nuevo valor es la fecha de expiración máxima compatible con los elementos de la raíz de la unidad. |

## <a name="october-2017"></a>Octubre de 2017

### <a name="azure-ad-apis"></a>API de Azure AD

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
|Adición|Beta|Se han agregado la entidad [identityProvider](/graph/api/resources/identityprovider?view=graph-rest-beta) y las operaciones [crear](/graph/api/identityprovider-post-identityproviders?view=graph-rest-beta), [enumerar](/graph/api/identityprovider-list?view=graph-rest-beta), [obtener](/graph/api/identityprovider-get?view=graph-rest-beta), [actualizar](/graph/api/identityprovider-update?view=graph-rest-beta) y [eliminar](/graph/api/identityprovider-delete?view=graph-rest-beta).|


### <a name="microsoft-intune-apis"></a>API de Microsoft Intune
|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Nuevas entidades agregadas:<br/>[androidDeviceComplianceLocalActionLockDeviceWithPasscode](/graph/api/resources/intune-deviceconfig-androiddevicecompliancelocalactionlockdevicewithpasscode?view=graph-rest-beta)<br/>[iosLobAppProvisioningConfigurationAssignment](/graph/api/resources/intune-apps-ioslobappprovisioningconfigurationassignment?view=graph-rest-beta)<br/>[iosVppEBookAssignment](/graph/api/resources/intune-books-iosvppebookassignment?view=graph-rest-beta)<br/>[managedDeviceMobileAppConfigurationAssignment](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationassignment?view=graph-rest-beta)<br/>[managedEBookAssignment](/graph/api/resources/intune-books-managedebookassignment?view=graph-rest-beta)<br/>[managedMobileApp](/graph/api/resources/intune-mam-managedmobileapp?view=graph-rest-beta)<br/>[mobileAppAssignment](/graph/api/resources/intune-apps-mobileappassignment?view=graph-rest-beta)<br/>[termsAndConditionsAssignment](/graph/api/resources/intune-companyterms-termsandconditionsassignment?view=graph-rest-beta)<br/>[vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta)<br/>[windows10PFXImportCertificateProfile](/graph/api/resources/intune-deviceconfig-windows10pfximportcertificateprofile?view=graph-rest-beta)<br/>[windowsAssignedAccessProfile](/graph/api/resources/intune-deviceconfig-windowsassignedaccessprofile?view=graph-rest-beta)<br/>[windowsDomainJoinConfiguration](/graph/api/resources/intune-deviceconfig-windowsdomainjoinconfiguration?view=graph-rest-beta)<br/>|
|Adición|Beta|Nuevos tipos complejos agregados:<br/>[iosLobAppAssignmentSettings](/graph/api/resources/intune-apps-ioslobappassignmentsettings?view=graph-rest-beta)<br/>[iosSingleSignOnSettings](/graph/api/resources/intune-deviceconfig-iossinglesignonsettings?view=graph-rest-beta)<br/>[iosStoreAppAssignmentSettings](/graph/api/resources/intune-apps-iosstoreappassignmentsettings?view=graph-rest-beta)<br/>[iosVppAppAssignmentSettings](/graph/api/resources/intune-apps-iosvppappassignmentsettings?view=graph-rest-beta)<br/>[mobileAppAssignmentSettings](/graph/api/resources/intune-apps-mobileappassignmentsettings?view=graph-rest-beta)<br/>[proxiedDomain](/graph/api/resources/intune-deviceconfig-proxieddomain?view=graph-rest-beta)<br/>[windowsInformationProtectionProxiedDomainCollection](/graph/api/resources/intune-mam-windowsinformationprotectionproxieddomaincollection?view=graph-rest-beta)<br/>[windowsStoreForBusinessAppAssignmentSettings](/graph/api/resources/intune-apps-windowsstoreforbusinessappassignmentsettings?view=graph-rest-beta)<br/>|
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-apps-mobileapp-assign?view=graph-rest-beta) a [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-apps-ioslobappprovisioningconfiguration-assign?view=graph-rest-beta) en [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-apps-manageddevicemobileappconfiguration-assign?view=graph-rest-beta) a [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-deviceconfig-devicecompliancepolicy-assign?view=graph-rest-beta) a [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [assignedAccessMultiModeProfiles](/graph/api/intune-deviceconfig-deviceconfiguration-assignedaccessmultimodeprofiles?view=graph-rest-beta) a [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [syncLicenses](/graph/api/intune-onboarding-vpptoken-synclicenses?view=graph-rest-beta) a [vppToken](/graph/api/resources/intune-onboarding-vpptoken?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [targetApps](/graph/api/intune-mam-managedapppolicy-targetapps?view=graph-rest-beta) a [managedAppPolicy](/graph/api/resources/intune-mam-managedapppolicy?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [targetApps](/graph/api/intune-mam-managedappprotection-targetapps?view=graph-rest-beta) a [managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [targetApps](/graph/api/intune-mam-targetedmanagedappconfiguration-targetapps?view=graph-rest-beta) a [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta) |
|Adición|Beta|Se agregó la acción [assign](/graph/api/intune-books-managedebook-assign?view=graph-rest-beta) a [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta) |
|Eliminación|Beta|Se quitaron las entidades siguientes:<br/>**cloudPkiSubscription**<br/>|
|Eliminación|Beta|Se quitaron los tipos complejos siguientes:<br/>**cloudPkiAdministratorCredentials**<br/>**windowsNetworkIsolationCloudResource**<br/>**windowsNetworkIsolationCloudResourceCollection**<br/>**windowsNetworkIsolationIPRangeCollection**<br/>**windowsNetworkIsolationResourceCollection**<br/>|
|Cambio|Beta|Se agregó la propiedad **gracePeriodInMinutes** a la entidad [androidDeviceComplianceLocalActionBase](/graph/api/resources/intune-deviceconfig-androiddevicecompliancelocalactionbase?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **enableSplitTunneling** a la entidad [androidForWorkVpnConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkvpnconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **versionName** y **versionCode** a la entidad [androidLobApp](/graph/api/resources/intune-apps-androidlobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **minimumRequiredPatchVersion** y **minimumWarningPatchVersion** a la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **minimumRequiredPatchVersion** y **minimumWarningPatchVersion** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **destino** a la entidad [deviceCompliancePolicyAssignment](/graph/api/resources/intune-deviceconfig-devicecompliancepolicyassignment?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **singleSignOnSettings** a la entidad [iosDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-iosdevicefeaturesconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **número de versión** y **buildNumber** a la entidad [iosLobApp](/graph/api/resources/intune-apps-ioslobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **bundleId** a la entidad [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **preSharedKey** a la entidad [iosWiFiConfiguration](/graph/api/resources/intune-deviceconfig-ioswificonfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **versionName** y **versionCode** a la entidad [managedAndroidLobApp](/graph/api/resources/intune-apps-managedandroidlobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **periodBeforePinReset** a la entidad [managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **subscriberCarrier**, **meid**, **totalStorageSpaceInBytes** y **freeStorageSpaceInBytes** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad **enrollmentType** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **versionNumber** y **buildNumber** a la entidad [managedIOSLobApp](/graph/api/resources/intune-apps-managedioslobapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **displayVersion** a la entidad [mobileAppInstallStatus](/graph/api/resources/intune-apps-mobileappinstallstatus?view=graph-rest-beta)|
|Cambio|Beta|Se quitaron las propiedades **defaultDeviceEnrollmentRestrictions**, **defaultDeviceEnrollmentWindowsHelloForBusinessSettings** y **defaultDeviceEnrollmentLimit** a la entidad [organización](/graph/api/resources/intune-onboarding-organization?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **isAssigned** a la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **isAssigned** a la entidad [targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **activeFirewallRequired**, **uacRequired**, **defenderEnabled**, **defenderVersion**, ** signatureOutOfDate** y **rtpEnabled** a la entidad [windows10CompliancePolicy](/graph/api/resources/intune-deviceconfig-windows10compliancepolicy?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **assignedAccessSingleModeUserName**, **assignedAccessSingleModeAppUserModelId**, **microsoftAccountSignInAssistantSettings**, ** authenticationAllowSecondaryDevice**, **cryptographyAllowFipsAlgorithmPolicy**, **securityBlockAzureADJoinedDevicesAutoEncryption**, ** systemTelemetryProxyServer**, **inkWorkspaceAccess**, **inkWorkspaceBlockSuggestedApps**, **defenderCloudBlockLevel** y **defenderCloudExtendedTimeout** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **protectedApps**, **enterpriseProxiedDomains** y **isAssigned** a la entidad [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad **productVersion** a la entidad [windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **apps** a la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **apps** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **vppTokens** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **assignments** a la entidad [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta)|
|Cambio|Beta|Se quitó la propiedad de navegación **deviceCompliancePolicy** a la entidad [deviceCompliancePolicyAssignment](/graph/api/resources/intune-deviceconfig-devicecompliancepolicyassignment?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **deviceCompliancePolicy** a la entidad [deviceCompliancePolicyGroupAssignment](/graph/api/resources/intune-deviceconfig-devicecompliancepolicygroupassignment?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **identityCertificateForClientAuthentication** a la entidad [iosDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-iosdevicefeaturesconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **assignments** a la entidad [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **apps** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **assignments** a la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **assignments** a la entidad [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **assignments** a la entidad [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **apps** a la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades de navegación **assignments** a la entidad [termsAndConditions](/graph/api/resources/intune-companyterms-termsandconditions?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **assignedAccessMultiModeProfiles** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta)|
|Cambio|Beta|Se agregó la propiedad de navegación **protectedAppLockerFiles** a la entidad [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta)|
|Cambio|Beta|Se agregaron las propiedades **port** y **forceTls** a la entidad de tipo complejo [airPrintDestination](/graph/api/resources/intune-deviceconfig-airprintdestination?view=graph-rest-beta)|
|Cambio|Beta|Se cambió el tipo de las siguientes propiedades de tipo complejo [deviceCompliancePolicySettingState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstate?view=graph-rest-beta):<br/>**errorCode** de Int32 a Int64<br/>|
|Cambio|Beta|Se cambió el tipo de las siguientes propiedades de tipo complejo [deviceConfigurationSettingState](/graph/api/resources/intune-deviceconfig-deviceconfigurationsettingstate?view=graph-rest-beta):<br/>**errorCode** de Int32 a Int64<br/>|
|Cambio|Beta|Se cambió el tipo de las siguientes propiedades de tipo complejo [windowsNetworkIsolationPolicy](/graph/api/resources/intune-deviceconfig-windowsnetworkisolationpolicy?view=graph-rest-beta):<br/>**enterpriseCloudResources** de [windowsNetworkIsolationCloudResourceCollection](/graph/api/resources/intune-deviceconfig-windowsnetworkisolationcloudresourcecollection?view=graph-rest-beta) a la colección [proxiedDomain](/graph/api/resources/intune-deviceconfig-proxieddomain?view=graph-rest-beta)<br/>**enterpriseInternalProxyServers** de windowsNetworkIsolationResourceCollection a la colección de cadenas<br/>**enterpriseIPRanges** de windowsNetworkIsolationIPRangeCollection a la colección [ipRange](/graph/api/resources/intune-deviceconfig-iprange?view=graph-rest-beta)<br/>**enterpriseNetworkDomainNames** de windowsNetworkIsolationResourceCollection a la colección de cadena<br/>**enterpriseProxyServers** de windowsNetworkIsolationResourceCollection a la colección de cadenas<br/>**neutralDomainResources** de windowsNetworkIsolationResourceCollection a la colección de cadenas<br/>|

### <a name="microsoft-teams-apis"></a>API de Microsoft Teams

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Agregar una nueva entidad de [equipo](/graph/api/resources/team?view=graph-rest-beta).|
|Adición|Beta|Agregar las operaciones [crear](/graph/api/team-put-teams?view=graph-rest-beta), [obtener](/graph/api/team-get?view=graph-rest-beta), y [actualizar](/graph/api/team-update?view=graph-rest-beta) en la entidad [equipo](/graph/api/resources/team?view=graph-rest-beta).|

### <a name="outlook-messages"></a>Mensajes de Outlook

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Cambio          | V1.0 y beta | Esta mejora de comportamiento es acerca de cómo conseguir una carpeta de correo compartida o el contenido del mensaje, cuando un usuario ha compartido una carpeta de correo con el usuario que ha iniciado sesión, o cuando ha delegado el buzón al usuario que ha iniciado sesión. En estos casos, una aplicación puede especificar la Id. del usuario o el nombre principal del usuario para [obtener la carpeta de correo compartida](/graph/api/mailfolder-get?view=graph-rest-1.0), o [obtener los mensajes en el calendario compartido](/graph/api/user-list-messages?view=graph-rest-1.0), siempre que el usuario que ha iniciado sesión haya proporcionado permisos delegados para la aplicación. |


### <a name="outlook-user-choices"></a>Opciones de usuario de Outlook

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
|Adición | Beta | Agregar la nueva propiedad **workingHours** a [mailboxSettings](/graph/api/resources/mailboxsettings?view=graph-rest-beta). Vea [tipo de recurso workingHours](/graph/api/resources/workinghours?view=graph-rest-beta) para obtener información sobre los casos de uso compatibles.|
|Adición | Beta | Se han agregado los nuevos tipos complejos: <br> [workingHours](/graph/api/resources/workinghours?view=graph-rest-beta) <br> [timeZoneBase](/graph/api/resources/timezonebase?view=graph-rest-beta) <br> [customTimeZone](/graph/api/resources/customtimezone?view=graph-rest-beta) <br> [standardTimeZoneOffset](/graph/api/resources/standardtimezoneoffset?view=graph-rest-beta) <br> [daylightTimeZoneOffset](/graph/api/resources/daylighttimezoneoffset?view=graph-rest-beta)|


### <a name="reports-apis"></a>API de informes
| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Cambio      | Beta    | Se han agregado las API [getEmailActivityUserDetail](/graph/api/reportroot-getemailactivityuserdetail?view=graph-rest-beta), [getEmailActivityCounts](/graph/api/reportroot-getemailactivitycounts?view=graph-rest-beta) y [getEmailActivityUserCounts](/graph/api/reportroot-getemailactivityusercounts?view=graph-rest-beta). Estas han reemplazado a la API EmailActivity. |
| Cambio      | Beta    | Se han agregado las API [getEmailAppUsageUserDetail](/graph/api/reportroot-getemailappusageuserdetail?view=graph-rest-beta), [getEmailAppUsageAppsUserCounts](/graph/api/reportroot-getemailappusageappsusercounts?view=graph-rest-beta), [getEmailAppUsageUserCounts](/graph/api/reportroot-getemailappusageusercounts?view=graph-rest-beta) y [getEmailAppUsageVersionsUserCounts](/graph/api/reportroot-getemailappusageversionsusercounts?view=graph-rest-beta). Estas han reemplazado a la API EmailAppUsage. |
| Cambio      | Beta    | Se han agregado las API [getMailboxUsageDetail](/graph/api/reportroot-getmailboxusagedetail?view=graph-rest-beta), [getMailboxUsageMailboxCounts](/graph/api/reportroot-getmailboxusagemailboxcounts?view=graph-rest-beta), [getMailboxUsageQuotaStatusMailboxCounts](/graph/api/reportroot-getmailboxusagequotastatusmailboxcounts?view=graph-rest-beta), y [getMailboxUsageStorage](/graph/api/reportroot-getmailboxusagestorage?view=graph-rest-beta). Estas han reemplazado a la API MailboxUsage. |
| Cambio      | Beta    | Se han agregado las API [getOffice365ActivationsUserDetail](/graph/api/reportroot-getoffice365activationsuserdetail?view=graph-rest-beta), [getOffice365ActivationCounts](/graph/api/reportroot-getoffice365activationcounts?view=graph-rest-beta) y [getOffice365ActivationsUserCounts](/graph/api/reportroot-getoffice365activationsusercounts?view=graph-rest-beta). Estas han reemplazado a la API Office365Activations. |
| Cambio      | Beta    | Se han agregado las API [getOffice365ActiveUserDetail](/graph/api/reportroot-getoffice365activeuserdetail?view=graph-rest-beta), [getOffice365ActiveUserCounts](/graph/api/reportroot-getoffice365activeusercounts?view=graph-rest-beta) y [getOffice365ServicesUserCounts](/graph/api/reportroot-getoffice365servicesusercounts?view=graph-rest-beta). Estas han reemplazado a la API Office365ActiveUser. |
| Cambio      | Beta    | Se han agregado las API [getOffice365GroupsActivityDetail](/graph/api/reportroot-getoffice365groupsactivitydetail?view=graph-rest-beta), [getOffice365GroupsActivityCounts](/graph/api/reportroot-getoffice365groupsactivitycounts?view=graph-rest-beta),[getOffice365GroupsActivityGroupCounts](/graph/api/reportroot-getoffice365groupsactivitygroupcounts?view=graph-rest-beta), [getOffice365GroupsActivityStorage](/graph/api/reportroot-getoffice365groupsactivitystorage?view=graph-rest-beta) y [getOffice365GroupsActivityFileCounts](/graph/api/reportroot-getoffice365groupsactivityfilecounts?view=graph-rest-beta). Estas han reemplazado a la API Office365GroupsActivity. |
| Cambio      | Beta    | Se han agregado las API [getOneDriveActivityUserDetail](/graph/api/reportroot-getonedriveactivityuserdetail?view=graph-rest-beta), [getOneDriveActivityUserCounts](/graph/api/reportroot-getonedriveactivityusercounts?view=graph-rest-beta) y [getOneDriveActivityFileCounts](/graph/api/reportroot-getonedriveactivityfilecounts?view=graph-rest-beta). Estas han reemplazado a la API OneDriveActivity. |
| Cambio      | Beta    | Se han agregado las API [getOneDriveUsageAccountDetail](/graph/api/reportroot-getonedriveusageaccountdetail?view=graph-rest-beta), [getOneDriveUsageAccountCounts](/graph/api/reportroot-getonedriveusageaccountcounts?view=graph-rest-beta), [getOneDriveUsageFileCounts](/graph/api/reportroot-getonedriveusagefilecounts?view=graph-rest-beta) y [getOneDriveUsageStorage](/graph/api/reportroot-getonedriveusagestorage?view=graph-rest-beta). Estas han reemplazado a la API OneDriveUsage. |
| Cambio      | Beta    | Se han agregado las API [getSharePointActivityUserDetail](/graph/api/reportroot-getsharepointactivityuserdetail?view=graph-rest-beta), [getSharePointActivityFileCounts](/graph/api/reportroot-getsharepointactivityfilecounts?view=graph-rest-beta), [getSharePointActivityUserCounts](/graph/api/reportroot-getsharepointactivityusercounts?view=graph-rest-beta) y [getSharePointActivityPages](/graph/api/reportroot-getsharepointactivitypages?view=graph-rest-beta). Estas han reemplazado a la API SharePointActivity. |
| Cambio      | Beta    | Se han agregado las API [getSharePointSiteUsageDetail](/graph/api/reportroot-getsharepointsiteusagedetail?view=graph-rest-beta), [getSharePointSiteUsageFileCounts](/graph/api/reportroot-getsharepointsiteusagefilecounts?view=graph-rest-beta), [getSharePointSiteUsageSiteCounts](/graph/api/reportroot-getsharepointsiteusagesitecounts?view=graph-rest-beta), [getSharePointSiteUsageStorage](/graph/api/reportroot-getsharepointsiteusagestorage?view=graph-rest-beta) y [getSharePointSiteUsagePages](/graph/api/reportroot-getsharepointsiteusagepages?view=graph-rest-beta). Estas han reemplazado a la API SharePointSiteUsage. |
| Cambio      | Beta    | Se han agregado las API [getSkypeForBusinessActivityUserDetail](/graph/api/reportroot-getskypeforbusinessactivityuserdetail?view=graph-rest-beta), [getSkypeForBusinessActivityCounts](/graph/api/reportroot-getskypeforbusinessactivitycounts?view=graph-rest-beta) y [getSkypeForBusinessActivityUserCounts](/graph/api/reportroot-getskypeforbusinessactivityusercounts?view=graph-rest-beta). Estas han reemplazado a la API SfbActivity. |
| Cambio      | Beta    | Se han agregado las API [getSkypeForBusinessDeviceUsageUserDetail](/graph/api/reportroot-getskypeforbusinessdeviceusageuserdetail?view=graph-rest-beta), [getSkypeForBusinessDeviceUsageDistributionUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusagedistributionusercounts?view=graph-rest-beta) y [getSkypeForBusinessDeviceUsageUserCounts](/graph/api/reportroot-getskypeforbusinessdeviceusageusercounts?view=graph-rest-beta). Estas han reemplazado a la API SfbDeviceUsage. |
| Cambio      | Beta    | Se han agregado las API [getSkypeForBusinessOrganizerActivityCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivitycounts?view=graph-rest-beta), [getSkypeForBusinessOrganizerActivityUserCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityusercounts?view=graph-rest-beta) y [getSkypeForBusinessOrganizerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessorganizeractivityminutecounts?view=graph-rest-beta). Estas han reemplazado a la API SfbOrganizerActivity. |
| Cambio      | Beta    | Se han agregado las API [getSkypeForBusinessParticipantActivityCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivitycounts?view=graph-rest-beta), [getSkypeForBusinessParticipantActivityUserCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityusercounts?view=graph-rest-beta) y [getSkypeForBusinessParticipantActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinessparticipantactivityminutecounts?view=graph-rest-beta). Estas han reemplazado a la API SfbParticipantActivity. |
| Cambio      | Beta    | Se han agregado las API [getSkypeForBusinessPeerToPeerActivityCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivitycounts?view=graph-rest-beta), [getSkypeForBusinessPeerToPeerActivityUserCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityusercounts?view=graph-rest-beta) y [getSkypeForBusinessPeerToPeerActivityMinuteCounts](/graph/api/reportroot-getskypeforbusinesspeertopeeractivityminutecounts?view=graph-rest-beta). Estas han reemplazado a la API SfbP2PActivity. |
| Cambio      | Beta    | Se han agregado las API [getYammerActivityUserDetail](/graph/api/reportroot-getyammeractivityuserdetail?view=graph-rest-beta), [getYammerActivityCounts](/graph/api/reportroot-getyammeractivitycounts?view=graph-rest-beta) y [getYammerActivityUserCounts](/graph/api/reportroot-getyammeractivityusercounts?view=graph-rest-beta). Estas han reemplazado a la API YammerActivity. |
| Cambio      | Beta    | Se han agregado las API [getYammerDeviceUsageUserDetail](/graph/api/reportroot-getyammerdeviceusageuserdetail?view=graph-rest-beta), [getYammerDeviceUsageDistributionUserCounts](/graph/api/reportroot-getyammerdeviceusagedistributionusercounts?view=graph-rest-beta) y [getYammerDeviceUsageUserCounts](/graph/api/reportroot-getyammerdeviceusageusercounts?view=graph-rest-beta). Estas han reemplazado a la API YammerDeviceUsage. |
| Cambio      | Beta    | Se han agregado las API [getYammerGroupsActivityDetail](/graph/api/reportroot-getyammergroupsactivitydetail?view=graph-rest-beta), [getYammerGroupsActivityGroupCounts](/graph/api/reportroot-getyammergroupsactivitygroupcounts?view=graph-rest-beta) y [getYammerGroupsActivityCounts](/graph/api/reportroot-getyammergroupsactivitycounts?view=graph-rest-beta). Estas han reemplazado a la API YammerGroupsActivity. |



## <a name="september-2017"></a>Septiembre de 2017

### <a name="intune-apis"></a>API de Intune

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Nuevas entidades agregadas:<br/>[activeDirectoryWindowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-activedirectorywindowsautopilotdeploymentprofile?view=graph-rest-beta)<br/>[azureADWindowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile?view=graph-rest-beta)<br/>[deviceEnrollmentConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentconfiguration?view=graph-rest-beta)<br/>[deviceEnrollmentLimitConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentlimitconfiguration?view=graph-rest-beta)<br/>[deviceEnrollmentPlatformRestrictionsConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration?view=graph-rest-beta)<br/>[deviceEnrollmentWindowsHelloForBusinessConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration?view=graph-rest-beta)<br/>[deviceManagementPartner](/graph/api/resources/intune-onboarding-devicemanagementpartner?view=graph-rest-beta)<br/>[enrollmentConfigurationAssignment](/graph/api/resources/intune-onboarding-enrollmentconfigurationassignment?view=graph-rest-beta)<br/>[windows10EnrollmentCompletionPageConfiguration](/graph/api/resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration?view=graph-rest-beta)<br/>[windows10NetworkBoundaryConfiguration](/graph/api/resources/intune-deviceconfig-windows10networkboundaryconfiguration?view=graph-rest-beta)<br/>[windowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-windowsautopilotdeploymentprofile?view=graph-rest-beta)<br/>[windowsAutopilotDeviceIdentity](/graph/api/resources/intune-enrollment-windowsautopilotdeviceidentity?view=graph-rest-beta)<br/>[windowsAutopilotSettings](/graph/api/resources/intune-enrollment-windowsautopilotsettings?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Nuevos tipos complejos agregados:<br/>[adminConsent](/graph/api/resources/intune-devices-adminconsent?view=graph-rest-beta)<br/>[allDevicesAssignmentTarget](/graph/api/resources/intune-shared-alldevicesassignmenttarget?view=graph-rest-beta)<br/>[allLicensedUsersAssignmentTarget](/graph/api/resources/intune-shared-alllicensedusersassignmenttarget?view=graph-rest-beta)<br/>[deviceAndAppManagementAssignmentTarget](/graph/api/resources/intune-shared-deviceandappmanagementassignmenttarget?view=graph-rest-beta)<br/>[deviceEnrollmentPlatformRestriction](/graph/api/resources/intune-onboarding-deviceenrollmentplatformrestriction?view=graph-rest-beta)<br/>[deviceHealthAttestationState](/graph/api/resources/intune-devices-devicehealthattestationstate?view=graph-rest-beta)<br/>[exclusionGroupAssignmentTarget](/graph/api/resources/intune-shared-exclusiongroupassignmenttarget?view=graph-rest-beta)<br/>[groupAssignmentTarget](/graph/api/resources/intune-shared-groupassignmenttarget?view=graph-rest-beta)<br/>[outOfBoxExperienceSettings](/graph/api/resources/intune-enrollment-outofboxexperiencesettings?view=graph-rest-beta)<br/>[windowsFirewallNetworkProfile](/graph/api/resources/intune-deviceconfig-windowsfirewallnetworkprofile?view=graph-rest-beta)<br/>windowsNetworkIsolationCloudResource<br/>windowsNetworkIsolationCloudResourceCollection<br/>windowsNetworkIsolationIPRangeCollection<br/>[windowsNetworkIsolationPolicy](/graph/api/resources/intune-deviceconfig-windowsnetworkisolationpolicy?view=graph-rest-beta)<br/>windowsNetworkIsolationResourceCollection<br/> |
| Adición    | Beta    | Se agregó la acción [sincronizar](/graph/api/intune-enrollment-windowsautopilotsettings-sync?view=graph-rest-beta) en [windowsAutopilotSettings](/graph/api/resources/intune-enrollment-windowsautopilotsettings?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción [asignar](/graph/api/intune-enrollment-windowsautopilotdeploymentprofile-assign?view=graph-rest-beta) en [windowsAutopilotDeploymentProfile](/graph/api/resources/intune-enrollment-windowsautopilotdeploymentprofile?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción localActions en [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción [setPriority](/graph/api/intune-onboarding-deviceenrollmentconfiguration-setpriority?view=graph-rest-beta) en [deviceEnrollmentConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentconfiguration?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción [asignar](/graph/api/intune-onboarding-deviceenrollmentconfiguration-assign?view=graph-rest-beta) en [deviceEnrollmentConfiguration](/graph/api/resources/intune-onboarding-deviceenrollmentconfiguration?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción uploadDepToken en la colección [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción syncWithAppleDeviceEnrollmentProgram en la colección [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción updateMobileAppIdentifierDeployments en [iosManagedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción asignar en [targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción asignar en [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la acción asignar en [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta). |
| Adición    | Beta    | Se agregó la función getEncryptionPublicKey en la colección [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **requireSafetyNetAttestationBasicIntegrity**, **requireSafetyNetAttestationCertifiedDevice**, **requireGooglePlayServices**, ** requireUpToDateSecurityProviders**, **requireCompanyPortalAppIntegrity** y **conditionStatementId** a la entidad [androidCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidcompliancepolicy?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **requireAppVerify**, **requireSafetyNetAttestationBasicIntegrity**, **requireSafetyNetAttestationCertifiedDevice**, **requireGooglePlayServices**, **requireUpToDateSecurityProviders** y **requireCompanyPortalAppIntegrity** a la entidad [androidForWorkCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidforworkcompliancepolicy?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **blockCrossProfileCopyPaste** y **requireAppVerify** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **kioskModeApps** y **requireAppVerify** a la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad **kioskModeManagedApps** de la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **cloudPkiProvider**, **createdDateTime**, **description**, **lastModifiedDateTime**, **displayName **, **syncStatus**, **lastSyncError**, **lastSyncDateTime**, **credentials**, **trustedRootCertificate** y **version** de la entidad cloudPkiSubscription. |
| Cambio      | Beta    | Se quitaron las propiedades **assignmentStatus**, **assignmentProgress** y **assignmentErrorMessage** de la entidad [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **adminConsent** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **vppTokenOrganizationName**, **vppTokenAccountType** y **vppTokenAppleId** a la entidad [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **deviceEnrollmentType**, **wiFiMacAddress** y **deviceHealthAttestationState** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **legacyAppConfiguration** a la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **notApplicableCount** a la entidad [managedDeviceMobileAppConfigurationDeviceSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicesummary?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **notApplicableCount** a la entidad [managedDeviceMobileAppConfigurationUserSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationusersummary?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **firewallBlockStatefulFTP**, **firewallIdleTimeoutForSecurityAssociationInSeconds**, **firewallPreSharedKeyEncodingMethod**, **firewallIPSecExemptionsAllowNeighborDiscovery**, **firewallIPSecExemptionsAllowICMP**, **firewallIPSecExemptionsAllowRouterDiscovery**, **firewallIPSecExemptionsAllowDHCP**, **firewallCertificateRevocationListCheckMethod**, **firewallMergeKeyingModuleSettings**, ** firewallPacketQueueingMethod**, **firewallProfileDomain**, **firewallProfilePublic**, **firewallProfilePrivate**, **defenderAttackSurfaceReductionExcludedPaths**, **defenderOfficeAppsOtherProcessInjectionType**, **defenderOfficeAppsExecutableContentCreationOrLaunchType **, **defenderOfficeAppsLaunchChildProcessType**, **defenderOfficeMacroCodeAllowWin32ImportsType**, **defenderScriptObfuscatedMacroCodeType**, **defenderScriptDownloadedPayloadExecutionType**, **defenderEmailContentExecutionType**, ** defenderGuardMyFoldersType**, **defenderGuardedFoldersAllowedAppPaths**, **defenderAdditionalGuardedFolders**, ** defenderNetworkProtectionType**, **defenderExploitProtectionXml**, **defenderExploitProtectionXmlFileName**, **defenderSecurityCenterBlockExploitProtectionOverride**, **appLockerApplicationControl**, **applicationGuardBlockClipboardSharing**, **applicationGuardAllowPrintToPDF**, **applicationGuardAllowPrintToXPS**, **applicationGuardAllowPrintToLocalPrinters**, **applicationGuardAllowPrintToNetworkPrinters** y **bitLockerDisableWarningForOtherDiskEncryption** a la entidad [ windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **displayAppListWithGdiDPIScalingTurnedOn**, **displayAppListWithGdiDPIScalingTurnedOff**, **messagingBlockSync**, **messagingBlockMMS** y **messagingBlockRichCommunicationServices** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad **bluetoothDeviceName** de la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **deviceAccountBlockExchangeServices**, **deviceAccountEmailAddress**, **deviceAccountExchangeServerAddress**, **deviceAccountRequirePasswordRotation** y **deviceAccountSessionInitiationProtocolAddress** de la entidad [windows10TeamGeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10teamgeneralconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad de navegación **localActions** a la entidad [androidCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidcompliancepolicy?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **windowsAutopilotSettings**, **windowsAutopilotDeviceIdentities**, **windowsAutopilotDeploymentProfiles**, **deviceEnrollmentConfigurations**, **deviceManagementPartners** y **depOnboardingSettings** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad de navegación **cloudPkiSubscriptions** de la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad de navegación **assignments** a la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad de navegación **assignments** a la entidad [targetedManagedAppProtection](/graph/api/resources/intune-mam-targetedmanagedappprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad de navegación **assignments** a la entidad [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta). |

### <a name="onedrive"></a>OneDrive

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó la propiedad **system** al recurso [Drive][]. |
| Adición        | v1.0        | Se agregó la relación **list** al recurso [Drive][]. |
| Adición        | v1.0        | Se agregó la relación **listItem** al recurso [DriveItem][]. |
| Adición        | v1.0        | Se agregaron las relaciones **lista** y **listItem** al recurso [SharedDriveItem][]. |
| Adición        | v1.0        | Nuevos tipos complejos agregados: [FolderView][]  |
| Adición        | v1.0        | Se agregó la propiedad **view** al tipo complejo [Folder][]. |
| Adición        | v1.0        | Se agregó la propiedad **driveType** al tipo complejo [ItemReference][]. |
| Adición        | v1.0        | Se agregaron las propiedades **audioBitsPerSample**, **audioChannels**, **audioFormat**, **audioSamplesPerSecond**, **defourCC** y **frameRate** al tipo complejo [Video][]. |
| Adición        | beta        | Se agregó la propiedad **system** al recurso [Drive][Drive-beta]. |
| Adición        | beta        | Se agregó la relación **activities** al recurso [Drive][Drive-beta]. |
| Adición        | beta        | Se agregó la propiedad **publication ** al recurso [DriveItem][DriveItem-beta]. |
| Adición        | beta        | Se agregaron las relaciones **activities** y **versions** al recurso [DriveItem][DriveItem-beta]. |
| Adición        | beta        | Nuevas entidades agregadas: [DriveItemVersion][DriveItemVersion-beta], [ItemActivity][ItemActivity-beta]. |
| Adición        | beta        | Nuevos tipos complejos agregados: [CommentAction][CommentAction-beta], [CreateAction][CreateAction-beta], [DeleteAction][DeleteAction-beta], [ EditAction][EditAction-beta], [ItemActionSet][ItemActionSet-beta], [ItemActivityTimeSet] [ ItemActivityTimeSet-beta], [MentionAction][MentionAction-beta], [MoveAction][MoveAction-beta], [PublicationFacet] [ PublicationFacet-beta], [RenameAction][RenameAction-beta], [RestoreAction][RestoreAction-beta], [ShareAction] [ ShareAction-beta] y [VersionAction][VersionAction-beta]. |
| Adición        | beta        | Se agregó la propiedad **driveType** al tipo complejo [ItemReference][ItemReference-beta]. |
| Eliminación        | beta        | Se quitó la propiedad **tenantId** del tipo complejo [SharepointIds][SharepointIds-beta]. |
| Adición        | v1.0        | Se agregaron las propiedades **audioBitsPerSample**, **audioChannels**, **audioFormat**, **audioSamplesPerSecond**, **defourCC** y **frameRate** al tipo complejo [Video][Video-beta]. |
| Adición        | beta        | Se agregaron las acciones [CheckIn] [ CheckIn-beta] y [CheckOut][CheckOut-beta] al recurso [DriveItem][DriveItem-beta]. |
| Adición        | beta        | Se agregaron las propiedades **expirationDateTime**, **password**, **message** y **recipients** de la acción [CreateLink][CreateLink-beta] en un recurso [DriveItem][DriveItem-beta]. |

[Drive]: /graph/api/resources/drive?view=graph-rest-1.0
[DriveItem]: /graph/api/resources/driveitem?view=graph-rest-1.0
[SharedDriveItem]: /graph/api/resources/shareddriveitem?view=graph-rest-1.0
[FolderView]: /graph/api/resources/folderview?view=graph-rest-1.0
[Folder]: /graph/api/resources/folder?view=graph-rest-1.0
[ItemReference]: /graph/api/resources/itemreference?view=graph-rest-1.0
[Video]: /graph/api/resources/video?view=graph-rest-1.0
[Drive-beta]: /graph/api/resources/drive?view=graph-rest-beta
[DriveItem-beta]: /graph/api/resources/driveitem?view=graph-rest-beta
[DriveItemVersion-beta]: /graph/api/resources/driveitemversion?view=graph-rest-beta
[ItemActivity-beta]: /graph/api/resources/itemactivity?view=graph-rest-beta
[CommentAction-beta]: /graph/api/resources/commentaction?view=graph-rest-beta
[CreateAction-beta]: /graph/api/resources/createaction?view=graph-rest-beta
[DeleteAction-beta]: /graph/api/resources/deleteaction?view=graph-rest-beta
[EditAction-beta]: /graph/api/resources/editaction?view=graph-rest-beta
[ItemActionSet-beta]: /graph/api/resources/itemactionset?view=graph-rest-beta
[ItemActivityTimeSet-beta]: /graph/api/resources/itemactivitytimeset?view=graph-rest-beta
[MentionAction-beta]: /graph/api/resources/mentionaction?view=graph-rest-beta
[MoveAction-beta]: /graph/api/resources/moveaction?view=graph-rest-beta
[PublicationFacet-beta]: /graph/api/resources/publicationfacet?view=graph-rest-beta
[RenameAction-beta]: /graph/api/resources/renameaction?view=graph-rest-beta
[RestoreAction-beta]: /graph/api/resources/restoreaction?view=graph-rest-beta
[ShareAction-beta]: /graph/api/resources/shareaction?view=graph-rest-beta
[VersionAction-beta]: /graph/api/resources/versionaction?view=graph-rest-beta
[ItemReference-beta]: /graph/api/resources/itemreference?view=graph-rest-beta
[SharepointIds-beta]: /graph/api/resources/sharepointids?view=graph-rest-beta
[Video-beta]: /graph/api/resources/video?view=graph-rest-beta
[CheckIn-beta]: /graph/api/driveitem-checkin?view=graph-rest-beta
[CheckOut-beta]: /graph/api/driveitem-checkout?view=graph-rest-beta
[CreateLink-beta]: /graph/api/driveitem-createlink?view=graph-rest-beta


### <a name="outlook-calendar"></a>Calendario de Outlook

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | Beta          | Se agregaron las funciones [findRoomLists](/graph/api/user-findroomlists?view=graph-rest-beta) y [findRooms](/graph/api/user-findrooms?view=graph-rest-beta) a la entidad [user](/graph/api/resources/user?view=graph-rest-beta). |
| Adición        | Beta          | Se agregó la propiedad **locations** al recurso [event](/graph/api/resources/event?view=graph-rest-beta) para ayudar en la organización de un evento al que puedan asistir los asistentes de más de una ubicación. |
| Adición        | Beta          | Se agregó la propiedad **locationType** para el tipo complejo [ubicación](/graph/api/resources/location?view=graph-rest-beta). |
| Adición        | Beta          | Se agregaron las propiedades **uniqueId** y **uniqueIdType** al tipo complejo [location](/graph/api/resources/location?view=graph-rest-beta). Estas propiedades son solo para uso interno en este momento. |
| Cambio          | V1.0 y beta | Esta mejora de comportamiento es acerca de cómo conseguir un calendario compartido o el contenido de los eventos, cuando un usuario ha compartido un calendario con el usuario que ha iniciado sesión o ha delegado el buzón al usuario que ha iniciado sesión. En estos casos, una aplicación puede especificar la Id. del usuario o el nombre principal del usuario para [obtener el calendario compartido](/graph/api/calendar-get?view=graph-rest-1.0), o [obtener los eventos en el calendario compartido](/graph/api/user-list-events?view=graph-rest-1.0), siempre que el usuario que ha iniciado sesión haya proporcionado permisos delegados para la aplicación. |

### <a name="outlook-contacts"></a>Contactos de Outlook

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Cambio          | V1.0 y beta | Esta mejora de comportamiento es acerca de cómo conseguir una carpeta de contactos compartida o el contenido de contactos, cuando un usuario ha compartido una carpeta de contactos con el usuario que ha iniciado sesión, o cuando ha delegado el buzón al usuario que ha iniciado sesión. En estos casos, una aplicación puede especificar la Id. del usuario o el nombre principal del usuario para [obtener la carpeta de contactos compartida](/graph/api/contactfolder-get?view=graph-rest-1.0), o [obtener los contactos en la carpeta compartida](/graph/api/user-list-contacts?view=graph-rest-1.0), siempre que el usuario que ha iniciado sesión haya proporcionado permisos delegados para la aplicación. |

### <a name="outlook-mail"></a>Correo de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la propiedad **internetMessageHeaders** a la entidad [message](/graph/api/resources/message?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó el tipo complejo [internetMessageHeader](/graph/api/resources/internetmessageheader?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó la propiedad de navegación **messageRules** a la entidad [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-beta). **messageRules** es una colección de instancias de [messageRule](/graph/api/resources/messagerule?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó la entidad [messageRule](/graph/api/resources/messagerule?view=graph-rest-beta) y los tipos complejos [messageRuleActions](/graph/api/resources/messageruleactions?view=graph-rest-beta), [messageRulePredicates](/graph/api/resources/messagerulepredicates?view=graph-rest-beta), y [sizeRange](/graph/api/resources/sizerange?view=graph-rest-beta). |
| Adición        | Beta        | Se agregaron las siguientes operaciones de CRUD para reglas de mensaje: [crear](/graph/api/mailfolder-post-messagerules?view=graph-rest-beta), [lista](/graph/api/mailfolder-list-messagerules?view=graph-rest-beta), [obtener](/graph/api/messagerule-get?view=graph-rest-beta), [actualizar](/graph/api/messagerule-update?view=graph-rest-beta), y [eliminar](/graph/api/messagerule-delete?view=graph-rest-beta). |


### <a name="outlook-user-choices"></a>Opciones de usuario de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la nueva propiedad de navegación **masterCategories** a la entidad [outlookUser](/graph/api/resources/outlookuser?view=graph-rest-beta). **masterCategories** es una colección de objetos [outlookCategory](/graph/api/resources/outlookcategory?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó la entidad [outlookCategory](/graph/api/resources/outlookcategory?view=graph-rest-beta). |
| Adición        | Beta        | Se agregaron las siguientes operaciones de CRUD para [outlookCategory](/graph/api/resources/outlookcategory?view=graph-rest-beta): [crear](/graph/api/outlookuser-post-mastercategories?view=graph-rest-beta), [obtener](/graph/api/outlookcategory-get?view=graph-rest-beta), [actualizar](/graph/api/outlookcategory-update?view=graph-rest-beta) y [eliminar](/graph/api/outlookcategory-delete?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó la nueva función [supportedLanguages](/graph/api/outlookuser-supportedlanguages?view=graph-rest-beta) a la entidad [outlookUser](/graph/api/resources/outlookuser?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó la nueva función [supportedTimeZones](/graph/api/outlookuser-supportedtimezones?view=graph-rest-beta) a la entidad [outlookUser](/graph/api/resources/outlookuser?view=graph-rest-beta). |


### <a name="sharepoint-lists"></a>Listas de SharePoint

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Nuevas entidades agregadas: [ColumnDefinition][], [ColumnLink][], [ContentType][], [List][], [ListItem][]. |
| Adición        | v1.0        | Se agregaron las relaciones **columns**, **contentTypes**, **items** y **lists** al recurso [site][]. |
| Adición        | v1.0        | Nuevos tipos complejos agregados: [BooleanColumn][], [CalculatedColumn][], [ChoiceColumn][], [ContentTypeInfo][], [ContentTypeOrder][], [CurrencyColumn][], [DateTimeColumn][], [DefaultColumnValue][], [ListInfo][], [LookupColumn][], [NumberColumn][], [PersonOrGroupColumn][], [SystemFacet][], [TextColumn][]. |
| Adición        | beta        | Nuevas entidades agregadas: [BaseItemVersion][BaseItemVersion-beta], [ColumnLink][ColumnLink-beta], [ContentType][ContentType-beta], [ListItemVersion][ListItemVersion-beta], |
| Adición        | beta        | Se agregaron las propiedades **columnGroup**, **currency**, **defaultValue** y **displayName** a [ColumnDefinition ][ColumnDefinition-beta]. |
| Adición        | beta        | Se agregaron las propiedades **displayName** y **system** al recurso [List][List-beta]. |
| Adición        | beta        | Se agregaron las relaciones **activities** y **contentTypes** al recurso [List][List-beta]. |
| Adición        | beta        | Se agregó la propiedad **contentType** al recurso [ListItem][ListItem-beta]. |
| Adición        | beta        | Se agregaron las relaciones **activities** y **versions** al recurso [ListItem][ListItem-beta]. |
| Adición        | beta        | Se agregó la relación **contentTypes** al recurso [Site][Site-beta]. |
| Adición        | beta        | Se agregó la propiedad **outputType** al tipo [BooleanColumn][BooleanColumn-beta]. |
| Adición        | beta        | Nuevos tipos complejos agregados: [ContentTypeInfo][ContentTypeInfo-beta], [ContentTypeOrder][ContentTypeOrder-beta], [CurrencyColumn][CurrencyColumn-beta] y [SystemFacet][SystemFacet-beta]. |
| Adición        | beta        | Se agregó la propiedad **contentTypesEnabled** al tipo complejo [ListInfo][ListInfo-beta]. |
| Adición        | beta        | Se agregó la propiedad **allowUnlimitedLength** al tipo complejo [LookupColumn][LookupColumn-beta]. |
| Cambio          | beta        | Se cambió el nombre de la propiedad **allowMultipleValue** a **allowMultipleValues** en el tipo complejo [LookupColumn][LookupColumn-beta]. |
| Cambio          | beta        | Se cambió el nombre de la propiedad **chooseFrom** a **chooseFromType** en el tipo complejo [PersonOrGroupColumn][PersonOrGroupColumn-beta]. |
| Eliminación        | beta        | Se quitó la propiedad **locale** en el tipo complejo [NumberColumn][NumberColumn-beta]. |
| Eliminación        | beta        | Se quitó la propiedad **enforceUniqueValues** del tipo complejo [PersonOrGroupColumn][PersonOrGroupColumn-beta]. |

[BaseItemVersion-beta]: /graph/api/resources/baseitemversion?view=graph-rest-beta
[BooleanColumn-beta]:  /graph/api/resources/booleanColumn?view=graph-rest-beta
[BooleanColumn]: /graph/api/resources/booleancolumn?view=graph-rest-1.0
[CalculatedColumn]: /graph/api/resources/calculatedcolumn?view=graph-rest-1.0
[ChoiceColumn]: /graph/api/resources/choicecolumn?view=graph-rest-1.0
[ColumnDefinition-beta]: /graph/api/resources/columndefinition?view=graph-rest-beta
[ColumnDefinition]: /graph/api/resources/columndefinition?view=graph-rest-1.0
[ColumnLink-beta]: /graph/api/resources/columnlink?view=graph-rest-beta
[ColumnLink]: /graph/api/resources/columnlink?view=graph-rest-1.0
[ContentType-beta]: /graph/api/resources/contenttype?view=graph-rest-beta
[ContentType]: /graph/api/resources/contenttype?view=graph-rest-1.0
[ContentTypeInfo-beta]: /graph/api/resources/contenttypeinfo?view=graph-rest-beta
[ContentTypeInfo]: /graph/api/resources/contenttypeinfo?view=graph-rest-1.0
[ContentTypeOrder-beta]: /graph/api/resources/contenttypeorder?view=graph-rest-beta
[ContentTypeOrder]: /graph/api/resources/contenttypeorder?view=graph-rest-1.0
[CurrencyColumn-beta]: /graph/api/resources/currencycolumn?view=graph-rest-beta
[CurrencyColumn]: /graph/api/resources/currencycolumn?view=graph-rest-1.0
[DateTimeColumn]: /graph/api/resources/datetimecolumn?view=graph-rest-1.0
[DefaultColumnValue]: /graph/api/resources/defaultcolumnvalue?view=graph-rest-1.0
[List-beta]: /graph/api/resources/list?view=graph-rest-beta
[List]: /graph/api/resources/list?view=graph-rest-1.0
[ListInfo-beta]: /graph/api/resources/listinfo?view=graph-rest-beta
[ListInfo]: /graph/api/resources/listinfo?view=graph-rest-1.0
[ListItem-beta]: /graph/api/resources/listitem?view=graph-rest-beta
[ListItem]: /graph/api/resources/listitem?view=graph-rest-1.0
[ListItemVersion-beta]: /graph/api/resources/listitemversion?view=graph-rest-beta
[LookupColumn-beta]: /graph/api/resources/lookupcolumn?view=graph-rest-beta
[LookupColumn]: /graph/api/resources/lookupcolumn?view=graph-rest-1.0
[NumberColumn-beta]: /graph/api/resources/numbercolumn?view=graph-rest-beta
[NumberColumn]: /graph/api/resources/numbercolumn?view=graph-rest-1.0
[PersonOrGroupColumn-beta]: /graph/api/resources/personorgroupcolumn?view=graph-rest-beta
[PersonOrGroupColumn]: /graph/api/resources/personorgroupcolumn?view=graph-rest-1.0
[Site-beta]: /graph/api/resources/site?view=graph-rest-beta
[Site]: /graph/api/resources/site?view=graph-rest-1.0
[SystemFacet-beta]: /graph/api/resources/systemfacet?view=graph-rest-beta
[SystemFacet]: /graph/api/resources/systemfacet?view=graph-rest-1.0
[TextColumn]: /graph/api/resources/textcolumn?view=graph-rest-1.0


### <a name="sharepoint-sites"></a>Sitios de SharePoint

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | beta        | Se agregaron las propiedades **dataLocationCode** y **root** al tipo complejo [SiteCollection][SiteCollection-beta]. |

[SiteCollection-beta]: /graph/api/resources/sitecollection?view=graph-rest-beta


## <a name="august-2017"></a>Agosto de 2017

### <a name="group-lifecycle-policy"></a>Directiva de ciclo de vida del grupo

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se ha agregado la entidad [groupLifecyclePolicy](/graph/api/resources/grouplifecyclepolicy?view=graph-rest-beta). |
| Adición        | Beta        | Se han agregado las siguientes API para la directiva de ciclo de vida del grupo: [crear](/graph/api/grouplifecyclepolicy-post-grouplifecyclepolicies?view=graph-rest-beta), [enumerar](/graph/api/grouplifecyclepolicy-list?view=graph-rest-beta), [obtener](/graph/api/grouplifecyclepolicy-get?view=graph-rest-beta), [actualizar](/graph/api/grouplifecyclepolicy-update?view=graph-rest-beta), [eliminar](/graph/api/grouplifecyclepolicy-delete?view=graph-rest-beta), [agregar grupo](/graph/api/grouplifecyclepolicy-addgroup?view=graph-rest-beta), [quitar grupo ](/graph/api/grouplifecyclepolicy-removegroup?view=graph-rest-beta) y [renovar un grupo](/graph/api/grouplifecyclepolicy-renewgroup?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó la función [List groupLifecylePolicies](/graph/api/group-list-grouplifecyclepolicies?view=graph-rest-beta) (Mostrar groupLifecylePolicies) a la entidad [grupo](/graph/api/resources/group?view=graph-rest-beta). |

### <a name="intune-apis"></a>API de Intune
| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Nuevas entidades agregadas:<br/>[windowsPrivacyDataAccessControlItem](/graph/api/resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Nuevos tipos complejos agregados:<br/>[configurationManagerClientEnabledFeatures](/graph/api/resources/intune-devices-configurationmanagerclientenabledfeatures?view=graph-rest-beta)<br/>[windowsDefenderScanActionResult](/graph/api/resources/intune-devices-windowsdefenderscanactionresult?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Se agregó la acción [windowsDefenderScan](/graph/api/intune-devices-manageddevice-windowsdefenderscan?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [windowsDefenderUpdateSignatures](/graph/api/intune-devices-manageddevice-windowsdefenderupdatesignatures?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [windowsPrivacyAccessControls](/graph/api/intune-deviceconfig-deviceconfiguration-windowsprivacyaccesscontrols?view=graph-rest-beta) en [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **automaticallyUpdateApps** y **countryOrRegion** para la entidad [appleVolumePurchaseProgramToken](/graph/api/resources/intune-apps-applevolumepurchaseprogramtoken?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **enableAuthenticationViaCompanyPortal** para la entidad [depEnrollmentProfile](/graph/api/resources/intune-corpenrollment-depenrollmentprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **notificationMessageCCList** a la entidad [deviceComplianceActionItem](/graph/api/resources/intune-deviceconfig-devicecomplianceactionitem?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **notApplicableCount** a la entidad [deviceComplianceDeviceOverview](/graph/api/resources/intune-deviceconfig-devicecompliancedeviceoverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **notApplicableCount** a la entidad [deviceComplianceUserOverview](/graph/api/resources/intune-deviceconfig-devicecomplianceuseroverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **notApplicableCount** a la entidad [deviceConfigurationDeviceOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationdeviceoverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **notApplicableCount** a la entidad [deviceConfigurationUserOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationuseroverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **configurationManagerClientEnabledFeatures** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **intuneBrand** de la entidad [organization](/graph/api/resources/intune-onboarding-organization?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **smartScreenEnableInShell**, **smartScreenBlockOverrideForFiles**, **applicationGuardEnabled**, **applicationGuardBlockFileTransfer**, **applicationGuardBlockNonEnterpriseContent**, **applicationGuardAllowPersistence** y **applicationGuardForceAuditing** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **searchBlockDiacritics**, **searchDisableAutoLanguageDetection**, **searchDisableIndexingEncryptedItems**, **searchEnableRemoteQueries**, **searchDisableUseLocation**, **searchDisableIndexerBackoff**, **searchDisableIndexingRemovableDrive**, **searchEnableAutomaticIndexSizeManangement**, **smartScreenEnableAppInstallControl** y **privacyAdvertisingId** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **settingsDeviceName** de la entidad [windows10TeamGeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10teamgeneralconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **restartMode** a la entidad [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **detectedApps** y **managedDevices** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **privacyAccessControls** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **secureByDefault** al tipo complejo [deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **restartMode** al tipo complejo [windowsUpdateScheduledInstall](/graph/api/resources/intune-deviceconfig-windowsupdatescheduledinstall?view=graph-rest-beta) |

### <a name="onenote"></a>OneNote

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0 y beta | Se ha agregado la propiedad de navegación [onenote](/graph/api/resources/onenote?view=graph-rest-1.0) a **site**. |
| Adición        | Beta          | Se ha agregado los parámetros *siteCollectionId* y *siteId* de destino para las operaciones de copia. Por ejemplo: [CopyNotebook](/graph/api/notebook-copynotebook?view=graph-rest-1.0). |

### <a name="people"></a>Contactos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregaron las [API de contactos](/graph/api/resources/person?view=graph-rest-1.0) a v1.0. Para obtener información sobre la API de contactos, vea el artículo [Obtener información relevante sobre los contactos](people-example.md). |
| Adición        | v1.0        | Se agregó el permiso People.Read.All. Para obtener más información vea [Permisos](permissions-reference.md). |
| Adición        | v1.0        | Se agregó el recurso [personType](/graph/api/resources/persontype?view=graph-rest-1.0). |
| Cambio          | v1.0        | El recurso [scoredEmailAddress](/graph/api/resources/scoredemailaddress?view=graph-rest-1.0) reemplazó al recurso **rankedEmailAddress**. |
| Cambio          | v1.0        | El recurso [person](/graph/api/resources/person?view=graph-rest-1.0) se actualizó de esta forma:<ul><li>La propiedad **scoredEmailAddresses** (una colección del tipo [scoredEmailAddress](/graph/api/resources/scoredemailaddress?view=graph-rest-1.0)) reemplazó a la propiedad **emailAddresses**.</li><li>La propiedad **jobTitle** reemplazó a la propiedad **title**.</li><li>Se quitaron las propiedades **sources** y **mailboxType**.</li><li>La propiedad **personType** es ahora del tipo [personType](/graph/api/resources/persontype?view=graph-rest-1.0), en lugar del tipo cadena, y reemplaza a la función de las propiedades anteriores **sources** y **mailboxType**.</li><li>Se agregó la propiedad **imAddress**.</li></ul> |
| Eliminación        | v1.0        | Se quitó el recurso **personDataSource**. |

### <a name="user"></a>Usuario

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | beta        | Agregar la propiedad **employeeId** al [usuario](/graph/api/resources/user?view=graph-rest-beta) |

## <a name="july-2017"></a>Julio de 2017

### <a name="group-settings"></a>Configuración de grupo

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se ha agregado compatibilidad para configuraciones de grupo.<br/>Nuevos tipos de recursos: [groupSetting](/graph/api/resources/groupsetting?view=graph-rest-1.0), [groupSettingTemplate](/graph/api/resources/groupsettingtemplate?view=graph-rest-1.0), [settingValue](/graph/api/resources/settingvalue?view=graph-rest-1.0) y [settingTemplateValue](/graph/api/resources/settingtemplatevalue?view=graph-rest-1.0) |
| Cambio          | v1.0        | Se han agregado la propiedad **classification** y la propiedad de navegación **settings** a [group](/graph/api/resources/group?view=graph-rest-1.0) |

### <a name="intune-apis"></a>API de Intune

| Tipo de&nbsp;cambio | Versión | Descripción                              |
| :--------------- | :------ | :--------------------------------------- |
| Adición         | Beta    | Se ha agregado la acción [assign](/graph/api/intune-apps-iosmobileappconfiguration-assign?view=graph-rest-beta) en [iosMobileAppConfiguration](/graph/api/resources/intune-apps-iosmobileappconfiguration?view=graph-rest-beta) |
| Adición         | Beta    | Se ha agregado la acción [syncDevice](/graph/api/intune-devices-manageddevice-syncdevice?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Cambio           | Beta    | Se han agregado las propiedades **appsInstallAllowList**, **appsLaunchBlockList** y **appsHideList** a la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **disableAppEncryptionIfDeviceEncryptionIsEnabled** a la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **disableAppEncryptionIfDeviceEncryptionIsEnabled** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **complianceGracePeriodExpirationDateTime** a la entidad [deviceComplianceDeviceStatus](/graph/api/resources/intune-deviceconfig-devicecompliancedevicestatus?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **complianceGracePeriodExpirationDateTime** a la entidad [deviceComplianceSettingState](/graph/api/resources/intune-deviceconfig-devicecompliancesettingstate?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **complianceGracePeriodExpirationDateTime** a la entidad [deviceConfigurationDeviceStatus](/graph/api/resources/intune-deviceconfig-deviceconfigurationdevicestatus?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **subscriptions** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **version** a la entidad [deviceManagementExchangeConnector](/graph/api/resources/intune-onboarding-devicemanagementexchangeconnector?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **utcTimeOffsetInMinutes** a la entidad [iosUpdateConfiguration](/graph/api/resources/intune-deviceconfig-iosupdateconfiguration?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **complianceGracePeriodExpirationDateTime** a la entidad [iosUpdateDeviceStatus](/graph/api/resources/intune-deviceconfig-iosupdatedevicestatus?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **preSharedKey** a la entidad [macOSWiFiConfiguration](/graph/api/resources/intune-deviceconfig-macoswificonfiguration?view=graph-rest-beta) |
| Cambio           | Beta    | Se han agregado las propiedades **phoneNumber**, **androidSecurityPatchLevel** y **userDisplayName** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Cambio           | Beta    | Se han agregado las propiedades **userName**, **deviceModel**, **platform** y **complianceGracePeriodExpirationDateTime** a la entidad [managedDeviceMobileAppConfigurationDeviceStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicestatus?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **userPrincipalName** a la entidad [mobileAppInstallStatus](/graph/api/resources/intune-apps-mobileappinstallstatus?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **overrideDefaultRule** a la entidad [onPremisesConditionalAccessSettings](/graph/api/resources/intune-onboarding-onpremisesconditionalaccesssettings?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad **userPrincipalName** a la entidad [userAppInstallStatus](/graph/api/resources/intune-apps-userappinstallstatus?view=graph-rest-beta) |
| Cambio           | Beta    | Se han agregado las propiedades **connectAppBlockAutoLaunch**, **deviceAccountBlockExchangeServices**, **deviceAccountEmailAddress**, **deviceAccountExchangeServerAddress**, **deviceAccountRequirePasswordRotation**, **deviceAccountSessionInitiationProtocolAddress**, **settingsBlockMyMeetingsAndFiles**, **settingsBlockSessionResume**, **settingsBlockSigninSuggestions**, **settingsDefaultVolume**, **settingsScreenTimeoutInMinutes**, **settingsSessionTimeoutInMinutes** y **settingsSleepTimeoutInMinutes** a la entidad [windows10TeamGeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10teamgeneralconfiguration?view=graph-rest-beta) |
| Cambio           | Beta    | Se ha agregado la propiedad de navegación **deploymentSummary** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta) |
| Cambio           | Beta    | Se han agregado las propiedades **settingName**, **userId**, **userName**, **userEmail** y **currentValue** al tipo complejo [deviceCompliancePolicySettingState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstate?view=graph-rest-beta) |
| Cambio           | Beta    | Se agregaron las propiedades **settingName**, **userId**, **userName**, **userEmail** y **currentValue** al tipo complejo [deviceConfigurationSettingState](/graph/api/resources/intune-deviceconfig-deviceconfigurationsettingstate?view=graph-rest-beta). |
| Cambio           | Beta    | Se ha agregado la propiedad **unknownCount** al tipo complejo [deviceOperatingSystemSummary](/graph/api/resources/intune-devices-deviceoperatingsystemsummary?view=graph-rest-beta) |



## <a name="june-2017"></a>Junio de 2017

### <a name="project-rome"></a>Project Rome

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se han agregado los siguientes recursos y API:<br/>[Actividad](/graph/api/resources/projectrome-activity?view=graph-rest-beta)<br/>[Crear o reemplazar una actividad](/graph/api/projectrome-put-activity?view=graph-rest-beta)<br/>[Eliminar una actividad](/graph/api/projectrome-delete-activity?view=graph-rest-beta)<br/>[Elemento de historial](/graph/api/resources/projectrome-historyitem?view=graph-rest-beta)<br/>[Crear o reemplazar un elemento de historial](/graph/api/projectrome-put-historyitem?view=graph-rest-beta)<br/>[Eliminar un elemento de historial](/graph/api/projectrome-delete-historyitem?view=graph-rest-beta) |

### <a name="outlook-calendar"></a>Calendario de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Las siguientes 4 propiedades de [calendar](/graph/api/resources/calendar?view=graph-rest-1.0) se promovieron a la versión 1.0: **canEdit**, **canShare**, **canViewPrivateItems** y **owner**. |


### <a name="intune-apis"></a>API de Intune

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Se agregaron nuevas entidades:<br/>[defaultDeviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-defaultdevicecompliancepolicy?view=graph-rest-beta)<br/>[deviceConfigurationUserStateSummary](/graph/api/resources/intune-deviceconfig-deviceconfigurationuserstatesummary?view=graph-rest-beta)<br/>[deviceManagementScriptDeviceState](/graph/api/resources/intune-devicefe-devicemanagementscriptdevicestate?view=graph-rest-beta)<br/>[deviceManagementScriptRunSummary](/graph/api/resources/intune-devicefe-devicemanagementscriptrunsummary?view=graph-rest-beta)<br/>[deviceManagementScriptUserState](/graph/api/resources/intune-devicefe-devicemanagementscriptuserstate?view=graph-rest-beta)<br/>[iosUpdateDeviceStatus](/graph/api/resources/intune-deviceconfig-iosupdatedevicestatus?view=graph-rest-beta)<br/>[windowsManagedDevice](/graph/api/resources/intune-devicefe-windowsmanageddevice?view=graph-rest-beta)<br/>[windowsManagementAppHealthState](/graph/api/resources/intune-devicefe-windowsmanagementapphealthstate?view=graph-rest-beta)<br/>[windowsManagementAppHealthSummary](/graph/api/resources/intune-devicefe-windowsmanagementapphealthsummary?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Se agregaron nuevos tipos complejos:<br/>[bitLockerFixedDrivePolicy](/graph/api/resources/intune-deviceconfig-bitlockerfixeddrivepolicy?view=graph-rest-beta)<br/>[bitLockerRecoveryOptions](/graph/api/resources/intune-deviceconfig-bitlockerrecoveryoptions?view=graph-rest-beta)<br/>[bitLockerRemovableDrivePolicy](/graph/api/resources/intune-deviceconfig-bitlockerremovabledrivepolicy?view=graph-rest-beta)<br/>[deleteUserFromSharedAppleDeviceActionResult](/graph/api/resources/intune-devicefe-deleteuserfromsharedappledeviceactionresult?view=graph-rest-beta)<br/>[iosNetworkUsageRule](/graph/api/resources/intune-deviceconfig-iosnetworkusagerule?view=graph-rest-beta)<br/> |
| Eliminación    | Beta    | Se quitaron las entidades siguientes:<br/>**deviceManagementScriptState**<br/> |
| Eliminación    | Beta    | Se quitó la acción wipeByDeviceTag en [user](/graph/api/resources/intune-devicefe-user?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **innerAuthenticationProtocolForEapTtls**, **innerAuthenticationProtocolForPeap** y **outerIdentityPrivacyTemporaryValue** a la entidad [androidEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidenterprisewificonfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **nonEapAuthenticationMethodForEapTtls**, **nonEapAuthenticationMethodForPeap** y **enableOuterIdentityPrivacy** de la entidad [androidEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidenterprisewificonfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **deployedAppCount** a la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **instanceDisplayName** y **settingPlatform** de la entidad [complianceSettingStateSummary](/graph/api/resources/compliancesettingstatesummary?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **deployedAppCount** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **excludeGroup** a la entidad [deviceCompliancePolicyGroupAssignment](/graph/api/resources/intune-deviceconfig-devicecompliancepolicygroupassignment?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **instanceDisplayName** y **settingPlatform** de la entidad [deviceCompliancePolicySettingStateSummary](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad **devicePlatform** de la entidad [deviceComplianceSettingState](/graph/api/resources/intune-deviceconfig-devicecompliancesettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **assignmentStatus**, **assignmentProgress** y **assignmentErrorMessage** a la entidad [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **intuneBrand** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **enforceSignatureCheck** y **fileName** a la entidad [deviceManagementScript](/graph/api/resources/intune-devicefe-devicemanagementscript?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **innerAuthenticationProtocolForEapTtls** y **outerIdentityPrivacyTemporaryValue** a la entidad [iosEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-iosenterprisewificonfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **nonEapAuthenticationMethodForEapTtls** y **enableOuterIdentityPrivacy** de la entidad [iosEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-iosenterprisewificonfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **classroomAppForceUnpromptedScreenObservation**, **keyboardBlockDictation**, **networkUsageRules** y **wiFiConnectOnlyToConfiguredNetworks** a la entidad [iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **deployedAppCount** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **preSharedKey** a la entidad [iosWiFiConfiguration](/graph/api/resources/intune-deviceconfig-ioswificonfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **innerAuthenticationProtocolForEapTtls** y **outerIdentityPrivacyTemporaryValue** a la entidad [macOSEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-macosenterprisewificonfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **nonEapAuthenticationMethodForEapTtls** y **enableOuterIdentityPrivacy** de la entidad [macOSEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-macosenterprisewificonfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **lastModifiedTime** y **deployedAppCount** de la entidad [managedAppPolicy](/graph/api/resources/intune-mam-managedapppolicy?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **serialNumber** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad **managementAgents** de la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **deployedAppCount** a la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **bitLockerFixedDrivePolicy** y **bitLockerRemovableDrivePolicy** a la entidad [windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **enterpriseCloudPrintDiscoveryEndPoint**, **enterpriseCloudPrintOAuthAuthority**, **enterpriseCloudPrintOAuthClientIdentifier**, **enterpriseCloudPrintResourceIdentifier**, **enterpriseCloudPrintDiscoveryMaxLimit**, **enterpriseCloudPrintMopriaDiscoveryResourceIdentifier**, **edgeBlockAddressBarDropdown**, **edgeBlockCompatibilityList**, **edgeClearBrowsingDataOnExit**, **edgeAllowStartPagesModification**, **edgeDisableFirstRunPage**, **edgeBlockLiveTileDataCollection** y **edgeSyncFavoritesWithInternetExplorer** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **availableVersion** a la entidad [windowsManagementApp](/graph/api/resources/intune-devicefe-windowsmanagementapp?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **onboardingStatus**, **deployedVersion** y **lastModifiedTime** de la entidad [windowsManagementApp](/graph/api/resources/intune-devicefe-windowsmanagementapp?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **packageIdentityName** a la entidad [windowsStoreForBusinessApp](/graph/api/resources/intune-apps-windowsstoreforbusinessapp?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **mobileAppIdentifierDeployments** y **deploymentSummary** a la entidad [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad de navegación **mobileAppIdentifierDeployments** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **deviceConfigurationUserStateSummaries** y **iosUpdateStatuses** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad de navegación **complianceSettingStateSummaries** de la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **runSummary**, **deviceRunStates** y **userRunStates** a la entidad [deviceManagementScript](/graph/api/resources/intune-devicefe-devicemanagementscript?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad de navegación **runStates** de la entidad [deviceManagementScript](/graph/api/resources/intune-devicefe-devicemanagementscript?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **mobileAppIdentifierDeployments** y **deploymentSummary** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades de navegación **mobileAppIdentifierDeployments** y **deploymentSummary** de la entidad [managedAppPolicy](/graph/api/resources/intune-mam-managedapppolicy?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **mobileAppIdentifierDeployments** y **deploymentSummary** a la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **healthSummary** y **healthStates** a la entidad [windowsManagementApp](/graph/api/resources/intune-devicefe-windowsmanagementapp?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **applicationId**, **appName**, **platformId**, **userFailures** y **deviceFailures** al tipo complejo [appInstallationFailure](/graph/api/resources/intune-apps-appinstallationfailure?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **encryptionMethod**, **startupAuthenticationRequired**, **startupAuthenticationBlockWithoutTpmChip**, **startupAuthenticationTpmUsage**, **startupAuthenticationTpmPinUsage**, **startupAuthenticationTpmKeyUsage**, **startupAuthenticationTpmPinAndKeyUsage**, **recoveryOptions** y **prebootRecoveryEnableMessageAndUrl** al tipo complejo [bitLockerSystemDrivePolicy](/graph/api/resources/intune-deviceconfig-bitlockersyst?view=graph-rest-betarivepolicy). |
| Cambio      | Beta    | Se quitaron las propiedades **settingName**, **userId**, **userName**, **userEmail** y **currentValue** del tipo complejo [deviceCompliancePolicySettingState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitaron las propiedades **settingName**, **userId**, **userName**, **userEmail** y **currentValue** del tipo complejo [deviceConfigurationSettingState](/graph/api/resources/intune-deviceconfig-deviceconfigurationsettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **windowsCommercialId** y **windowsCommercialIdLastModifiedTime** al tipo complejo [deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **address** al tipo complejo [vpnServer](/graph/api/resources/intune-deviceconfig-vpnserver?view=graph-rest-beta). |


## <a name="may-2017"></a>Mayo de 2017

### <a name="application-api-changes"></a>Cambios en la API de la aplicación

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Actualización de la API de la aplicación. Este es el primer conjunto de cambios que incluye una reestructuración y un cambio de nombre de las propiedades de la entidad [application](/graph/api/resources/application?view=graph-rest-beta).<br/>**Nuevas entidades:** [api](/graph/api/resources/api?view=graph-rest-beta]), [informationalUrl](/graph/api/resources/informationalurl?view=graph-rest-beta), [installedClient](/graph/api/resources/installedclient?view=graph-rest-beta), [permissionScope](/graph/api/resources/permissionscope?view=graph-rest-beta), [preauthorizedApplication](/graph/api/resources/preauthorizedapplication?view=graph-rest-beta) y [web](/graph/api/resources/web?view=graph-rest-beta).<br/>**Propiedades quitadas:** addIns, appRoles, availableToOtherOrganizations, knownClientApplications, oauth2AllowUrlPathMatching, recordConsentConditions.<br/>**Propiedades a las que se les ha cambiado el nombre:** appId se ha cambiado a id, identifierUris, a applicationAliases, availableToOtherTenants, a orgRestrictions, mainLogo, a logo, oauth2Permissions, a publishedPermissionsScopes, publicClient, a allowPublicClient y replyUrls, a redirectUrls.<br/>**Nuevas propiedades:** etiquetas. |

### <a name="remove-deprecated-planner-api"></a>Quitar API de Planner en desuso
| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Eliminación        | Beta        | Se quitaron las entidades siguientes:<br/>**task**<br/>**plan**<br/>**bucket**<br/>**taskDetails**<br/>**planDetails**<br/>**taskBoardTaskFormat**<br/>**planTaskBoard** |

### <a name="project-rome"></a>Project Rome

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó compatibilidad con Project Rome, que incluye [la obtención de una lista de dispositivos](/graph/api/user-list-devices?view=graph-rest-beta), [el envío de un comando a un dispositivo](/graph/api/send-device-command?view=graph-rest-beta) y [la comprobación del estado de un comando](/graph/api/get-device-command-status?view=graph-rest-beta). |
| Adición        | Beta        | Se agregó compatibilidad con [actividades](/graph/api/resources/projectrome-activity?view=graph-rest-beta) de usuario y [historyItems](/graph/api/resources/projectrome-historyitem?view=graph-rest-beta), incluidas la [operación upsert de una actividad](/graph/api/projectrome-put-activity?view=graph-rest-beta) y la [operación upsert de un historyItem](/graph/api/projectrome-put-historyitem?view=graph-rest-beta). |

### <a name="administrative-units-property-changes"></a>Cambios de propiedades de las unidades administrativas

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Se cambió el tipo de propiedad roleMemberInfo a [identity](/graph/api/resources/identity?view=graph-rest-1.0) para la entidad [scopedRoleMembership](/graph/api/resources/scopedrolemembership?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambió la propiedad de navegación scopedAdministratorOf a scopedRoleMemberOf para la entidad [user](/graph/api/resources/user?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambió la propiedad de navegación scopedAdministrators a scopedRoleMembers para la entidad [administrativeUnit](/graph/api/resources/administrativeunit?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambió la propiedad de navegación scopedAdministrators a scopedRoleMembers para la entidad [directoryRole](/graph/api/resources/directoryrole?view=graph-rest-beta) |

### <a name="add-users-and-groups-webhook-support-in-preview"></a>Agregar compatibilidad con el webhook de usuarios y grupos en la versión preliminar

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
| Cambio        | Beta       | Se agregó compatibilidad a los [webhooks](/graph/api/resources/webhooks?view=graph-rest-beta) de usuarios y grupos.

### <a name="add-delta-query-to-v10"></a>Agregar consulta delta a v1.0

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | En la versión 1.0, se agregó la compatibilidad con la función delta. Se agrega a las siguientes entidades para realizar una [consulta delta](delta-query-overview.md):<br/>contact<br/>contactFolder<br/>evento<br/>grupo<br/>mailFolder<br/>mensaje<br/>usuario<br/>Vea los ejemplos siguientes:<br/>[Obtener los cambios incrementales en los grupos](delta-query-groups.md)<br/>[Obtener los cambios incrementales en los mensajes de una carpeta](delta-query-messages.md)<br/>[Obtener los cambios incrementales en los usuarios](delta-query-users.md) |
| Cambio          | Beta        | Agregue una consulta opcional adicional filtrando la capacidad (por id.) para [users](/graph/api/user-delta?view=graph-rest-beta) y [groups](/graph/api/group-delta?view=graph-rest-beta). |

### <a name="added-user-resource-support-for-deleted-items"></a>Compatibilidad con los recursos de usuario agregada para los elementos eliminados

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó compatibilidad para [restaurar usuarios y eliminarlos permanentemente](/graph/api/resources/directory?view=graph-rest-beta). |

### <a name="added-onpremisesprovisioningerror"></a>Propiedad OnPremisesProvisioningError agregada

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | beta        | Nueva entidad: [OnPremisesProvisioningError](/graph/api/resources/onpremisesprovisioningerror?view=graph-rest-beta) |
| Cambio          | beta        | Se agregó la propiedad OnPremisesProvisioningError a [user](/graph/api/resources/user?view=graph-rest-beta), [group](/graph/api/resources/group?view=graph-rest-beta) y [orgcontact](/graph/api/resources/orgcontact?view=graph-rest-beta) |

### <a name="added-deleteddatetime-property"></a>Propiedad deletedDateTime agregada

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Cambio|beta|Se agregó la propiedad deletedDateTime a la entidad [user](/graph/api/resources/user?view=graph-rest-beta).
|Cambio|beta|Se agregó la propiedad deletedDateTime a la entidad [group](/graph/api/resources/group?view=graph-rest-beta).
|Cambio|beta|Se agregó la propiedad deletedDateTime a la entidad [application](/graph/api/resources/application?view=graph-rest-beta).

### <a name="added-domain-operations-to-v10"></a>Operaciones de dominio agregadas a v1.0

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregaron operaciones en [domains](/graph/api/resources/domain?view=graph-rest-1.0).<br/>Nuevas entidades:</br>[domain](/graph/api/resources/domain?view=graph-rest-1.0)<br/>[domainDnsRecord](/graph/api/resources/domaindnsrecord?view=graph-rest-1.0)<br/>[domainDnsCnameRecord](/graph/api/resources/domaindnscnamerecord?view=graph-rest-1.0)<br/>[domainDnsMxRecord](/graph/api/resources/domaindnsmxrecord?view=graph-rest-1.0)<br/>[domainDnsSrvRecord](/graph/api/resources/domaindnssrvrecord?view=graph-rest-1.0)<br/>[domainDnsTxtRecord](/graph/api/resources/domaindnstxtrecord?view=graph-rest-1.0)<br/>[domainDnsUnavailableRecord](/graph/api/resources/domaindnsunavailablerecord?view=graph-rest-1.0)<br/>Nuevas acciones:</br>[comprobar](/graph/api/domain-verify?view=graph-rest-1.0) |

### <a name="added-contracts-to-v10"></a>Contratos agregados a v1.0

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Nueva entidad:</br>[contract](/graph/api/resources/contract?view=graph-rest-1.0) |

### <a name="added-licensedetails-to-v10"></a>Propiedad licenseDetails agregada a v1.0

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Nueva entidad:</br>[licenseDetails](/graph/api/resources/licensedetails?view=graph-rest-1.0) |
| Cambio          | v1.0        | Nueva propiedad de navegación [licensedetails](/graph/api/user-list-licensedetails?view=graph-rest-1.0) en [users](/graph/api/resources/user?view=graph-rest-1.0) |


### <a name="drive-api"></a>API de unidad

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:----------|:--------------|
| Adición | v1.0 | Se agregó el tipo de recurso **baseItem**, que se compone de las propiedades básicas de **driveItem**.
| Adición | v1.0 y Beta | Se agregó la propiedad **sourceItemId** a **thumbnail**. <br/> Se agregó la propiedad **siteUrl** a **sharepointIds**. <br/> Se agregaron las propiedades **sharedBy** y **sharedDateTime** a **shared**. <br/> Se agregó la propiedad **shared** a **remoteItem**. <br/> Se agregó la propiedad **sharepointIds** a **drive** y a **itemReference**. <br/> Se agregó **lastAccessedDateTime** a **fileSystemInfo**. <br/> Se agregaron las propiedades de navegación **driveItem** y **site** a **sharedDriveItem**. <br/> Se agregó la propiedad **parentReference** a **baseItem**.
| Cambio | v1.0 y Beta | Se cambiaron **driveItem** y **sharedDriveItem** para que hereden de **baseItem**. <br/> Se marcó **identity** como Tipo abierto.
| Cambio | Beta | Se agregaron las propiedades **configuratorUrl** y **webHtml** a **sharingLink**. <br/> Se agregaron el tipo de recurso **folderView** y la propiedad **view** al tipo de recurso **folder**. <br/> Se agregó la propiedad de navegación **listItem** a **driveItem**. <br/> Se agregó la propiedad de navegación **list** a **drive**.


### <a name="extensions-open-extensions"></a>Extensiones (extensiones abiertas)

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0          | Compatibilidad con [openTypeExtension](/graph/api/resources/opentypeextension?view=graph-rest-1.0) en los siguientes recursos: [device](/graph/api/resources/device?view=graph-rest-1.0), [group](/graph/api/resources/group?view=graph-rest-1.0), [organization](/graph/api/resources/organization?view=graph-rest-1.0) y [user](/graph/api/resources/user?view=graph-rest-1.0). |
| Adición        | V1.0 y beta | Cuando el usuario ha iniciado sesión con una cuenta personal de Microsoft, son compatibles con las extensiones abiertas los siguientes recursos: event, post, group, message, contact y user. (Cuando el usuario inicia sesión mediante una cuenta profesional o educativa, a la compatibilidad con extensiones abiertas se le agregan, además de estos, los recursos device, group, organization y user). |
| Adición        | v1.0 y beta | Compatibilidad con `$expand` para [obtener extensiones abiertas](/graph/api/opentypeextension-get?view=graph-rest-1.0) en los siguientes recursos: [device](/graph/api/resources/device?view=graph-rest-1.0), [group](/graph/api/resources/group?view=graph-rest-1.0), [organization](/graph/api/resources/organization?view=graph-rest-1.0), [post](/graph/api/resources/post?view=graph-rest-1.0) y [user](/graph/api/resources/user?view=graph-rest-1.0). |
| Adición        | Beta          | Compatibilidad con `$expand` para [obtener extensiones abiertas](/graph/api/opentypeextension-get?view=graph-rest-1.0) en [administrativeUnit](/graph/api/resources/administrativeunit?view=graph-rest-beta). |


### <a name="extensions-schema-extensions"></a>Extensiones (extensiones de esquema)

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0          | Nuevo recurso [schemaExtension](/graph/api/resources/schemaextension?view=graph-rest-1.0) y métodos CRUD para administrar definiciones de extensión para los siguientes recursos: [contact](/graph/api/resources/contact?view=graph-rest-1.0), [device](/graph/api/resources/device?view=graph-rest-1.0), [event](/graph/api/resources/event?view=graph-rest-1.0), [group](/graph/api/resources/group?view=graph-rest-1.0), [message](/graph/api/resources/message?view=graph-rest-1.0), [organization](/graph/api/resources/organization?view=graph-rest-1.0), [post](/graph/api/resources/post?view=graph-rest-1.0) y [user](/graph/api/resources/user?view=graph-rest-1.0). Tenga en cuenta que la compatibilidad con [administrativeUnit](/graph/api/resources/administrativeunit?view=graph-rest-beta) sigue estando limitada a la versión beta como antes. |
| Adición        | v1.0          | Los métodos POST, GET y PATCH existentes de los recursos [contact](/graph/api/resources/contact?view=graph-rest-1.0), [device](/graph/api/resources/device?view=graph-rest-1.0), [event](/graph/api/resources/event?view=graph-rest-1.0), [group](/graph/api/resources/group?view=graph-rest-1.0), [message](/graph/api/resources/message?view=graph-rest-1.0), [organization](/graph/api/resources/organization?view=graph-rest-1.0), [post](/graph/api/resources/post?view=graph-rest-1.0) y [user](/graph/api/resources/user?view=graph-rest-1.0) ya son compatibles con la adición, la obtención, la actualización y la eliminación de los datos personalizados que están almacenados como extensiones de esquema en las instancias de recurso correspondientes. |
| Adición        | V1.0 y beta | Ahora puede usar `$filter` para buscar instancias de recurso con propiedades que coincidan con valores de propiedad de extensión específicos, como los nombres de extensión. Consulte este [ejemplo](extensibility-schema-groups.md#5-get-a-group-and-its-extension-data) para obtener detalles. |
| Cambio          | v1.0 y beta | [Eliminar una definición de extensión de esquema](/graph/api/schemaextension-delete?view=graph-rest-1.0) ya no afecta al acceso a los datos personalizados que se han agregado a partir de esa definición. |
| Cambio          | v1.0 y beta | Ahora puede establecer un tipo complejo de extensión de esquema como nulo para quitar una extensión de esquema de una instancia de recurso. |


### <a name="group"></a>Group

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:----------|:--------------|
| Adición | v1.0 y beta | Se han agregado las propiedades de navegación **drives** y **sites** a **group**.

### <a name="insights-apis"></a>API de información

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Se ha agregado la [API compartida](/graph/api/resources/insights-shared?view=graph-rest-beta).<br />Nuevos recursos:<br />[sharingDetail](/graph/api/resources/insights-sharingdetail?view=graph-rest-beta) <br />[insightIdentity](/graph/api/resources/insights-insightidentity?view=graph-rest-beta) <br />
|Adición|Beta|Se ha agregado la [API usada](/graph/api/resources/insights-used?view=graph-rest-beta).<br />Nuevos recursos:<br />[usageDetails](/graph/api/resources/insights-usagedetails?view=graph-rest-beta) <br />
|Cambio|Beta|Nueva propiedad **Type** en:<br />recurso [resourceVisualization](/graph/api/resources/insights-resourcevisualization?view=graph-rest-beta). <br />
|Eliminación|Beta|Se han quitado las entidades siguientes:<br/>**workingWith**<br/>**trendingAround**<br/>|

### <a name="intune-apis"></a>API de Intune

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Nuevas entidades agregadas:<br/>[androidForWorkMobileAppConfiguration](/graph/api/resources/intune-apps-androidforworkmobileappconfiguration?view=graph-rest-beta)<br/>[cartToClassAssociation](/graph/api/resources/intune-deviceconfig-carttoclassassociation?view=graph-rest-beta)<br/>[deviceCompliancePolicySettingStateSummary](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary?view=graph-rest-beta)<br/>[eBookInstallSummary](/graph/api/resources/intune-books-ebookinstallsummary?view=graph-rest-beta)<br/>[eBookVppGroupAssignment](/graph/api/resources/intune-books-ebookvppgroupassignment?view=graph-rest-beta)<br/>[iosUpdateConfiguration](/graph/api/resources/intune-deviceconfig-iosupdateconfiguration?view=graph-rest-beta)<br/>[remoteAssistancePartner](/graph/api/resources/intune-remoteassistance-remoteassistancepartner?view=graph-rest-beta)<br/>[windows10EndpointProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10endpointprotectionconfiguration?view=graph-rest-beta)<br/>[windowsDeviceMalwareState](/graph/api/resources/intune-endpointprotection-windowsdevicemalwarestate?view=graph-rest-beta)<br/>[windowsInformationProtectionAppLearningSummary](/graph/api/resources/intune-wip-windowsinformationprotectionapplearningsummary?view=graph-rest-beta)<br/>[windowsMalwareInformation](/graph/api/resources/intune-endpointprotection-windowsmalwareinformation?view=graph-rest-beta)<br/>[windowsProtectionState](/graph/api/resources/intune-endpointprotection-windowsprotectionstate?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Nuevos tipos complejos agregados:<br/>[androidPermissionAction](/graph/api/resources/intune-apps-androidpermissionaction?view=graph-rest-beta)<br/>[bitLockerSystemDrivePolicy](/graph/api/resources/intune-deviceconfig-bitlockersyst?view=graph-rest-betarivepolicy)<br/>[defenderDetectedMalwareActions](/graph/api/resources/intune-deviceconfig-defenderdetectedmalwareactions?view=graph-rest-beta)<br/>[settingSource](/graph/api/resources/intune-deviceconfig-settingsource?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Se ha agregado la acción [assign](/graph/api/intune-books-managedebook-assign?view=graph-rest-beta) a [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta). |
| Adición    | Beta    | Se ha agregado la acción [beginOnboarding](/graph/api/intune-remoteassistance-remoteassistancepartner-beginonboarding?view=graph-rest-beta) a [remoteAssistancePartner](/graph/api/resources/intune-remoteassistance-remoteassistancepartner?view=graph-rest-beta). |
| Adición    | Beta    | Se ha agregado la acción [disconnect](/graph/api/intune-remoteassistance-remoteassistancepartner-disconnect?view=graph-rest-beta) a [remoteAssistancePartner](/graph/api/resources/intune-remoteassistance-remoteassistancepartner?view=graph-rest-beta). |
| Eliminación    | Beta    | Se han quitado las entidades siguientes:<br/>**outlookTask**<br/>**outlookTaskFolder**<br/>**outlookTaskGroup**<br/>**outlookUser**<br/>**windowsManagementAppHealthState**<br/> |
| Eliminación    | Beta    | Se han quitado los tipos complejos siguientes:<br/>**applePushNotificationCertificateSetting**<br/>**eventCreationOptions**<br/> |
| Cambio      | Beta    | Se han agregado las propiedades **workProfilePasswordBlockFingerprintUnlock**, **workProfilePasswordBlockTrustAgents**, **workProfilePasswordExpirationDays**, **workProfilePasswordMinimumLength**, **workProfilePasswordMinutesOfInactivityBeforeScreenTimeout**, **workProfilePasswordPreviousPasswordBlockCount**, **workProfilePasswordSignInFailureCountBeforeFactoryReset**, **workProfilePasswordRequiredType** y **workProfileRequirePassword** a la entidad [androidForWorkGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **subjectAlternativeNameFormatString** a la entidad [androidForWorkPkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkpkcscertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **subjectNameFormatString** y **subjectAlternativeNameFormatString** a la entidad [androidForWorkScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkscepcertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **kioskModeManagedApps** a la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad **kioskModeManagedAppId** de la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **subjectAlternativeNameFormatString** a la entidad [androidPkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-androidpkcscertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **subjectNameFormatString** y **subjectAlternativeNameFormatString** a la entidad [androidScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidscepcertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad **hexColor** de la entidad [calendar](/graph/api/resources/calendar?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **setting** y **platformType** a la entidad [complianceSettingStateSummary](/graph/api/resources/intune-deviceconfig-compliancesettingstatesummary?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad **windowsManagementAppEnabled** de la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **userName**, **deviceModel** y **platform** a la entidad [deviceComplianceDeviceStatus](/graph/api/resources/intune-deviceconfig-devicecompliancedevicestatus?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **userPrincipalName** y **deviceModel** a la entidad [deviceComplianceSettingState](/graph/api/resources/intune-deviceconfig-devicecompliancesettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **platformType**, **setting**, **userId** y **userEmail** a la entidad [deviceComplianceSettingState](/graph/api/resources/intune-deviceconfig-devicecompliancesettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregó la propiedad **inGracePeriodCount** a la entidad [deviceCompliancePolicyDeviceStateSummary](/graph/api/resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **userName**, **deviceModel** y **platform** a la entidad [deviceConfigurationDeviceStatus](/graph/api/resources/intune-deviceconfig-deviceconfigurationdevicestatus?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad **creationOptions** de la entidad [event](/graph/api/resources/event?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad **isDelegated** de la entidad [eventMessage](/graph/api/resources/eventmessage?view=graph-rest-beta). |
| Cambio      | Beta    | Se han quitado las propiedades **unseenConversationsCount** y **unseenMessagesCount** de la entidad [group](/graph/api/resources/group?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **settingXml** y **settings** a la entidad [iosMobileAppConfiguration](/graph/api/resources/intune-apps-iosmobileappconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **subjectAlternativeNameFormatString** a la entidad [iosPkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-iospkcscertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **subjectAlternativeNameFormatString** a la entidad [iosScepCertificateProfile](/graph/api/resources/intune-deviceconfig-iosscepcertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **systemIntegrityProtectionEnabled** a la entidad [macOSCompliancePolicy](/graph/api/resources/intune-deviceconfig-macoscompliancepolicy?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **subjectAlternativeNameFormatString** a la entidad [macOSScepCertificateProfile](/graph/api/resources/intune-deviceconfig-macosscepcertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **complianceGracePeriodExpirationDateTime**, **imei** y **userPrincipalName** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
| Cambio      | Beta    | Se han quitado las propiedades **settingXml** y **settings** de la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **useSharedComputerActivation**, **updateChannel**, **officePlatformArchitecture** y **localesToInstall** a la entidad [officeSuiteApp](/graph/api/resources/intune-apps-officesuiteapp?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad **applePushNotificationCertificateSetting** de la entidad [organization](/graph/api/resources/intune-onboarding-organization?view=graph-rest-beta). |
| Cambio      | Beta    | Se han cambiado las propiedades siguientes en la entidad [post](/graph/api/resources/post?view=graph-rest-beta):<br/>**sender**, de opcional a obligatorio.<br/> |
| Cambio      | Beta    | Se han agregado las propiedades **compliantUserCount**, **nonCompliantUserCount**, **remediatedUserCount**, **errorUserCount**, **unknownUserCount**, **conflictUserCount** y **notApplicableUserCount** a la entidad [softwareUpdateStatusSummary](/graph/api/resources/intune-deviceconfig-softwareupdatestatussummary?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **bluetoothAllowedServices**, **bluetoothBlockPrePairing**, **cellularData**, **defenderDetectedMalwareActions**, **defenderPotentiallyUnwantedAppAction**, **lockScreenAllowTimeoutConfiguration**, **lockScreenBlockCortana**, **lockScreenBlockToastNotifications**, **lockScreenTimeoutInSeconds**, **passwordBlockSimple**, **privacyAutoAcceptPairingAndConsentPrompts**, **privacyBlockInputPersonalization**, **startMenuHideChangeAccountSettings**, **startMenuHideHibernate**, **startMenuHideLock**, **startMenuHideShutDown**, **startMenuHideSignOut**, **startMenuHideSleep**, **startMenuHideSwitchAccount**, **settingsBlockAppsPage**, **settingsBlockGamingPage**, **windowsSpotlightBlockConsumerSpecificFeatures**, **windowsSpotlightBlocked**, **windowsSpotlightBlockOnActionCenter**, **windowsSpotlightBlockTailoredExperiences**, **windowsSpotlightBlockThirdPartyNotifications**, **windowsSpotlightBlockWelcomeExperience**, **windowsSpotlightBlockWindowsTips**, **windowsSpotlightConfigureOnLockScreen** y **connectedDevicesServiceBlocked** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se han quitado las propiedades **automaticUpdateMode**, **automaticUpdateSchedule**, **automaticUpdateTime**, **prereleaseFeatures**, **experienceBlockWindowsSpotlight**, **experienceBlockWindowsTips** y **experienceBlockConsumerSpecificFeatures** de la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **subjectAlternativeNameFormatString** a la entidad [windows10PkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-windows10pkcscertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **subjectNameFormatString** y **subjectAlternativeNameFormatString** a la entidad [windows81SCEPCertificateProfile](/graph/api/resources/intune-deviceconfig-windows81scepcertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **indexingEncryptedStoresOrItemsBlocked** y **smbAutoEncryptedFileExtensions** a la entidad [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta). |
| Cambio      | Beta    | Se han cambiado las propiedades siguientes en la entidad [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta):<br/>**rightsManagementServicesTemplateId**, de obligatorio a opcional.<br/> |
| Cambio      | Beta    | Se han cambiado las propiedades siguientes en la entidad [windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-beta):<br/>**productCode**, de obligatorio a opcional.<br/> |
| Cambio      | Beta    | Se han agregado las propiedades **subjectNameFormatString** y **subjectAlternativeNameFormatString** a la entidad [windowsPhone81SCEPCertificateProfile](/graph/api/resources/intune-deviceconfig-windowsphone81scepcertificateprofile?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad de navegación **mobileAppConfigurations** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **cartToClassAssociations**, **deviceCompliancePolicySettingStateSummaries**, **remoteAssistancePartners**, **windowsInformationProtectionAppLearningSummaries** y **windowsMalwareInformation** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad de navegación **eBook** a la entidad [eBookGroupAssignment](/graph/api/resources/intune-books-ebookgroupassignment?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad de navegación **windowsProtectionState** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad de navegación **installSummary** a la entidad [managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad de navegación **outlook** de la entidad [user](/graph/api/resources/intune-deviceconfig-user?view=graph-rest-beta). |
| Cambio      | Beta    | Se quitó la propiedad de navegación **healthStates** de la entidad [windowsManagementApp](/graph/api/resources/intune-deviceconfig-windowsmanagementapp?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha agregado la propiedad **androidForWorkRestrictions** al tipo complejo [defaultDeviceEnrollmentRestrictions](/graph/api/resources/intune-onboarding-defaultdeviceenrollmentrestrictions?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **userPrincipalName** y **sources** al tipo complejo [deviceCompliancePolicySettingState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se han agregado las propiedades **userPrincipalName** y **sources** al tipo complejo [deviceConfigurationSettingState](/graph/api/resources/intune-deviceconfig-deviceconfigurationsettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se agregaron las propiedades **settingName**, **userId**, **userName**, **userEmail** y **currentValue** al tipo complejo [deviceConfigurationSettingState](/graph/api/resources/intune-deviceconfig-deviceconfigurationsettingstate?view=graph-rest-beta). |
| Cambio      | Beta    | Se ha quitado la propiedad **archiveFolder** del tipo complejo [mailboxSettings](/graph/api/resources/mailboxsettings?view=graph-rest-beta). |


### <a name="outlook-calendar"></a>Calendario de Outlook

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | Para **findMeetingTimes**, se agregó el nuevo valor de enumeración **unrestricted** que debe especificar como propiedad **activityDomain**, que forma parte del parámetro **timeConstraint**. Esto permite que **findMeetingTimes** busque las horas adecuadas para el tipo de actividad que está programando. Consulte los detalles en la sección [Cuerpo de la solicitud](/graph/api/user-findmeetingtimes?view=graph-rest-1.0#request-body). |
| Adición        | Beta          | Compatibilidad con la obtención del cuerpo de un **evento** en texto sin formato como alternativa al formato HTML predeterminado. Consulte los eventos [get](/graph/api/event-get?view=graph-rest-beta) y [list](/graph/api/user-list-events?view=graph-rest-beta) para obtener detalles. |

### <a name="outlook-mail"></a>Correo de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Compatibilidad con la obtención del cuerpo de un **mensaje** en texto sin formato como alternativa al formato HTML predeterminado. Consulte los eventos [get](/graph/api/message-get?view=graph-rest-beta) y [list](/graph/api/user-list-messages?view=graph-rest-beta) para obtener detalles. |


### <a name="outlook-tasks"></a>Tareas de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la propiedad de navegación nueva **outlook** a [user](/graph/api/resources/user?view=graph-rest-beta) para obtener acceso a las tareas de Outlook. |
| Adición        | Beta        | Nuevas entidades: [outlookuser](/graph/api/resources/outlookuser?view=graph-rest-beta), [outlookTaskGroup](/graph/api/resources/outlooktaskgroup?view=graph-rest-beta), [outlookTaskFolder](/graph/api/resources/outlooktaskfolder?view=graph-rest-beta) y [outlookTask](/graph/api/resources/outlooktask?view=graph-rest-beta) (sus métodos son compatibles con la organización de las tareas de Outlook y el acceso a estas). |
| Adición        | Beta        | Las tareas de Outlook son compatibles con los archivos adjuntos (recursos [attachment](/graph/api/resources/attachment?view=graph-rest-beta), [fileAttachment](/graph/api/resources/fileattachment?view=graph-rest-beta), [itemAttachment](/graph/api/resources/itemattachment?view=graph-rest-beta) y [referenceAttachment](/graph/api/resources/referenceattachment?view=graph-rest-beta)). |
| Adición        | Beta        | Las tareas de Outlook son compatibles con las [propiedades extendidas](/graph/api/resources/extended-properties-overview?view=graph-rest-beta) (recursos [singleValueLegacyExtendedProperty](/graph/api/resources/singlevaluelegacyextendedproperty?view=graph-rest-beta) y [multiValueLegacyExtendedProperty](/graph/api/resources/multivaluelegacyextendedproperty?view=graph-rest-beta)). |

### <a name="planner-apis"></a>API de Planner

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó la [API de Planner](/graph/api/resources/planner-overview?view=graph-rest-1.0).<br />Nuevos recursos:<br />[plannerPlan](/graph/api/resources/plannerplan?view=graph-rest-1.0) <br />[plannerTask](/graph/api/resources/plannertask?view=graph-rest-1.0) <br />[plannerPlanDetails](/graph/api/resources/plannerplandetails?view=graph-rest-1.0) <br />[plannerTaskDetails](/graph/api/resources/plannertaskdetails?view=graph-rest-1.0) <br />[plannerBucket](/graph/api/resources/plannerbucket?view=graph-rest-1.0) <br />[plannerAssignedToTaskBoardTaskFormat](/graph/api/resources/plannerassignedtotaskboardtaskformat?view=graph-rest-1.0) <br />[plannerBucketTaskBoardTaskFormat](/graph/api/resources/plannerbuckettaskboardtaskformat?view=graph-rest-1.0) <br />[plannerProgressTaskBoardTaskFormat](/graph/api/resources/plannerprogresstaskboardtaskformat?view=graph-rest-1.0) |

### <a name="sharepoint-sites"></a>Sitios de SharePoint

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:----------|:--------------|
| Adición      | v1.0      | El recurso de sitios ya está disponible en el punto de conexión v1.0.<br/> Se agregaron los tipos de recurso **site** y **siteCollection**.
| Cambio        | beta      | El formato del identificador del recurso **site** ha cambiado. Se trata de un cambio importante en la API beta.
| Eliminación       | beta      | La entidad **sharePoint** se ha quitado de la API beta. La funcionalidad ya está disponible en la colección **sites**.

### <a name="sharepoint-lists"></a>Listas de SharePoint

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:----------|:--------------|
| Cambio | beta | Se han quitado las propiedades de navegación **sharepoint**. Ahora, se obtiene acceso a los sitios directamente a través de la propiedad de navegación **sites**. <br/> Se ha quitado el recurso **fieldDefinition**. Se ha reemplazado por **columnDefinition**. <br/> Se han quitado las propiedades **siteCollectionId** y **siteId** de **site**. Use **sharepointIds** en su lugar. <br/> Se ha quitado la propiedad **listItemId** de **listItem**. Use **sharepointIds** en su lugar. <br/> Se ha cambiado el nombre de la propiedad **columnSet** de **listItem** a **fields**. <br/> Se cambiaron los recursos **site** para que usen el nombre de host de SharePoint como parte de su ID.
| Adición | beta | Se agregaron los tipos de recurso **booleanColumn**, **calculatedColumn**, **choiceColumn**, **dateTimeColumn**, **lookupColumn**, **numberColumn**, **personOrGroupColumn** y **textColumn**. <br/> Se agregó la propiedad **displayName** a **site**. <br/> Se agregó la propiedad de navegación **columns** a **site**. <br/> Se agregaron las propiedades de navegación **list** y **listItem** a **sharedDriveItem**. <br/> Se agregó la propiedad **sharepointIds** a **list**, a **listItem** y a **site**. <br/> Se agregó el tipo de recurso **columnDefinition**.




## <a name="april-2017"></a>Abril de 2017

### <a name="administrative-units-property-changes"></a>Cambios de propiedades de las unidades administrativas

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Las API de la unidad administrativa se actualizarán en vista preliminar (beta). El primer conjunto de cambios se aplicará el 3 de mayo de 2017. Los cambios incluyen el siguiente cambio de nombre de propiedad:<br />- **roleMemberInfo** tipo complejo para **identidad** tipo complejo para la entidad scopedRoleMembership<br />- **scopedAdministratorOf** propiedad de navegación para **scopedRoleMemberOf** para la entidad usuario<br />- **scopedAdministrators** propiedad de navegación para **scopedRoleMembers** para la entidad administrativeUnit<br />- **scopedAdministrators** propiedad de navegación para **scopedMembers** para la entidad directoryRole |

### <a name="application-and-serviceprincipal-api-changes"></a>Cambios en la API servicePrincipal y en aplicaciones

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Las API [application](/graph/api/resources/application?view=graph-rest-beta) y [servicePrincipal](/graph/api/resources/serviceprincipal?view=graph-rest-beta) se actualizarán en la versión preliminar (beta). El primer conjunto de cambios se aplicará el 15 de mayo de 2017. Entre los cambios, se incluyen la reestructuración y el cambio de nombre de propiedades. Algunas propiedades (como appRoles y addIns) no estarán disponibles hasta que se completen los cambios. Los cambios se publicarán en versión preliminar (beta) antes de publicarse la versión 1.0. |

### <a name="added-preview-support-for-cloud-solution-provider-developers"></a>Se agregó soporte técnico de versión preliminar para desarrolladores del Proveedor de soluciones en la nube

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó una nueva capacidad de versión preliminar para que las aplicaciones del Proveedor de soluciones en la nube aceptadas previamente puedan llamar a Microsoft Graph, descrita en un nuevo [tema de autorización](auth-cloudsolutionprovider.md). |

### <a name="added-onpremises-properties-to-user-entity"></a>Se agregaron propiedades onPremises a la entidad de usuario

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron nuevas propiedades onPremises (onPremisesDomainName, OnPremisesSamAccountName y onPremisesUserPrincipalName) a la entidad [user](/graph/api/resources/user?view=graph-rest-beta). |

### <a name="new-planner-apis-and-an-update-to-the-group-visibility-property"></a>Nuevas API de Planner y una actualización de la propiedad de visibilidad del grupo

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Se agregó **HiddenMembership** como valor adicional para la propiedad de visibilidad de la entidad [Group](/graph/api/resources/group?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó una nueva [API de Planner](/graph/api/resources/planner-overview?view=graph-rest-beta).<br />Nuevos recursos:<br />[plannerPlan](/graph/api/resources/plannerplan?view=graph-rest-beta) <br />[plannerTask](/graph/api/resources/plannertask?view=graph-rest-beta) <br />[plannerPlanDetails](/graph/api/resources/plannerplandetails?view=graph-rest-beta) <br />[plannerTaskDetails](/graph/api/resources/plannertaskdetails?view=graph-rest-beta) <br />[plannerBucket](/graph/api/resources/plannerbucket?view=graph-rest-beta) <br />[plannerAssignedToTaskBoardTaskFormat](/graph/api/resources/plannerassignedtotaskboardtaskformat?view=graph-rest-beta) <br />[plannerBucketTaskBoardTaskFormat](/graph/api/resources/plannerbuckettaskboardtaskformat?view=graph-rest-beta) <br />[plannerProgressTaskBoardTaskFormat](/graph/api/resources/plannerprogresstaskboardtaskformat?view=graph-rest-beta) |

### <a name="intune-apis"></a>API de Intune
| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Nuevas entidades agregadas:<br/>[androidForWorkCompliancePolicy](/graph/api/resources/intune-deviceconfig-androidforworkcompliancepolicy?view=graph-rest-beta)<br/>[deviceComplianceSettingState](/graph/api/resources/intune-deviceconfig-devicecompliancesettingstate?view=graph-rest-beta)<br/>[deviceInstallState](/graph/api/resources/intune-books-deviceinstallstate?view=graph-rest-beta)<br/>[deviceManagementScript](/graph/api/resources/intune-deviceconfig-devicemanagementscript?view=graph-rest-beta)<br/>[deviceManagementScriptGroupAssignment](/graph/api/resources/intune-deviceconfig-devicemanagementscriptgroupassignment?view=graph-rest-beta)<br/>[deviceManagementScriptState](/graph/api/resources/intune-deviceconfig-devicemanagementscriptstate?view=graph-rest-beta)<br/>[eBookGroupAssignment](/graph/api/resources/intune-books-ebookgroupassignment?view=graph-rest-beta)<br/>[iosVppEBook](/graph/api/resources/intune-books-iosvppebook?view=graph-rest-beta)<br/>[managedEBook](/graph/api/resources/intune-books-managedebook?view=graph-rest-beta)<br/>[userInstallStateSummary](/graph/api/resources/intune-books-userinstallstatesummary?view=graph-rest-beta)<br/>[windowsManagementApp](/graph/api/resources/intune-deviceconfig-windowsmanagementapp?view=graph-rest-beta)<br/>[windowsManagementAppHealthState](/graph/api/resources/intune-deviceconfig-windowsmanagementapphealthstate?view=graph-rest-beta)<br/> |
| Adición        | Beta        | Nuevos tipos complejos agregados:<br/>[dailySchedule](/graph/api/resources/intune-deviceconfig-dailyschedule?view=graph-rest-beta)<br/>[hourlySchedule](/graph/api/resources/intune-deviceconfig-hourlyschedule?view=graph-rest-beta)<br/>[iosBookmark](/graph/api/resources/intune-deviceconfig-iosbookmark?view=graph-rest-beta)<br/>[iosWebContentFilterAutoFilter](/graph/api/resources/intune-deviceconfig-ioswebcontentfilterautofilter?view=graph-rest-beta)<br/>[iosWebContentFilterBase](/graph/api/resources/intune-deviceconfig-ioswebcontentfilterbase?view=graph-rest-beta)<br/>[iosWebContentFilterSpecificWebsitesAccess](/graph/api/resources/intune-deviceconfig-ioswebcontentfilterspecificwebsitesaccess?view=graph-rest-beta)<br/>[runSchedule](/graph/api/resources/intune-deviceconfig-runschedule?view=graph-rest-beta)<br/>[sharedAppleDeviceUser](/graph/api/resources/intune-deviceconfig-sharedappledeviceuser?view=graph-rest-beta)<br/>[windows10NetworkProxyServer](/graph/api/resources/intune-deviceconfig-windows10networkproxyserver?view=graph-rest-beta)<br/> |
| Adición        | Beta        | Se agregó la acción [requestRemoteAssistance](/graph/api/intune-devices-manageddevice-requestremoteassistance?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la acción [cleanWindowsDevice](/graph/api/intune-devices-manageddevice-cleanwindowsdevice?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la acción [logoutSharedAppleDeviceActiveUser](/graph/api/intune-devices-manageddevice-logoutsharedappledeviceactiveuser?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la acción [deleteUserFromSharedAppleDevice](/graph/api/intune-devices-manageddevice-deleteuserfromsharedappledevice?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la acción [assign](/graph/api/intune-deviceconfig-devicemanagementscript-assign?view=graph-rest-beta) en [deviceManagementScript](/graph/api/resources/intune-deviceconfig-devicemanagementscript?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la acción [syncLicenses](/graph/api/intune-onboarding-applevolumepurchaseprogramtoken-synclicenses?view=graph-rest-beta) en [appleVolumePurchaseProgramToken](/graph/api/resources/intune-apps-applevolumepurchaseprogramtoken?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función **getTopMobileApps** en la colección [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función [downloadApplePushNotificationCertificateSigningRequest](/graph/api/intune-deviceconfig-applepushnotificationcertificate-downloadapplepushnotificationcertificatesigningrequest?view=graph-rest-beta) en [applePushNotificationCertificate](/graph/api/resources/intune-deviceconfig-applepushnotificationcertificate?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función [getDeviceComplianceSettingStates](/graph/api/intune-deviceconfig-devicemanagement-getdevicecompliancesettingstates?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función [deviceConfigurationUserActivity](/graph/api/intune-deviceconfig-reportroot-deviceconfigurationuseractivity?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta) |
| Adición        | Beta        | Se agregó la función [deviceConfigurationDeviceActivity](/graph/api/intune-deviceconfig-reportroot-deviceconfigurationdeviceactivity?view=graph-rest-beta) en [reportRoot](/graph/api/resources/intune-deviceconfig-reportroot?view=graph-rest-beta) |
| Eliminación        | Beta        | Se quitaron los tipos complejos siguientes:<br/>**enterpriseCloudResource**<br/>**windowsInformationProtectionAppRule**<br/>**windowsInformationProtectionAppRuleAppLockerPolicyFileTemplate**<br/>**windowsInformationProtectionAppRuleDesktopTemplate**<br/>**windowsInformationProtectionAppRuleStoreAppTemplate**<br/>**windowsInformationProtectionAppRuleTemplate**<br/>**windowsInformationProtectionCorporateNetworkLocation**<br/>**windowsInformationProtectionProtectedLocation**<br/>**windowsInformationProtectionProtectedLocationEnterpriseCloudResources**<br/>**windowsInformationProtectionProtectedLocationEnterpriseInternalProxyServers**<br/>**windowsInformationProtectionProtectedLocationEnterpriseIPv4Ranges**<br/>**windowsInformationProtectionProtectedLocationEnterpriseIPv6Ranges**<br/>**windowsInformationProtectionProtectedLocationEnterpriseNetworkDomainNames**<br/>**windowsInformationProtectionProtectedLocationEnterpriseProxyServers**<br/>**windowsInformationProtectionProtectedLocationNeutralResources**<br/> |
| Cambio          | Beta        | Se agregó la propiedad **deviceSharingAllowed** a la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio          | Beta        | Se quitó la propiedad **deviceSharingBlocked** de la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **minimumRequiredSdkVersion** a la entidad [defaultManagedAppProtection](/graph/api/resources/intune-mam-defaultmanagedappprotection?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **windowsManagementAppEnabled** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **notificationTemplateId** a la entidad [deviceComplianceActionItem](/graph/api/resources/intune-deviceconfig-devicecomplianceactionitem?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **excludeGroup** a la entidad [deviceConfigurationGroupAssignment](/graph/api/resources/intune-deviceconfig-deviceconfigurationgroupassignment?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambiaron las propiedades siguientes en la entidad [iosCustomConfiguration](/graph/api/resources/intune-deviceconfig-ioscustomconfiguration?view=graph-rest-beta):<br/>**payloadFileName** de required a optional<br/> |
| Cambio          | Beta        | Se agregó la propiedad **contentFilterSettings** a la entidad [iosDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-iosdevicefeaturesconfiguration?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregaron las propiedades **cellularBlockPersonalHotspot** y **passcodeBlockFingerprintModification** a la entidad [iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **minimumRequiredSdkVersion** a la entidad [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambiaron las propiedades siguientes en la entidad [macOSCustomConfiguration](/graph/api/resources/intune-deviceconfig-macoscustomconfiguration?view=graph-rest-beta):<br/>**payloadFileName** de required a optional<br/> |
| Cambio          | Beta        | Se agregaron las propiedades **disableAppPinIfDevicePinIsSet**, **minimumRequiredOsVersion**, **minimumWarningOsVersion**, **minimumRequiredAppVersion** y **minimumWarningAppVersion** a la entidad [managedAppProtection](/graph/api/resources/intune-mam-managedappprotection?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregaron las propiedades **remoteAssistanceSessionUrl**, **isEncrypted**, **model** y **manufacturer** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambiaron las propiedades siguientes de la entidad [getMobileAppCount](/graph/api/intune-apps-mobileapp-getmobileappcount?view=graph-rest-beta):<br/>**bindingParameter** de **mobileApp** a una **colección** de *mobileApp*<br/>**estado** de un GUID a una cadena<br/> |
| Cambio          | Beta        | Se agregó la propiedad **vpnConfigurationId** a la entidad [mobileAppGroupAssignment](/graph/api/resources/intune-apps-mobileappgroupassignment?view=graph-rest-beta) |
| Cambio          | Beta        | Se quitó la propiedad **fromEmailAddress** de la entidad [notificationMessageTemplate](/graph/api/resources/intune-deviceconfig-notificationmessagetemplate?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **excludedApps** a la entidad [officeSuiteApp](/graph/api/resources/intune-apps-officesuiteapp?view=graph-rest-beta) |
| Cambio          | Beta        | Se quitó la propiedad **excludedOfficeApps** de la entidad [officeSuiteApp](/graph/api/resources/intune-apps-officesuiteapp?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **enabled** a la entidad [sharedPCConfiguration](/graph/api/resources/intune-deviceconfig-sharedpcconfiguration?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregaron las propiedades **networkProxyApplySettingsDeviceWide**, **networkProxyDisableAutoDetect**, **networkProxyAutomaticConfigurationUrl**, **networkProxyServer**, **bluetoothDeviceName**, **wiFiScanInterval**, **wirelessDisplayBlockProjectionToThisDevice**, **wirelessDisplayBlockUserInputFromReceiver**, **wirelessDisplayRequirePinForPairing**, **experienceBlockDeviceDiscovery**, **experienceBlockErrorDialogWhenNoSIM**, **experienceBlockTaskSwitcher**, **startMenuPinnedFolderDocuments**, **startMenuPinnedFolderDownloads**, **startMenuPinnedFolderFileExplorer**, **startMenuPinnedFolderHomeGroup**, **startMenuPinnedFolderMusic**, **startMenuPinnedFolderNetwork**, **startMenuPinnedFolderPersonalFolder**, **startMenuPinnedFolderPictures**, **startMenuPinnedFolderSettings**, **startMenuPinnedFolderVideos**, **startMenuAppListVisibility**, **startMenuHideFrequentlyUsedApps**, **startMenuHideRecentJumpLists**, **startMenuHideRecentlyAddedApps**, **startMenuHideRestartOptions**, **startMenuHideUserTile**, **startMenuHidePowerButton**, **startMenuLayoutEdgeAssetsXml**, **personalizationDesktopImageUrl** y **personalizationLockScreenImageUrl** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambió el tipo de las propiedades siguientes en la entidad [windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-beta):<br/>**productCode** de Guid a String<br/> |
| Cambio          | Beta        | Se cambiaron las propiedades siguientes en la entidad [windowsPhone81AppX](/graph/api/resources/intune-apps-windowsphone81appx?view=graph-rest-beta):<br/>**phoneProductIdentifier** de required a optional<br/>**phonePublisherId** de required a optional<br/> |
| Cambio          | Beta        | Se cambiaron las propiedades siguientes en la entidad [windowsPhone81AppXBundle](/graph/api/resources/intune-apps-windowsphone81appxbundle?view=graph-rest-beta):<br/>**appXPackageInformationList** de required a optional<br/> |
| Cambio          | Beta        | Se agregaron las propiedades **productKey** y **licenseType** a la entidad [windowsStoreForBusinessApp](/graph/api/resources/intune-apps-windowsstoreforbusinessapp?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregó la propiedad **previewBuildSetting** a la entidad [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregaron las propiedades de navegación **windowsManagementApp** y **managedEBooks** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregaron las propiedades de navegación **deviceManagementScripts**, **managedDeviceOverview** y **cloudPkiSubscriptions** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregaron las propiedades **osMinimumVersion** y **osMaximumVersion** al tipo complejo [deviceEnrollmentPlatformRestrictions](/graph/api/resources/intune-onboarding-deviceenrollmentplatformrestrictions?view=graph-rest-beta) |
| Cambio          | Beta        | Se agregaron las propiedades **isSharedDevice** y **sharedDeviceCachedUsers** al tipo complejo [hardwareInformation](/graph/api/resources/intune-deviceconfig-hardwareinformation?view=graph-rest-beta) |
| Cambio          | Beta        | Se cambiaron las propiedades siguientes en el tipo complejo [omaSettingBase64](/graph/api/resources/intune-deviceconfig-omasettingbase64?view=graph-rest-beta):<br/>**fileName** de required a optional<br/> |
| Cambio          | Beta        | Se cambiaron las propiedades siguientes en el tipo complejo [omaSettingStringXml](/graph/api/resources/intune-deviceconfig-omasettingstringxml?view=graph-rest-beta):<br/>**fileName** de required a optional<br/> |

## <a name="march-2017"></a>Marzo de 2017

### <a name="intune-apis"></a>API de Intune

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Nuevas entidades agregadas:<br/>[androidForWorkApp](/graph/api/resources/intune-apps-androidforworkapp?view=graph-rest-beta)<br/>[androidForWorkAppConfigurationSchema](/graph/api/resources/intune-androidforwork-androidforworkappconfigurationschema?view=graph-rest-beta)<br/>[androidForWorkSettings](/graph/api/resources/intune-androidforwork-androidforworksettings?view=graph-rest-beta)<br/>[androidForWorkVpnConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkvpnconfiguration?view=graph-rest-beta)<br/>[applePushNotificationCertificate](/graph/api/resources/intune-deviceconfig-applepushnotificationcertificate?view=graph-rest-beta)<br/>[complianceSettingStateSummary](/graph/api/resources/intune-deviceconfig-compliancesettingstatesummary?view=graph-rest-beta)<br/>[deviceCompliancePolicyDeviceStateSummary](/graph/api/resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary?view=graph-rest-beta)<br/>[deviceCompliancePolicyState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicystate?view=graph-rest-beta)<br/>[deviceConfigurationDeviceStateSummary](/graph/api/resources/intune-deviceconfig-deviceconfigurationdevicestatesummary?view=graph-rest-beta)<br/>[deviceConfigurationState](/graph/api/resources/intune-deviceconfig-deviceconfigurationstate?view=graph-rest-beta)<br/>[enterpriseCodeSigningCertificate](/graph/api/resources/intune-apps-enterprisecodesigningcertificate?view=graph-rest-beta)<br/>[iosEduDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosedudeviceconfiguration?view=graph-rest-beta)<br/>[managedDeviceCertificateState](/graph/api/resources/intune-devices-manageddevicecertificatestate?view=graph-rest-beta)<br/>[managedDeviceMobileAppConfigurationDeviceSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicesummary?view=graph-rest-beta)<br/>[managedDeviceMobileAppConfigurationUserSummary](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationusersummary?view=graph-rest-beta)<br/>[mdmWindowsInformationProtectionPolicy](/graph/api/resources/intune-mam?view=graph-rest-betamwindowsinformationprotectionpolicy)<br/>[mobileAppInstallSummary](/graph/api/resources/intune-apps-mobileappinstallsummary?view=graph-rest-beta)<br/>[mobileAppProvisioningConfigGroupAssignment](/graph/api/resources/intune-apps-mobileappprovisioningconfiggroupassignment?view=graph-rest-beta)<br/>[mobileThreatDefenseConnector](/graph/api/resources/intune-onboarding-mobilethreatdefenseconnector?view=graph-rest-beta)<br/>[officeSuiteApp](/graph/api/resources/intune-apps-officesuiteapp?view=graph-rest-beta)<br/>[settingStateDeviceSummary](/graph/api/resources/intune-deviceconfig-settingstatedevicesummary?view=graph-rest-beta)<br/>[softwareUpdateStatusSummary](/graph/api/resources/intune-deviceconfig-softwareupdatestatussummary?view=graph-rest-beta)<br/>[symantecCodeSigningCertificate](/graph/api/resources/intune-apps-symanteccodesigningcertificate?view=graph-rest-beta)<br/>[windowsDefenderAdvancedThreatProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration?view=graph-rest-beta)<br/>[windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta)<br/>[windowsInformationProtectionAppLockerFile](/graph/api/resources/intune-mam-windowsinformationprotectionapplockerfile?view=graph-rest-beta)<br/>[windowsInformationProtectionPolicy](/graph/api/resources/intune-mam-windowsinformationprotectionpolicy?view=graph-rest-beta)<br/>[windowsMobileMSI](/graph/api/resources/intune-apps-windowsmobilemsi?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Nuevos tipos complejos agregados:<br/>[androidForWorkAppConfigurationExample](/graph/api/resources/intune-androidforwork-androidforworkappconfigurationexample?view=graph-rest-beta)<br/>[androidForWorkAppConfigurationExampleJson](/graph/api/resources/intune-androidforwork-androidforworkappconfigurationexamplejson?view=graph-rest-beta)<br/>[androidForWorkAppConfigurationSchemaItem](/graph/api/resources/intune-androidforwork-androidforworkappconfigurationschemaitem?view=graph-rest-beta)<br/>[deviceCompliancePolicySettingState](/graph/api/resources/intune-deviceconfig-devicecompliancepolicysettingstate?view=graph-rest-beta)<br/>[deviceConfigurationSettingState](/graph/api/resources/intune-deviceconfig-deviceconfigurationsettingstate?view=graph-rest-beta)<br/>[deviceExchangeAccessStateSummary](/graph/api/resources/intune-deviceconfig-deviceexchangeaccessstatesummary?view=graph-rest-beta)<br/>[edgeSearchEngine](/graph/api/resources/intune-deviceconfig-edgesearchengine?view=graph-rest-beta)<br/>[edgeSearchEngineBase](/graph/api/resources/intune-deviceconfig-edgesearchenginebase?view=graph-rest-beta)<br/>[edgeSearchEngineCustom](/graph/api/resources/intune-deviceconfig-edgesearchenginecustom?view=graph-rest-beta)<br/>[excludedApps](/graph/api/resources/intune-apps-excludedapps?view=graph-rest-beta)<br/>[iosEduCertificateSettings](/graph/api/resources/intune-deviceconfig-ioseducertificatesettings?view=graph-rest-beta)<br/>[ipRange](/graph/api/resources/intune-deviceconfig-iprange?view=graph-rest-beta)<br/>[windowsInformationProtectionApp](/graph/api/resources/intune-mam-windowsinformationprotectionapp?view=graph-rest-beta)<br/>[windowsInformationProtectionCloudResource](/graph/api/resources/intune-mam-windowsinformationprotectioncloudresource?view=graph-rest-beta)<br/>[windowsInformationProtectionCloudResourceCollection](/graph/api/resources/intune-mam-windowsinformationprotectioncloudresourcecollection?view=graph-rest-beta)<br/>[windowsInformationProtectionDesktopApp](/graph/api/resources/intune-mam-windowsinformationprotectiondesktopapp?view=graph-rest-beta)<br/>[windowsInformationProtectionIPRangeCollection](/graph/api/resources/intune-mam-windowsinformationprotectioniprangecollection?view=graph-rest-beta)<br/>[windowsInformationProtectionResourceCollection](/graph/api/resources/intune-mam-windowsinformationprotectionresourcecollection?view=graph-rest-beta)<br/>[windowsInformationProtectionStoreApp](/graph/api/resources/intune-mam-windowsinformationprotectionstoreapp?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Se agregó la acción [requestSignupUrl](/graph/api/intune-androidforwork-androidforworksettings-requestsignupurl?view=graph-rest-beta) en [androidForWorkSettings](/graph/api/resources/intune-androidforwork-androidforworksettings?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [completeSignup](/graph/api/intune-androidforwork-androidforworksettings-completesignup?view=graph-rest-beta) en [androidForWorkSettings](/graph/api/resources/intune-androidforwork-androidforworksettings?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [syncApps](/graph/api/intune-androidforwork-androidforworksettings-syncapps?view=graph-rest-beta) en [androidForWorkSettings](/graph/api/resources/intune-androidforwork-androidforworksettings?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [unbind](/graph/api/intune-androidforwork-androidforworksettings-unbind?view=graph-rest-beta) en [androidForWorkSettings](/graph/api/resources/intune-androidforwork-androidforworksettings?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [assign](/graph/api/intune-apps-ioslobappprovisioningconfiguration-assign?view=graph-rest-beta) en [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [recoverPasscode](/graph/api/intune-devices-manageddevice-recoverpasscode?view=graph-rest-beta) en [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [removeApplePushNotificationCertificate](/graph/api/intune-onboarding-organization-removeapplepushnotificationcertificate?view=graph-rest-beta) en [organization](/graph/api/resources/intune-onboarding-organization?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateMobileAppIdentifierDeployments](/graph/api/intune-mam-iosmanagedappprotection-updatemobileappidentifierdeployments?view=graph-rest-beta) en [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateMobileAppIdentifierDeployments](/graph/api/intune-mam-androidmanagedappprotection-updatemobileappidentifierdeployments?view=graph-rest-beta) en [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateMobileAppIdentifierDeployments](/graph/api/intune-mam-targetedmanagedappconfiguration-updatemobileappidentifierdeployments?view=graph-rest-beta) en [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateTargetedSecurityGroups](/graph/api/intune-mam-iosmanagedappprotection-updatetargetedsecuritygroups?view=graph-rest-beta) en [iosManagedAppProtection](/graph/api/resources/intune-mam-iosmanagedappprotection?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateTargetedSecurityGroups](/graph/api/intune-mam-androidmanagedappprotection-updatetargetedsecuritygroups?view=graph-rest-beta) en [androidManagedAppProtection](/graph/api/resources/intune-mam-androidmanagedappprotection?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateTargetedSecurityGroups](/graph/api/intune-mam-windowsinformationprotection-updatetargetedsecuritygroups?view=graph-rest-beta) en [windowsInformationProtection](/graph/api/resources/intune-mam-windowsinformationprotection?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateTargetedSecurityGroups](/graph/api/intune-mam-windowsinformationprotection-updatetargetedsecuritygroups?view=graph-rest-beta) en [windowsInformationProtectionPolicy](/graph/api/resources/intune-mam-windowsinformationprotectionpolicy?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateTargetedSecurityGroups](/graph/api/intune-mam?view=graph-rest-betamwindowsinformationprotectionpolicy-updatetargetedsecuritygroups) en [mdmWindowsInformationProtectionPolicy](/graph/api/resources/intune-mam?view=graph-rest-betamwindowsinformationprotectionpolicy) |
| Adición    | Beta    | Se agregó la acción [wipeManagedAppRegistrationByDeviceTag](/graph/api/intune-mam-user-wipemanagedappregistrationbydevicetag?view=graph-rest-beta) en [user](/graph/api/resources/intune-deviceconfig-user?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la función [getTopMobileApps](/graph/api/intune-apps-mobileapp-gettopmobileapps?view=graph-rest-beta) en [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la función [verifyWindowsEnrollmentAutoDiscovery](/graph/api/intune-corpenrollment-devicemanagement-verifywindowsenrollmentautodiscovery?view=graph-rest-beta) en [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta) |
| Eliminación    | Beta    | Se quitaron las entidades siguientes:<br/>**appProvisioningConfigGroupAssignment**<br/>**defaultManagedAppConfiguration**<br/>**enterpriseCertificate**<br/>**managedDeviceMobileAppProvisioningConfigurationDeviceStatus**<br/>**symantecCertificate**<br/>**windows10WindowsInformationProtectionConfiguration**<br/> |
| Eliminación    | Beta    | Se quitaron los tipos complejos siguientes:<br/>**mobileAppInstallSummary**<br/>**windowsArchitecture**<br/>**windowsDeviceType**<br/> |
| Cambio      | Beta    | Se agregó la propiedad **webBrowserBlockPopups** a la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **webBrowserAllowPopups** de la entidad [androidGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-androidgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **appIdentifier** a la entidad [androidStoreApp](/graph/api/resources/intune-apps-androidstoreapp?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **applicationCount**, **failedApplicationCount** y **appInstallFailures** de la entidad [appReportingOverviewStatus](/graph/api/resources/appreportingoverviewstatus?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **sharedIPadMaximumUserCount** y **enableSharedIPad** a la entidad [depEnrollmentProfile](/graph/api/resources/intune-corpenrollment-depenrollmentprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **shareTokenWithSchoolDataSyncService** y **lastSyncErrorCode** a la entidad [depOnboardingSetting](/graph/api/resources/intune-onboarding-deponboardingsetting?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceComplianceDeviceOverview](/graph/api/resources/intune-deviceconfig-devicecompliancedeviceoverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **numberOfPendingDevices**, **numberOfSucceededDevices**, **numberOfErrorDevices**, **numberOfFailedDevices**, **lastUpdateTime** y **policyRevision** de la entidad [deviceComplianceDeviceOverview](/graph/api/resources/intune-deviceconfig-devicecompliancedeviceoverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceComplianceUserOverview](/graph/api/resources/intune-deviceconfig-devicecomplianceuseroverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **numberOfPendingUsers**, **numberOfSucceededUsers**, **numberOfErrorUsers**, **numberOfFailedUsers**, **lastUpdateTime** y **policyRevision** de la entidad [deviceComplianceUserOverview](/graph/api/resources/intune-deviceconfig-devicecomplianceuseroverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceConfigurationDeviceOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationdeviceoverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **numberOfPendingDevices**, **numberOfSucceededDevices**, **numberOfErrorDevices**, **numberOfFailedDevices**, **lastUpdateTime** y **policyRevision** de la entidad [deviceConfigurationDeviceOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationdeviceoverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceConfigurationUserOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationuseroverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **numberOfPendingUsers**, **numberOfSucceededUsers**, **numberOfErrorUsers**, **numberOfFailedUsers**, **lastUpdateTime** y **policyRevision** de la entidad [deviceConfigurationUserOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationuseroverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **subscriptionState** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **managedEmailProfileRequired** a la entidad [iosCompliancePolicy](/graph/api/resources/intune-deviceconfig-ioscompliancepolicy?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **appsSingleAppModeList** a la entidad [iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **appsSingleAppModeBundleIds** de la entidad [iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **expirationDateTime** a la entidad [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **expiration** de la entidad [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **passwordMinimumCharacterSetCount**, **osMinimumVersion**, **osMaximumVersion**, **deviceThreatProtectionEnabled**, **deviceThreatProtectionRequiredSecurityLevel** y **storageRequireEncryption** a la entidad [macOSCompliancePolicy](/graph/api/resources/intune-deviceconfig-macoscompliancepolicy?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **manifest** de la entidad [managedAndroidLobApp](/graph/api/resources/intune-apps-managedandroidlobapp?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **isSupervised**, **exchangeLastSuccessfulSyncDateTime**, **exchangeAccessState** y **exchangeAccessStateReason** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **deviceExchangeAccessStateSummary** a la entidad [managedDeviceOverview](/graph/api/resources/intune-devices-manageddeviceoverview?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **manifest** de la entidad [managedIOSLobApp](/graph/api/resources/intune-apps-managedioslobapp?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **installSummary** de la entidad [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **uploadState** a la entidad [mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambiaron las propiedades siguientes de la entidad [mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-beta):<br/>**azureStorageUriExpirationDateTime** de required a optional<br/> |
| Cambio      | Beta    | Se agregaron las propiedades **initiatedByUserPrincipalName**, **deviceOwnerUserPrincipalName**, **deviceIMEI** y **actionState** a la entidad [remoteActionAudit](/graph/api/resources/intune-deviceconfig-remoteactionaudit?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **oneDriveDisableFileSync**, **safeSearchFilter**, **edgeSearchEngine**, **settingsBlockSettingsApp**, **settingsBlockSystemPage**, **settingsBlockDevicesPage**, **settingsBlockNetworkInternetPage**, **settingsBlockPersonalizationPage**, **settingsBlockAccountsPage**, **settingsBlockTimeLanguagePage**, **settingsBlockEaseOfAccessPage**, **settingsBlockPrivacyPage**, **settingsBlockUpdateSecurityPage**, **experienceBlockWindowsSpotlight**, **experienceBlockWindowsTips**, **experienceBlockConsumerSpecificFeatures**, **startMenuLayoutXml**, **startMenuMode**, **logonBlockFastUserSwitching** y **startBlockUnpinningAppsFromTaskbar** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **allowPrinting**, **allowScreenCapture** y **allowTextSuggestion** a la entidad [windows10SecureAssessmentConfiguration](/graph/api/resources/intune-deviceconfig-windows10secureassessmentconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **blockPrinting**, **blockScreenCapture** y **blockTextSuggestion** de la entidad [windows10SecureAssessmentConfiguration](/graph/api/resources/intune-deviceconfig-windows10secureassessmentconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **identityName** a la entidad [windowsAppX](/graph/api/resources/intune-apps-windowsappx?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambió el tipo de las propiedades siguientes en la entidad [windowsAppX](/graph/api/resources/intune-apps-windowsappx?view=graph-rest-beta):<br/>**applicableArchitectures** de [windowsArchitecture](/graph/api/resources/windowsarchitecture?view=graph-rest-beta) a String<br/> |
| Cambio      | Beta    | Se agregó la propiedad **identityName** a la entidad [windowsPhone81AppX](/graph/api/resources/intune-apps-windowsphone81appx?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambió el tipo de las propiedades siguientes en la entidad [windowsPhone81AppX](/graph/api/resources/intune-apps-windowsphone81appx?view=graph-rest-beta):<br/>**applicableArchitectures** de [windowsArchitecture](/graph/api/resources/windowsarchitecture?view=graph-rest-beta) a String<br/> |
| Cambio      | Beta    | Se agregaron las propiedades **identityName**, **identityPublisherHash** y **identityResourceIdentifier** a la entidad [windowsUniversalAppX](/graph/api/resources/intune-apps-windowsuniversalappx?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambió el tipo de las propiedades siguientes en la entidad [windowsUniversalAppX](/graph/api/resources/intune-apps-windowsuniversalappx?view=graph-rest-beta):<br/>**applicableArchitectures** de [windowsArchitecture](/graph/api/resources/windowsarchitecture?view=graph-rest-beta) a String<br/>**applicableDeviceTypes** de [windowsDeviceType](/graph/api/resources/windowsdevicetype?view=graph-rest-beta) a String<br/> |
| Cambio      | Beta    | Se agregó la propiedad **restartMode** a la entidad [windowsUpdateForBusinessConfiguration](/graph/api/resources/intune-deviceconfig-windowsupdateforbusinessconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [androidForWorkScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkscepcertificateprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [androidScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidscepcertificateprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **enterpriseCodeSigningCertificates**, **symantecCodeSigningCertificate**, **sideLoadingKeys**, **managedAppPolicies**, **iosManagedAppProtections**, **androidManagedAppProtections**, **defaultManagedAppProtections**, **targetedManagedAppConfigurations**, **mdmWindowsInformationProtectionPolicies**, **windowsInformationProtectionPolicies**, **managedAppRegistrations** y **managedAppStatuses** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades de navegación **appReportingOverview**, **enterpriseCerts** y **symantecCert** de la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **deviceSettingStateSummaries** a la entidad [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **deviceSettingStateSummaries** a la entidad [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **termsAndConditions**, **androidForWorkSettings**, **androidForWorkAppConfigurationSchemas**, **applePushNotificationCertificate**, **softwareUpdateStatusSummary**, **deviceCompliancePolicyDeviceStateSummary**, **complianceSettingStateSummaries**, **deviceConfigurationDeviceStateSummaries** y **mobileThreatDefenseConnectors** a la entidad [deviceManagement](/graph/api/resources/intune-shared-devicemanagement?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades de navegación **teacherRootCertificates**, **teacherIdentityCertificate**, **studentRootCertificates** y **studentIdentityCertificate** de la entidad [iosEducationDeviceConfiguration](/graph/api/resources/intune-deviceconfig-ioseducationdeviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambió el tipo de las propiedades siguientes en la entidad [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta):<br/>**deviceStatuses** de la colección [managedDeviceMobileAppProvisioningConfigurationDeviceStatus](/graph/api/resources/manageddevicemobileappprovisioningconfigurationdevicestatus?view=graph-rest-beta) a la colección [managedDeviceMobileAppConfigurationDeviceStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicestatus?view=graph-rest-beta)<br/>**groupAssignments** de la colección [appProvisioningConfigGroupAssignment](/graph/api/resources/appprovisioningconfiggroupassignment?view=graph-rest-beta) a la colección [mobileAppProvisioningConfigGroupAssignment](/graph/api/resources/intune-apps-mobileappprovisioningconfiggroupassignment?view=graph-rest-beta)<br/> |
| Cambio      | Beta    | Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [iosScepCertificateProfile](/graph/api/resources/intune-deviceconfig-iosscepcertificateprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [macOSScepCertificateProfile](/graph/api/resources/intune-deviceconfig-macosscepcertificateprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **deviceConfigurationStates** y **deviceCompliancePolicyStates** a la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **deviceStatusSummary** y **userStatusSummary** a la entidad [managedDeviceMobileAppConfiguration](/graph/api/resources/intune-apps-manageddevicemobileappconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **installSummary** a la entidad [mobileApp](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad de navegación **sideLoadingKeys** de la entidad [organization](/graph/api/resources/intune-onboarding-organization?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [windows81SCEPCertificateProfile](/graph/api/resources/intune-deviceconfig-windows81scepcertificateprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [windowsPhone81SCEPCertificateProfile](/graph/api/resources/intune-deviceconfig-windowsphone81scepcertificateprofile?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **applicationId**, **appName**, **platformId**, **userFailures** y **deviceFailures** del tipo complejo [appInstallationFailure](/graph/api/resources/intune-apps-appinstallationfailure?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **displayName** al tipo complejo [iosHomeScreenFolderPage](/graph/api/resources/intune-deviceconfig-ioshomescreenfolderpage?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **displayName** al tipo complejo [iosHomeScreenPage](/graph/api/resources/intune-deviceconfig-ioshomescreenpage?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **subjectName**, **description**, **expirationDateTime** y **certificate** al tipo complejo [windowsInformationProtectionDataRecoveryCertificate](/graph/api/resources/intune-mam-windowsinformationprotectiondatarecoverycertificate?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **dataRecoveryCertificate** y **certificateFileName** del tipo complejo [windowsInformationProtectionDataRecoveryCertificate](/graph/api/resources/intune-mam-windowsinformationprotectiondatarecoverycertificate?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **displayName** al tipo complejo [windowsPackageInformation](/graph/api/resources/intune-apps-windowspackageinformation?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambió el tipo de las propiedades siguientes en el tipo complejo [windowsPackageInformation](/graph/api/resources/intune-apps-windowspackageinformation?view=graph-rest-beta):<br/>**applicableArchitecture** de [windowsArchitecture](/graph/api/resources/windowsarchitecture?view=graph-rest-beta) a String<br/> |
| Cambio      | Beta    | Se cambiaron las propiedades siguientes en el tipo complejo [windowsPackageInformation](/graph/api/resources/intune-apps-windowspackageinformation?view=graph-rest-beta):<br/>**applicableArchitecture** de optional a required<br/> |

### <a name="add-contracts-to-microsoft-graph"></a>Agregar contratos a Microsoft Graph

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Nuevo recurso:</br>[contract](/graph/api/resources/contract?view=graph-rest-beta) |

### <a name="add-domain-operations-to-microsoft-graph"></a>Agregar operaciones de dominio a Microsoft Graph

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron funciones en [domains](/graph/api/resources/domain?view=graph-rest-beta).<br/>Nuevas entidades:</br>[domain](/graph/api/resources/domain?view=graph-rest-beta)<br/>[domainDnsRecord](/graph/api/resources/domaindnsrecord?view=graph-rest-beta)<br/>[domainDnsCnameRecord](/graph/api/resources/domaindnscnamerecord?view=graph-rest-beta)<br/>[domainDnsMxRecord](/graph/api/resources/domaindnsmxrecord?view=graph-rest-beta)<br/>[domainDnsSrvRecord](/graph/api/resources/domaindnssrvrecord?view=graph-rest-beta)<br/>[domainDnsTxtRecord](/graph/api/resources/domaindnstxtrecord?view=graph-rest-beta)<br/>[domainDnsUnavailableRecord](/graph/api/resources/domaindnsunavailablerecord?view=graph-rest-beta)<br/>Nuevas acciones:</br>[forceDelete](/graph/api/domain-forcedelete?view=graph-rest-beta)</br>[verify](/graph/api/domain-verify?view=graph-rest-beta) |

### <a name="add-custom-data-to-microsoft-graph-using-schema-extensions"></a>Agregar datos personalizados a Microsoft Graph mediante extensiones de esquema

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Ampliar Microsoft Graph con datos de aplicaciones mediante [extensiones de esquema](extensibility-overview.md#schema-extensions).  Esto es compatible con los siguientes recursos:<br/>unidad administrativa<br/>evento de calendario<br/>dispositivo<br/>grupo<br/>mensaje<br/>organización<br/>contacto personal<br/>publicar<br/>usuario<br/>Vea el ejemplo siguiente:<br/>[Agregar datos personalizados a grupos mediante extensiones de esquema (vista previa)](extensibility-schema-groups.md) |
| Adición        | Beta        | Se ha proporcionado una forma alternativa de crear una definición de extensión de esquema sin necesidad de un dominio personal .com comprobado. Vea las [extensiones de esquema](extensibility-overview.md#schema-extensions) para obtener más información. |

### <a name="add-custom-data-to-microsoft-graph-using-open-extensions"></a>Agregar datos personalizados a Microsoft Graph mediante extensiones abiertas

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Cambio          | V1.0 y beta | Se cambió el nombre anterior "extensiones de datos de Office 365" por "extensiones abiertas". |
| Adición        | Beta          | Se agregaron recursos que admiten las [extensiones abiertas](extensibility-overview.md#open-extensions): <br/>unidad administrativa<br/>dispositivo<br/>grupo<br/>organización<br/>usuario<br/>Vea el ejemplo siguiente:<br/>[Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](extensibility-open-users.md) |

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó compatibilidad para [restaurar y eliminar permanentemente grupos](/graph/api/resources/directory?view=graph-rest-beta).<br/>Nueva entidad: directorio con la propiedad de navegación deleteditems. |
| Adición        | Beta        | Nueva entidad:</br>[Punto de conexión](/graph/api/resources/endpoint?view=graph-rest-beta) |
| Cambio          | Beta        | Nueva propiedad de navegación de [endpoints](/graph/api/group-list-endpoints?view=graph-rest-beta) en [groups](/graph/api/resources/group?view=graph-rest-beta) |
| Adición        | Beta        | Nueva entidad:</br>[licenseDetails](/graph/api/resources/licensedetails?view=graph-rest-beta) |
| Cambio          | Beta        | Nueva propiedad de navegación [licensedetails](/graph/api/user-list-licensedetails?view=graph-rest-beta) en [users](/graph/api/resources/user?view=graph-rest-beta) |

### <a name="reports-apis"></a>API de informes

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se ha presentado la nueva API de versión preliminar de Informes de Office 365. Puede usarla para obtener informes de uso de cómo usan las personas de su empresa los servicios de Office 365. Por ejemplo, puede identificar quién usa mucho un servicio y alcanza cuotas o quién puede que no necesite una licencia de Office 365. Para obtener más información, vea [report](/graph/api/resources/report?view=graph-rest-beta). |

### <a name="directory-apis"></a>API de directorio

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Nueva entidad:</br>[contract](/graph/api/resources/contract?view=graph-rest-beta) |

## <a name="february-2017"></a>Febrero de 2017

### <a name="intune-apis"></a>API de Intune

| Tipo de cambio | Versión | Descripción                              |
| :---------- | :------ | :--------------------------------------- |
| Adición    | Beta    | Nuevas entidades agregadas:<br/>[androidForWorkCertificateProfileBase](/graph/api/resources/intune-deviceconfig-androidforworkcertificateprofilebase?view=graph-rest-beta)<br/>[androidForWorkEasEmailProfileBase](/graph/api/resources/intune-deviceconfig-androidforworkeasemailprofilebase?view=graph-rest-beta)<br/>[androidForWorkEnterpriseWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkenterprisewificonfiguration?view=graph-rest-beta)<br/>[androidForWorkGmailEasConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkgmaileasconfiguration?view=graph-rest-beta)<br/>[androidForWorkNineWorkEasConfiguration](/graph/api/resources/intune-deviceconfig-androidforworknineworkeasconfiguration?view=graph-rest-beta)<br/>[androidForWorkPkcsCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkpkcscertificateprofile?view=graph-rest-beta)<br/>[androidForWorkScepCertificateProfile](/graph/api/resources/intune-deviceconfig-androidforworkscepcertificateprofile?view=graph-rest-beta)<br/>[androidForWorkTrustedRootCertificate](/graph/api/resources/intune-deviceconfig-androidforworktrustedrootcertificate?view=graph-rest-beta)<br/>[androidForWorkWiFiConfiguration](/graph/api/resources/intune-deviceconfig-androidforworkwificonfiguration?view=graph-rest-beta)<br/>[appleDeviceFeaturesConfigurationBase](/graph/api/resources/intune-deviceconfig-appledevicefeaturesconfigurationbase?view=graph-rest-beta)<br/>[appProvisioningConfigGroupAssignment](/graph/api/resources/intune-apps-appprovisioningconfiggroupassignment?view=graph-rest-beta)<br/>[deviceComplianceUserOverview](/graph/api/resources/intune-deviceconfig-devicecomplianceuseroverview?view=graph-rest-beta)<br/>[deviceConfigurationUserOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationuseroverview?view=graph-rest-beta)<br/>[enterpriseCertificate](/graph/api/resources/intune-apps-enterprisecertificate?view=graph-rest-beta)<br/>[iosEducationDeviceConfiguration](/graph/api/resources/intune-deviceconfig-ioseducationdeviceconfiguration?view=graph-rest-beta)<br/>[macOSDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-macosdevicefeaturesconfiguration?view=graph-rest-beta)<br/>[managedAndroidLobApp](/graph/api/resources/intune-apps-managedandroidlobapp?view=graph-rest-beta)<br/>[managedDeviceMobileAppProvisioningConfigurationDeviceStatus](/graph/api/resources/intune-apps-manageddevicemobileappprovisioningconfigurationdevicestatus?view=graph-rest-beta)<br/>[managedIOSLobApp](/graph/api/resources/intune-apps-managedioslobapp?view=graph-rest-beta)<br/>[managedMobileLobApp](/graph/api/resources/intune-apps-managedmobilelobapp?view=graph-rest-beta)<br/>[symantecCertificate](/graph/api/resources/intune-apps-symanteccertificate?view=graph-rest-beta)<br/>[windowsAppX](/graph/api/resources/intune-apps-windowsappx?view=graph-rest-beta)<br/>[windowsCertificateProfileBase](/graph/api/resources/intune-deviceconfig-windowscertificateprofilebase?view=graph-rest-beta)<br/>[windowsPhone81AppX](/graph/api/resources/intune-apps-windowsphone81appx?view=graph-rest-beta)<br/>[windowsPhone81AppXBundle](/graph/api/resources/intune-apps-windowsphone81appxbundle?view=graph-rest-beta)<br/>[windowsPhoneXAP](/graph/api/resources/intune-apps-windowsphonexap?view=graph-rest-beta)<br/>[windowsUniversalAppX](/graph/api/resources/intune-apps-windowsuniversalappx?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Nuevos tipos complejos agregados:<br/>[airPrintDestination](/graph/api/resources/intune-deviceconfig-airprintdestination?view=graph-rest-beta)<br/>[windowsArchitecture](/graph/api/resources/intune-apps-windowsarchitecture?view=graph-rest-beta)<br/>[windowsDeviceType](/graph/api/resources/intune-apps-windowsdevicetype?view=graph-rest-beta)<br/>[windowsMinimumOperatingSystem](/graph/api/resources/intune-apps-windowsminimumoperatingsystem?view=graph-rest-beta)<br/>[windowsPackageInformation](/graph/api/resources/intune-apps-windowspackageinformation?view=graph-rest-beta)<br/> |
| Adición    | Beta    | Se agregó la acción [assign](/graph/api/intune-apps-ioslobappprovisioningconfiguration-assign?view=graph-rest-beta) a la entidad [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [scheduleActionsForRules](/graph/api/intune-deviceconfig-devicecompliancepolicy-scheduleactionsforrules?view=graph-rest-beta) a la entidad [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la acción [updateTargetedSecurityGroups](/graph/api/intune-mam-targetedmanagedappconfiguration-updatetargetedsecuritygroups?view=graph-rest-beta) a la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta) |
| Adición    | Beta    | Se agregó la función [getScopesForUser](/graph/api/intune-rbac-resourceoperation-getscopesforintune-devices-user?view=graph-rest-beta) a la entidad [resourceOperation](/graph/api/resources/intune-rbac-resourceoperation?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **manifiesto** de la entidad [androidLobApp](/graph/api/resources/intune-apps-androidlobapp?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **assetTagTemplate**, **lockScreenFootnote**, **homeScreenDockIcons** y **homeScreenPages** a la entidad [iosDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-iosdevicefeaturesconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **deviceSharingAssetTagInformation**, **deviceSharingLockScreenFootnote**, **homeScreenLayoutDockIcons** y **homeScreenLayoutPages** de la entidad [iosDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-iosdevicefeaturesconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **appsSingleAppModeBundleIds** a la entidad [iosGeneralDeviceConfiguration](/graph/api/resources/intune-deviceconfig-iosgeneraldeviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **manifiesto** de la entidad [iosLobApp](/graph/api/resources/intune-apps-ioslobapp?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **createdDateTime**, **description**, **lastModifiedDateTime**, **displayName** y **version** a la entidad [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **createdDateTime** y **lastModifiedDateTime** a la entidad [managedAppPolicy](/graph/api/resources/intune-mam-managedapppolicy?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **deviceRegistrationState** de la entidad [managedDevice](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **manifest** a la entidad [mobileAppContentFile](/graph/api/resources/intune-apps-mobileappcontentfile?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **osDescription** y **userName** a la entidad [mobileAppInstallStatus](/graph/api/resources/intune-apps-mobileappinstallstatus?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **deviceType** property de la entidad [mobileAppInstallStatus](/graph/api/resources/intune-apps-mobileappinstallstatus?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambió el tipo de las propiedades siguientes en la entidad [mobileAppInstallStatus](/graph/api/resources/intune-apps-mobileappinstallstatus?view=graph-rest-beta):<br/>**mobileAppInstallStatusValue** de Int32 a String |
| Cambio      | Beta    | Se agregaron las propiedades **targetedSecurityGroupIds** y **targetedSecurityGroupsCount** a la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **numberOfTargetedSecurityGroups** de la entidad [targetedManagedAppConfiguration](/graph/api/resources/intune-mam-targetedmanagedappconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad **id** a la entidad [user](/graph/api/resources/intune-devices-user?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **renewalThresholdPercentage**, **keyStorageProvider**, **subjectNameFormat**, **subjectAlternativeNameType**, **certificateValidityPeriodValue** y **certificateValidityPeriodScale** de la entidad [windows10CertificateProfileBase](/graph/api/resources/intune-deviceconfig-windows10certificateprofilebase?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **renewalThresholdPercentage**, **keyStorageProvider**, **subjectNameFormat**, **subjectAlternativeNameType**, **certificateValidityPeriodValue** y **certificateValidityPeriodScale** de la entidad [windows81CertificateProfileBase](/graph/api/resources/intune-deviceconfig-windows81certificateprofilebase?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitó la propiedad **applyToWindows10Mobile** de la entidad [windowsPhone81GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windowsphone81generalconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **enterpriseCerts**, **iosLobAppProvisioningConfigurations** y **symantecCert** a la entidad [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **userStatusOverview**  a la entidad [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregó la propiedad de navegación **userStatusOverview** a la entidad [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades de navegación **groupAssignments**, **deviceStatuses** y **userStatuses** a la entidad [iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta) |
| Cambio      | Beta    | Se cambió el tipo de las propiedades siguientes en la entidad [windows10VpnConfiguration](/graph/api/resources/intune-deviceconfig-windows10vpnconfiguration?view=graph-rest-beta):<br/>**identityCertificate** de [windows10CertificateProfileBase](/graph/api/resources/intune-deviceconfig-windows10certificateprofilebase?view=graph-rest-beta) a [windowsCertificateProfileBase](/graph/api/resources/intune-deviceconfig-windowscertificateprofilebase?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **deviceComplianceCheckinThresholdDays** e **isScheduledActionEnabled** al tipo complejo [deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **windowsCommercialId** y **windowsCommercialIdLastModifiedTime** del tipo complejo [deviceManagementSettings](/graph/api/resources/intune-deviceconfig-devicemanagementsettings?view=graph-rest-beta) |
| Cambio      | Beta    | Se agregaron las propiedades **bundleID**, **appName**, **publisher**, **enabled** y **showOnLockScreen** al tipo complejo [iosNotificationSettings](/graph/api/resources/intune-deviceconfig-iosnotificationsettings?view=graph-rest-beta) |
| Cambio      | Beta    | Se quitaron las propiedades **bundleIdentifier**, **notificationsEnabled** y **showInLockScreen** del tipo complejo [iosNotificationSettings](/graph/api/resources/intune-deviceconfig-iosnotificationsettings?view=graph-rest-beta) |



## <a name="january-2017"></a>Enero de 2017

### <a name="outlook-calendar"></a>Calendario de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Nueva acción [findMeetingTimes](/graph/api/user-findmeetingtimes?view=graph-rest-1.0) para el recurso [user](/graph/api/resources/user?view=graph-rest-1.0). |
| Adición        | v1.0        | Nuevo tipo complejo [attendeeBase](/graph/api/resources/attendeebase?view=graph-rest-1.0) que consta de una propiedad de tipo para el tipo de asistente. |
| Adición        | v1.0        | Nuevos tipos complejos:<br/>[attendeeAvailability](/graph/api/resources/attendeeavailability?view=graph-rest-1.0)<br/>[locationConstraint](/graph/api/resources/locationconstraint?view=graph-rest-1.0) <br/>[locationConstraintItem](/graph/api/resources/locationconstraintitem?view=graph-rest-1.0)<br/>[meetingTimeSuggestion](/graph/api/resources/meetingtimesuggestion?view=graph-rest-1.0)<br/>[meetingTimeSuggestionsResult](/graph/api/resources/meetingtimesuggestionsresult?view=graph-rest-1.0)<br/>[timeConstraint](/graph/api/resources/timeconstraint?view=graph-rest-1.0)<br/>[timeSlot](/graph/api/resources/timeslot?view=graph-rest-1.0) |
| Cambio          | v1.0        | El tipo complejo [attendee](/graph/api/resources/attendee?view=graph-rest-1.0) ahora se deriva de attendeeBase, que a su vez se deriva de [recipient](/graph/api/resources/recipient?view=graph-rest-1.0). Incluidas las propiedades heredadas, consta de las mismas propiedades **status**, **type** 7 **emailAddress** que antes. |
| Adición        | Beta        | hexColor se agregó al recurso [calendar](/graph/api/resources/calendar?view=graph-rest-beta). |

### <a name="intune-apis"></a>API de Intune

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Nuevas entidades agregadas: <br/>[appReportingOverviewStatus](/graph/api/resources/intune-apps-appreportingoverviewstatus?view=graph-rest-beta)<br/>[deviceComplianceDeviceOverview](/graph/api/resources/intune-deviceconfig-devicecompliancedeviceoverview?view=graph-rest-beta)<br/>[deviceConfigurationDeviceOverview](/graph/api/resources/intune-deviceconfig-deviceconfigurationdeviceoverview?view=graph-rest-beta)<br/>[deviceManagementExchangeOnpremisesPolicy](/graph/api/resources/intune-onboarding-devicemanagementexchangeonpremisespolicy?view=graph-rest-beta)<br/>[iosDeviceFeaturesConfiguration](/graph/api/resources/intune-deviceconfig-iosdevicefeaturesconfiguration?view=graph-rest-beta)<br/>[iosEducationDeviceConfiguration](/graph/api/resources/intune-deviceconfig-ioseducationdeviceconfiguration?view=graph-rest-beta)<br/>[iosLobAppProvisioningConfiguration](/graph/api/resources/intune-apps-ioslobappprovisioningconfiguration?view=graph-rest-beta)<br/>[onpremisesConditionalAccessSettings](/graph/api/resources/intune-onboarding-onpremisesconditionalaccesssettings?view=graph-rest-beta)<br/>[sharedPCConfiguration](/graph/api/resources/intune-deviceconfig-sharedpcconfiguration?view=graph-rest-beta)<br/>[windows10EnterpriseModernAppManagementConfiguration](/graph/api/resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration?view=graph-rest-beta)<br/>[windows10SecureAssessmentConfiguration](/graph/api/resources/intune-deviceconfig-windows10secureassessmentconfiguration?view=graph-rest-beta)<br/>[windows10WindowsInformationProtectionConfiguration](/graph/api/resources/intune-deviceconfig-windows10windowsinformationprotectionconfiguration?view=graph-rest-beta) |
|Adición|Beta|Nuevos tipos complejos agregados: <br/> [appInstallationFailure](/graph/api/resources/intune-apps-appinstallationfailure?view=graph-rest-beta)<br/>[enterpriseCloudResource](/graph/api/resources/intune-deviceconfig-enterprisecloudresource?view=graph-rest-beta)<br/>[iosHomeScreenApp](/graph/api/resources/intune-deviceconfig-ioshomescreenapp?view=graph-rest-beta)<br/>[iosHomeScreenFolder](/graph/api/resources/intune-deviceconfig-ioshomescreenfolder?view=graph-rest-beta)<br/>[iosHomeScreenFolderPage](/graph/api/resources/intune-deviceconfig-ioshomescreenfolderpage?view=graph-rest-beta)<br/>[iosHomeScreenItem](/graph/api/resources/intune-deviceconfig-ioshomescreenitem?view=graph-rest-beta)<br/>[iosHomeScreenPage](/graph/api/resources/intune-deviceconfig-ioshomescreenpage?view=graph-rest-beta)<br/>[iosNotificationSettings](/graph/api/resources/intune-deviceconfig-iosnotificationsettings?view=graph-rest-beta)<br/>[iPv6Range](/graph/api/resources/intune-deviceconfig-ipv6range?view=graph-rest-beta)<br/>[sharedPCAccountManagerPolicy](/graph/api/resources/intune-deviceconfig-sharedpcaccountmanagerpolicy?view=graph-rest-beta)<br/>[windowsInformationProtectionAppRule](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionapprule?view=graph-rest-beta)<br/>[windowsInformationProtectionAppRuleAppLockerPolicyFileTemplate](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionappruleapplockerpolicyfiletemplate?view=graph-rest-beta)<br/>[windowsInformationProtectionAppRuleDesktopTemplate](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionappruledesktoptemplate?view=graph-rest-beta)<br/>[windowsInformationProtectionAppRuleStoreAppTemplate](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionapprulestoreapptemplate?view=graph-rest-beta)<br/>[windowsInformationProtectionAppRuleTemplate](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionappruletemplate?view=graph-rest-beta)<br/>[windowsInformationProtectionCorporateNetworkLocation](/graph/api/resources/intune-deviceconfig-windowsinformationprotectioncorporatenetworklocation?view=graph-rest-beta)<br/>[windowsInformationProtectionDataRecoveryCertificate](/graph/api/resources/intune-deviceconfig-windowsinformationprotectiondatarecoverycertificate?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocation](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocation?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocationEnterpriseCloudResources](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocationenterprisecloudresources?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocationEnterpriseInternalProxyServers](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocationenterpriseinternalproxyservers?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocationEnterpriseIPv4Ranges](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocationenterpriseipv4ranges?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocationEnterpriseIPv6Ranges](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocationenterpriseipv6ranges?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocationEnterpriseNetworkDomainNames](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocationenterprisenetworkdomainnames?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocationEnterpriseProxyServers](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocationenterpriseproxyservers?view=graph-rest-beta)<br/>[windowsInformationProtectionProtectedLocationNeutralResources](/graph/api/resources/intune-deviceconfig-windowsinformationprotectionprotectedlocationneutralresources?view=graph-rest-beta)
|Eliminación|Beta|Se quitaron los tipos complejos siguientes y se reemplazaron por microsoft.graph.Json:<br/>managedAppDeploymentSummary <br/>managedAppSummary<br /> |
|Cambio|Beta|Se reemplazó el tipo de propiedad appConfigComplianceStatus por complianceStatus en las siguientes entidades: <br/>[managedDeviceMobileAppConfigurationDeviceStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicestatus?view=graph-rest-beta)<br/>[managedDeviceMobileAppConfigurationUserStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationuserstatus?view=graph-rest-beta)|
|Cambio|Beta|Para el recurso [managedAppStatusRaw](/graph/api/resources/intune-mam-managedappstatusraw?view=graph-rest-beta), se cambió el contenido de tipo de propiedad de managedAppSummary a Json.|
|Cambio|Beta|Se quitó la función getUsersWithFlaggedAppRegistration de la colección [managedAppRegistration](/graph/api/resources/intune-mam-managedappregistration?view=graph-rest-beta).|
|Cambio|Beta|Se cambió la propiedad de navegación **vppToken** de la entidad [iosVppApp](/graph/api/resources/intune-apps-iosvppapp?view=graph-rest-beta) para que ya no sea una colección contenida.|
|Cambio|Beta|Se agregó la propiedad **deviceStatusOverview** a las entidades [deviceConfiguration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-beta) y [deviceCompliancePolicy](/graph/api/resources/intune-deviceconfig-devicecompliancepolicy?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **appReportingOverview** al singleton [deviceAppManagement](/graph/api/resources/intune-apps-deviceappmanagement?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **deviceDisplayName** y **userPrincipalName** a las entidades [deviceConfigurationDeviceStatus](/graph/api/resources/intune-deviceconfig-deviceconfigurationdevicestatus?view=graph-rest-beta), [deviceComplianceDeviceStatus](/graph/api/resources/intune-deviceconfig-devicecompliancedevicestatus?view=graph-rest-beta) y [managedDeviceMobileAppConfigurationDeviceStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationdevicestatus?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **ruleName** a la entidad [deviceComplianceScheduledActionForRule](/graph/api/resources/intune-deviceconfig-devicecompliancescheduledactionforrule?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **devicesCount**, **userDisplayName** y **userPrincipalName** a las entidades [deviceConfigurationUserStatus](/graph/api/resources/intune-deviceconfig-deviceconfigurationuserstatus?view=graph-rest-beta), [deviceComplianceUserStatus](/graph/api/resources/intune-deviceconfig-devicecomplianceuserstatus?view=graph-rest-beta) y [managedDeviceMobileAppConfigurationUserStatus](/graph/api/resources/intune-apps-manageddevicemobileappconfigurationuserstatus?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la colección [notificationMessageTemplates](/graph/api/resources/intune-notification-notificationmessagetemplate?view=graph-rest-beta) al singleton [deviceManagement](/graph/api/resources/intune-deviceconfig-devicemanagement?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **isDefault**, **lastModifiedDateTime**, **locale**, **messageTemplate** y **subject** a la entidad [localizedNotificationMessage](/graph/api/resources/intune-deviceconfig-localizednotificationmessage?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **azureActiveDirectoryDeviceId**, **deviceCategory**, **deviceRegistrationState** y **managementAgent** a la entidad [managedDevice](/graph/api/resources/intune-onboarding-manageddevice?view=graph-rest-beta).|
|Cambio|Beta|Se agregó la propiedad **lastModifiedDateTime** a la entidad [mobileAppCategory](/graph/api/resources/intune-apps-mobileappcategory?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **brandingOptions**, **defaultLocale**, **displayName**, **fromEmailAddress**, **lastModifiedDateTime**, **localizedNotificationMessages** a la entidad [notificationMessageTemplate](/graph/api/resources/intune-notification-notificationmessagetemplate?view=graph-rest-beta).|
|Cambio|Beta|Se agregaron las propiedades **appsAllowTrustedAppsSideloading**, **appsBlockWindowsStoreOriginatedApps**, **developerUnlockSetting**, **edgeBlockAccessToAboutFlags**, **edgeBlockDeveloperTools**, **edgeBlockExtensions**, **edgeBlockInPrivateBrowsing**, **edgeFirstRunUrl**, **edgeHomepageUrls**, **gameDvrBlocked**, **settingsBlockAddProvisioningPackage**, **settingsBlockChangeLanguage**, **settingsBlockChangePowerSleep**, **settingsBlockChangeRegion**, **settingsBlockChangeSystemTime**, **settingsBlockEditDeviceName**, **settingsBlockRemoveProvisioningPackage**, **sharedUserAppDataAllowed**, **smartScreenBlockPromptOverride**, **smartScreenBlockPromptOverrideForFiles**, **storageRestrictAppDataToSystemVolume**, **storageRestrictAppInstallToSystemVolume**, **webRtcBlockLocalhostIpAddress**, **windowsStoreBlockAutoUpdate** y **windowsStoreEnablePrivateStoreOnly** a la entidad [windows10GeneralConfiguration](/graph/api/resources/intune-deviceconfig-windows10generalconfiguration?view=graph-rest-beta).|

## <a name="december-2016"></a>Diciembre de 2016

### <a name="delta-query"></a>Consulta de delta

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Agregar una nueva función de delta para las siguientes entidades para realizar [consulta de delta](delta-query-overview.md):<br/>contacto<br/>contactFolder<br/>evento<br/>grupo<br/>mailFolder<br/>mensaje<br/>usuario<br/>Vea los ejemplos siguientes:<br/>[Obtener los cambios incrementales de grupos (versión preliminar)](delta-query-groups.md)<br/>[Obtener los cambios incrementales para los mensajes de una carpeta (versión preliminar)](delta-query-messages.md)<br/>[Obtener los cambios incrementales de usuarios (versión preliminar)](delta-query-users.md) |

### <a name="excel-apis"></a>API de Excel

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregaron recurso workbookPivotTable, acción refresh y refreshAll en tablas dinámicas, recurso worbookRangeView, acción visibleView en el intervalo filtrado para devolver workbookRangeView al usuario, obtiene una recopilación de filas y recursos del intervalo de las funciones visibleView, columnsAfter, comunsBefore, resizedRange, rowsAbove y rowsBelow del recurso del intervalo y nuevas propiedades de tablas. |

### <a name="intune-apis"></a>API de Intune

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Recursos agregados y API de método para Microsoft Intune. Este es un conjunto grande de recursos y métodos para admitir la versión preliminar pública de Intune en Azure Portal. Para obtener información sobre el servicio Intune, vea la [documentación de Intune](https://go.microsoft.com/fwlink/?linkid=836405). Para obtener información sobre los recursos y las API de Intune, vea [Trabajar con Intune en Microsoft Graph](/graph/api/resources/intune-graph-overview?view=graph-rest-beta). |

## <a name="october-2016"></a>Octubre de 2016

### <a name="authorization-provider"></a>Proveedor de autorización

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | La versión 2.0 del punto de conexión de autenticación ahora es compatible con la concesión de OAuth client_credentials, que se puede usar para [demonios y procesos de ejecución prolongada en escenarios empresariales](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow). |
| Adición        | V1.0 y beta | La versión 2.0 del punto de conexión de autenticación ahora es compatible con [ámbitos de permisos que requieren el consentimiento del administrador](permissions-reference.md) a través del [punto de conexión de consentimiento de administrador](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent#admin-restricted-permissions). |
| Adición        | V1.0 y beta | La versión 2.0 del punto de conexión de autenticación ahora es compatible con el consentimiento administrativo para todos los usuarios de un inquilino a través del [punto de conexión de consentimiento de administrador](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent#admin-restricted-permissions). |

### <a name="invitation-apis"></a>API de invitación

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la propiedad invitedUserType al tipo de entidad de invitación, que define el tipo de usuario (**Guest** o **Member**) al que se invita. |
| Eliminación        | Beta        | Se quitará la propiedad invitedToGroups del tipo de entidad de invitación el 11/11/2016. Esto quiere decir que ya no se podrá agregar un usuario invitado a un grupo con esta API. En su lugar, para agregar un usuario a un grupo, use la [API para agregar miembros](/graph/api/group-post-members?view=graph-rest-1.0). |

## <a name="september-2016"></a>Septiembre de 2016

### <a name="azure-ad-application-proxy"></a>Proxy de aplicación de Azure AD

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Las API del Proxy de aplicación de Azure AD están ahora disponibles en la versión Beta del punto de conexión de Microsoft Graph. Estas API permiten publicar de forma segura aplicaciones locales para usuarios externos a la red corporativa con Azure AD como plano de control común para el acceso. Puede usar las API publicadas para escribir una aplicación que pueda recuperar y actualizar diversos aspectos del proxy de aplicación como _connectors_, _connectorGroups_ y la configuración de _onPremisesPublishing_ de una aplicación. |

### <a name="drive"></a>Unidad de disco

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la colección _shared_ para permitir el acceso a driveItems por shareId o la URL de uso compartido. |
| Adición        | Beta        | Se agregó la función _search_ a una unidad, que permite buscar más elementos de los que se encuentran en la carpeta raíz de la unidad. |


### <a name="driveitem"></a>DriveItem

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la compatibilidad con _createUploadSession_, que permite subir archivos con un tamaño superior a 4 MB a OneDrive, OneDrive para la Empresa y a bibliotecas de documentos de SharePoint. |
| Adición        | Beta        | Se agregó la propiedad _sharepointIds_ a driveItem, que devuelve identificadores de la API de SharePoint tradicional para driveItems almacenados en SharePoint. |
| Adición        | Beta        | Se agregaron propiedades adicionales en _remoteItem_. |
| Adición        | Beta        | Se agregó el valor _quickXorHash_ para archivos en OneDrive para la Empresa. |
| Adición        | Beta        | Se agregó un ámbito a _createSharingLink_ para permitir la creación de vínculos que se pueden compartir en la compañía o para vínculos que se pueden compartir de forma anónima. |

### <a name="extended-properties"></a>Propiedades extendidas

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Las [propiedades extendidas](/graph/api/resources/extended-properties-overview?view=graph-rest-1.0) ahora son compatibles con los recursos siguientes: message, mailFolder, event, calendar, contact, contactFolder, group event, group calendar, group post. |

### <a name="groups"></a>Grupos

Se agregó soporte para la pertenencia a grupos dinámicos con la API de vista previa pública, incluidos los añadidos listados en la tabla siguiente.

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la propiedad **membershipRule**, que contiene reglas que controlan la pertenencia a este grupo, si el grupo es un grupo dinámico. |
| Adición        | Beta        | Se agregó la propiedad **membershipRuleProcessingState** para controlar si el procesamiento de pertenencia dinámica está activado o pausado para este grupo. |
| Adición        | Beta        | Se estableció la propiedad **groupTypes** para que contenga **DynamicMembership** para activar la función de grupos dinámicos para este grupo. |
| Adición        | Beta        | Se agregó la propiedad **preferredLanguage** para indicar el idioma preferido de un grupo de Office 365. |
| Adición        | Beta        | Se agregó la propiedad **theme** para especificar un tema de color del grupo de Office 365. |

### <a name="hybrid-deployment-support"></a>Compatibilidad con implementaciones híbridas

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Las aplicaciones pueden usar la API de Correo, calendario y contactos de Outlook versión 1.0 para obtener acceso a buzones locales en una implementación híbrida con Exchange 2016 actualización acumulativa 3 (CU3). Encontrará más información sobre la compatibilidad de API de REST en [implementaciones híbridas](hybrid-rest-support.md) específicas. **Nota:** Si utiliza estos conjuntos de API en v1.0, verá ahora que sus aplicaciones, incluidas las aplicaciones de producción, funcionan en buzones locales que cumplan requisitos de implementación híbrida específicos. Esta funcionalidad solo se encuentra en vista previa. |

### <a name="identityriskevents"></a>IdentityRiskEvents

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Como parte del cambio del esquema donde el tipo de dos propiedades de ubicación se reemplaza por un nuevo tipo complejo en el punto de conexión de identityRiskEvents, las propiedades siguientes se modifican o agregan en el punto de conexión de identityRiskEvents:</br>**location**: cambia de Edm.String a ComplexType signInLocation.<br/>**previousLocation**: cambia de Edm.String a ComplexType signInLocation.<br/>**signInLocation**: nuevo ComplexType que contiene las propiedades city, state, countryOrRegion y geoCoordinates.<br/>**geoCoordinates**: nuevo ComplexType que contiene las propiedades latitude y longitude. |

### <a name="invitation-manager"></a>Administrador de invitaciones

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Las API del administrador de invitaciones están ahora disponibles en el punto de conexión beta de Microsoft Graph. Puede usar la API del administrador de invitaciones para crear una invitación con el fin de agregar un usuario externo a la organización. Como parte de la invitación, también puede agregar los usuarios invitados a un grupo de Office 365. Para obtener más información, consulte [Administrador de invitaciones](/graph/api/resources/invitation?view=graph-rest-beta). |

### <a name="onedrive"></a>OneDrive

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó el método **CreateUploadSession** en **driveItem**, que permite subir archivos de gran tamaño y reanudar operaciones de carga. |
| Adición        | v1.0        | Se agregaron propiedades para realizar un seguimiento de id. de SharePoint en elementos de SharePoint (**sharepointIds**) y una propiedad para identificar carpetas raíz (**root**). |
| Adición        | v1.0        | Se agregó la colección raíz **Shares**, que se puede usar con shareIds o con vínculos de uso compartido para obtener acceso a elementos compartidos en OneDrive y SharePoint. Devuelve un nuevo tipo, sharedDriveItem. |
| Adición        | v1.0        | Se agregó el método **Invite** en driveItem, que permite agregar permisos a elementos. |
| Adición        | v1.0        | Se agregó el método **Search** en drive, que permite buscar elementos en la unidad y en elementos compartidos. |
| Adición        | v1.0        | Se agregó la propiedad **processingMetadata** en el tipo complejo de archivos quickXorHash en tipo complejo de hash. |
| Adición        | v1.0        | Propiedad **quickXorHash** en tipo complejo de hash. |

### <a name="outlook-calendar"></a>Calendario de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó la propiedad **onlineMeetingUrl** al recurso [event](/graph/api/resources/event?view=graph-rest-1.0). |
| Adición        | Beta        | Se agregó la acción [forward](/graph/api/event-forward?view=graph-rest-beta) al recurso event. |
| Adición        | Beta        | Se agregaron propiedades al recurso [calendar](/graph/api/resources/calendar?view=graph-rest-beta) para admitir el uso compartido de calendarios: **canEdit**, **canShare**, **canViewPrivateItems**, **isShared**, **isShareWithMe**, **owner**. |

### <a name="outlook-mail"></a>Correo de Outlook

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó el tipo complejo [mailboxSettings](/graph/api/resources/mailboxsettings?view=graph-rest-1.0), que incluye las propiedades **automaticRepliesSetting**, **timeZone** y **language**. |
| Adición        | v1.0        | Se agregó la propiedad **mailboxSettings** al recurso [user](/graph/api/resources/user?view=graph-rest-1.0). |
| Adición        | Beta        | Se agregó la compatibilidad para crear, generar listas, obtener y eliminar una o más instancias de una [mención](/graph/api/resources/mention?view=graph-rest-beta) en un mensaje. Las menciones admiten las llamadas para captar la atención de otros usuarios en un mensaje. |
| Adición        | Beta        | Se agregó la compatibilidad con la acción [getMailTips](/graph/api/user-getmailtips?view=graph-rest-beta) para obtener las sugerencias de correo electrónico para destinatarios específicos. Se agregaron los siguientes recursos: [automaticRepliesMailTips](/graph/api/resources/automaticrepliesmailtips?view=graph-rest-beta), [mailTips](/graph/api/resources/mailtips?view=graph-rest-beta) y [mailTipsError](/graph/api/resources/mailtipserror?view=graph-rest-beta). |

### <a name="query-parameters"></a>Parámetros de consulta

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | Se admiten los parámetros de consulta sin prefijos "$" desde el 26/09/16. El prefijo "$" en parámetros de consulta es opcional. Para obtener más detalles, consulte la publicación de blog [Compatibilidad con los parámetros de consulta sin el prefijo "$" en Microsoft Graph](https://dev.office.com/queryparametersinMicrosoftGraph). |

### <a name="sharepoint"></a>SharePoint

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Acceso a sitios de SharePoint y [listado por id.](/graph/api/list-get?view=graph-rest-beta) o [ruta/URL](/graph/api/baseitem-getbyurl?view=graph-rest-beta). |
| Adición        | Beta        | Compatibilidad con la [generación de listas, creación, obtención y eliminación de instancias de listItem](/graph/api/resources/listitem?view=graph-rest-beta). |

### <a name="users"></a>Usuarios

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la propiedad de solo lectura **refreshTokensValidFromDateTime** para indicar desde cuándo son válidos los tokens de actualización o sesión. Los tokens emitidos anteriormente no son válidos y cualquier intento de usarlos obligaría al usuario a volver a iniciar sesión. |
| Adición        | Beta        | Se agregó la propiedad **showInAddressList** para controlar si la lista global de direcciones de Outlook tiene que contener este usuario. |
| Adición        | Beta        | Se agregó la acción de servicio **invalidateAllRefreshTokens**, que invalida todos los tokens de actualización y de sesión del usuario emitidos a las aplicaciones, al restablecer la propiedad de usuario **refreshTokensValidFromDateTime** a la fecha y hora actuales. |


### <a name="webhooks"></a>Webhooks

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron elementos raíz de Drive a webhooks como un recurso al que se puede suscribir. |

## <a name="august-2016"></a>Agosto de 2016

### <a name="contacts"></a>Contactos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Como parte del cambio del esquema donde algunas propiedades se quitan y las colecciones correspondientes se agregan al punto de conexión de contactos, las propiedades siguientes se agregan al punto de conexión de contactos: _Websites Collection(ComplexType: Website)_,_Phones Collection (ComplexType: Phone)_, _PostalAddress Collection(ComplexType: PhysicalAddress)_. Para obtener más información, vea la entrada del blog [Cambios próximos a las API de Contactos y Personas](https://developer.microsoft.com/office/blogs/upcoming-changes-to-contacts-and-people-apis/). |
| Eliminación        | Beta        | Como parte del cambio del esquema donde algunas propiedades se quitan y las colecciones correspondientes se agregan al punto de conexión de contactos, las propiedades siguientes se quitan del punto de conexión de contactos: _BusinessHomePage_,_HomePhones_, _MobilePhone1_, _BusinessPhones_, _HomeAddress_, _BusinessAddress_, _OtherAddress_. Para obtener más información, vea la entrada del blog [Cambios próximos a las API de Contactos y Personas](https://developer.microsoft.com/office/blogs/upcoming-changes-to-contacts-and-people-apis/). |

### <a name="excel-apis"></a>API de Excel

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | La API de REST de Excel en Microsoft Graph ya está disponible. Ahora, se pueden crear integraciones complejas y avanzadas con libros de Excel en Office 365. Vea la entrada del blog [Potencie sus aplicaciones con la nueva API de REST de Excel en Microsoft Graph](https://developer.microsoft.com/office/blogs/power-your-apps-with-the-new-excel-rest-api/) para obtener más información. |

### <a name="people"></a>Contactos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio          | Beta        | La propiedad _WebSite_ cambia de nombre por _Websites_. Para obtener más información, vea [Cambios próximos a las API de Contactos y Personas](https://developer.microsoft.com/office/blogs/upcoming-changes-to-contacts-and-people-apis/). |

### <a name="privileged-identity-management"></a>Privileged Identity Management

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Las API de REST de Privileged Identity Management (PIM) ahora están disponibles en el punto de conexión beta de Microsoft Graph. [Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-configure) ofrece la activación Just-In-Time para roles organizativos de Azure AD con privilegios, como Administrador global, Administrador de facturación, etc. Puede usar las API publicadas para escribir aplicaciones que recuperen y actualicen asignaciones de roles con privilegios y activar usuarios en roles. Para obtener más información, consulte [Microsoft Graph: versión preliminar de API Privileged Identity Management de Azure AD disponibles en beta](https://developer.microsoft.com/office/blogs/microsoft-graph-azure-ad-privileged-identity-management-apis-beta/) y [Privileged Identity Management de Azure AD](/graph/api/resources/privilegedidentitymanagement-root?view=graph-rest-beta). |

## <a name="july-2016"></a>Julio de 2016

### <a name="administrative-units"></a>Unidades administrativas

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se introdujo la nueva API en versión preliminar de unidades administrativas. Las unidades administrativas permiten a las organizaciones subdividir Azure Active Directory y delegar tareas administrativas en dichas subdivisiones. Las subdivisiones pueden representar regiones, departamentos, centros de costes, etc. Esto puede administrarse ahora mediante la API de Microsoft Graph. |

## <a name="june-2016"></a>Junio de 2016

### <a name="identityriskevents"></a>IdentityRiskEvents

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se introdujo la nueva API en versión preliminar IdentityRiskEvents. Esta API funciona junto con la protección de identidad de Azure Active Directory. Se puede usar para eventos de riesgo de consulta generados por Identity Protection. Para más información, consulte [Introducción de la nueva API de vista previa en Microsoft Graph: IdentityRiskEvents](https://developer.microsoft.com/office/blogs/identityriskevents-api-preview/).

### <a name="subscriptions"></a>Suscripciones

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Los ámbitos de solo aplicación ahora son compatibles con las suscripciones de _correo_ y _contactos_. |

## <a name="may-2016"></a>Mayo de 2016

### <a name="calendar"></a>Calendario

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio importante|Beta|Cambios en la API findMeetingTimes. Para obtener más información, consulte la publicación de blog [Actualización de la API findMeetingTimes de Microsoft Graph](https://dev.office.com/microsoft-graph-findmeetingtimes-api-update). Este cambio entró en vigor el 19 de mayo de 2016.

### <a name="contact"></a>Contacto

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó _extensions_, que es un tipo abstracto, para permitir la compatibilidad con OData v4 Open Type openTypeExtension. |

### <a name="directory"></a>Directorio

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Cambio importante | Beta        | Se cambió el nombre de _settingTemplateId_ a _templateId_. Este cambio tendrá efecto el 19 de mayo de 2016. |

### <a name="event"></a>Evento

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó _extensions_, que es un tipo abstracto, para permitir la compatibilidad con OData v4 Open Type openTypeExtension. |

### <a name="eventmessages"></a>EventMessages

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregaron _inferenceClassification_ y _extensions_ a _eventMessages_. |
| Adición        | Beta        | Se agregó _responseRequested_ a _eventMessageRequest_. |

### <a name="messages"></a>Mensajes

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregaron _inferenceClassification_ y _extensions_ a _messages_. |
| Adición        | Beta        | Se agregó _wellknownname_ a _contactFolder_. |

### <a name="post"></a>Publicación

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó _extensions_, que es un tipo abstracto, para permitir la compatibilidad con OData v4 Open Type openTypeExtension. |

### <a name="user"></a>Usuario

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó el tipo de recurso _inferenceClassification_. |
| Adición        | Beta        | Se agregó _timeZone_ a _mailboxsettings_.   |
| Adición        | Beta        | Se agregó _findMeetingTimes_ de API a _user_.   |

## <a name="april-2016"></a>Abril de 2016

### <a name="general"></a>General

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | Se agregó compatibilidad para respetar _Accept-Encoding:gzip_. |
| Adición        | v1.0          | Agregada compatibilidad con el segmento de transmisión en la ruta de acceso de $expand. Por ejemplo, "https://graph.microsoft.com/v1.0/me/messages?$expand=microsoft.graph.eventMessage/event". |
| Adición        | Beta          | Se agregó compatibilidad con la solicitud PATCH en propiedades estructurales. Por ejemplo: 'PATCH /me/mailboxSettings'. |
| Adición        | Beta          | Azure Active Directory ahora se usa como una reserva para solicitudes de /beta/users/id/photo cuando Outlook no puede procesar las solicitudes (por ejemplo, si el usuario no tiene una licencia de buzón o si el espacio empresarial no tiene una suscripción a Exchange Online). NOTA: Esta reserva está disponible para GET y PATCH. |
| Adición        | Beta          | Agregada compatibilidad con el segmento de transmisión en la ruta de acceso de $expand. Por ejemplo: "https://graph.microsoft.com/v1.0/me/messages?$expand=microsoft.graph.eventMessage/event". |

### <a name="onedrive"></a>OneDrive

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Solución             | v1.0        | Se solucionó el problema en el que las solicitudes de createLink de OneDrive producían el error 500 y el error "Tipo de propiedad de extensión no admitida". |

## <a name="march-2016"></a>Marzo de 2016

### <a name="calendar"></a>Calendario

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_. |
| Adición        | Beta        | Se agregó la propiedad _suggestionHint_ a _meetingTimeCandidate_. |
| Adición        | Beta        | Se agregó la propiedad _locationUri_ a _location_. |
| Adición        | Beta        | Se agregaron _type_ y _postOfficeBox_ a _physicalAddress_. |
| Cambio          | Beta        | _findMeetingTimes_ acepta ahora el nuevo parámetro _ReturnSuggestionHints_. |
| Cambio          | Beta        | _findMeetingTimes_ devuelve ahora una colección de _meetingTimeCandidate_. |

### <a name="drive"></a>Unidad de disco

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | Se agregó la función _recent_ para hacer una lista de un conjunto de elementos usados recientemente por el usuario que ha iniciado sesión. Esta lista incluye elementos que están en la unidad de disco del usuario, así como elementos de otras unidades de disco a los que tiene acceso. Ejemplo: GET /me/drive/recent. |
| Adición        | V1.0 y beta | Se agregó la función _sharedWithMe_ para hacer una lista de un conjunto de elementos que se comparten actualmente con el usuario actual. Ejemplo: GET /me/drive/sharedWithMe. |

### <a name="driveitem"></a>DriveItem

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | Se agregó el tipo _remoteItem_ que proporciona un vínculo a un elemento en otra unidad de disco. |
| Adición        | V1.0 y beta | Se agregó el tipo _sharingInvitation_ que proporciona detalles de cualquier invitación para uso compartido asociada a este permiso. |
| Adición        | V1.0 y beta | Se agregó la función _delta_ para el control de cambios a elementos de una unidad de disco. Ejemplo: GET /me/drive/items/{item-id}/delta |
| Adición        | V1.0 y beta | Se agregó _copy_, que crea una copia de un _driveItem_ (incluidos los elementos secundarios), en un nuevo elemento primario o con un nuevo nombre. Ejemplo: POST /me/drive/items/{item-id}/copy. |
| Adición        | V1.0 y beta | Los atributos de la instancia _conflictBehavior_ son ahora aplicables a _driveItem_. |
|Adición|Beta|Se agregó la función _invite_ para enviar una invitación para uso compartido a un elemento existente. Una invitación para uso compartido crea un enlace único para compartir y envía un correo al destinatario de la invitación que incluye el vínculo para compartir. Ejemplo: POST /drive/items/{item-id}/invite.

### <a name="event"></a>Evento

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron una nueva propiedad _onlineMeetingUrl_ y un nuevo método _cancel_. |

### <a name="event-messages"></a>Mensajes de eventos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron las propiedades _startDateTime_, _endDateTime_, _location_, _type_, _recurrence_, _isOutOfDate_, _conversationIndex_, _unsubscribe_, _unsubscribeData_, _unsubscribeEnabled_ y _flag_ al objeto _eventmessage_ |
| Adición        | Beta        | Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_. |
| Adición        | Beta        | Se agregó el nuevo método _unsubscribe_.          |

### <a name="excel"></a>Excel

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Agregamos nuevas API del REST de Excel que permiten leer y modificar datos en un libro de Excel. Ahora, es posible crear aplicaciones inteligentes que permiten a los usuarios aprovechar el contenido almacenado en un libro de Excel proporcionado información sobre los datos. Se aprovechan las competencias analíticas de Excel, crear tablas y gráficos y extraer una imagen de gráfico visualmente atractiva: todo desde la aplicación. Para más información, consulte [Trabajar con Excel en Microsoft Graph](/graph/api/resources/excel?view=graph-rest-beta). |

### <a name="general"></a>General

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | Se mejoran los mensajes de error al resolver alias de inquilino y tokens de JWT (AAD) rechazados. |
| Adición        | V1.0 y beta | La ubicación del punto de conexión de servicio de autorización ahora se devuelve en el encabezado _www-authenticate_ cuando se recibe una solicitud con un token de portador vacío. |
| Adición        | V1.0 y beta | Se solucionó la capacidad para filtrar en una propiedad de identificador de entidad. Ejemplo: GET https://graph.microsoft.com/v1.0/users?$filter=id+eq+"x"<br/>Anteriormente, cualquier solicitud POST para acciones de servicio y funciones necesitaba el nombre de la acción o función con el prefijo microsoft.graph. Por ejemplo, POST https://graph.microsoft.com/v1.0/me/Microsoft.Graph.getMemberGroups.<br/>El prefijo ya no es necesario (aunque todavía se puede especificar). Por lo que ahora también funcionaría lo siguiente: POST https://graph.microsoft.com/v1.0/me/getMemberGroups. |
| Cambio          | Beta          | Se limpiaron los nombres de propiedad de suscripción.  |
| Adición        | Beta          | Se agregó la capacidad de detectar (a través de _directorySettingTemplates_) y de invalidar el comportamiento predeterminado (al crear una _configuración_ a partir de la plantilla) para entidades y su función asociada. Inicialmente, esta plantilla solo se proporciona para controlar comportamientos en los grupos de Office. |

### <a name="mail-folder"></a>Carpeta de correo

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron las propiedades _wellKnownName_ y _userConfigurations_. |
| Adición        | Beta        | Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_. |

### <a name="messages"></a>Mensajes

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | v1.0          | Se agregó la propiedad _mobilePhone_.            |
| Adición        | V1.0 y beta | Se agregó la propiedad _internetMessageId_. El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt). |
| Cambio          | Beta          | El nombre de la propiedad _mobilePhone1_ se cambió a _mobilePhone_. |
| Cambio          | Beta          | _createReply_ y _createReplyAll_ aceptan los nuevos parámetros _Message_ y _comment_. |
| Cambio          | Beta          | _createForward_ acepta los nuevos parámetros _Message_, _ToRecipients_ y _comment_. |
| Cambio          | Beta          | _reply_, _replyAll_ y _forward_ aceptan el nuevo parámetro _Message_. |

### <a name="permission"></a>Permiso

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | Se agregó la propiedad _sharingInvitation_ que proporciona detalles de cualquier invitación para uso compartido asociada a este permiso. |

### <a name="person"></a>Usuario

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron las nuevas propiedades _birthday_, _personNotes_, _isFavorite_, _phones_, _permission_, _postalAddresses_,_websites_,_yomiCompany_, _department_, _profession_, _mailboxType_ y _personType_. |
| Adición        | Beta        | Se agregaron los nuevos tipos de enumeración _physicalAddressType_, _webSite _, _phone_ y _webSiteType_. |

### <a name="reference-attachment"></a>Datos adjuntos de referencia

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron las nuevas propiedades _sourceUrl_, _providerType_, _thumbnailUrl_, _previewUrl_, _permission_ y _isFolder_. |
| Adición        | Beta        | Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_. |
| Adición        | Beta        | Se agregaron los nuevos tipos de enumeración _referenceAttachmentProvider_ y _referenceAttachmentPermission_. |

### <a name="subscriptions"></a>Suscripciones

| **Tipo de cambio** | **Punto de conexión** | **Descripción**                          |
| :-------------- | :----------- | :--------------------------------------- |
| Adición        | v1.0         | Los webhooks ya están disponibles para el público en general en la versión 1.0 del punto de conexión con el recurso _/Subscriptions_. Permiten crear, leer, renovar y eliminar suscripciones para recibir notificaciones sobre datos de conversaciones de grupo de Office 365 y Outlook. |

### <a name="user"></a>User

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregaron la propiedad _mailboxSettings_ y los tipos correspondientes. |

## <a name="february-2016"></a>Febrero de 2016

### <a name="driveitem"></a>DriveItem

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Adición        | V1.0 y beta | Nueva propiedad _remoteItem_ en driveItem para cuentas de Microsoft. |

### <a name="general"></a>General

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Cambio          | V1.0 y beta | -_/me/drive_ funciona ahora para cuentas de Microsoft y cuentas profesionales y educativas. |
| Cambio          | V1.0 y beta | Las solicitudes de unidad de disco para cuentas cuyo almacenamiento de OneDrive se aprovisionó a petición funcionan de manera más confiable y en más escenarios en los que los sitios de SharePoint predeterminados de inquilinos utilizan nombres no estándar. |
| Eliminación        | Beta          | Se quitaron diversos tipos no implementados del esquema beta para que se parezca más al esquema 1.0. |

### <a name="subscriptions"></a>Suscripciones

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Validación de notificationUrl en la creación de la suscripción. Para obtener más información, consulte [Actualización de WebHooks de Microsoft Graph: enero de 2016](https://developer.microsoft.com/office/blogs/Microsoft-Graph-WebHooks-Update-January-2016/). |
| Adición        | Beta        | Las entidades de suscripción ahora se pueden eliminar: DELETE https://graph.microsoft.com/beta/subscriptions/ |

### <a name="users"></a>Usuarios

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Cambio          | V1.0 y beta | _displayName_ ahora se devuelve para cuentas Microsoft. |

## <a name="january-2016"></a>Enero de 2016

### <a name="contacts"></a>Contactos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | v1.0        | Se agregó la propiedad mobilePhone al conjunto de entidades de contactos personales. |

### <a name="directoryobjects"></a>directoryObjects

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Solución             | V1.0 y beta | Se solucionaron las acciones de llamada que estaban enlazadas a directoryObjects y que producían el error siguiente:  El tipo de valor devuelto de la operación no se admite con el conjunto de entidades especificado. Se aplica a las siguientes acciones: _microsoft.graph.checkMemberObjects_, _microsoft.graph.getMemberObjects_, _microsoft.graph.checkMemberGroups_, _microsoft.graph.assignLicense_, _microsoft.graph.changePassword_. |

## <a name="december-2015"></a>Diciembre de 2015

### <a name="contacts"></a>Contactos

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó la propiedad mobilePhone al conjunto de entidades de contactos personales. |

### <a name="general"></a>General

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Solución             | V1.0 y beta | Se solucionaron las solicitudes en las que se usaban expresiones de $filter y se especificaba la misma propiedad más de una vez, que producían el siguiente error 500: Ya se ha agregado un elemento con la misma clave. |
| Solución             | V1.0 y beta | Se solucionó el problema de no distinción de mayúsculas de minúsculas para nombres de parámetros de acción y sus valores. |
| Solución             | V1.0 y beta | Se solucionó el procesamiento de solicitudes de cargas que contenían valores nulos para algunas propiedades complejas integradas y que generaban una excepción de referencia nula. |
| Adición        | V1.0 y beta | Se agregó la compatibilidad con la ordenación y filtrado de propiedades de tipo complejo. |
| Adición        | V1.0 y beta | Se agregó la propiedad authorization_uri en el encabezado www-authenticate de una respuesta 401. Este URI se puede usar para iniciar el flujo de adquisición de tokens. |
| Adición        | V1.0 y beta | Se mejoraron los mensajes de error en usuarios y grupos. |

### <a name="groups"></a>Grupos

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Solución             | V1.0 y beta | Se solucionaron las llamadas a las siguientes acciones de grupo: _microsoft.graph.addFavorite_, _microsoft.graph.removeFavorite_ y _microsoft.graph.resetUnseenCount_. |

### <a name="messages"></a>Mensajes

| **Tipo de cambio** | **Versión** | **Descripción**                          |
| :-------------- | :---------- | :--------------------------------------- |
| Adición        | Beta        | Se agregó el subtipo eventMessageRequest de las propiedades eventMessage y startDateTime, endDateTime, location, type, recurrence e isOutOfDate al tipo eventMessage. |

### <a name="users"></a>Usuarios

| **Tipo de cambio** | **Versión**   | **Descripción**                          |
| :-------------- | :------------ | :--------------------------------------- |
| Solución             | V1.0 y beta | Se solucionó la capacidad de seleccionar determinadas propiedades de usuario en otros usuarios, cuando se hacía referencia al usuario con el nombre principal de usuario (UPN). Por ejemplo: https://graph.microsoft.com/v1.0/users/anotherUser@contoso.com?$select=aboutMe |
| Solución             | V1.0 y beta | Se solucionó la llamada a la función enlazada de usuario _microsoft.graph.reminderView_, que generaba el siguiente error: No se pudo encontrar una propiedad denominada businessPhones en el tipo Microsoft.OutlookServices.Reminder. |
| Solución             | V1.0 y beta | Se solucionó la creación y actualización de usuarios (POST/PATCH /v1.0/users), que generaba el error 400. |
