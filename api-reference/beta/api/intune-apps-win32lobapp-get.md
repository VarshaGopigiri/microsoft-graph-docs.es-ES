---
title: Obtener win32LobApp
description: Leer las propiedades y las relaciones del objeto win32LobApp.
author: tfitzmac
ms.openlocfilehash: f4ca14ac3205cd4ede825e8817260b815606cf59
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310727"
---
# <a name="get-win32lobapp"></a><span data-ttu-id="3a46e-103">Obtener win32LobApp</span><span class="sxs-lookup"><span data-stu-id="3a46e-103">Get win32LobApp</span></span>

> <span data-ttu-id="3a46e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3a46e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3a46e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3a46e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3a46e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a46e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a46e-107">Leer las propiedades y las relaciones del objeto [win32LobApp](../resources/intune-apps-win32lobapp.md) .</span><span class="sxs-lookup"><span data-stu-id="3a46e-107">Read properties and relationships of the [win32LobApp](../resources/intune-apps-win32lobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3a46e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a46e-108">Prerequisites</span></span>
<span data-ttu-id="3a46e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3a46e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3a46e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a46e-111">Permission type</span></span>|<span data-ttu-id="3a46e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a46e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3a46e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a46e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3a46e-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="3a46e-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="3a46e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a46e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3a46e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a46e-116">Not supported.</span></span>|
|<span data-ttu-id="3a46e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a46e-117">Application</span></span>|<span data-ttu-id="3a46e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a46e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3a46e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a46e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
GET /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3a46e-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3a46e-120">Optional query parameters</span></span>
<span data-ttu-id="3a46e-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a46e-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3a46e-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a46e-122">Request headers</span></span>
|<span data-ttu-id="3a46e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a46e-123">Header</span></span>|<span data-ttu-id="3a46e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3a46e-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3a46e-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="3a46e-125">Authorization</span></span>|<span data-ttu-id="3a46e-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3a46e-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3a46e-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3a46e-127">Accept</span></span>|<span data-ttu-id="3a46e-128">application/json</span><span class="sxs-lookup"><span data-stu-id="3a46e-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3a46e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a46e-129">Request body</span></span>
<span data-ttu-id="3a46e-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3a46e-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3a46e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a46e-131">Response</span></span>
<span data-ttu-id="3a46e-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [win32LobApp](../resources/intune-apps-win32lobapp.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a46e-132">If successful, this method returns a `200 OK` response code and [win32LobApp](../resources/intune-apps-win32lobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3a46e-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a46e-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="3a46e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a46e-134">Request</span></span>
<span data-ttu-id="3a46e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a46e-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="3a46e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a46e-136">Response</span></span>
<span data-ttu-id="3a46e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a46e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2533

{
  "value": {
    "@odata.type": "#microsoft.graph.win32LobApp",
    "id": "9607b530-b530-9607-30b5-079630b50796",
    "displayName": "Display Name value",
    "description": "Description value",
    "publisher": "Publisher value",
    "largeIcon": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "isFeatured": true,
    "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
    "informationUrl": "https://example.com/informationUrl/",
    "owner": "Owner value",
    "developer": "Developer value",
    "notes": "Notes value",
    "uploadState": 11,
    "publishingState": "processing",
    "committedContentVersion": "Committed Content Version value",
    "fileName": "File Name value",
    "size": 4,
    "installCommandLine": "Install Command Line value",
    "uninstallCommandLine": "Uninstall Command Line value",
    "applicableArchitectures": "x86",
    "minimumSupportedOperatingSystem": {
      "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
      "v8_0": true,
      "v8_1": true,
      "v10_0": true,
      "v10_1607": true,
      "v10_1703": true,
      "v10_1709": true,
      "v10_1803": true
    },
    "minimumFreeDiskSpaceInMB": 8,
    "minimumMemoryInMB": 1,
    "minimumNumberOfProcessors": 9,
    "minimumCpuSpeedInMHz": 4,
    "detectionRules": [
      {
        "@odata.type": "microsoft.graph.win32LobAppRegistryDetection",
        "check32BitOn64System": true,
        "keyPath": "Key Path value",
        "valueName": "Value Name value",
        "detectionType": "exists",
        "operator": "equal",
        "detectionValue": "Detection Value value"
      }
    ],
    "installExperience": {
      "@odata.type": "microsoft.graph.win32LobAppInstallExperience",
      "runAsAccount": "user"
    },
    "returnCodes": [
      {
        "@odata.type": "microsoft.graph.win32LobAppReturnCode",
        "returnCode": 10,
        "type": "success"
      }
    ],
    "msiInformation": {
      "@odata.type": "microsoft.graph.win32LobAppMsiInformation",
      "productCode": "Product Code value",
      "productVersion": "Product Version value",
      "upgradeCode": "Upgrade Code value",
      "requiresReboot": true,
      "packageType": "perUser"
    },
    "setupFilePath": "Setup File Path value"
  }
}
```





