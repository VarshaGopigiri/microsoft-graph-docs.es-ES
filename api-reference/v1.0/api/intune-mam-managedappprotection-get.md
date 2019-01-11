---
title: Obtener managedAppProtection
description: Lea las propiedades y las relaciones del objeto managedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2c4c0c9e077965268aa700068bde8bdd53953eb4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830600"
---
# <a name="get-managedappprotection"></a><span data-ttu-id="35899-103">Obtener managedAppProtection</span><span class="sxs-lookup"><span data-stu-id="35899-103">Get managedAppProtection</span></span>

> <span data-ttu-id="35899-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35899-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35899-105">Lea las propiedades y las relaciones del objeto [managedAppProtection](../resources/intune-mam-managedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="35899-105">Read properties and relationships of the [managedAppProtection](../resources/intune-mam-managedappprotection.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="35899-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="35899-106">Prerequisites</span></span>
<span data-ttu-id="35899-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35899-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="35899-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35899-109">Permission type</span></span>|<span data-ttu-id="35899-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35899-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="35899-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35899-111">Delegated (work or school account)</span></span>|<span data-ttu-id="35899-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="35899-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="35899-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35899-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="35899-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35899-114">Not supported.</span></span>|
|<span data-ttu-id="35899-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35899-115">Application</span></span>|<span data-ttu-id="35899-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35899-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="35899-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35899-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="35899-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="35899-118">Optional query parameters</span></span>
<span data-ttu-id="35899-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35899-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="35899-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35899-120">Request headers</span></span>
|<span data-ttu-id="35899-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35899-121">Header</span></span>|<span data-ttu-id="35899-122">Valor</span><span class="sxs-lookup"><span data-stu-id="35899-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="35899-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="35899-123">Authorization</span></span>|<span data-ttu-id="35899-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="35899-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="35899-125">Accept</span><span class="sxs-lookup"><span data-stu-id="35899-125">Accept</span></span>|<span data-ttu-id="35899-126">application/json</span><span class="sxs-lookup"><span data-stu-id="35899-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="35899-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35899-127">Request body</span></span>
<span data-ttu-id="35899-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35899-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35899-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35899-129">Response</span></span>
<span data-ttu-id="35899-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppProtection](../resources/intune-mam-managedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35899-130">If successful, this method returns a `200 OK` response code and [managedAppProtection](../resources/intune-mam-managedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="35899-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35899-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="35899-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35899-132">Request</span></span>
<span data-ttu-id="35899-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35899-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies/{managedAppPolicyId}
```

### <a name="response"></a><span data-ttu-id="35899-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35899-134">Response</span></span>
<span data-ttu-id="35899-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35899-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1631

{
  "value": {
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
}
```



