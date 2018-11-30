---
title: Obtener targetedManagedAppProtection
description: Lea las propiedades y las relaciones del objeto targetedManagedAppProtection.
ms.openlocfilehash: f86cf0efafc54d17c6f27443c1e89caccaf49787
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032147"
---
# <a name="get-targetedmanagedappprotection"></a><span data-ttu-id="b88df-103">Obtener targetedManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="b88df-103">Get targetedManagedAppProtection</span></span>

> <span data-ttu-id="b88df-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b88df-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b88df-105">Lea las propiedades y las relaciones del objeto [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="b88df-105">Read properties and relationships of the [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b88df-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b88df-106">Prerequisites</span></span>
<span data-ttu-id="b88df-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b88df-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b88df-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b88df-109">Permission type</span></span>|<span data-ttu-id="b88df-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b88df-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b88df-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b88df-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b88df-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b88df-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="b88df-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b88df-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b88df-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b88df-114">Not supported.</span></span>|
|<span data-ttu-id="b88df-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b88df-115">Application</span></span>|<span data-ttu-id="b88df-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b88df-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b88df-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b88df-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b88df-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b88df-118">Optional query parameters</span></span>
<span data-ttu-id="b88df-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b88df-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b88df-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b88df-120">Request headers</span></span>
|<span data-ttu-id="b88df-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b88df-121">Header</span></span>|<span data-ttu-id="b88df-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b88df-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b88df-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b88df-123">Authorization</span></span>|<span data-ttu-id="b88df-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b88df-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b88df-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b88df-125">Accept</span></span>|<span data-ttu-id="b88df-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b88df-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b88df-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b88df-127">Request body</span></span>
<span data-ttu-id="b88df-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b88df-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b88df-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b88df-129">Response</span></span>
<span data-ttu-id="b88df-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b88df-130">If successful, this method returns a `200 OK` response code and [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b88df-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b88df-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="b88df-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b88df-132">Request</span></span>
<span data-ttu-id="b88df-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b88df-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies/{managedAppPolicyId}
```

### <a name="response"></a><span data-ttu-id="b88df-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b88df-134">Response</span></span>
<span data-ttu-id="b88df-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b88df-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1664

{
  "value": {
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
}
```



