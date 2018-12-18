---
title: Obtener targetedManagedAppProtection
description: Lea las propiedades y las relaciones del objeto targetedManagedAppProtection.
author: tfitzmac
ms.openlocfilehash: 515525914e42c6d429c6addce74eec0f4e58b609
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330740"
---
# <a name="get-targetedmanagedappprotection"></a><span data-ttu-id="f981b-103">Obtener targetedManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="f981b-103">Get targetedManagedAppProtection</span></span>

> <span data-ttu-id="f981b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f981b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f981b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f981b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f981b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f981b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f981b-107">Lea las propiedades y las relaciones del objeto [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="f981b-107">Read properties and relationships of the [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f981b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f981b-108">Prerequisites</span></span>
<span data-ttu-id="f981b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f981b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f981b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f981b-111">Permission type</span></span>|<span data-ttu-id="f981b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f981b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f981b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f981b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f981b-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="f981b-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="f981b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f981b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f981b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f981b-116">Not supported.</span></span>|
|<span data-ttu-id="f981b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f981b-117">Application</span></span>|<span data-ttu-id="f981b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f981b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f981b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f981b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f981b-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f981b-120">Optional query parameters</span></span>
<span data-ttu-id="f981b-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f981b-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f981b-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f981b-122">Request headers</span></span>
|<span data-ttu-id="f981b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f981b-123">Header</span></span>|<span data-ttu-id="f981b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f981b-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f981b-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="f981b-125">Authorization</span></span>|<span data-ttu-id="f981b-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f981b-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f981b-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f981b-127">Accept</span></span>|<span data-ttu-id="f981b-128">application/json</span><span class="sxs-lookup"><span data-stu-id="f981b-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f981b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f981b-129">Request body</span></span>
<span data-ttu-id="f981b-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f981b-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f981b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f981b-131">Response</span></span>
<span data-ttu-id="f981b-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f981b-132">If successful, this method returns a `200 OK` response code and [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f981b-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f981b-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="f981b-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f981b-134">Request</span></span>
<span data-ttu-id="f981b-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f981b-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedAppPolicies/{managedAppPolicyId}
```

### <a name="response"></a><span data-ttu-id="f981b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f981b-136">Response</span></span>
<span data-ttu-id="f981b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f981b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2008

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
    "minimumWipeOsVersion": "Minimum Wipe Os Version value",
    "minimumWipeAppVersion": "Minimum Wipe App Version value",
    "appActionIfDeviceComplianceRequired": "wipe",
    "appActionIfMaximumPinRetriesExceeded": "wipe",
    "pinRequiredInsteadOfBiometricTimeout": "-PT3M9.8396734S",
    "isAssigned": true,
    "targetedAppManagementLevels": "unmanaged"
  }
}
```





