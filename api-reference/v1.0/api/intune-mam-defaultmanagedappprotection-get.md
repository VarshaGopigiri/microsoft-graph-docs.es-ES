---
title: Obtener defaultManagedAppProtection
description: Lea las propiedades y las relaciones del objeto defaultManagedAppProtection.
author: tfitzmac
ms.openlocfilehash: 9d2b7a72f4adec0616533092ec8001d89a55dd13
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309467"
---
# <a name="get-defaultmanagedappprotection"></a><span data-ttu-id="abefd-103">Obtener defaultManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="abefd-103">Get defaultManagedAppProtection</span></span>

> <span data-ttu-id="abefd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abefd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abefd-105">Lea las propiedades y las relaciones del objeto [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="abefd-105">Read properties and relationships of the [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="abefd-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="abefd-106">Prerequisites</span></span>
<span data-ttu-id="abefd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="abefd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="abefd-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="abefd-109">Permission type</span></span>|<span data-ttu-id="abefd-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="abefd-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="abefd-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="abefd-111">Delegated (work or school account)</span></span>|<span data-ttu-id="abefd-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="abefd-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="abefd-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="abefd-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="abefd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abefd-114">Not supported.</span></span>|
|<span data-ttu-id="abefd-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="abefd-115">Application</span></span>|<span data-ttu-id="abefd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abefd-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="abefd-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="abefd-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="abefd-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="abefd-118">Optional query parameters</span></span>
<span data-ttu-id="abefd-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abefd-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="abefd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="abefd-120">Request headers</span></span>
|<span data-ttu-id="abefd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abefd-121">Header</span></span>|<span data-ttu-id="abefd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="abefd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="abefd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="abefd-123">Authorization</span></span>|<span data-ttu-id="abefd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="abefd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="abefd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="abefd-125">Accept</span></span>|<span data-ttu-id="abefd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="abefd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="abefd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="abefd-127">Request body</span></span>
<span data-ttu-id="abefd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="abefd-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="abefd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abefd-129">Response</span></span>
<span data-ttu-id="abefd-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abefd-130">If successful, this method returns a `200 OK` response code and [defaultManagedAppProtection](../resources/intune-mam-defaultmanagedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="abefd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="abefd-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="abefd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="abefd-132">Request</span></span>
<span data-ttu-id="abefd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="abefd-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}
```

### <a name="response"></a><span data-ttu-id="abefd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abefd-134">Response</span></span>
<span data-ttu-id="abefd-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="abefd-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2264

{
  "value": {
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
    "faceIdBlocked": true
  }
}
```



