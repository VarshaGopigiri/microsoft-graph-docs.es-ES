# <a name="changelog-for-microsoft-graph"></a>Registro de cambios para Microsoft Graph

Este historial abarca qué ha cambiado en Microsoft Graph, incluidos el extremo v1.0 y las API de Microsoft Graph beta.  

## <a name="april-2017"></a>Abril de 2017

### <a name="administrative-units-property-changes"></a>Cambios de propiedades de las unidades administrativas

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Cambio|Beta| Las API de la unidad administrativa se actualizarán en vista preliminar (beta). El primer conjunto de cambios se aplicará el 3 de mayo de 2017. Los cambios incluyen el siguiente cambio de nombre de propiedad:<br />- **roleMemberInfo** tipo complejo para **identidad** tipo complejo para la entidad scopedRoleMembership<br />- **scopedAdministratorOf** propiedad de navegación para **scopedRoleMemberOf** para la entidad usuario<br />- **scopedAdministrators** propiedad de navegación para **scopedRoleMembers** para la entidad administrativeUnit<br />- **scopedAdministrators** propiedad de navegación para **scopedMembers** para la entidad directoryRole |

### <a name="application-and-serviceprincipal-api-changes"></a>Cambios en la API servicePrincipal y en aplicaciones

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Cambio|Beta| Las API [application](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/application) y [servicePrincipal](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/serviceprincipal) se actualizarán en la versión preliminar (beta). El primer conjunto de cambios se aplicará el 8 de mayo de 2017. Entre los cambios, se incluyen la reestructuración y el cambio de nombre de propiedad. Algunas propiedades (como appRoles y addIns) no estarán disponibles hasta que se completen los cambios. Los cambios se publicarán en versión preliminar (beta) antes de publicarse la versión 1.0. |

### <a name="added-preview-support-for-cloud-solution-provider-developers"></a>Se agregó soporte técnico de versión preliminar para desarrolladores del Proveedor de soluciones en la nube

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Se agregó una nueva capacidad de versión preliminar para que las aplicaciones del Proveedor de soluciones en la nube aceptadas previamente puedan llamar a Microsoft Graph, descrita en un nuevo [tema de autorización](https://graph.microsoft.io/en-us/docs/authorization/auth_cloudsolutionprovider). |

### <a name="added-onpremises-properties-to-user-entity"></a>Se agregaron propiedades onPremises a la entidad de usuario

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Se agregaron nuevas propiedades onPremises (onPremisesDomainName, OnPremisesSamAccountName y onPremisesUserPrincipalName) a la entidad [user](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/user). |

### <a name="new-planner-apis-and-an-update-to-the-group-visibility-property"></a>Nuevas API de Planner y una actualización de la propiedad de visibilidad del grupo

|**Tipo de cambio**|**Versión**|**Descripción**| 
|:-------------|:-----------|:--------------|
|Cambio|Beta|Se agregó **HiddenMembership** como valor adicional para la propiedad de visibilidad de la entidad [Group](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/group) |
|Adición|Beta|Se agregó una nueva [API de Planner](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/planner_overview).<br />Nuevos recursos:<br />[plannerPlan](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerPlan) <br />[plannerTask](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerTask) <br />[plannerPlanDetails](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerPlanDetails) <br />[plannerTaskDetails](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerTaskDetails) <br />[plannerBucket](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerBucket) <br />[plannerAssignedToTaskBoardTaskFormat](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerassignedtotaskboardtaskformat) <br />[plannerBucketTaskBoardTaskFormat](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerbuckettaskboardtaskformat) <br />[plannerProgressTaskBoardTaskFormat](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/plannerprogresstaskboardtaskformat) | 

### <a name="intune-apis"></a>API de Intune
|**Tipo de cambio**|**Versión**|**Descripción**|
|:---|:---|:---|
|Adición|Beta|Nuevas entidades agregadas:<br/>[androidForWorkCompliancePolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkcompliancepolicy)<br/>[deviceComplianceSettingState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancesettingstate)<br/>[deviceInstallState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_books_deviceinstallstate)<br/>[deviceManagementScript](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_devicemanagementscript)<br/>[deviceManagementScriptGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_devicemanagementscriptgroupassignment)<br/>[deviceManagementScriptState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_devicemanagementscriptstate)<br/>[eBookGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_books_ebookgroupassignment)<br/>[iosVppEBook](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_books_iosvppebook)<br/>[managedEBook](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_books_managedebook)<br/>[userInstallStateSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_books_userinstallstatesummary)<br/>[windowsManagementApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_windowsmanagementapp)<br/>[windowsManagementAppHealthState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_windowsmanagementapphealthstate)<br/>|
|Adición|Beta|Nuevos tipos complejos agregados:<br/>[dailySchedule](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_dailyschedule)<br/>[hourlySchedule](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_hourlyschedule)<br/>[iosBookmark](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosbookmark)<br/>[iosWebContentFilterAutoFilter](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioswebcontentfilterautofilter)<br/>[iosWebContentFilterBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioswebcontentfilterbase)<br/>[iosWebContentFilterSpecificWebsitesAccess](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioswebcontentfilterspecificwebsitesaccess)<br/>[runSchedule](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_runschedule)<br/>[sharedAppleDeviceUser](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_sharedappledeviceuser)<br/>[windows10NetworkProxyServer](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10networkproxyserver)<br/>|
|Adición|Beta|Se agregó la acción [requestRemoteAssistance](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_devicefe_manageddevice_requestremoteassistance) en [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice) |
|Adición|Beta|Se agregó la acción [cleanWindowsDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_devicefe_manageddevice_cleanwindowsdevice) en [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice) |
|Adición|Beta|Se agregó la acción [logoutSharedAppleDeviceActiveUser](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_devicefe_manageddevice_logoutsharedappledeviceactiveuser) en [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice) |
|Adición|Beta|Se agregó la acción [deleteUserFromSharedAppleDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_devicefe_manageddevice_deleteuserfromsharedappledevice) en [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice) |
|Adición|Beta|Se agregó la acción [assign](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_devicefe_devicemanagementscript_assign) en [deviceManagementScript](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_devicemanagementscript) |
|Adición|Beta|Se agregó la acción [syncLicenses](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_onboarding_applevolumepurchaseprogramtoken_synclicenses) en [appleVolumePurchaseProgramToken](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_applevolumepurchaseprogramtoken) |
|Adición|Beta|Se agregó la función **getTopMobileApps** en la colección [mobileApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileapp) |
|Adición|Beta|Se agregó la función [downloadApplePushNotificationCertificateSigningRequest](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_devicefe_applepushnotificationcertificate_downloadapplepushnotificationcertificatesigningrequest) en [applePushNotificationCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_applepushnotificationcertificate) |
|Adición|Beta|Se agregó la función [getDeviceComplianceSettingStates](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_deviceconfig_devicemanagement_getdevicecompliancesettingstates) en [deviceManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_devicemanagement) |
|Adición|Beta|Se agregó la función [deviceConfigurationUserActivity](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_deviceconfig_reportroot_deviceconfigurationuseractivity) en [reportRoot](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_reportroot) |
|Adición|Beta|Se agregó la función [deviceConfigurationDeviceActivity](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_deviceconfig_reportroot_deviceconfigurationdeviceactivity) en [reportRoot](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_reportroot) |
|Eliminación|Beta|Se quitaron los tipos complejos siguientes:<br/>**enterpriseCloudResource**<br/>**windowsInformationProtectionAppRule**<br/>**windowsInformationProtectionAppRuleAppLockerPolicyFileTemplate**<br/>**windowsInformationProtectionAppRuleDesktopTemplate**<br/>**windowsInformationProtectionAppRuleStoreAppTemplate**<br/>**windowsInformationProtectionAppRuleTemplate**<br/>**windowsInformationProtectionCorporateNetworkLocation**<br/>**windowsInformationProtectionProtectedLocation**<br/>**windowsInformationProtectionProtectedLocationEnterpriseCloudResources**<br/>**windowsInformationProtectionProtectedLocationEnterpriseInternalProxyServers**<br/>**windowsInformationProtectionProtectedLocationEnterpriseIPv4Ranges**<br/>**windowsInformationProtectionProtectedLocationEnterpriseIPv6Ranges**<br/>**windowsInformationProtectionProtectedLocationEnterpriseNetworkDomainNames**<br/>**windowsInformationProtectionProtectedLocationEnterpriseProxyServers**<br/>**windowsInformationProtectionProtectedLocationNeutralResources**<br/>|
|Cambio|Beta|Se agregó la propiedad **deviceSharingAllowed** a la entidad [androidGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidgeneraldeviceconfiguration)|
|Cambio|Beta|Se quitó la propiedad **deviceSharingBlocked** de la entidad [androidGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidgeneraldeviceconfiguration)|
|Cambio|Beta|Se agregó la propiedad **minimumRequiredSdkVersion** a la entidad [defaultManagedAppProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_defaultmanagedappprotection)|
|Cambio|Beta|Se agregó la propiedad **windowsManagementAppEnabled** a la entidad [deviceAppManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_deviceappmanagement)|
|Cambio|Beta|Se agregó la propiedad **notificationTemplateId** a la entidad [deviceComplianceActionItem](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecomplianceactionitem)|
|Cambio|Beta|Se agregó la propiedad **excludeGroup** a la entidad [deviceConfigurationGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationgroupassignment)|
|Cambio|Beta|Se cambiaron las propiedades siguientes en la entidad [iosCustomConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioscustomconfiguration):<br/>**payloadFileName** de required a optional<br/>|
|Cambio|Beta|Se agregó la propiedad **contentFilterSettings** a la entidad [iosDeviceFeaturesConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosdevicefeaturesconfiguration)|
|Cambio|Beta|Se agregaron las propiedades **cellularBlockPersonalHotspot** y **passcodeBlockFingerprintModification** a la entidad [iosGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosgeneraldeviceconfiguration)|
|Cambio|Beta|Se agregó la propiedad **minimumRequiredSdkVersion** a la entidad [iosManagedAppProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_iosmanagedappprotection)|
|Cambio|Beta|Se cambiaron las propiedades siguientes en la entidad [macOSCustomConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_macoscustomconfiguration):<br/>**payloadFileName** de required a optional<br/>|
|Cambio|Beta|Se agregaron las propiedades **disableAppPinIfDevicePinIsSet**, **minimumRequiredOsVersion**, **minimumWarningOsVersion**, **minimumRequiredAppVersion** y **minimumWarningAppVersion** a la entidad [managedAppProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_managedappprotection)|
|Cambio|Beta|Se agregaron las propiedades **remoteAssistanceSessionUrl**, **isEncrypted**, **model** y **manufacturer** a la entidad [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice)|
|Cambio|Beta|Se cambiaron las propiedades siguientes de la entidad [getMobileAppCount](https://developer.microsoft.com/en-us/graph/docs/docs/api-reference/beta/api/intune_apps_mobileapp_getmobileappcount):<br/>**bindingParameter** de **mobileApp** a una **colección** de *mobileApp*<br/>**estado** de un GUID a una cadena<br/>|
|Cambio|Beta|Se agregó la propiedad **vpnConfigurationId** a la entidad [mobileAppGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappgroupassignment)|
|Cambio|Beta|Se quitó la propiedad **fromEmailAddress** de la entidad [notificationMessageTemplate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_notificationmessagetemplate)|
|Cambio|Beta|Se agregó la propiedad **excludedApps** a la entidad [officeSuiteApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_officesuiteapp)|
|Cambio|Beta|Se quitó la propiedad **excludedOfficeApps** de la entidad [officeSuiteApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_officesuiteapp)|
|Cambio|Beta|Se agregó la propiedad **enabled** a la entidad [sharedPCConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_sharedpcconfiguration)|
|Cambio|Beta|Se agregaron las propiedades **networkProxyApplySettingsDeviceWide**, **networkProxyDisableAutoDetect**, **networkProxyAutomaticConfigurationUrl**, **networkProxyServer**, **bluetoothDeviceName**, **wiFiScanInterval**, **wirelessDisplayBlockProjectionToThisDevice**, **wirelessDisplayBlockUserInputFromReceiver**, **wirelessDisplayRequirePinForPairing**, **experienceBlockDeviceDiscovery**, **experienceBlockErrorDialogWhenNoSIM**, **experienceBlockTaskSwitcher**, **startMenuPinnedFolderDocuments**, **startMenuPinnedFolderDownloads**, **startMenuPinnedFolderFileExplorer**, **startMenuPinnedFolderHomeGroup**, **startMenuPinnedFolderMusic**, **startMenuPinnedFolderNetwork**, **startMenuPinnedFolderPersonalFolder**, **startMenuPinnedFolderPictures**, **startMenuPinnedFolderSettings**, **startMenuPinnedFolderVideos**, **startMenuAppListVisibility**, **startMenuHideFrequentlyUsedApps**, **startMenuHideRecentJumpLists**, **startMenuHideRecentlyAddedApps**, **startMenuHideRestartOptions**, **startMenuHideUserTile**, **startMenuHidePowerButton**, **startMenuLayoutEdgeAssetsXml**, **personalizationDesktopImageUrl** y **personalizationLockScreenImageUrl** a la entidad [windows10GeneralConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10generalconfiguration)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [windowsMobileMSI](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsmobilemsi):<br/>**productCode** de Guid a String<br/>|
|Cambio|Beta|Se cambiaron las propiedades siguientes en la entidad [windowsPhone81AppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsphone81appx):<br/>**phoneProductIdentifier** de required a optional<br/>**phonePublisherId** de required a optional<br/>|
|Cambio|Beta|Se cambiaron las propiedades siguientes en la entidad [windowsPhone81AppXBundle](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsphone81appxbundle):<br/>**appXPackageInformationList** de required a optional<br/>|
|Cambio|Beta|Se agregaron las propiedades **productKey** y **licenseType** a la entidad [windowsStoreForBusinessApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsstoreforbusinessapp)|
|Cambio|Beta|Se agregó la propiedad **previewBuildSetting** a la entidad [windowsUpdateForBusinessConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsupdateforbusinessconfiguration)|
|Cambio|Beta|Se agregaron las propiedades de navegación **windowsManagementApp** y **managedEBooks** a la entidad [deviceAppManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_deviceappmanagement)|
|Cambio|Beta|Se agregaron las propiedades de navegación **deviceManagementScripts**, **managedDeviceOverview** y **cloudPkiSubscriptions** a la entidad [deviceManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_devicemanagement)|
|Cambio|Beta|Se agregaron las propiedades **osMinimumVersion** y **osMaximumVersion** al tipo complejo [deviceEnrollmentPlatformRestrictions](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_deviceenrollmentplatformrestrictions)|
|Cambio|Beta|Se agregaron las propiedades **isSharedDevice** y **sharedDeviceCachedUsers** al tipo complejo [hardwareInformation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_hardwareinformation)|
|Cambio|Beta|Se cambiaron las propiedades siguientes en el tipo complejo [omaSettingBase64](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_omasettingbase64):<br/>**fileName** de required a optional<br/>|
|Cambio|Beta|Se cambiaron las propiedades siguientes en el tipo complejo [omaSettingStringXml](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_omasettingstringxml):<br/>**fileName** de required a optional<br/>|

## <a name="march-2017"></a>Marzo de 2017

### <a name="intune-apis"></a>API de Intune

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Nuevas entidades agregadas:<br/>[androidForWorkApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_androidforworkapp)<br/>[androidForWorkAppConfigurationSchema](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworkappconfigurationschema)<br/>[androidForWorkSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworksettings)<br/>[androidForWorkVpnConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkvpnconfiguration)<br/>[applePushNotificationCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_applepushnotificationcertificate)<br/>[complianceSettingStateSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_compliancesettingstatesummary)<br/>[deviceCompliancePolicyDeviceStateSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary)<br/>[deviceCompliancePolicyState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancepolicystate)<br/>[deviceConfigurationDeviceStateSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationdevicestatesummary)<br/>[deviceConfigurationState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationstate)<br/>[enterpriseCodeSigningCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_enterprisecodesigningcertificate)<br/>[iosEduDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosedudeviceconfiguration)<br/>[managedDeviceCertificateState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevicecertificatestate)<br/>[managedDeviceMobileAppConfigurationDeviceSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfigurationdevicesummary)<br/>[managedDeviceMobileAppConfigurationUserSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfigurationusersummary)<br/>[mdmWindowsInformationProtectionPolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_mdmwindowsinformationprotectionpolicy)<br/>[mobileAppInstallSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappinstallsummary)<br/>[mobileAppProvisioningConfigGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappprovisioningconfiggroupassignment)<br/>[mobileThreatDefenseConnector](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_mobilethreatdefenseconnector)<br/>[officeSuiteApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_officesuiteapp)<br/>[settingStateDeviceSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_settingstatedevicesummary)<br/>[softwareUpdateStatusSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_softwareupdatestatussummary)<br/>[symantecCodeSigningCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_symanteccodesigningcertificate)<br/>[windowsDefenderAdvancedThreatProtectionConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsdefenderadvancedthreatprotectionconfiguration)<br/>[windowsInformationProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotection)<br/>[windowsInformationProtectionAppLockerFile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectionapplockerfile)<br/>[windowsInformationProtectionPolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectionpolicy)<br/>[windowsMobileMSI](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsmobilemsi)<br/>|
|Adición|Beta|Nuevos tipos complejos agregados:<br/>[androidForWorkAppConfigurationExample](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworkappconfigurationexample)<br/>[androidForWorkAppConfigurationExampleJson](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworkappconfigurationexamplejson)<br/>[androidForWorkAppConfigurationSchemaItem](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworkappconfigurationschemaitem)<br/>[deviceCompliancePolicySettingState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancepolicysettingstate)<br/>[deviceConfigurationSettingState](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationsettingstate)<br/>[deviceExchangeAccessStateSummary](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_deviceexchangeaccessstatesummary)<br/>[edgeSearchEngine](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_edgesearchengine)<br/>[edgeSearchEngineBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_edgesearchenginebase)<br/>[edgeSearchEngineCustom](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_edgesearchenginecustom)<br/>[excludedApps](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_excludedapps)<br/>[iosEduCertificateSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioseducertificatesettings)<br/>[ipRange](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iprange)<br/>[windowsInformationProtectionApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectionapp)<br/>[windowsInformationProtectionCloudResource](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectioncloudresource)<br/>[windowsInformationProtectionCloudResourceCollection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectioncloudresourcecollection)<br/>[windowsInformationProtectionDesktopApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectiondesktopapp)<br/>[windowsInformationProtectionIPRangeCollection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectioniprangecollection)<br/>[windowsInformationProtectionResourceCollection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectionresourcecollection)<br/>[windowsInformationProtectionStoreApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectionstoreapp)<br/>|
|Adición|Beta|Se agregó la acción [requestSignupUrl](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_androidforwork_androidforworksettings_requestsignupurl) en [androidForWorkSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworksettings) |
|Adición|Beta|Se agregó la acción [completeSignup](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_androidforwork_androidforworksettings_completesignup) en [androidForWorkSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworksettings) |
|Adición|Beta|Se agregó la acción [syncApps](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_androidforwork_androidforworksettings_syncapps) en [androidForWorkSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworksettings) |
|Adición|Beta|Se agregó la acción [unbind](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_androidforwork_androidforworksettings_unbind) en [androidForWorkSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_androidforworksettings) |
|Adición|Beta|Se agregó la acción [assign](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_apps_ioslobappprovisioningconfiguration_assign) en [iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration) |
|Adición|Beta|Se agregó la acción [recoverPasscode](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_devicefe_manageddevice_recoverpasscode) en [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice) |
|Adición|Beta|Se agregó la acción [removeApplePushNotificationCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_onboarding_organization_removeapplepushnotificationcertificate) en [organization](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_organization) |
|Adición|Beta|Se agregó la acción [updateMobileAppIdentifierDeployments](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_iosmanagedappprotection_updatemobileappidentifierdeployments) en [iosManagedAppProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_iosmanagedappprotection) |
|Adición|Beta|Se agregó la acción [updateMobileAppIdentifierDeployments](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_androidmanagedappprotection_updatemobileappidentifierdeployments) en [androidManagedAppProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_androidmanagedappprotection) |
|Adición|Beta|Se agregó la acción [updateMobileAppIdentifierDeployments](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_targetedmanagedappconfiguration_updatemobileappidentifierdeployments) en [targetedManagedAppConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_targetedmanagedappconfiguration) |
|Adición|Beta|Se agregó la acción [updateTargetedSecurityGroups](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_iosmanagedappprotection_updatetargetedsecuritygroups) en [iosManagedAppProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_iosmanagedappprotection) |
|Adición|Beta|Se agregó la acción [updateTargetedSecurityGroups](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_androidmanagedappprotection_updatetargetedsecuritygroups) en [androidManagedAppProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_androidmanagedappprotection) |
|Adición|Beta|Se agregó la acción [updateTargetedSecurityGroups](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_windowsinformationprotection_updatetargetedsecuritygroups) en [windowsInformationProtection](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotection) |
|Adición|Beta|Se agregó la acción [updateTargetedSecurityGroups](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_windowsinformationprotection_updatetargetedsecuritygroups) en [windowsInformationProtectionPolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectionpolicy) |
|Adición|Beta|Se agregó la acción [updateTargetedSecurityGroups](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_mdmwindowsinformationprotectionpolicy_updatetargetedsecuritygroups) en [mdmWindowsInformationProtectionPolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_mdmwindowsinformationprotectionpolicy) |
|Adición|Beta|Se agregó la acción [wipeManagedAppRegistrationByDeviceTag](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_user_wipemanagedappregistrationbydevicetag) en [user](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_user) |
|Adición|Beta|Se agregó la función [getTopMobileApps](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_apps_mobileapp_gettopmobileapps) en [mobileApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileapp) |
|Adición|Beta|Se agregó la función [verifyWindowsEnrollmentAutoDiscovery](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_corpenrollment_devicemanagement_verifywindowsenrollmentautodiscovery) en [deviceManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_devicemanagement) |
|Eliminación|Beta|Se quitaron las entidades siguientes:<br/>**appProvisioningConfigGroupAssignment**<br/>**defaultManagedAppConfiguration**<br/>**enterpriseCertificate**<br/>**managedDeviceMobileAppProvisioningConfigurationDeviceStatus**<br/>**symantecCertificate**<br/>**windows10WindowsInformationProtectionConfiguration**<br/>|
|Eliminación|Beta|Se quitaron los tipos complejos siguientes:<br/>**mobileAppInstallSummary**<br/>**windowsArchitecture**<br/>**windowsDeviceType**<br/>|
|Cambio|Beta|Se agregó la propiedad **webBrowserBlockPopups** a la entidad [androidGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidgeneraldeviceconfiguration)|
|Cambio|Beta|Se quitó la propiedad **webBrowserAllowPopups** de la entidad [androidGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidgeneraldeviceconfiguration)|
|Cambio|Beta|Se agregó la propiedad **appIdentifier** a la entidad [androidStoreApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_androidstoreapp)|
|Cambio|Beta|Se quitaron las propiedades **applicationCount**, **failedApplicationCount** y **appInstallFailures** de la entidad [appReportingOverviewStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/appReportingOverviewStatus)|
|Cambio|Beta|Se agregaron las propiedades **sharedIPadMaximumUserCount** y **enableSharedIPad** a la entidad [depEnrollmentProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_corpenrollment_depenrollmentprofile)|
|Cambio|Beta|Se agregaron las propiedades **shareTokenWithSchoolDataSyncService** y **lastSyncErrorCode** a la entidad [depOnboardingSetting](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_deponboardingsetting)|
|Cambio|Beta|Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceComplianceDeviceOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancedeviceoverview)|
|Cambio|Beta|Se quitaron las propiedades **numberOfPendingDevices**, **numberOfSucceededDevices**, **numberOfErrorDevices**, **numberOfFailedDevices**, **lastUpdateTime** y **policyRevision** de la entidad [deviceComplianceDeviceOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancedeviceoverview)|
|Cambio|Beta|Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceComplianceUserOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecomplianceuseroverview)|
|Cambio|Beta|Se quitaron las propiedades **numberOfPendingUsers**, **numberOfSucceededUsers**, **numberOfErrorUsers**, **numberOfFailedUsers**, **lastUpdateTime** y **policyRevision** de la entidad [deviceComplianceUserOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecomplianceuseroverview)|
|Cambio|Beta|Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceConfigurationDeviceOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationdeviceoverview)|
|Cambio|Beta|Se quitaron las propiedades **numberOfPendingDevices**, **numberOfSucceededDevices**, **numberOfErrorDevices**, **numberOfFailedDevices**, **lastUpdateTime** y **policyRevision** de la entidad [deviceConfigurationDeviceOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationdeviceoverview)|
|Cambio|Beta|Se agregaron las propiedades **pendingCount**, **successCount**, **errorCount**, **failedCount**, **lastUpdateDateTime** y **configurationVersion** a la entidad [deviceConfigurationUserOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationuseroverview)|
|Cambio|Beta|Se quitaron las propiedades **numberOfPendingUsers**, **numberOfSucceededUsers**, **numberOfErrorUsers**, **numberOfFailedUsers**, **lastUpdateTime** y **policyRevision** de la entidad [deviceConfigurationUserOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationuseroverview)|
|Cambio|Beta|Se agregó la propiedad **subscriptionState** a la entidad [deviceManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_devicemanagement)|
|Cambio|Beta|Se agregó la propiedad **managedEmailProfileRequired** a la entidad [iosCompliancePolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioscompliancepolicy)|
|Cambio|Beta|Se agregó la propiedad **appsSingleAppModeList** a la entidad [iosGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosgeneraldeviceconfiguration)|
|Cambio|Beta|Se quitó la propiedad **appsSingleAppModeBundleIds** de la entidad [iosGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosgeneraldeviceconfiguration)|
|Cambio|Beta|Se agregó la propiedad **expirationDateTime** a la entidad [iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration)|
|Cambio|Beta|Se quitó la propiedad **expiration** de la entidad [iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration)|
|Cambio|Beta|Se agregaron las propiedades **passwordMinimumCharacterSetCount**, **osMinimumVersion**, **osMaximumVersion**, **deviceThreatProtectionEnabled**, **deviceThreatProtectionRequiredSecurityLevel** y **storageRequireEncryption** a la entidad [macOSCompliancePolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_macoscompliancepolicy)|
|Cambio|Beta|Se quitó la propiedad **manifest** de la entidad [managedAndroidLobApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_managedandroidlobapp)|
|Cambio|Beta|Se agregaron las propiedades **isSupervised**, **exchangeLastSuccessfulSyncDateTime**, **exchangeAccessState** y **exchangeAccessStateReason** a la entidad [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice)|
|Cambio|Beta|Se agregó la propiedad **deviceExchangeAccessStateSummary** a la entidad [managedDeviceOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddeviceoverview)|
|Cambio|Beta|Se quitó la propiedad **manifest** de la entidad [managedIOSLobApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_managedioslobapp)|
|Cambio|Beta|Se quitó la propiedad **installSummary** de la entidad [mobileApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileapp)|
|Cambio|Beta|Se agregó la propiedad **uploadState** a la entidad [mobileAppContentFile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappcontentfile)|
|Cambio|Beta|Se cambiaron las propiedades siguientes de la entidad [mobileAppContentFile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappcontentfile):<br/>**azureStorageUriExpirationDateTime** de required a optional<br/>|
|Cambio|Beta|Se agregaron las propiedades **initiatedByUserPrincipalName**, **deviceOwnerUserPrincipalName**, **deviceIMEI** y **actionState** a la entidad [remoteActionAudit](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_remoteactionaudit)|
|Cambio|Beta|Se agregaron las propiedades **oneDriveDisableFileSync**, **safeSearchFilter**, **edgeSearchEngine**, **settingsBlockSettingsApp**, **settingsBlockSystemPage**, **settingsBlockDevicesPage**, **settingsBlockNetworkInternetPage**, **settingsBlockPersonalizationPage**, **settingsBlockAccountsPage**, **settingsBlockTimeLanguagePage**, **settingsBlockEaseOfAccessPage**, **settingsBlockPrivacyPage**, **settingsBlockUpdateSecurityPage**, **experienceBlockWindowsSpotlight**, **experienceBlockWindowsTips**, **experienceBlockConsumerSpecificFeatures**, **startMenuLayoutXml**, **startMenuMode**, **logonBlockFastUserSwitching** y **startBlockUnpinningAppsFromTaskbar** a la entidad [windows10GeneralConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10generalconfiguration)|
|Cambio|Beta|Se agregaron las propiedades **allowPrinting**, **allowScreenCapture** y **allowTextSuggestion** a la entidad [windows10SecureAssessmentConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10secureassessmentconfiguration)|
|Cambio|Beta|Se quitaron las propiedades **blockPrinting**, **blockScreenCapture** y **blockTextSuggestion** de la entidad [windows10SecureAssessmentConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10secureassessmentconfiguration)|
|Cambio|Beta|Se agregó la propiedad **identityName** a la entidad [windowsAppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsappx)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [windowsAppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsappx):<br/>**applicableArchitectures** de [windowsArchitecture](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/windowsArchitecture) a String<br/>|
|Cambio|Beta|Se agregó la propiedad **identityName** a la entidad [windowsPhone81AppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsphone81appx)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [windowsPhone81AppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsphone81appx):<br/>**applicableArchitectures** de [windowsArchitecture](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/windowsArchitecture) a String<br/>|
|Cambio|Beta|Se agregaron las propiedades **identityName**, **identityPublisherHash** y **identityResourceIdentifier** a la entidad [windowsUniversalAppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsuniversalappx)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [windowsUniversalAppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsuniversalappx):<br/>**applicableArchitectures** de [windowsArchitecture](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/windowsArchitecture) a String<br/>**applicableDeviceTypes** de [windowsDeviceType](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/windowsDeviceType) a String<br/>|
|Cambio|Beta|Se agregó la propiedad **restartMode** a la entidad [windowsUpdateForBusinessConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsupdateforbusinessconfiguration)|
|Cambio|Beta|Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [androidForWorkScepCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkscepcertificateprofile)|
|Cambio|Beta|Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [androidScepCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidscepcertificateprofile)|
|Cambio|Beta|Se agregaron las propiedades de navegación **enterpriseCodeSigningCertificates**, **symantecCodeSigningCertificate**, **sideLoadingKeys**, **managedAppPolicies**, **iosManagedAppProtections**, **androidManagedAppProtections**, **defaultManagedAppProtections**, **targetedManagedAppConfigurations**, **mdmWindowsInformationProtectionPolicies**, **windowsInformationProtectionPolicies**, **managedAppRegistrations** y **managedAppStatuses** a la entidad [deviceAppManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_deviceappmanagement)|
|Cambio|Beta|Se quitaron las propiedades de navegación **appReportingOverview**, **enterpriseCerts** y **symantecCert** de la entidad [deviceAppManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_deviceappmanagement)|
|Cambio|Beta|Se agregó la propiedad de navegación **deviceSettingStateSummaries** a la entidad [deviceCompliancePolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancepolicy)|
|Cambio|Beta|Se agregó la propiedad de navegación **deviceSettingStateSummaries** a la entidad [deviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfiguration)|
|Cambio|Beta|Se agregaron las propiedades de navegación **termsAndConditions**, **androidForWorkSettings**, **androidForWorkAppConfigurationSchemas**, **applePushNotificationCertificate**, **softwareUpdateStatusSummary**, **deviceCompliancePolicyDeviceStateSummary**, **complianceSettingStateSummaries**, **deviceConfigurationDeviceStateSummaries** y **mobileThreatDefenseConnectors** a la entidad [deviceManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_androidforwork_devicemanagement)|
|Cambio|Beta|Se quitaron las propiedades de navegación **teacherRootCertificates**, **teacherIdentityCertificate**, **studentRootCertificates** y **studentIdentityCertificate** de la entidad [iosEducationDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioseducationdeviceconfiguration)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration):<br/>**deviceStatuses** de la colección [managedDeviceMobileAppProvisioningConfigurationDeviceStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/managedDeviceMobileAppProvisioningConfigurationDeviceStatus) a la colección [managedDeviceMobileAppConfigurationDeviceStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfigurationdevicestatus)<br/>**groupAssignments** de la colección [appProvisioningConfigGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/appProvisioningConfigGroupAssignment) a la colección [mobileAppProvisioningConfigGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappprovisioningconfiggroupassignment)<br/>|
|Cambio|Beta|Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [iosScepCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosscepcertificateprofile)|
|Cambio|Beta|Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [macOSScepCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_macosscepcertificateprofile)|
|Cambio|Beta|Se agregaron las propiedades de navegación **deviceConfigurationStates** y **deviceCompliancePolicyStates** a la entidad [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devicefe_manageddevice)|
|Cambio|Beta|Se agregaron las propiedades de navegación **deviceStatusSummary** y **userStatusSummary** a la entidad [managedDeviceMobileAppConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfiguration)|
|Cambio|Beta|Se agregó la propiedad de navegación **installSummary** a la entidad [mobileApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileapp)|
|Cambio|Beta|Se quitó la propiedad de navegación **sideLoadingKeys** de la entidad [organization](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_organization)|
|Cambio|Beta|Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [windows81SCEPCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows81scepcertificateprofile)|
|Cambio|Beta|Se agregó la propiedad de navegación **managedDeviceCertificateStates** a la entidad [windowsPhone81SCEPCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsphone81scepcertificateprofile)|
|Cambio|Beta|Se quitaron las propiedades **applicationId**, **appName**, **platformId**, **userFailures** y **deviceFailures** del tipo complejo [appInstallationFailure](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_appinstallationfailure)|
|Cambio|Beta|Se agregó la propiedad **displayName** al tipo complejo [iosHomeScreenFolderPage](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioshomescreenfolderpage)|
|Cambio|Beta|Se agregó la propiedad **displayName** al tipo complejo [iosHomeScreenPage](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioshomescreenpage)|
|Cambio|Beta|Se agregaron las propiedades **subjectName**, **description**, **expirationDateTime** y **certificate** al tipo complejo [windowsInformationProtectionDataRecoveryCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectiondatarecoverycertificate)|
|Cambio|Beta|Se quitaron las propiedades **dataRecoveryCertificate** y **certificateFileName** del tipo complejo [windowsInformationProtectionDataRecoveryCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_windowsinformationprotectiondatarecoverycertificate)|
|Cambio|Beta|Se agregó la propiedad **displayName** al tipo complejo [windowsPackageInformation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowspackageinformation)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en el tipo complejo [windowsPackageInformation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowspackageinformation):<br/>**applicableArchitecture** de [windowsArchitecture](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/windowsArchitecture) a String<br/>|
|Cambio|Beta|Se cambiaron las propiedades siguientes en el tipo complejo [windowsPackageInformation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowspackageinformation):<br/>**applicableArchitecture** de optional a required<br/>|

### <a name="add-contracts-to-microsoft-graph"></a>Agregar contratos a Microsoft Graph

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Nuevo recurso:</br>[contract](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/contract) |

### <a name="add-domain-operations-to-microsoft-graph"></a>Agregar operaciones de dominio a Microsoft Graph

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Se agregaron funciones en [domains](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domain).<br/>Nuevas entidades:</br>[domain](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domain)<br/>[domainDnsRecord](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domaindnsrecord)<br/>[domainDnsCnameRecord](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domainDnsCnameRecord)<br/>[domainDnsMxRecord](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domainDnsMxRecord)<br/>[domainDnsSrvRecord](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domainDnsSrvRecord)<br/>[domainDnsTxtRecord](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domainDnsTxtRecord)<br/>[domainDnsUnavailableRecord](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/domainDnsUnavailableRecord)<br/>Nuevas acciones:</br>[forceDelete](https://graph.microsoft.io/en-us/docs/api-reference/beta/api/domain_forcedelete)</br>[verify](https://graph.microsoft.io/en-us/docs/api-reference/beta/api/domain_verify) |

### <a name="add-custom-data-to-microsoft-graph-using-schema-extensions"></a>Agregar datos personalizados a Microsoft Graph mediante extensiones de esquema

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Ampliar Microsoft Graph con datos de aplicaciones mediante [extensiones de esquema](https://developer.microsoft.com/en-us/graph/docs/concepts/extensibility_overview#schema-extensions-preview).  Esto es compatible con los siguientes recursos:<br/>unidad administrativa<br/>evento de calendario<br/>Dispositivo<br/>grupo<br/>mensaje<br/>organización<br/>contacto personal<br/>publicar<br/>usuario<br/>Vea el ejemplo siguiente:<br/>[Agregar datos personalizados a grupos mediante extensiones de esquema (vista previa)](https://developer.microsoft.com/en-us/graph/docs/concepts/extensibility_schema_groups)|
|Adición|Beta|Se ha proporcionado una forma alternativa de crear una definición de extensión de esquema sin necesidad de un dominio personal .com comprobado. Vea las [extensiones de esquema](https://developer.microsoft.com/en-us/graph/docs/concepts/extensibility_overview#schema-extensions-preview) para obtener más información.|

### <a name="add-custom-data-to-microsoft-graph-using-open-extensions"></a>Agregar datos personalizados a Microsoft Graph mediante extensiones abiertas

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Cambio| V1.0 y beta | Se cambió el nombre anterior "extensiones de datos de Office 365" por "extensiones abiertas". |
|Adición|Beta|Se agregaron recursos que admiten las [extensiones abiertas](https://developer.microsoft.com/en-us/graph/docs/concepts/extensibility_overview#open-extensions): <br/>unidad administrativa<br/>dispositivo<br/>grupo<br/>organización<br/>usuario<br/>Vea el ejemplo siguiente:<br/>[Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](https://developer.microsoft.com/en-us/graph/docs/concepts/extensibility_open_users)|

### <a name="directory-apis"></a>API de directorio

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Se agregó compatibilidad para [restaurar y eliminar permanentemente grupos](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/directory).<br/>Nueva entidad: directorio con la propiedad de navegación deleteditems. |
|Adición|Beta|Nueva entidad:</br>[Extremo](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/endpoint) |
|Cambio  |Beta|Nueva propiedad de navegación de [extremos](https://graph.microsoft.io/en-us/docs/api-reference/beta/api/group_list_endpoints) en [grupos](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/group) |
|Adición|Beta|Nueva entidad:</br>[licenseDetails](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/licensedetails) |
|Cambio  |Beta|Nueva propiedad de navegación [licensedetails](https://graph.microsoft.io/en-us/docs/api-reference/beta/api/user_list_licensedetails) en [users](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/user) |

### <a name="reports-apis"></a>API de informes

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Se ha presentado la nueva API de versión preliminar de Informes de Office 365. Puede usarla para obtener informes de uso de cómo usan las personas de su empresa los servicios de Office 365. Por ejemplo, puede identificar quién usa mucho un servicio y alcanza cuotas o quién puede que no necesite una licencia de Office 365. Para obtener más información, vea [report](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/report).|

### <a name="directory-apis"></a>API de directorio

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Nueva entidad:</br>[contract](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/contract) |

## <a name="february-2017"></a>Febrero de 2017

### <a name="intune-apis"></a>API de Intune

|Tipo de cambio|Versión|Descripción|
|:---|:---|:---|
|Adición|Beta|Nuevas entidades agregadas:<br/>[androidForWorkCertificateProfileBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkcertificateprofilebase)<br/>[androidForWorkEasEmailProfileBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkeasemailprofilebase)<br/>[androidForWorkEnterpriseWiFiConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkenterprisewificonfiguration)<br/>[androidForWorkGmailEasConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkgmaileasconfiguration)<br/>[androidForWorkNineWorkEasConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworknineworkeasconfiguration)<br/>[androidForWorkPkcsCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkpkcscertificateprofile)<br/>[androidForWorkScepCertificateProfile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkscepcertificateprofile)<br/>[androidForWorkTrustedRootCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworktrustedrootcertificate)<br/>[androidForWorkWiFiConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_androidforworkwificonfiguration)<br/>[appleDeviceFeaturesConfigurationBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_appledevicefeaturesconfigurationbase)<br/>[appProvisioningConfigGroupAssignment](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_appprovisioningconfiggroupassignment)<br/>[deviceComplianceUserOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecomplianceuseroverview)<br/>[deviceConfigurationUserOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationuseroverview)<br/>[enterpriseCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_enterprisecertificate)<br/>[iosEducationDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioseducationdeviceconfiguration)<br/>[macOSDeviceFeaturesConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_macosdevicefeaturesconfiguration)<br/>[managedAndroidLobApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_managedandroidlobapp)<br/>[managedDeviceMobileAppProvisioningConfigurationDeviceStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappprovisioningconfigurationdevicestatus)<br/>[managedIOSLobApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_managedioslobapp)<br/>[managedMobileLobApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_managedmobilelobapp)<br/>[symantecCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_symanteccertificate)<br/>[windowsAppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsappx)<br/>[windowsCertificateProfileBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowscertificateprofilebase)<br/>[windowsPhone81AppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsphone81appx)<br/>[windowsPhone81AppXBundle](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsphone81appxbundle)<br/>[windowsPhoneXAP](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsphonexap)<br/>[windowsUniversalAppX](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsuniversalappx)<br/>|
|Adición|Beta|Nuevos tipos complejos agregados:<br/>[airPrintDestination](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_airprintdestination)<br/>[windowsArchitecture](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsarchitecture)<br/>[windowsDeviceType](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsdevicetype)<br/>[windowsMinimumOperatingSystem](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowsminimumoperatingsystem)<br/>[windowsPackageInformation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_windowspackageinformation)<br/>|
|Adición|Beta|Se agregó la acción [assign](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_apps_ioslobappprovisioningconfiguration_assign) a la entidad [iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration)|
|Adición|Beta|Se agregó la acción [scheduleActionsForRules](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_deviceconfig_devicecompliancepolicy_scheduleactionsforrules) a la entidad [deviceCompliancePolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancepolicy)|
|Adición|Beta|Se agregó la acción [updateTargetedSecurityGroups](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_mam_targetedmanagedappconfiguration_updatetargetedsecuritygroups) a la entidad [targetedManagedAppConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_targetedmanagedappconfiguration)|
|Adición|Beta|Se agregó la función [getScopesForUser](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/intune_rbac_resourceoperation_getscopesforintune_devices_user) a la entidad [resourceOperation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_rbac_resourceoperation)|
|Cambio|Beta|Se quitó la propiedad **manifiesto** de la entidad [androidLobApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_androidlobapp)|
|Cambio|Beta|Se agregaron las propiedades **assetTagTemplate**, **lockScreenFootnote**, **homeScreenDockIcons** y **homeScreenPages** a la entidad [iosDeviceFeaturesConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosdevicefeaturesconfiguration)|
|Cambio|Beta|Se quitaron las propiedades **deviceSharingAssetTagInformation**, **deviceSharingLockScreenFootnote**, **homeScreenLayoutDockIcons** y **homeScreenLayoutPages** de la entidad [iosDeviceFeaturesConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosdevicefeaturesconfiguration)|
|Cambio|Beta|Se agregó la propiedad **appsSingleAppModeBundleIds** a la entidad [iosGeneralDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosgeneraldeviceconfiguration)|
|Cambio|Beta|Se quitó la propiedad **manifiesto** de la entidad [iosLobApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobapp)|
|Cambio|Beta|Se agregaron las propiedades **createdDateTime**, **description**, **lastModifiedDateTime**, **displayName** y **version** a la entidad [iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration)|
|Cambio|Beta|Se agregaron las propiedades **createdDateTime** y **lastModifiedDateTime** a la entidad [managedAppPolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_managedapppolicy)|
|Cambio|Beta|Se quitó la propiedad **deviceRegistrationState** de la entidad [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devices_manageddevice)|
|Cambio|Beta|Se agregó la propiedad **manifest** a la entidad [mobileAppContentFile](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappcontentfile)|
|Cambio|Beta|Se agregaron las propiedades **osDescription** y **userName** a la entidad [mobileAppInstallStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappinstallstatus)|
|Cambio|Beta|Se quitó la propiedad **deviceType** property de la entidad [mobileAppInstallStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappinstallstatus)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [mobileAppInstallStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappinstallstatus):<br/>**mobileAppInstallStatusValue** de Int32 a String|
|Cambio|Beta|Se agregaron las propiedades **targetedSecurityGroupIds** y **targetedSecurityGroupsCount** a la entidad [targetedManagedAppConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_targetedmanagedappconfiguration)|
|Cambio|Beta|Se quitó la propiedad **numberOfTargetedSecurityGroups** de la entidad [targetedManagedAppConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_targetedmanagedappconfiguration)|
|Cambio|Beta|Se agregó la propiedad **id** a la entidad [user](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_devices_user)|
|Cambio|Beta|Se quitaron las propiedades **renewalThresholdPercentage**, **keyStorageProvider**, **subjectNameFormat**, **subjectAlternativeNameType**, **certificateValidityPeriodValue** y **certificateValidityPeriodScale** de la entidad [windows10CertificateProfileBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10certificateprofilebase)|
|Cambio|Beta|Se quitaron las propiedades **renewalThresholdPercentage**, **keyStorageProvider**, **subjectNameFormat**, **subjectAlternativeNameType**, **certificateValidityPeriodValue** y **certificateValidityPeriodScale** de la entidad [windows81CertificateProfileBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows81certificateprofilebase)|
|Cambio|Beta|Se quitó la propiedad **applyToWindows10Mobile** de la entidad [windowsPhone81GeneralConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsphone81generalconfiguration)|
|Cambio|Beta|Se agregaron las propiedades de navegación **enterpriseCerts**, **iosLobAppProvisioningConfigurations** y **symantecCert** a la entidad [deviceAppManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_deviceappmanagement)|
|Cambio|Beta|Se agregó la propiedad de navegación **userStatusOverview**  a la entidad [deviceCompliancePolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancepolicy)|
|Cambio|Beta|Se agregó la propiedad de navegación **userStatusOverview** a la entidad [deviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfiguration)|
|Cambio|Beta|Se agregaron las propiedades de navegación **groupAssignments**, **deviceStatuses** y **userStatuses** a la entidad [iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration)|
|Cambio|Beta|Se cambió el tipo de las propiedades siguientes en la entidad [windows10VpnConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10vpnconfiguration):<br/>**identityCertificate** de [windows10CertificateProfileBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10certificateprofilebase) a [windowsCertificateProfileBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowscertificateprofilebase)|
|Cambio|Beta|Se agregaron las propiedades **deviceComplianceCheckinThresholdDays** e **isScheduledActionEnabled** al tipo complejo [deviceManagementSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicemanagementsettings)|
|Cambio|Beta|Se quitaron las propiedades **windowsCommercialId** y **windowsCommercialIdLastModifiedTime** del tipo complejo [deviceManagementSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicemanagementsettings)|
|Cambio|Beta|Se agregaron las propiedades **bundleID**, **appName**, **publisher**, **enabled** y **showOnLockScreen** al tipo complejo [iosNotificationSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosnotificationsettings)|
|Cambio|Beta|Se quitaron las propiedades **bundleIdentifier**, **notificationsEnabled** y **showInLockScreen** del tipo complejo [iosNotificationSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosnotificationsettings)|



## <a name="january-2017"></a>Enero de 2017

### <a name="outlook-calendar"></a>Calendario de Outlook

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|v1.0|Nueva acción [findMeetingTimes](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_findmeetingtimes) para el recurso [user](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/user).|
|Adición|v1.0|Nuevo tipo complejo [attendeeBase](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/attendeebase) que consta de una propiedad de tipo para el tipo de asistente.|
|Adición|v1.0|Nuevos tipos complejos:<br/>[attendeeAvailability](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/attendeeavailability)<br/>[locationConstraint](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/locationconstraint) <br/>[locationConstraintItem](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/locationconstraintitem)<br/>[meetingTimeSuggestion](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/meetingtimesuggestion)<br/>[meetingTimeSuggestionsResult](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/meetingtimesuggestionsresult)<br/>[timeConstraint](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/timeconstraint)<br/>[timeSlot](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/timeslot)|
|Cambio|v1.0|El tipo complejo [attendee](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/attendee) ahora se deriva de attendeeBase, que a su vez se deriva de [recipient](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/recipient). Incluidas las propiedades heredadas, consta de las mismas propiedades **status**, **type** 7 **emailAddress** que antes.|
|Adición|Beta|hexColor se agregó al recurso [calendar](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/calendar).|

### <a name="intune-apis"></a>API de Intune

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Nuevas entidades agregadas: <br/>[appReportingOverviewStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_appreportingoverviewstatus)<br/>[deviceComplianceDeviceOverview](https://developer.microsoft.com/en-us/graph/docs//api-reference/beta/resources/intune_deviceconfig_devicecompliancedeviceoverview)<br/>[deviceConfigurationDeviceOverview](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationdeviceoverview)<br/>[deviceManagementExchangeOnpremisesPolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_devicemanagementexchangeonpremisespolicy)<br/>[iosDeviceFeaturesConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosdevicefeaturesconfiguration)<br/>[iosEducationDeviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioseducationdeviceconfiguration)<br/>[iosLobAppProvisioningConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_ioslobappprovisioningconfiguration)<br/>[onpremisesConditionalAccessSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_onpremisesconditionalaccesssettings)<br/>[sharedPCConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_sharedpcconfiguration)<br/>[windows10EnterpriseModernAppManagementConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration)<br/>[windows10SecureAssessmentConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10secureassessmentconfiguration)<br/>[windows10WindowsInformationProtectionConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10windowsinformationprotectionconfiguration)|
|Adición|Beta|Nuevos tipos complejos agregados: <br/> [appInstallationFailure](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_appinstallationfailure)<br/>[enterpriseCloudResource](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_enterprisecloudresource)<br/>[iosHomeScreenApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioshomescreenapp)<br/>[iosHomeScreenFolder](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioshomescreenfolder)<br/>[iosHomeScreenFolderPage](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioshomescreenfolderpage)<br/>[iosHomeScreenItem](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioshomescreenitem)<br/>[iosHomeScreenPage](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ioshomescreenpage)<br/>[iosNotificationSettings](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_iosnotificationsettings)<br/>[iPv6Range](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_ipv6range)<br/>[sharedPCAccountManagerPolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_sharedpcaccountmanagerpolicy)<br/>[windowsInformationProtectionAppRule](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionapprule)<br/>[windowsInformationProtectionAppRuleAppLockerPolicyFileTemplate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionappruleapplockerpolicyfiletemplate)<br/>[windowsInformationProtectionAppRuleDesktopTemplate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionappruledesktoptemplate)<br/>[windowsInformationProtectionAppRuleStoreAppTemplate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionapprulestoreapptemplate)<br/>[windowsInformationProtectionAppRuleTemplate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionappruletemplate)<br/>[windowsInformationProtectionCorporateNetworkLocation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectioncorporatenetworklocation)<br/>[windowsInformationProtectionDataRecoveryCertificate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectiondatarecoverycertificate)<br/>[windowsInformationProtectionProtectedLocation](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocation)<br/>[windowsInformationProtectionProtectedLocationEnterpriseCloudResources](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocationenterprisecloudresources)<br/>[windowsInformationProtectionProtectedLocationEnterpriseInternalProxyServers](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocationenterpriseinternalproxyservers)<br/>[windowsInformationProtectionProtectedLocationEnterpriseIPv4Ranges](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocationenterpriseipv4ranges)<br/>[windowsInformationProtectionProtectedLocationEnterpriseIPv6Ranges](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocationenterpriseipv6ranges)<br/>[windowsInformationProtectionProtectedLocationEnterpriseNetworkDomainNames](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocationenterprisenetworkdomainnames)<br/>[windowsInformationProtectionProtectedLocationEnterpriseProxyServers](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocationenterpriseproxyservers)<br/>[windowsInformationProtectionProtectedLocationNeutralResources](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windowsinformationprotectionprotectedlocationneutralresources)
|Eliminación|Beta|Se quitaron los tipos complejos siguientes y se reemplazaron por microsoft.graph.Json:<br/>managedAppDeploymentSummary <br/>managedAppSummary<br /> |
|Cambio|Beta|Se reemplazó el tipo de propiedad appConfigComplianceStatus por complianceStatus en las siguientes entidades: <br/>[managedDeviceMobileAppConfigurationDeviceStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfigurationdevicestatus)<br/>[managedDeviceMobileAppConfigurationUserStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfigurationuserstatus)|
|Cambio|Beta|Para el recurso [managedAppStatusRaw](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_managedappstatusraw), se cambió el contenido de tipo de propiedad de managedAppSummary a Json.|
|Cambio|Beta|Se quitó la función getUsersWithFlaggedAppRegistration de la colección [managedAppRegistration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_mam_managedappregistration).|
|Cambio|Beta|Se cambió la propiedad de navegación **vppToken** de la entidad [iosVppApp](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_iosvppapp) para que ya no sea una colección contenida.|
|Cambio|Beta|Se agregó la propiedad **deviceStatusOverview** a las entidades [deviceConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfiguration) y [deviceCompliancePolicy](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancepolicy).|
|Cambio|Beta|Se agregó la propiedad **appReportingOverview** al singleton [deviceAppManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_deviceappmanagement).|
|Cambio|Beta|Se agregaron las propiedades **deviceDisplayName** y **userPrincipalName** a las entidades [deviceConfigurationDeviceStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationdevicestatus), [deviceComplianceDeviceStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancedevicestatus) y [managedDeviceMobileAppConfigurationDeviceStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfigurationdevicestatus).|
|Cambio|Beta|Se agregó la propiedad **ruleName** a la entidad [deviceComplianceScheduledActionForRule](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecompliancescheduledactionforrule).|
|Cambio|Beta|Se agregaron las propiedades **devicesCount**, **userDisplayName** y **userPrincipalName** a las entidades [deviceConfigurationUserStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_deviceconfigurationuserstatus), [deviceComplianceUserStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicecomplianceuserstatus) y [managedDeviceMobileAppConfigurationUserStatus](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_manageddevicemobileappconfigurationuserstatus).|
|Cambio|Beta|Se agregó la colección [notificationMessageTemplates](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_notification_notificationmessagetemplate) al singleton [deviceManagement](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_devicemanagement).|
|Cambio|Beta|Se agregaron las propiedades **isDefault**, **lastModifiedDateTime**, **locale**, **messageTemplate** y **subject** a la entidad [localizedNotificationMessage](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_localizednotificationmessage).|
|Cambio|Beta|Se agregaron las propiedades **azureActiveDirectoryDeviceId**, **deviceCategory**, **deviceRegistrationState** y **managementAgent** a la entidad [managedDevice](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_onboarding_manageddevice).|
|Cambio|Beta|Se agregó la propiedad **lastModifiedDateTime** a la entidad [mobileAppCategory](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_apps_mobileappcategory).|
|Cambio|Beta|Se agregaron las propiedades **brandingOptions**, **defaultLocale**, **displayName**, **fromEmailAddress**, **lastModifiedDateTime**, **localizedNotificationMessages** a la entidad [notificationMessageTemplate](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_notification_notificationmessagetemplate).|
|Cambio|Beta|Se agregaron las propiedades **appsAllowTrustedAppsSideloading**, **appsBlockWindowsStoreOriginatedApps**, **developerUnlockSetting**, **edgeBlockAccessToAboutFlags**, **edgeBlockDeveloperTools**, **edgeBlockExtensions**, **edgeBlockInPrivateBrowsing**, **edgeFirstRunUrl**, **edgeHomepageUrls**, **gameDvrBlocked**, **settingsBlockAddProvisioningPackage**, **settingsBlockChangeLanguage**, **settingsBlockChangePowerSleep**, **settingsBlockChangeRegion**, **settingsBlockChangeSystemTime**, **settingsBlockEditDeviceName**, **settingsBlockRemoveProvisioningPackage**, **sharedUserAppDataAllowed**, **smartScreenBlockPromptOverride**, **smartScreenBlockPromptOverrideForFiles**, **storageRestrictAppDataToSystemVolume**, **storageRestrictAppInstallToSystemVolume**, **webRtcBlockLocalhostIpAddress**, **windowsStoreBlockAutoUpdate** y **windowsStoreEnablePrivateStoreOnly** a la entidad [windows10GeneralConfiguration](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_deviceconfig_windows10generalconfiguration).|

## <a name="december-2016"></a>Diciembre de 2016

### <a name="delta-query"></a>Consulta de delta

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Agregar una nueva función de delta para las siguientes entidades para realizar [consulta de delta](https://developer.microsoft.com/en-us/graph/docs/concepts/delta_query_overview):<br/>contacto<br/>contactFolder<br/>evento<br/>grupo<br/>mailFolder<br/>mensaje<br/>usuario<br/>Vea los ejemplos siguientes:<br/>[Obtener los cambios incrementales de grupos (versión preliminar)](https://developer.microsoft.com/en-us/graph/docs/concepts/delta_query_groups)<br/>[Obtener los cambios incrementales para los mensajes de una carpeta (versión preliminar)](https://developer.microsoft.com/en-us/graph/docs/concepts/delta_query_message)<br/>[Obtener los cambios incrementales de usuarios (versión preliminar)](https://developer.microsoft.com/en-us/graph/docs/concepts/delta_query_users)|

### <a name="excel-apis"></a>API de Excel

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|v1.0|Se agregaron recurso workbookPivotTable, acción refresh y refreshAll en tablas dinámicas, recurso worbookRangeView, acción visibleView en el intervalo filtrado para devolver workbookRangeView al usuario, obtiene una recopilación de filas y recursos del intervalo de las funciones visibleView, columnsAfter, comunsBefore, resizedRange, rowsAbove y rowsBelow del recurso del intervalo y nuevas propiedades de tablas.|

### <a name="intune-apis"></a>API de Intune

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Recursos agregados y API de método para Microsoft Intune. Este es un conjunto grande de recursos y métodos para admitir la versión preliminar pública de Intune en Azure Portal. Para obtener información sobre el servicio Intune, vea la [documentación de Intune](https://go.microsoft.com/fwlink/?linkid=836405). Para obtener información sobre los recursos y las API de Intune, vea [Trabajar con Intune en Microsoft Graph](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/intune_graph_overview).|

## <a name="october-2016"></a>Octubre de 2016

### <a name="authorization-provider"></a>Proveedor de autorización

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|V1.0 y beta|La versión 2.0 del punto de conexión de autenticación ahora es compatible con la concesión de OAuth client_credentials, que se puede usar para [demonios y procesos de ejecución prolongada en escenarios empresariales](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols-oauth-client-creds/).|
|Adición|V1.0 y beta|La versión 2.0 del punto de conexión de autenticación ahora es compatible con [ámbitos de permisos que requieren el consentimiento del administrador](http://developer.microsoft.com/en-us/graph/docs/authorization/permission_scopes#permission-scope-details) a través del [punto de conexión de consentimiento de administrador](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-scopes/#admin-restricted-scopes).|
|Adición|V1.0 y beta|La versión 2.0 del punto de conexión de autenticación ahora es compatible con el consentimiento administrativo para todos los usuarios de un inquilino a través del [punto de conexión de consentimiento de administrador](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-scopes/#admin-restricted-scopes).|

### <a name="invitation-apis"></a>API de invitación

|**Tipo de cambio**|**Versión**|**Descripción**|
|:-------------|:-----------|:--------------|
|Adición|Beta|Se agregó la propiedad invitedUserType al tipo de entidad de invitación, que define el tipo de usuario (**Guest** o **Member**) al que se invita.|
|Eliminación|Beta|Se quitará la propiedad invitedToGroups del tipo de entidad de invitación el 11/11/2016. Esto quiere decir que ya no se podrá agregar un usuario invitado a un grupo con esta API. En su lugar, para agregar un usuario a un grupo, use la [API para agregar miembros](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/group_post_members).|

## <a name="september-2016"></a>Septiembre de 2016

### <a name="azure-ad-application-proxy"></a>Proxy de aplicación de Azure AD

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Las API del Proxy de aplicación de Azure AD están ahora disponibles en la versión Beta del extremo de Microsoft Graph. Estas API permiten publicar de forma segura aplicaciones locales para usuarios externos a la red corporativa con Azure AD como plano de control común para el acceso. Puede usar las API publicadas para escribir una aplicación que pueda recuperar y actualizar diversos aspectos del proxy de aplicación como _connectors_, _connectorGroups_ y la configuración de _onPremisesPublishing_ de una aplicación.|

### <a name="drive"></a>Unidad de disco

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregó la colección _shared_ para permitir el acceso a driveItems por shareId o la URL de uso compartido.|
|Adición|Beta|Se agregó la función _search_ a una unidad, que permite buscar más elementos de los que se encuentran en la carpeta raíz de la unidad.|


### <a name="driveitem"></a>DriveItem

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregó la compatibilidad con _createUploadSession_, que permite subir archivos con un tamaño superior a 4 MB a OneDrive, OneDrive para la Empresa y a bibliotecas de documentos de SharePoint.|
|Adición|Beta|Se agregó la propiedad _sharepointIds_ a driveItem, que devuelve identificadores de la API de SharePoint tradicional para driveItems almacenados en SharePoint.|
|Adición|Beta|Se agregaron propiedades adicionales en _remoteItem_.|
|Adición|Beta|Se agregó el valor _quickXorHash_ para archivos en OneDrive para la Empresa.|
|Adición|Beta|Se agregó un ámbito a _createSharingLink_ para permitir la creación de vínculos que se pueden compartir en la compañía o para vínculos que se pueden compartir de forma anónima.|

### <a name="extended-properties"></a>Propiedades extendidas

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Las [propiedades extendidas](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/extended-properties-overview) ahora son compatibles con los recursos siguientes: message, mailFolder, event, calendar, contact, contactFolder, group event, group calendar, group post.|

### <a name="groups"></a>Grupos

Se agregó soporte para la pertenencia a grupos dinámicos con la API de vista previa pública, incluidos los añadidos listados en la tabla siguiente.

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregó la propiedad **membershipRule**, que contiene reglas que controlan la pertenencia a este grupo, si el grupo es un grupo dinámico.|
|Adición|Beta|Se agregó la propiedad **membershipRuleProcessingState** para controlar si el procesamiento de pertenencia dinámica está activado o pausado para este grupo.|
|Adición|Beta|Se estableció la propiedad **groupTypes** para que contenga **DynamicMembership** para activar la función de grupos dinámicos para este grupo.|
|Adición|Beta|Se agregó la propiedad **preferredLanguage** para indicar el idioma preferido de un grupo de Office 365.|
|Adición|Beta|Se agregó la propiedad **theme** para especificar un tema de color del grupo de Office 365.|

### <a name="hybrid-deployment-support"></a>Compatibilidad con implementaciones híbridas

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Las aplicaciones pueden usar la API de Correo, calendario y contactos de Outlook versión 1.0 para obtener acceso a buzones locales en una implementación híbrida con Exchange 2016 actualización acumulativa 3 (CU3). Encontrará más información sobre la compatibilidad de API de REST en [implementaciones híbridas](https://developer.microsoft.com/en-us/graph/docs/overview/hybrid_rest_support) específicas. **Nota:** Si utiliza estos conjuntos de API en v1.0, verá ahora que sus aplicaciones, incluidas las aplicaciones de producción, funcionan en buzones locales que cumplan requisitos de implementación híbrida específicos. Esta funcionalidad solo se encuentra en vista previa.|

### <a name="identityriskevents"></a>IdentityRiskEvents

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio|Beta|Como parte del cambio del esquema donde el tipo de dos propiedades de ubicación se reemplaza por un nuevo tipo complejo en el punto de conexión de identityRiskEvents, las propiedades siguientes se modifican o agregan en el punto de conexión de identityRiskEvents:</br>**location**: cambia de Edm.String a ComplexType signInLocation.<br/>**previousLocation**: cambia de Edm.String a ComplexType signInLocation.<br/>**signInLocation**: nuevo ComplexType que contiene las propiedades city, state, countryOrRegion y geoCoordinates.<br/>**geoCoordinates**: nuevo ComplexType que contiene las propiedades latitude y longitude.|

### <a name="invitation-manager"></a>Administrador de invitaciones

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Las API del administrador de invitaciones están ahora disponibles en el extremo beta de Microsoft Graph. Puede usar la API del administrador de invitaciones para crear una invitación con el fin de agregar un usuario externo a la organización. Como parte de la invitación, también puede agregar los usuarios invitados a un grupo de Office 365. Para obtener más información, consulte [Administrador de invitaciones](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/invitation).|

### <a name="onedrive"></a>OneDrive

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó el método **CreateUploadSession** en **driveItem**, que permite subir archivos de gran tamaño y reanudar operaciones de carga.|
|Adición|v1.0|Se agregaron propiedades para realizar un seguimiento de id. de SharePoint en elementos de SharePoint (**sharepointIds**) y una propiedad para identificar carpetas raíz (**root**).|
|Adición|v1.0|Se agregó la colección raíz **Shares**, que se puede usar con shareIds o con vínculos de uso compartido para obtener acceso a elementos compartidos en OneDrive y SharePoint. Devuelve un nuevo tipo, sharedDriveItem.|
|Adición|v1.0|Se agregó el método **Invite** en driveItem, que permite agregar permisos a elementos. |
|Adición|v1.0|Se agregó el método **Search** en drive, que permite buscar elementos en la unidad y en elementos compartidos. |
|Adición|v1.0|Se agregó la propiedad **processingMetadata** en el tipo complejo de archivos quickXorHash en tipo complejo de hash. |
|Adición|v1.0|Propiedad **quickXorHash** en tipo complejo de hash. |

### <a name="outlook-calendar"></a>Calendario de Outlook

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó la propiedad **onlineMeetingUrl** al recurso [event](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/event).|
|Adición|Beta|Se agregó la acción [forward](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/event_forward) al recurso event.|
|Adición|Beta|Se agregaron propiedades al recurso [calendar](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/calendar) para admitir el uso compartido de calendarios: **canEdit**, **canShare**, **canViewPrivateItems**, **isShared**, **isShareWithMe**, **owner**.|

### <a name="outlook-mail"></a>Correo de Outlook

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó el tipo complejo [mailboxSettings](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/mailboxsettings), que incluye las propiedades **automaticRepliesSetting**, **timeZone** y **language**.|
|Adición|v1.0|Se agregó la propiedad **mailboxSettings** al recurso [user](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/user).|
|Adición|Beta|Se agregó la compatibilidad para crear, generar listas, obtener y eliminar una o más instancias de una [mención](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/mention) en un mensaje. Las menciones admiten las llamadas para captar la atención de otros usuarios en un mensaje.|
|Adición|Beta|Se agregó la compatibilidad con la acción [getMailTips](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/user_getmailtips) para obtener las sugerencias de correo electrónico para destinatarios específicos. Se agregaron los siguientes recursos: automaticRepliesMailTips, mailTips, mailTipsError.|

### <a name="query-parameters"></a>Parámetros de consulta

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio|Beta|Se admiten los parámetros de consulta sin prefijos "$" desde el 26/09/16. El prefijo "$" en parámetros de consulta es opcional. Para obtener más detalles, consulte la publicación de blog [Compatibilidad con los parámetros de consulta sin el prefijo "$" en Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph).|

### <a name="sharepoint"></a>SharePoint

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Acceso a sitios de SharePoint y [listado por id.](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/list_get) o [ruta/URL](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/baseitem_getbyurl).|
|Adición|Beta|Compatibilidad con la [generación de listas, creación, obtención y eliminación de instancias de listItem](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/listitem).|

### <a name="users"></a>Usuarios

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregó la propiedad de solo lectura **refreshTokensValidFromDateTime** para indicar desde cuándo son válidos los tokens de actualización o sesión. Los tokens emitidos anteriormente no son válidos y cualquier intento de usarlos obligaría al usuario a volver a iniciar sesión.|
|Adición|Beta|Se agregó la propiedad **showInAddressList** para controlar si la lista global de direcciones de Outlook tiene que contener este usuario.|
|Adición|Beta|Se agregó la acción de servicio **invalidateAllRefreshTokens**, que invalida todos los tokens de actualización y de sesión del usuario emitidos a las aplicaciones, al restablecer la propiedad de usuario **refreshTokensValidFromDateTime** a la fecha y hora actuales.|


### <a name="webhooks"></a>Webhooks

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron elementos raíz de Drive a webhooks como un recurso al que se puede suscribir.|

## <a name="august-2016"></a>Agosto de 2016

### <a name="contacts"></a>Contactos

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Como parte del cambio del esquema donde algunas propiedades se quitan y las colecciones correspondientes se agregan al punto de conexión de contactos, las propiedades siguientes se agregan al punto de conexión de contactos: _Websites Collection(ComplexType: Website)_,_Phones Collection (ComplexType: Phone)_, _PostalAddress Collection(ComplexType: PhysicalAddress)_. Para obtener más información, vea la entrada del blog [Cambios próximos a las API de Contactos y Personas](https://blogs.msdn.microsoft.com/exchangedev/2016/06/09/upcoming-changes-to-contacts-and-people-apis/).|
|Eliminación|Beta|Como parte del cambio del esquema donde algunas propiedades se quitan y las colecciones correspondientes se agregan al punto de conexión de contactos, las propiedades siguientes se quitan del punto de conexión de contactos: _BusinessHomePage_,_HomePhones_, _MobilePhone1_, _BusinessPhones_, _HomeAddress_, _BusinessAddress_, _OtherAddress_. Para obtener más información, vea la entrada del blog [Cambios próximos a las API de Contactos y Personas](https://blogs.msdn.microsoft.com/exchangedev/2016/06/09/upcoming-changes-to-contacts-and-people-apis/).|

### <a name="excel-apis"></a>API de Excel

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|La API de REST de Excel en Microsoft Graph ya está disponible. Ahora, se pueden crear integraciones complejas y avanzadas con libros de Excel en Office 365. Vea la entrada del blog [Potencie sus aplicaciones con la nueva API de REST de Excel en Microsoft Graph](http://dev.office.com/blogs/power-your-apps-with-the-new-excel-rest-api) para obtener más información.|

### <a name="people"></a>Contactos

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio|Beta|La propiedad _WebSite_ cambia de nombre por _Websites_. Para obtener más información, vea [Cambios próximos a las API de Contactos y Personas](https://blogs.msdn.microsoft.com/exchangedev/2016/06/09/upcoming-changes-to-contacts-and-people-apis/).|

### <a name="privileged-identity-management"></a>Privileged Identity Management

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Las API de REST de Privileged Identity Management (PIM) ahora están disponibles en el punto de conexión beta de Microsoft Graph. [Privileged Identity Management](https://azure.microsoft.com/en-us/documentation/articles/active-directory-privileged-identity-management-configure/) ofrece la activación Just-In-Time para roles organizativos de Azure AD con privilegios, como Administrador global, Administrador de facturación, etc. Puede usar las API publicadas para escribir aplicaciones que recuperen y actualicen asignaciones de roles con privilegios y activar usuarios en roles. Para obtener más información, consulte [Microsoft Graph: versión preliminar de API Privileged Identity Management de Azure AD disponibles en beta](http://dev.office.com/blogs/microsoft-graph-azure-ad-privileged-identity-management-apis-beta) y [Privileged Identity Management de Azure AD](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/privilegedidentitymanagement_root).|

## <a name="july-2016"></a>Julio de 2016

### <a name="administrative-units"></a>Unidades administrativas

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se introdujo la nueva API en versión preliminar de unidades administrativas. Las unidades administrativas permiten a las organizaciones subdividir Azure Active Directory y delegar tareas administrativas en dichas subdivisiones. Las subdivisiones pueden representar regiones, departamentos, centros de costes, etc. Esto puede administrarse ahora mediante la API de Microsoft Graph.|

## <a name="june-2016"></a>Junio de 2016

### <a name="identityriskevents"></a>IdentityRiskEvents

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se introdujo la nueva API en versión preliminar IdentityRiskEvents. Esta API funciona junto con la protección de identidad de Azure Active Directory. Se puede usar para eventos de riesgo de consulta generados por Identity Protection. Para más información, consulte [Introducción de la nueva API de vista previa en Microsoft Graph: IdentityRiskEvents](http://dev.office.com/blogs/identityriskevents-api-preview).

### <a name="subscriptions"></a>Suscripciones

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Los ámbitos de solo aplicación ahora son compatibles con las suscripciones de _correo_ y _contactos_.|

## <a name="may-2016"></a>Mayo de 2016

### <a name="calendar"></a>Calendario

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio importante|Beta|Cambios en la API findMeetingTimes. Para obtener más información, consulte la publicación de blog [Actualización de la API findMeetingTimes API de Microsoft Graph](http://dev.office.com/microsoft-graph-findmeetingtimes-api-update). Este cambio entró en vigor el 19 de mayo de 2016.

### <a name="contact"></a>Contacto

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó _extensions_, que es un tipo abstracto, para permitir la compatibilidad con OData v4 Open Type openTypeExtension.|

### <a name="directory"></a>Directorio

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio importante|Beta|Se cambió el nombre de _settingTemplateId_ a _templateId_. Este cambio tendrá efecto el 19 de mayo de 2016.|

### <a name="event"></a>Evento

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó _extensions_, que es un tipo abstracto, para permitir la compatibilidad con OData v4 Open Type openTypeExtension.|

### <a name="eventmessages"></a>EventMessages

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregaron _inferenceClassification_ y _extensions_ a _eventMessages_.|
|Adición|Beta|Se agregó _responseRequested_ a _eventMessageRequest_.|

### <a name="messages"></a>Mensajes

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregaron _inferenceClassification_ y _extensions_ a _messages_.|
|Adición|Beta|Se agregó _wellknownname_ a _contactFolder_.|Cambios en la API _findMeetingTimes_. Para obtener más información, consulte la publicación de blog [Actualización de la API findMeetingTimes API de Microsoft Graph](http://dev.office.com/microsoft-graph-findmeetingtimes-api-update). Este cambio tendrá efecto el 19 de mayo de 2016.|

### <a name="post"></a>Publicación

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó _extensions_, que es un tipo abstracto, para permitir la compatibilidad con OData v4 Open Type openTypeExtension.|

### <a name="user"></a>Usuario

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó el tipo de recurso _inferenceClassification_.|
|Adición|Beta|Se agregó _timeZone_ a _mailboxsettings_.|
|Adición|Beta|Se agregó _findMeetingTimes_ de API a _user_.|

## <a name="april-2016"></a>Abril de 2016

### <a name="general"></a>General

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|V1.0 y beta|Se agregó compatibilidad para respetar _Accept-Encoding:gzip_.|
|Adición|v1.0|Agregada compatibilidad con el segmento de transmisión en la ruta de acceso de $expand. Por ejemplo, 'https://graph.microsoft.com/v1.0/me/messages?$expand=microsoft.graph.eventMessage/event'.|
|Adición|Beta|Se agregó compatibilidad con la solicitud PATCH en propiedades estructurales. Por ejemplo: 'PATCH /me/mailboxSettings'.|
|Adición|Beta|Azure Active Directory ahora se usa como una reserva para solicitudes de /beta/users/id/photo cuando Outlook no puede procesar las solicitudes (por ejemplo, si el usuario no tiene una licencia de buzón o si el espacio empresarial no tiene una suscripción a Exchange Online). NOTA: Esta reserva está disponible para GET y PATCH.|
|Adición|Beta|Agregada compatibilidad con el segmento de transmisión en la ruta de acceso de $expand. Por ejemplo: 'https://graph.microsoft.com/v1.0/me/messages?$expand=microsoft.graph.eventMessage/event'.|

### <a name="onedrive"></a>OneDrive

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Solución|v1.0|Se solucionó el problema en el que las solicitudes de createLink de OneDrive producían el error 500 y el error "Tipo de propiedad de extensión no admitida".|

## <a name="march-2016"></a>Marzo de 2016

### <a name="calendar"></a>Calendario

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_.|
|Adición|Beta|Se agregó la propiedad _suggestionHint_ a _meetingTimeCandidate_.|
|Adición|Beta|Se agregó la propiedad _locationUri_ a _location_.|
|Adición|Beta|Se agregaron _type_ y _postOfficeBox_ a _physicalAddress_.|
|Cambio|Beta|_findMeetingTimes_ acepta ahora el nuevo parámetro _ReturnSuggestionHints_.|
|Cambio|Beta|_findMeetingTimes_ devuelve ahora una colección de _meetingTimeCandidate_.|

### <a name="drive"></a>Unidad de disco

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|V1.0 y beta|Se agregó la función _recent_ para hacer una lista de un conjunto de elementos usados recientemente por el usuario que ha iniciado sesión. Esta lista incluye elementos que están en la unidad de disco del usuario, así como elementos de otras unidades de disco a los que tiene acceso. Ejemplo: GET /me/drive/recent.|
|Adición|V1.0 y beta|Se agregó la función _sharedWithMe_ para hacer una lista de un conjunto de elementos que se comparten actualmente con el usuario actual. Ejemplo: GET /me/drive/sharedWithMe.|

### <a name="driveitem"></a>DriveItem

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|V1.0 y beta|Se agregó el tipo _remoteItem_ que proporciona un vínculo a un elemento en otra unidad de disco.|
|Adición|V1.0 y beta|Se agregó el tipo _sharingInvitation_ que proporciona detalles de cualquier invitación para uso compartido asociada a este permiso.|
|Adición|V1.0 y beta|Se agregó la función _delta_ para el control de cambios a elementos de una unidad de disco. Ejemplo: GET /me/drive/items/{item-id}/delta|
|Adición|V1.0 y beta|Se agregó _copy_, que crea una copia de un _driveItem_ (incluidos los elementos secundarios), en un nuevo elemento primario o con un nuevo nombre. Ejemplo: POST /me/drive/items/{item-id}/copy.|
|Adición|V1.0 y beta|Los atributos de la instancia _conflictBehavior_ son ahora aplicables a _driveItem_.|
|Adición|Beta|Se agregó la función _invite_ para enviar una invitación para uso compartido a un elemento existente. Una invitación para uso compartido crea un enlace único para compartir y envía un correo al destinatario de la invitación que incluye el vínculo para compartir. Ejemplo: POST /drive/items/{item-id}/invite.

### <a name="event"></a>Evento

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron una nueva propiedad _onlineMeetingUrl_ y un nuevo método _cancel_.|

### <a name="event-messages"></a>Mensajes de eventos

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron las propiedades _startDateTime_, _endDateTime_, _location_, _type_, _recurrence_, _isOutOfDate_, _conversationIndex_, _unsubscribe_, _unsubscribeData_, _unsubscribeEnabled_ y _flag_ al objeto _eventmessage_|
|Adición|Beta|Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_.|
|Adición|Beta|Se agregó el nuevo método _unsubscribe_.|

### <a name="excel"></a>Excel

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Agregamos nuevas API del REST de Excel que permiten leer y modificar datos en un libro de Excel. Ahora, es posible crear aplicaciones inteligentes que permiten a los usuarios aprovechar el contenido almacenado en un libro de Excel proporcionado información sobre los datos. Se aprovechan las competencias analíticas de Excel, crear tablas y gráficos y extraer una imagen de gráfico visualmente atractiva: todo desde la aplicación. Para más información, consulte [Trabajar con Excel en Microsoft Graph](http://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/excel).|

### <a name="general"></a>General

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|V1.0 y beta|Se mejoran los mensajes de error al resolver alias de inquilino y tokens de JWT (AAD) rechazados.|
|Adición|V1.0 y beta|La ubicación del punto de conexión de servicio de autorización ahora se devuelve en el encabezado _www-authenticate_ cuando se recibe una solicitud con un token de portador vacío.|
|Adición|V1.0 y beta|Se solucionó la capacidad para filtrar en una propiedad de identificador de entidad. Ejemplo: GET https://graph.microsoft.com/v1.0/users?$filter=id+eq+'x'<br/>Anteriormente, cualquier solicitud POST para acciones de servicio y funciones necesitaba el nombre de la acción o función con el prefijo microsoft.graph. Por ejemplo: POST https://graph.microsoft.com/v1.0/me/Microsoft.Graph.getMemberGroups.<br/>El prefijo ya no es necesario (aunque todavía se puede especificar). Por lo que ahora también funcionaría lo siguiente: POST https://graph.microsoft.com/v1.0/me/getMemberGroups.|
|Cambio|Beta|Se limpiaron los nombres de propiedad de suscripción.|
|Adición|Beta|Se agregó la capacidad de detectar (a través de _directorySettingTemplates_) y de invalidar el comportamiento predeterminado (al crear una _configuración_ a partir de la plantilla) para entidades y su función asociada. Inicialmente, esta plantilla solo se proporciona para controlar comportamientos en los grupos de Office.|

### <a name="mail-folder"></a>Carpeta de correo

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron las propiedades _wellKnownName_ y _userConfigurations_.|
|Adición|Beta|Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_.|

### <a name="messages"></a>Mensajes

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó la propiedad _mobilePhone_.|
|Adición|V1.0 y beta|Se agregó la propiedad _internetMessageId_. El identificador del mensaje en el formato especificado por [RFC2822](http://www.ietf.org/rfc/rfc2822.txt).|
|Cambio|Beta|El nombre de la propiedad _mobilePhone1_ se cambió a _mobilePhone_.|
|Cambio|Beta|_createReply_ y _createReplyAll_ aceptan los nuevos parámetros _Message_ y _comment_.|
|Cambio|Beta|_createForward_ acepta los nuevos parámetros _Message_, _ToRecipients_ y _comment_.|
|Cambio|Beta|_reply_, _replyAll_ y _forward_ aceptan el nuevo parámetro _Message_.|

### <a name="permission"></a>Permiso

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|V1.0 y beta|Se agregó la propiedad _sharingInvitation_ que proporciona detalles de cualquier invitación para uso compartido asociada a este permiso.|

### <a name="person"></a>Usuario

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron las nuevas propiedades _birthday_, _personNotes_, _isFavorite_, _phones_, _permission_, _postalAddresses_,_websites_,_yomiCompany_, _department_, _profession_, _mailboxType_ y _personType_.|
|Adición|Beta|Se agregaron los nuevos tipos de enumeración _physicalAddressType_, _webSite _, _phone_ y _webSiteType_.|

### <a name="reference-attachment"></a>Datos adjuntos de referencia

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron las nuevas propiedades _sourceUrl_, _providerType_, _thumbnailUrl_, _previewUrl_, _permission_ y _isFolder_.|
|Adición|Beta|Se agregaron las propiedades _singleValueExtendedProperties_ y _multiValueExtendedProperties_.|
|Adición|Beta|Se agregaron los nuevos tipos de enumeración _referenceAttachmentProvider_ y _referenceAttachmentPermission_.|

### <a name="subscriptions"></a>Suscripciones

|**Tipo de cambio**|**Extremo**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Los webhooks ahora son GA en el punto de conexión versión 1.0 a través del recurso _/Subscriptions_. Crear, leer, renovar y eliminar suscripciones para recibir notificaciones sobre datos de conversaciones de grupo de Office 365 y Outlook.|

### <a name="user"></a>Usuario

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregaron la propiedad _mailboxSettings_ y los tipos correspondientes.|

## <a name="february-2016"></a>Febrero de 2016

### <a name="driveitem"></a>DriveItem

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|V1.0 y beta|Nueva propiedad _remoteItem_ en driveItem para cuentas de Microsoft.|

### <a name="general"></a>General

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio|V1.0 y beta|-_/me/drive_ funciona ahora para cuentas de Microsoft y cuentas profesionales y educativas.|
|Cambio|V1.0 y beta|Las solicitudes de unidad de disco para cuentas cuyo almacenamiento de OneDrive se aprovisionó a petición funcionan de manera más confiable y en más escenarios en los que los sitios de SharePoint predeterminados de inquilinos utilizan nombres no estándar.|
|Eliminación|Beta|Se quitaron diversos tipos no implementados del esquema beta para que se parezca más al esquema 1.0.|

### <a name="subscriptions"></a>Suscripciones

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Validación de notificationUrl en la creación de la suscripción. Para obtener más información, consulte [Actualización de WebHooks de Microsoft Graph: enero de 2016](http://dev.office.com/blogs/Microsoft-Graph-WebHooks-Update-January-2016).|
|Adición|Beta|Las entidades de suscripción ahora se pueden eliminar: DELETE https://graph.microsoft.com/beta/subscriptions/|

### <a name="users"></a>Usuarios

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Cambio|V1.0 y beta|_displayName_ ahora se devuelve para cuentas Microsoft.|

## <a name="january-2016"></a>Enero de 2016

### <a name="contacts"></a>Contactos

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|v1.0|Se agregó la propiedad mobilePhone al conjunto de entidades de contactos personales.|

### <a name="directoryobjects"></a>directoryObjects

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Solución|V1.0 y beta|Se solucionaron las acciones de llamada que estaban enlazadas a directoryObjects y que producían el error siguiente:  El tipo de valor devuelto de la operación no se admite con el conjunto de entidades especificado. Se aplica a las siguientes acciones: _microsoft.graph.checkMemberObjects_, _microsoft.graph.getMemberObjects_, _microsoft.graph.checkMemberGroups_, _microsoft.graph.assignLicense_, _microsoft.graph.changePassword_.|

## <a name="december-2015"></a>Diciembre de 2015

### <a name="contacts"></a>Contactos

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregó la propiedad mobilePhone al conjunto de entidades de contactos personales.|

### <a name="general"></a>General

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Solución|V1.0 y beta|Se solucionaron las solicitudes en las que se usaban expresiones de $filter y se especificaba la misma propiedad más de una vez, que producían el siguiente error 500: Ya se ha agregado un elemento con la misma clave.|
|Solución|V1.0 y beta|Se solucionó el problema de no distinción de mayúsculas de minúsculas para nombres de parámetros de acción y sus valores.|
|Solución|V1.0 y beta|Se solucionó el procesamiento de solicitudes de cargas que contenían valores nulos para algunas propiedades complejas integradas y que generaban una excepción de referencia nula.|
|Adición|V1.0 y beta|Se agregó la compatibilidad con la ordenación y filtrado de propiedades de tipo complejo.|
|Adición|V1.0 y beta|Se agregó la propiedad authorization_uri en el encabezado www-authenticate de una respuesta 401. Este URI se puede usar para iniciar el flujo de adquisición de tokens.|
|Adición|V1.0 y beta|Se mejoraron los mensajes de error en usuarios y grupos.|

### <a name="groups"></a>Grupos

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Solución|V1.0 y beta|Se solucionaron las llamadas a las siguientes acciones de grupo: _microsoft.graph.addFavorite_, _microsoft.graph.removeFavorite_ y _microsoft.graph.resetUnseenCount_.|

### <a name="messages"></a>Mensajes

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Adición|Beta|Se agregó el subtipo eventMessageRequest de las propiedades eventMessage y startDateTime, endDateTime, location, type, recurrence e isOutOfDate al tipo eventMessage.|

### <a name="users"></a>Usuarios

|**Tipo de cambio**|**Versión**|**Descripción**|
|:--------------|:-----------|:--------------|
|Solución|V1.0 y beta|Se solucionó la capacidad para seleccionar determinadas propiedades de usuario en otros usuarios, cuando se hacía referencia al usuario con el nombre principal de usuario (UPN). Por ejemplo: https://graph.microsoft.com/v1.0/users/anotherUser@contoso.com?$select=aboutMe|
|Solución|V1.0 y beta|Se solucionó la llamada a la función enlazada de usuario _microsoft.graph.reminderView_, que generaba el siguiente error: No se pudo encontrar una propiedad denominada businessPhones en el tipo Microsoft.OutlookServices.Reminder.|
|Solución|V1.0 y beta|Se solucionó la creación y actualización de usuarios (POST/PATCH /v1.0/users), que generaba el error 400.|