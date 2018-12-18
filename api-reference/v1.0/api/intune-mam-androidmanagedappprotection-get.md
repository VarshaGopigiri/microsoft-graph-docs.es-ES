---
title: Obtener androidManagedAppProtection
description: Lea las propiedades y las relaciones del objeto androidManagedAppProtection.
author: tfitzmac
ms.openlocfilehash: 1342ae17333f86b7512ffbc4af1f8d97cce6cbfa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330138"
---
# <a name="get-androidmanagedappprotection"></a><span data-ttu-id="6734f-103">Obtener androidManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="6734f-103">Get androidManagedAppProtection</span></span>

> <span data-ttu-id="6734f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6734f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6734f-105">Lea las propiedades y las relaciones del objeto [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="6734f-105">Read properties and relationships of the [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6734f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6734f-106">Prerequisites</span></span>
<span data-ttu-id="6734f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6734f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6734f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6734f-109">Permission type</span></span>|<span data-ttu-id="6734f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6734f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6734f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6734f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6734f-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="6734f-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="6734f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6734f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6734f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6734f-114">Not supported.</span></span>|
|<span data-ttu-id="6734f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6734f-115">Application</span></span>|<span data-ttu-id="6734f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6734f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6734f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6734f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6734f-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6734f-118">Optional query parameters</span></span>
<span data-ttu-id="6734f-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6734f-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6734f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6734f-120">Request headers</span></span>
|<span data-ttu-id="6734f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6734f-121">Header</span></span>|<span data-ttu-id="6734f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6734f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6734f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6734f-123">Authorization</span></span>|<span data-ttu-id="6734f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6734f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6734f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6734f-125">Accept</span></span>|<span data-ttu-id="6734f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6734f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6734f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6734f-127">Request body</span></span>
<span data-ttu-id="6734f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6734f-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6734f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6734f-129">Response</span></span>
<span data-ttu-id="6734f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6734f-130">If successful, this method returns a `200 OK` response code and [androidManagedAppProtection](../resources/intune-mam-androidmanagedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6734f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6734f-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="6734f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6734f-132">Request</span></span>
<span data-ttu-id="6734f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6734f-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}
```

### <a name="response"></a><span data-ttu-id="6734f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6734f-134">Response</span></span>
<span data-ttu-id="6734f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6734f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1967

{
  "value": {
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
    "isAssigned": true,
    "screenCaptureBlocked": true,
    "disableAppEncryptionIfDeviceEncryptionIsEnabled": true,
    "encryptAppData": true,
    "deployedAppCount": 0,
    "minimumRequiredPatchVersion": "Minimum Required Patch Version value",
    "minimumWarningPatchVersion": "Minimum Warning Patch Version value"
  }
}
```



