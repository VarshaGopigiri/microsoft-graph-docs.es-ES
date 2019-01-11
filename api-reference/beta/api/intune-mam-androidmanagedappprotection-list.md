---
title: Enumerar androidManagedAppProtections
description: Enumere las propiedades y las relaciones de los objetos androidManagedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4e1fc0e76f2693ddb638a5436d265452f8594258
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821975"
---
# <a name="list-androidmanagedappprotections"></a><span data-ttu-id="03a75-103">Enumerar androidManagedAppProtections</span><span class="sxs-lookup"><span data-stu-id="03a75-103">List androidManagedAppProtections</span></span>

> <span data-ttu-id="03a75-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="03a75-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="03a75-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="03a75-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="03a75-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03a75-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03a75-107">Enumere las propiedades y las relaciones de los objetos [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="03a75-107">List properties and relationships of the [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03a75-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03a75-108">Prerequisites</span></span>
<span data-ttu-id="03a75-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03a75-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="03a75-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03a75-111">Permission type</span></span>|<span data-ttu-id="03a75-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03a75-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="03a75-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03a75-113">Delegated (work or school account)</span></span>|<span data-ttu-id="03a75-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="03a75-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="03a75-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03a75-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="03a75-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03a75-116">Not supported.</span></span>|
|<span data-ttu-id="03a75-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03a75-117">Application</span></span>|<span data-ttu-id="03a75-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03a75-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="03a75-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03a75-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/androidManagedAppProtections
```

## <a name="request-headers"></a><span data-ttu-id="03a75-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03a75-120">Request headers</span></span>
|<span data-ttu-id="03a75-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03a75-121">Header</span></span>|<span data-ttu-id="03a75-122">Valor</span><span class="sxs-lookup"><span data-stu-id="03a75-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="03a75-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="03a75-123">Authorization</span></span>|<span data-ttu-id="03a75-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="03a75-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="03a75-125">Accept</span><span class="sxs-lookup"><span data-stu-id="03a75-125">Accept</span></span>|<span data-ttu-id="03a75-126">application/json</span><span class="sxs-lookup"><span data-stu-id="03a75-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="03a75-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03a75-127">Request body</span></span>
<span data-ttu-id="03a75-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03a75-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03a75-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03a75-129">Response</span></span>
<span data-ttu-id="03a75-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03a75-130">If successful, this method returns a `200 OK` response code and a collection of [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03a75-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03a75-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="03a75-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03a75-132">Request</span></span>
<span data-ttu-id="03a75-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03a75-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/androidManagedAppProtections
```

### <a name="response"></a><span data-ttu-id="03a75-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03a75-134">Response</span></span>
<span data-ttu-id="03a75-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03a75-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2835

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidManagedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "cf517ced-7ced-cf51-ed7c-51cfed7c51cf",
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
      "isAssigned": true,
      "targetedAppManagementLevels": "unmanaged",
      "screenCaptureBlocked": true,
      "disableAppEncryptionIfDeviceEncryptionIsEnabled": true,
      "encryptAppData": true,
      "deployedAppCount": 0,
      "minimumRequiredPatchVersion": "Minimum Required Patch Version value",
      "minimumWarningPatchVersion": "Minimum Warning Patch Version value",
      "exemptedAppPackages": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ],
      "minimumWipePatchVersion": "Minimum Wipe Patch Version value",
      "allowedAndroidDeviceManufacturers": "Allowed Android Device Manufacturers value",
      "appActionIfAndroidDeviceManufacturerNotAllowed": "wipe"
    }
  ]
}
```





