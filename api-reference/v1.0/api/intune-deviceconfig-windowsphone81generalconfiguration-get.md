---
title: Obtener windowsPhone81GeneralConfiguration
description: Lea las propiedades y los relaciones del objeto windowsPhone81GeneralConfiguration.
author: tfitzmac
ms.openlocfilehash: aff275e4498910cecc6e14a4e7034df6edbab260
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337831"
---
# <a name="get-windowsphone81generalconfiguration"></a><span data-ttu-id="8ba7d-103">Obtener windowsPhone81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ba7d-103">Get windowsPhone81GeneralConfiguration</span></span>

> <span data-ttu-id="8ba7d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ba7d-105">Lea las propiedades y los relaciones del objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="8ba7d-105">Read properties and relationships of the [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8ba7d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8ba7d-106">Prerequisites</span></span>
<span data-ttu-id="8ba7d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8ba7d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8ba7d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ba7d-109">Permission type</span></span>|<span data-ttu-id="8ba7d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8ba7d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8ba7d-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="8ba7d-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="8ba7d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8ba7d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-114">Not supported.</span></span>|
|<span data-ttu-id="8ba7d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ba7d-115">Application</span></span>|<span data-ttu-id="8ba7d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8ba7d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ba7d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8ba7d-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8ba7d-118">Optional query parameters</span></span>
<span data-ttu-id="8ba7d-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="8ba7d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ba7d-120">Request headers</span></span>
|<span data-ttu-id="8ba7d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ba7d-121">Header</span></span>|<span data-ttu-id="8ba7d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8ba7d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8ba7d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8ba7d-123">Authorization</span></span>|<span data-ttu-id="8ba7d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8ba7d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8ba7d-125">Accept</span></span>|<span data-ttu-id="8ba7d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8ba7d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8ba7d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ba7d-127">Request body</span></span>
<span data-ttu-id="8ba7d-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8ba7d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ba7d-129">Response</span></span>
<span data-ttu-id="8ba7d-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-130">If successful, this method returns a `200 OK` response code and [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8ba7d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ba7d-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="8ba7d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ba7d-132">Request</span></span>
<span data-ttu-id="8ba7d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="8ba7d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ba7d-134">Response</span></span>
<span data-ttu-id="8ba7d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1740

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsPhone81GeneralConfiguration",
    "id": "f5e0e34d-e34d-f5e0-4de3-e0f54de3e0f5",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "applyOnlyToWindowsPhone81": true,
    "appsBlockCopyPaste": true,
    "bluetoothBlocked": true,
    "cameraBlocked": true,
    "cellularBlockWifiTethering": true,
    "compliantAppsList": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ],
    "compliantAppListType": "appsInListCompliant",
    "diagnosticDataBlockSubmission": true,
    "emailBlockAddingAccounts": true,
    "locationServicesBlocked": true,
    "microsoftAccountBlocked": true,
    "nfcBlocked": true,
    "passwordBlockSimple": true,
    "passwordExpirationDays": 6,
    "passwordMinimumLength": 5,
    "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
    "passwordMinimumCharacterSetCount": 0,
    "passwordPreviousPasswordBlockCount": 2,
    "passwordSignInFailureCountBeforeFactoryReset": 12,
    "passwordRequiredType": "alphanumeric",
    "passwordRequired": true,
    "screenCaptureBlocked": true,
    "storageBlockRemovableStorage": true,
    "storageRequireEncryption": true,
    "webBrowserBlocked": true,
    "wifiBlocked": true,
    "wifiBlockAutomaticConnectHotspots": true,
    "wifiBlockHotspotReporting": true,
    "windowsStoreBlocked": true
  }
}
```



