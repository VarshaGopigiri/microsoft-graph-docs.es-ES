---
title: Enumerar defaultManagedAppProtections
description: Enumere las propiedades y las relaciones de los objetos defaultManagedAppProtection.
ms.openlocfilehash: 344a3241639be941d8473c21d5aa55bbbddcd552
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090297"
---
# <a name="list-defaultmanagedappprotections"></a><span data-ttu-id="9370a-103">Enumerar defaultManagedAppProtections</span><span class="sxs-lookup"><span data-stu-id="9370a-103">List defaultManagedAppProtections</span></span>

> <span data-ttu-id="9370a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9370a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9370a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9370a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9370a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9370a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9370a-107">Enumere las propiedades y las relaciones de los objetos [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="9370a-107">List properties and relationships of the [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9370a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9370a-108">Prerequisites</span></span>
<span data-ttu-id="9370a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9370a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9370a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9370a-111">Permission type</span></span>|<span data-ttu-id="9370a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9370a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9370a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9370a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9370a-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="9370a-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="9370a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9370a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9370a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9370a-116">Not supported.</span></span>|
|<span data-ttu-id="9370a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9370a-117">Application</span></span>|<span data-ttu-id="9370a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9370a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9370a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9370a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/defaultManagedAppProtections
```

## <a name="request-headers"></a><span data-ttu-id="9370a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9370a-120">Request headers</span></span>
|<span data-ttu-id="9370a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9370a-121">Header</span></span>|<span data-ttu-id="9370a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9370a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9370a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9370a-123">Authorization</span></span>|<span data-ttu-id="9370a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9370a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9370a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9370a-125">Accept</span></span>|<span data-ttu-id="9370a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9370a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9370a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9370a-127">Request body</span></span>
<span data-ttu-id="9370a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9370a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9370a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9370a-129">Response</span></span>
<span data-ttu-id="9370a-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9370a-130">If successful, this method returns a `200 OK` response code and a collection of [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9370a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9370a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="9370a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9370a-132">Request</span></span>
<span data-ttu-id="9370a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9370a-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/defaultManagedAppProtections
```

### <a name="response"></a><span data-ttu-id="9370a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9370a-134">Response</span></span>
<span data-ttu-id="9370a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9370a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 3680

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.defaultManagedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "77064c51-4c51-7706-514c-0677514c0677",
      "version": "Version value",
      "periodOfflineBeforeAccessCheck": "-PT17.1357909S",
      "periodOnlineBeforeAccessCheck": "PT35.0018757S",
      "allowedInboundDataTransferSources": "managedApps",
      "allowedOutboundDataTransferDestinations": "managedApps",
      "organizationalCredentialsRequired": true,
      "allowedOutboundClipboardSharingLevel": "managedAppsWithPasteIn",
      "dataBackupBlocked": true,
      "deviceComplianceRequired": true,
      "managedBrowserToOpenLinksRequired": true,
      "saveAsBlocked": true,
      "periodOfflineBeforeWipeIsEnforced": "-PT3M22.1587532S",
      "pinRequired": true,
      "maximumPinRetries": 1,
      "simplePinBlocked": true,
      "minimumPinLength": 0,
      "pinCharacterSet": "alphanumericAndSymbol",
      "periodBeforePinReset": "PT3M29.6631862S",
      "allowedDataStorageLocations": [
        "sharePoint"
      ],
      "contactSyncBlocked": true,
      "printBlocked": true,
      "fingerprintBlocked": true,
      "disableAppPinIfDevicePinIsSet": true,
      "minimumRequiredOsVersion": "Minimum Required Os Version value",
      "minimumWarningOsVersion": "Minimum Warning Os Version value",
      "minimumRequiredAppVersion": "Minimum Required App Version value",
      "minimumWarningAppVersion": "Minimum Warning App Version value",
      "minimumWipeOsVersion": "Minimum Wipe Os Version value",
      "minimumWipeAppVersion": "Minimum Wipe App Version value",
      "appActionIfDeviceComplianceRequired": "wipe",
      "appActionIfMaximumPinRetriesExceeded": "wipe",
      "pinRequiredInsteadOfBiometricTimeout": "-PT3M9.8396734S",
      "appDataEncryptionType": "afterDeviceRestart",
      "screenCaptureBlocked": true,
      "encryptAppData": true,
      "disableAppEncryptionIfDeviceEncryptionIsEnabled": true,
      "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
      "customSettings": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ],
      "deployedAppCount": 0,
      "minimumRequiredPatchVersion": "Minimum Required Patch Version value",
      "minimumWarningPatchVersion": "Minimum Warning Patch Version value",
      "exemptedAppProtocols": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ],
      "exemptedAppPackages": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ],
      "faceIdBlocked": true,
      "minimumWipeSdkVersion": "Minimum Wipe Sdk Version value",
      "minimumWipePatchVersion": "Minimum Wipe Patch Version value",
      "allowedIosDeviceModels": "Allowed Ios Device Models value",
      "appActionIfIosDeviceModelNotAllowed": "wipe",
      "allowedAndroidDeviceManufacturers": "Allowed Android Device Manufacturers value",
      "appActionIfAndroidDeviceManufacturerNotAllowed": "wipe",
      "thirdPartyKeyboardsBlocked": true,
      "filterOpenInToOnlyManagedApps": true,
      "disableProtectionOfManagedOutboundOpenInData": true,
      "protectInboundDataFromUnknownSources": true
    }
  ]
}
```





