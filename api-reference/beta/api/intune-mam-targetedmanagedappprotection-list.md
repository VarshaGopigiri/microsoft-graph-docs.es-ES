---
title: Enumerar targetedManagedAppProtections
description: Enumere las propiedades y los relaciones de los objetos targetedManagedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 62dd9729bf7f0cd1bad48dd738a07b2c232ec4f7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939528"
---
# <a name="list-targetedmanagedappprotections"></a><span data-ttu-id="ad9d1-103">Enumerar targetedManagedAppProtections</span><span class="sxs-lookup"><span data-stu-id="ad9d1-103">List targetedManagedAppProtections</span></span>

> <span data-ttu-id="ad9d1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad9d1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ad9d1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ad9d1-107">Enumere las propiedades y los relaciones de los objetos [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ad9d1-107">List properties and relationships of the [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ad9d1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ad9d1-108">Prerequisites</span></span>
<span data-ttu-id="ad9d1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad9d1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad9d1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad9d1-111">Permission type</span></span>|<span data-ttu-id="ad9d1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad9d1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ad9d1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad9d1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ad9d1-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="ad9d1-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="ad9d1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad9d1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ad9d1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-116">Not supported.</span></span>|
|<span data-ttu-id="ad9d1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad9d1-117">Application</span></span>|<span data-ttu-id="ad9d1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ad9d1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad9d1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies
```

## <a name="request-headers"></a><span data-ttu-id="ad9d1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad9d1-120">Request headers</span></span>
|<span data-ttu-id="ad9d1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad9d1-121">Header</span></span>|<span data-ttu-id="ad9d1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ad9d1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ad9d1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ad9d1-123">Authorization</span></span>|<span data-ttu-id="ad9d1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ad9d1-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ad9d1-125">Accept</span></span>|<span data-ttu-id="ad9d1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ad9d1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ad9d1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad9d1-127">Request body</span></span>
<span data-ttu-id="ad9d1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ad9d1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad9d1-129">Response</span></span>
<span data-ttu-id="ad9d1-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-130">If successful, this method returns a `200 OK` response code and a collection of [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ad9d1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad9d1-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ad9d1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad9d1-132">Request</span></span>
<span data-ttu-id="ad9d1-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedAppPolicies
```

### <a name="response"></a><span data-ttu-id="ad9d1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad9d1-134">Response</span></span>
<span data-ttu-id="ad9d1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad9d1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2106

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.targetedManagedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "b6b92266-2266-b6b9-6622-b9b66622b9b6",
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
      "targetedAppManagementLevels": "unmanaged"
    }
  ]
}
```





