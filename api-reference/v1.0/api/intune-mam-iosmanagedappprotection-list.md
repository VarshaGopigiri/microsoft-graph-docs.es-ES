---
title: Enumerar iosManagedAppProtections
description: Enumere las propiedades y las relaciones de los objetos iosManagedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 78cff5489a4c7b9d652fda59e18b2c9b262bdc7a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978868"
---
# <a name="list-iosmanagedappprotections"></a><span data-ttu-id="c23a7-103">Enumerar iosManagedAppProtections</span><span class="sxs-lookup"><span data-stu-id="c23a7-103">List iosManagedAppProtections</span></span>

> <span data-ttu-id="c23a7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c23a7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c23a7-105">Enumere las propiedades y las relaciones de los objetos [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c23a7-105">List properties and relationships of the [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c23a7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c23a7-106">Prerequisites</span></span>
<span data-ttu-id="c23a7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c23a7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c23a7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c23a7-109">Permission type</span></span>|<span data-ttu-id="c23a7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c23a7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c23a7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c23a7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c23a7-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="c23a7-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="c23a7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c23a7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c23a7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c23a7-114">Not supported.</span></span>|
|<span data-ttu-id="c23a7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c23a7-115">Application</span></span>|<span data-ttu-id="c23a7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c23a7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c23a7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c23a7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosManagedAppProtections
```

## <a name="request-headers"></a><span data-ttu-id="c23a7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c23a7-118">Request headers</span></span>
|<span data-ttu-id="c23a7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c23a7-119">Header</span></span>|<span data-ttu-id="c23a7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c23a7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c23a7-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c23a7-121">Authorization</span></span>|<span data-ttu-id="c23a7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c23a7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c23a7-123">Accept</span><span class="sxs-lookup"><span data-stu-id="c23a7-123">Accept</span></span>|<span data-ttu-id="c23a7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c23a7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c23a7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c23a7-125">Request body</span></span>
<span data-ttu-id="c23a7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c23a7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c23a7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c23a7-127">Response</span></span>
<span data-ttu-id="c23a7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c23a7-128">If successful, this method returns a `200 OK` response code and a collection of [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c23a7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c23a7-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="c23a7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c23a7-130">Request</span></span>
<span data-ttu-id="c23a7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c23a7-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections
```

### <a name="response"></a><span data-ttu-id="c23a7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c23a7-132">Response</span></span>
<span data-ttu-id="c23a7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c23a7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1933

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosManagedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "5bc789cb-89cb-5bc7-cb89-c75bcb89c75b",
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
      "isAssigned": true,
      "appDataEncryptionType": "afterDeviceRestart",
      "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
      "deployedAppCount": 0,
      "faceIdBlocked": true
    }
  ]
}
```



