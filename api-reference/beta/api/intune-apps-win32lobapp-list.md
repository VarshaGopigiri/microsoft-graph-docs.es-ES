---
title: Lista win32LobApps
description: Propiedades de la lista y relaciones de los objetos win32LobApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 809bdf388d33641e6b797c7dd934d856dcdd227b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864613"
---
# <a name="list-win32lobapps"></a><span data-ttu-id="44f8a-103">Lista win32LobApps</span><span class="sxs-lookup"><span data-stu-id="44f8a-103">List win32LobApps</span></span>

> <span data-ttu-id="44f8a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="44f8a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="44f8a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="44f8a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="44f8a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="44f8a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="44f8a-107">Propiedades de la lista y relaciones de los objetos [win32LobApp](../resources/intune-apps-win32lobapp.md) .</span><span class="sxs-lookup"><span data-stu-id="44f8a-107">List properties and relationships of the [win32LobApp](../resources/intune-apps-win32lobapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="44f8a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="44f8a-108">Prerequisites</span></span>
<span data-ttu-id="44f8a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="44f8a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="44f8a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="44f8a-111">Permission type</span></span>|<span data-ttu-id="44f8a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="44f8a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="44f8a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="44f8a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="44f8a-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="44f8a-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="44f8a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="44f8a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="44f8a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="44f8a-116">Not supported.</span></span>|
|<span data-ttu-id="44f8a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="44f8a-117">Application</span></span>|<span data-ttu-id="44f8a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="44f8a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="44f8a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="44f8a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="44f8a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="44f8a-120">Request headers</span></span>
|<span data-ttu-id="44f8a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44f8a-121">Header</span></span>|<span data-ttu-id="44f8a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="44f8a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="44f8a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="44f8a-123">Authorization</span></span>|<span data-ttu-id="44f8a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="44f8a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="44f8a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="44f8a-125">Accept</span></span>|<span data-ttu-id="44f8a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="44f8a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="44f8a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="44f8a-127">Request body</span></span>
<span data-ttu-id="44f8a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="44f8a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="44f8a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44f8a-129">Response</span></span>
<span data-ttu-id="44f8a-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [win32LobApp](../resources/intune-apps-win32lobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44f8a-130">If successful, this method returns a `200 OK` response code and a collection of [win32LobApp](../resources/intune-apps-win32lobapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="44f8a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44f8a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="44f8a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="44f8a-132">Request</span></span>
<span data-ttu-id="44f8a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44f8a-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="44f8a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44f8a-134">Response</span></span>
<span data-ttu-id="44f8a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="44f8a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2689

{
  "value": [
    {
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
  ]
}
```





