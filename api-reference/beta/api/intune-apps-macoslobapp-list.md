---
title: Lista macOSLobApps
description: Propiedades de la lista y relaciones de los objetos macOSLobApp.
ms.openlocfilehash: 80c7baf887c18fe341f4f00780157034de03f868
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088037"
---
# <a name="list-macoslobapps"></a><span data-ttu-id="d86a7-103">Lista macOSLobApps</span><span class="sxs-lookup"><span data-stu-id="d86a7-103">List macOSLobApps</span></span>

> <span data-ttu-id="d86a7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d86a7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d86a7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d86a7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d86a7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d86a7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d86a7-107">Propiedades de la lista y relaciones de los objetos [macOSLobApp](../resources/intune-apps-macoslobapp.md) .</span><span class="sxs-lookup"><span data-stu-id="d86a7-107">List properties and relationships of the [macOSLobApp](../resources/intune-apps-macoslobapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d86a7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d86a7-108">Prerequisites</span></span>
<span data-ttu-id="d86a7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d86a7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d86a7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d86a7-111">Permission type</span></span>|<span data-ttu-id="d86a7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d86a7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d86a7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d86a7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d86a7-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="d86a7-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="d86a7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d86a7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d86a7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d86a7-116">Not supported.</span></span>|
|<span data-ttu-id="d86a7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d86a7-117">Application</span></span>|<span data-ttu-id="d86a7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d86a7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d86a7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d86a7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="d86a7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d86a7-120">Request headers</span></span>
|<span data-ttu-id="d86a7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d86a7-121">Header</span></span>|<span data-ttu-id="d86a7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d86a7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d86a7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d86a7-123">Authorization</span></span>|<span data-ttu-id="d86a7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d86a7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d86a7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d86a7-125">Accept</span></span>|<span data-ttu-id="d86a7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d86a7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d86a7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d86a7-127">Request body</span></span>
<span data-ttu-id="d86a7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d86a7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d86a7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d86a7-129">Response</span></span>
<span data-ttu-id="d86a7-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [macOSLobApp](../resources/intune-apps-macoslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d86a7-130">If successful, this method returns a `200 OK` response code and a collection of [macOSLobApp](../resources/intune-apps-macoslobapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d86a7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d86a7-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="d86a7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d86a7-132">Request</span></span>
<span data-ttu-id="d86a7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d86a7-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="d86a7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d86a7-134">Response</span></span>
<span data-ttu-id="d86a7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d86a7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1867

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.macOSLobApp",
      "id": "7be9250a-250a-7be9-0a25-e97b0a25e97b",
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
      "bundleId": "Bundle Id value",
      "minimumSupportedOperatingSystem": {
        "@odata.type": "microsoft.graph.macOSMinimumOperatingSystem",
        "v10_7": true,
        "v10_8": true,
        "v10_9": true,
        "v10_10": true,
        "v10_11": true,
        "v10_12": true,
        "v10_13": true
      },
      "buildNumber": "Build Number value",
      "versionNumber": "Version Number value",
      "childApps": [
        {
          "@odata.type": "microsoft.graph.macOSLobChildApp",
          "bundleId": "Bundle Id value",
          "buildNumber": "Build Number value",
          "versionNumber": "Version Number value"
        }
      ],
      "identityVersion": "Identity Version value",
      "md5HashChunkSize": 0,
      "md5Hash": [
        "Md5Hash value"
      ],
      "ignoreVersionDetection": true
    }
  ]
}
```




