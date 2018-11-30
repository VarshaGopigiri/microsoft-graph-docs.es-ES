---
title: Obtener iosGeneralDeviceConfiguration
description: Lea las propiedades y las relaciones del objeto iosGeneralDeviceConfiguration.
ms.openlocfilehash: cbbdb03accabdb2a410a285218a830031862e0cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083219"
---
# <a name="get-iosgeneraldeviceconfiguration"></a><span data-ttu-id="c7e38-103">Obtener iosGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7e38-103">Get iosGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="c7e38-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c7e38-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c7e38-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c7e38-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c7e38-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7e38-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7e38-107">Lea las propiedades y las relaciones del objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c7e38-107">Read properties and relationships of the [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7e38-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7e38-108">Prerequisites</span></span>
<span data-ttu-id="c7e38-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7e38-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7e38-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7e38-111">Permission type</span></span>|<span data-ttu-id="c7e38-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7e38-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7e38-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7e38-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c7e38-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7e38-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="c7e38-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7e38-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7e38-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7e38-116">Not supported.</span></span>|
|<span data-ttu-id="c7e38-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7e38-117">Application</span></span>|<span data-ttu-id="c7e38-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7e38-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7e38-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7e38-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c7e38-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c7e38-120">Optional query parameters</span></span>
<span data-ttu-id="c7e38-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7e38-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c7e38-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e38-122">Request headers</span></span>
|<span data-ttu-id="c7e38-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7e38-123">Header</span></span>|<span data-ttu-id="c7e38-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c7e38-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7e38-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7e38-125">Authorization</span></span>|<span data-ttu-id="c7e38-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c7e38-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7e38-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c7e38-127">Accept</span></span>|<span data-ttu-id="c7e38-128">application/json</span><span class="sxs-lookup"><span data-stu-id="c7e38-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7e38-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e38-129">Request body</span></span>
<span data-ttu-id="c7e38-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c7e38-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7e38-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7e38-131">Response</span></span>
<span data-ttu-id="c7e38-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7e38-132">If successful, this method returns a `200 OK` response code and [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7e38-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7e38-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7e38-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e38-134">Request</span></span>
<span data-ttu-id="c7e38-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7e38-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="c7e38-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7e38-136">Response</span></span>
<span data-ttu-id="c7e38-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7e38-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 9095

{
  "value": {
    "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
    "id": "ebba5202-5202-ebba-0252-baeb0252baeb",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "accountBlockModification": true,
    "activationLockAllowWhenSupervised": true,
    "airDropBlocked": true,
    "airDropForceUnmanagedDropTarget": true,
    "airPlayForcePairingPasswordForOutgoingRequests": true,
    "appleWatchBlockPairing": true,
    "appleWatchForceWristDetection": true,
    "appleNewsBlocked": true,
    "appsSingleAppModeList": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ],
    "appsVisibilityList": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ],
    "appsVisibilityListType": "appsInListCompliant",
    "appStoreBlockAutomaticDownloads": true,
    "appStoreBlocked": true,
    "appStoreBlockInAppPurchases": true,
    "appStoreBlockUIAppInstallation": true,
    "appStoreRequirePassword": true,
    "bluetoothBlockModification": true,
    "cameraBlocked": true,
    "cellularBlockDataRoaming": true,
    "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
    "cellularBlockPerAppDataModification": true,
    "cellularBlockPersonalHotspot": true,
    "cellularBlockVoiceRoaming": true,
    "certificatesBlockUntrustedTlsCertificates": true,
    "classroomAppBlockRemoteScreenObservation": true,
    "classroomAppForceUnpromptedScreenObservation": true,
    "compliantAppsList": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ],
    "compliantAppListType": "appsInListCompliant",
    "configurationProfileBlockChanges": true,
    "definitionLookupBlocked": true,
    "deviceBlockEnableRestrictions": true,
    "deviceBlockEraseContentAndSettings": true,
    "deviceBlockNameModification": true,
    "diagnosticDataBlockSubmission": true,
    "diagnosticDataBlockSubmissionModification": true,
    "documentsBlockManagedDocumentsInUnmanagedApps": true,
    "documentsBlockUnmanagedDocumentsInManagedApps": true,
    "emailInDomainSuffixes": [
      "Email In Domain Suffixes value"
    ],
    "enterpriseAppBlockTrust": true,
    "enterpriseAppBlockTrustModification": true,
    "faceTimeBlocked": true,
    "findMyFriendsBlocked": true,
    "gamingBlockGameCenterFriends": true,
    "gamingBlockMultiplayer": true,
    "gameCenterBlocked": true,
    "hostPairingBlocked": true,
    "iBooksStoreBlocked": true,
    "iBooksStoreBlockErotica": true,
    "iCloudBlockActivityContinuation": true,
    "iCloudBlockBackup": true,
    "iCloudBlockDocumentSync": true,
    "iCloudBlockManagedAppsSync": true,
    "iCloudBlockPhotoLibrary": true,
    "iCloudBlockPhotoStreamSync": true,
    "iCloudBlockSharedPhotoStream": true,
    "iCloudRequireEncryptedBackup": true,
    "iTunesBlockExplicitContent": true,
    "iTunesBlockMusicService": true,
    "iTunesBlockRadio": true,
    "keyboardBlockAutoCorrect": true,
    "keyboardBlockDictation": true,
    "keyboardBlockPredictive": true,
    "keyboardBlockShortcuts": true,
    "keyboardBlockSpellCheck": true,
    "kioskModeAllowAssistiveSpeak": true,
    "kioskModeAllowAssistiveTouchSettings": true,
    "kioskModeAllowAutoLock": true,
    "kioskModeAllowColorInversionSettings": true,
    "kioskModeAllowRingerSwitch": true,
    "kioskModeAllowScreenRotation": true,
    "kioskModeAllowSleepButton": true,
    "kioskModeAllowTouchscreen": true,
    "kioskModeAllowVoiceOverSettings": true,
    "kioskModeAllowVolumeButtons": true,
    "kioskModeBlockVolumeButtons": true,
    "kioskModeAllowZoomSettings": true,
    "kioskModeAppStoreUrl": "https://example.com/kioskModeAppStoreUrl/",
    "kioskModeBuiltInAppId": "Kiosk Mode Built In App Id value",
    "kioskModeRequireAssistiveTouch": true,
    "kioskModeRequireColorInversion": true,
    "kioskModeRequireMonoAudio": true,
    "kioskModeRequireVoiceOver": true,
    "kioskModeRequireZoom": true,
    "kioskModeManagedAppId": "Kiosk Mode Managed App Id value",
    "lockScreenBlockControlCenter": true,
    "lockScreenBlockNotificationView": true,
    "lockScreenBlockPassbook": true,
    "lockScreenBlockTodayView": true,
    "mediaContentRatingAustralia": {
      "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingCanada": {
      "@odata.type": "microsoft.graph.mediaContentRatingCanada",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingFrance": {
      "@odata.type": "microsoft.graph.mediaContentRatingFrance",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingGermany": {
      "@odata.type": "microsoft.graph.mediaContentRatingGermany",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingIreland": {
      "@odata.type": "microsoft.graph.mediaContentRatingIreland",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingJapan": {
      "@odata.type": "microsoft.graph.mediaContentRatingJapan",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingNewZealand": {
      "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingUnitedKingdom": {
      "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "mediaContentRatingUnitedStates": {
      "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
      "movieRating": "allBlocked",
      "tvRating": "allBlocked"
    },
    "networkUsageRules": [
      {
        "@odata.type": "microsoft.graph.iosNetworkUsageRule",
        "managedApps": [
          {
            "@odata.type": "microsoft.graph.appListItem",
            "name": "Name value",
            "publisher": "Publisher value",
            "appStoreUrl": "https://example.com/appStoreUrl/",
            "appId": "App Id value"
          }
        ],
        "cellularDataBlockWhenRoaming": true,
        "cellularDataBlocked": true
      }
    ],
    "mediaContentRatingApps": "allBlocked",
    "messagesBlocked": true,
    "notificationsBlockSettingsModification": true,
    "passcodeBlockFingerprintUnlock": true,
    "passcodeBlockFingerprintModification": true,
    "passcodeBlockModification": true,
    "passcodeBlockSimple": true,
    "passcodeExpirationDays": 6,
    "passcodeMinimumLength": 5,
    "passcodeMinutesOfInactivityBeforeLock": 5,
    "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
    "passcodeMinimumCharacterSetCount": 0,
    "passcodePreviousPasscodeBlockCount": 2,
    "passcodeSignInFailureCountBeforeWipe": 4,
    "passcodeRequiredType": "alphanumeric",
    "passcodeRequired": true,
    "podcastsBlocked": true,
    "safariBlockAutofill": true,
    "safariBlockJavaScript": true,
    "safariBlockPopups": true,
    "safariBlocked": true,
    "safariCookieSettings": "blockAlways",
    "safariManagedDomains": [
      "Safari Managed Domains value"
    ],
    "safariPasswordAutoFillDomains": [
      "Safari Password Auto Fill Domains value"
    ],
    "safariRequireFraudWarning": true,
    "screenCaptureBlocked": true,
    "siriBlocked": true,
    "siriBlockedWhenLocked": true,
    "siriBlockUserGeneratedContent": true,
    "siriRequireProfanityFilter": true,
    "spotlightBlockInternetResults": true,
    "voiceDialingBlocked": true,
    "wallpaperBlockModification": true,
    "wiFiConnectOnlyToConfiguredNetworks": true,
    "classroomForceRequestPermissionToLeaveClasses": true,
    "keychainBlockCloudSync": true,
    "pkiBlockOTAUpdates": true,
    "privacyForceLimitAdTracking": true,
    "enterpriseBookBlockBackup": true,
    "enterpriseBookBlockMetadataSync": true,
    "airPrintBlocked": true,
    "airPrintBlockCredentialsStorage": true,
    "airPrintForceTrustedTLS": true,
    "airPrintBlockiBeaconDiscovery": true,
    "blockSystemAppRemoval": true,
    "vpnBlockCreation": true
  }
}
```





