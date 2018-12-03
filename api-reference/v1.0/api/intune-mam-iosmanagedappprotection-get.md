---
title: Obtener iosManagedAppProtection
description: Lea las propiedades y las relaciones del objeto iosManagedAppProtection.
ms.openlocfilehash: 468467c14e74682d2acf400ad6dab18fef86f193
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028764"
---
# <a name="get-iosmanagedappprotection"></a><span data-ttu-id="439fb-103">Obtener iosManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="439fb-103">Get iosManagedAppProtection</span></span>

> <span data-ttu-id="439fb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="439fb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="439fb-105">Lea las propiedades y las relaciones del objeto [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="439fb-105">Read properties and relationships of the [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="439fb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="439fb-106">Prerequisites</span></span>
<span data-ttu-id="439fb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="439fb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="439fb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="439fb-109">Permission type</span></span>|<span data-ttu-id="439fb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="439fb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="439fb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="439fb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="439fb-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="439fb-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="439fb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="439fb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="439fb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="439fb-114">Not supported.</span></span>|
|<span data-ttu-id="439fb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="439fb-115">Application</span></span>|<span data-ttu-id="439fb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="439fb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="439fb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="439fb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="439fb-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="439fb-118">Optional query parameters</span></span>
<span data-ttu-id="439fb-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="439fb-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="439fb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="439fb-120">Request headers</span></span>
|<span data-ttu-id="439fb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="439fb-121">Header</span></span>|<span data-ttu-id="439fb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="439fb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="439fb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="439fb-123">Authorization</span></span>|<span data-ttu-id="439fb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="439fb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="439fb-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="439fb-125">Accept</span></span>|<span data-ttu-id="439fb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="439fb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="439fb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="439fb-127">Request body</span></span>
<span data-ttu-id="439fb-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="439fb-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="439fb-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="439fb-129">Response</span></span>
<span data-ttu-id="439fb-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="439fb-130">If successful, this method returns a `200 OK` response code and [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="439fb-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="439fb-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="439fb-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="439fb-132">Request</span></span>
<span data-ttu-id="439fb-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="439fb-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}
```

### <a name="response"></a><span data-ttu-id="439fb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="439fb-134">Response</span></span>
<span data-ttu-id="439fb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="439fb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1839

{
  "value": {
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
}
```


