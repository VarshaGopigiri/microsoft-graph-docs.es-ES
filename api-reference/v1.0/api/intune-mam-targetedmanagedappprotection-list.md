---
title: Enumerar targetedManagedAppProtections
description: Enumere las propiedades y los relaciones de los objetos targetedManagedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 097d15adff0a6de1bb56da7d9b169010594650dd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918416"
---
# <a name="list-targetedmanagedappprotections"></a><span data-ttu-id="415e8-103">Enumerar targetedManagedAppProtections</span><span class="sxs-lookup"><span data-stu-id="415e8-103">List targetedManagedAppProtections</span></span>

> <span data-ttu-id="415e8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="415e8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="415e8-105">Enumere las propiedades y los relaciones de los objetos [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="415e8-105">List properties and relationships of the [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="415e8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="415e8-106">Prerequisites</span></span>
<span data-ttu-id="415e8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="415e8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="415e8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="415e8-109">Permission type</span></span>|<span data-ttu-id="415e8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="415e8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="415e8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="415e8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="415e8-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="415e8-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="415e8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="415e8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="415e8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="415e8-114">Not supported.</span></span>|
|<span data-ttu-id="415e8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="415e8-115">Application</span></span>|<span data-ttu-id="415e8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="415e8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="415e8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="415e8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies
```

## <a name="request-headers"></a><span data-ttu-id="415e8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="415e8-118">Request headers</span></span>
|<span data-ttu-id="415e8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="415e8-119">Header</span></span>|<span data-ttu-id="415e8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="415e8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="415e8-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="415e8-121">Authorization</span></span>|<span data-ttu-id="415e8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="415e8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="415e8-123">Accept</span><span class="sxs-lookup"><span data-stu-id="415e8-123">Accept</span></span>|<span data-ttu-id="415e8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="415e8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="415e8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="415e8-125">Request body</span></span>
<span data-ttu-id="415e8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="415e8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="415e8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="415e8-127">Response</span></span>
<span data-ttu-id="415e8-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="415e8-128">If successful, this method returns a `200 OK` response code and a collection of [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="415e8-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="415e8-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="415e8-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="415e8-130">Request</span></span>
<span data-ttu-id="415e8-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="415e8-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies
```

### <a name="response"></a><span data-ttu-id="415e8-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="415e8-132">Response</span></span>
<span data-ttu-id="415e8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="415e8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1750

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
      "isAssigned": true
    }
  ]
}
```



