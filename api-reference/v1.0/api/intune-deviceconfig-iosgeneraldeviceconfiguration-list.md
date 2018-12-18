---
title: Enumerar iosGeneralDeviceConfigurations
description: Enumere las propiedades y las relaciones de los objetos iosGeneralDeviceConfiguration.
author: tfitzmac
ms.openlocfilehash: 4adebc3e61727241dbc6ec112c33731510ca933d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332049"
---
# <a name="list-iosgeneraldeviceconfigurations"></a><span data-ttu-id="74374-103">Enumerar iosGeneralDeviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="74374-103">List iosGeneralDeviceConfigurations</span></span>

> <span data-ttu-id="74374-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74374-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74374-105">Enumere las propiedades y las relaciones de los objetos [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="74374-105">List properties and relationships of the [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74374-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74374-106">Prerequisites</span></span>
<span data-ttu-id="74374-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74374-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="74374-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74374-109">Permission type</span></span>|<span data-ttu-id="74374-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74374-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="74374-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74374-111">Delegated (work or school account)</span></span>|<span data-ttu-id="74374-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="74374-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="74374-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74374-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="74374-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74374-114">Not supported.</span></span>|
|<span data-ttu-id="74374-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74374-115">Application</span></span>|<span data-ttu-id="74374-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74374-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="74374-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74374-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="74374-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74374-118">Request headers</span></span>
|<span data-ttu-id="74374-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74374-119">Header</span></span>|<span data-ttu-id="74374-120">Valor</span><span class="sxs-lookup"><span data-stu-id="74374-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="74374-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="74374-121">Authorization</span></span>|<span data-ttu-id="74374-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="74374-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="74374-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="74374-123">Accept</span></span>|<span data-ttu-id="74374-124">application/json</span><span class="sxs-lookup"><span data-stu-id="74374-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="74374-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74374-125">Request body</span></span>
<span data-ttu-id="74374-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="74374-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="74374-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74374-127">Response</span></span>
<span data-ttu-id="74374-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74374-128">If successful, this method returns a `200 OK` response code and a collection of [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74374-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74374-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="74374-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74374-130">Request</span></span>
<span data-ttu-id="74374-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74374-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="74374-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74374-132">Response</span></span>
<span data-ttu-id="74374-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74374-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 8922

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
      "id": "ebba5202-5202-ebba-0252-baeb0252baeb",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
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
      "wiFiConnectOnlyToConfiguredNetworks": true
    }
  ]
}
```



