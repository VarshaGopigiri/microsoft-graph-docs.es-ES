---
title: Obtener iosManagedAppProtection
description: Lea las propiedades y las relaciones del objeto iosManagedAppProtection.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 547f3313f77b0700b46505afd44a3ef5ba8fc4e4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928839"
---
# <a name="get-iosmanagedappprotection"></a><span data-ttu-id="baf40-103">Obtener iosManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="baf40-103">Get iosManagedAppProtection</span></span>

> <span data-ttu-id="baf40-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="baf40-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="baf40-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="baf40-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="baf40-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="baf40-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="baf40-107">Lea las propiedades y las relaciones del objeto [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="baf40-107">Read properties and relationships of the [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="baf40-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="baf40-108">Prerequisites</span></span>
<span data-ttu-id="baf40-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="baf40-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="baf40-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="baf40-111">Permission type</span></span>|<span data-ttu-id="baf40-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="baf40-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="baf40-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="baf40-113">Delegated (work or school account)</span></span>|<span data-ttu-id="baf40-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="baf40-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="baf40-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="baf40-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="baf40-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="baf40-116">Not supported.</span></span>|
|<span data-ttu-id="baf40-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="baf40-117">Application</span></span>|<span data-ttu-id="baf40-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="baf40-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="baf40-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="baf40-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="baf40-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="baf40-120">Optional query parameters</span></span>
<span data-ttu-id="baf40-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="baf40-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="baf40-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="baf40-122">Request headers</span></span>
|<span data-ttu-id="baf40-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="baf40-123">Header</span></span>|<span data-ttu-id="baf40-124">Valor</span><span class="sxs-lookup"><span data-stu-id="baf40-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="baf40-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="baf40-125">Authorization</span></span>|<span data-ttu-id="baf40-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="baf40-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="baf40-127">Accept</span><span class="sxs-lookup"><span data-stu-id="baf40-127">Accept</span></span>|<span data-ttu-id="baf40-128">application/json</span><span class="sxs-lookup"><span data-stu-id="baf40-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="baf40-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="baf40-129">Request body</span></span>
<span data-ttu-id="baf40-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="baf40-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="baf40-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="baf40-131">Response</span></span>
<span data-ttu-id="baf40-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="baf40-132">If successful, this method returns a `200 OK` response code and [iosManagedAppProtection](../resources/intune-mam-iosmanagedappprotection.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="baf40-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="baf40-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="baf40-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="baf40-134">Request</span></span>
<span data-ttu-id="baf40-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="baf40-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}
```

### <a name="response"></a><span data-ttu-id="baf40-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="baf40-136">Response</span></span>
<span data-ttu-id="baf40-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="baf40-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2736

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
    "minimumWipeOsVersion": "Minimum Wipe Os Version value",
    "minimumWipeAppVersion": "Minimum Wipe App Version value",
    "appActionIfDeviceComplianceRequired": "wipe",
    "appActionIfMaximumPinRetriesExceeded": "wipe",
    "pinRequiredInsteadOfBiometricTimeout": "-PT3M9.8396734S",
    "isAssigned": true,
    "targetedAppManagementLevels": "unmanaged",
    "appDataEncryptionType": "afterDeviceRestart",
    "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
    "deployedAppCount": 0,
    "faceIdBlocked": true,
    "exemptedAppProtocols": [
      {
        "@odata.type": "microsoft.graph.keyValuePair",
        "name": "Name value",
        "value": "Value value"
      }
    ],
    "minimumWipeSdkVersion": "Minimum Wipe Sdk Version value",
    "allowedIosDeviceModels": "Allowed Ios Device Models value",
    "appActionIfIosDeviceModelNotAllowed": "wipe",
    "thirdPartyKeyboardsBlocked": true,
    "filterOpenInToOnlyManagedApps": true,
    "disableProtectionOfManagedOutboundOpenInData": true,
    "protectInboundDataFromUnknownSources": true
  }
}
```





