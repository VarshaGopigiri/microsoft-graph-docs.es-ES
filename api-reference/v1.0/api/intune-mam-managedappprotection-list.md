---
title: Enumerar managedAppProtections
description: Enumere las propiedades y las relaciones de los objetos managedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a1c6d4462ae015af1e1c5b625feb7bbeec05aa5f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942874"
---
# <a name="list-managedappprotections"></a><span data-ttu-id="39c6c-103">Enumerar managedAppProtections</span><span class="sxs-lookup"><span data-stu-id="39c6c-103">List managedAppProtections</span></span>

> <span data-ttu-id="39c6c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39c6c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39c6c-105">Enumere las propiedades y las relaciones de los objetos [managedAppProtection](../resources/intune-mam-managedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39c6c-105">List properties and relationships of the [managedAppProtection](../resources/intune-mam-managedappprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39c6c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39c6c-106">Prerequisites</span></span>
<span data-ttu-id="39c6c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39c6c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39c6c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39c6c-109">Permission type</span></span>|<span data-ttu-id="39c6c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39c6c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39c6c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39c6c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="39c6c-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="39c6c-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="39c6c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39c6c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39c6c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39c6c-114">Not supported.</span></span>|
|<span data-ttu-id="39c6c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39c6c-115">Application</span></span>|<span data-ttu-id="39c6c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39c6c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="39c6c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39c6c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies
```

## <a name="request-headers"></a><span data-ttu-id="39c6c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39c6c-118">Request headers</span></span>
|<span data-ttu-id="39c6c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39c6c-119">Header</span></span>|<span data-ttu-id="39c6c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="39c6c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39c6c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="39c6c-121">Authorization</span></span>|<span data-ttu-id="39c6c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="39c6c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39c6c-123">Accept</span><span class="sxs-lookup"><span data-stu-id="39c6c-123">Accept</span></span>|<span data-ttu-id="39c6c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="39c6c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39c6c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39c6c-125">Request body</span></span>
<span data-ttu-id="39c6c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="39c6c-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="39c6c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39c6c-127">Response</span></span>
<span data-ttu-id="39c6c-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppProtection](../resources/intune-mam-managedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39c6c-128">If successful, this method returns a `200 OK` response code and a collection of [managedAppProtection](../resources/intune-mam-managedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39c6c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39c6c-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="39c6c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39c6c-130">Request</span></span>
<span data-ttu-id="39c6c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39c6c-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies
```

### <a name="response"></a><span data-ttu-id="39c6c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39c6c-132">Response</span></span>
<span data-ttu-id="39c6c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39c6c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1715

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "a6c064ce-64ce-a6c0-ce64-c0a6ce64c0a6",
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
      "minimumWarningAppVersion": "Minimum Warning App Version value"
    }
  ]
}
```



