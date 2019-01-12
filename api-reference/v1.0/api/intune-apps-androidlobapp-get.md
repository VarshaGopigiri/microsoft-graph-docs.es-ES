---
title: Obtener androidLobApp
description: Lea las propiedades y las relaciones del objeto androidLobApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b412e7675ad4a5af77207af6514364419de1ab18
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983852"
---
# <a name="get-androidlobapp"></a><span data-ttu-id="74323-103">Obtener androidLobApp</span><span class="sxs-lookup"><span data-stu-id="74323-103">Get androidLobApp</span></span>

> <span data-ttu-id="74323-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74323-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74323-105">Lea las propiedades y las relaciones del objeto [androidLobApp](../resources/intune-apps-androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="74323-105">Read properties and relationships of the [androidLobApp](../resources/intune-apps-androidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74323-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74323-106">Prerequisites</span></span>
<span data-ttu-id="74323-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74323-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="74323-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74323-109">Permission type</span></span>|<span data-ttu-id="74323-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74323-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="74323-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74323-111">Delegated (work or school account)</span></span>|<span data-ttu-id="74323-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="74323-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="74323-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74323-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="74323-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74323-114">Not supported.</span></span>|
|<span data-ttu-id="74323-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74323-115">Application</span></span>|<span data-ttu-id="74323-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74323-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="74323-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74323-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="74323-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="74323-118">Optional query parameters</span></span>
<span data-ttu-id="74323-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74323-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="74323-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74323-120">Request headers</span></span>
|<span data-ttu-id="74323-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74323-121">Header</span></span>|<span data-ttu-id="74323-122">Valor</span><span class="sxs-lookup"><span data-stu-id="74323-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="74323-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="74323-123">Authorization</span></span>|<span data-ttu-id="74323-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="74323-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="74323-125">Accept</span><span class="sxs-lookup"><span data-stu-id="74323-125">Accept</span></span>|<span data-ttu-id="74323-126">application/json</span><span class="sxs-lookup"><span data-stu-id="74323-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="74323-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74323-127">Request body</span></span>
<span data-ttu-id="74323-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="74323-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="74323-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74323-129">Response</span></span>
<span data-ttu-id="74323-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidLobApp](../resources/intune-apps-androidlobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74323-130">If successful, this method returns a `200 OK` response code and [androidLobApp](../resources/intune-apps-androidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74323-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74323-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="74323-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74323-132">Request</span></span>
<span data-ttu-id="74323-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74323-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="74323-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74323-134">Response</span></span>
<span data-ttu-id="74323-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74323-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1338

{
  "value": {
    "@odata.type": "#microsoft.graph.androidLobApp",
    "id": "4b9a27d0-27d0-4b9a-d027-9a4bd0279a4b",
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
    "publishingState": "processing",
    "committedContentVersion": "Committed Content Version value",
    "fileName": "File Name value",
    "size": 4,
    "packageId": "Package Id value",
    "minimumSupportedOperatingSystem": {
      "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
      "v4_0": true,
      "v4_0_3": true,
      "v4_1": true,
      "v4_2": true,
      "v4_3": true,
      "v4_4": true,
      "v5_0": true,
      "v5_1": true
    },
    "versionName": "Version Name value",
    "versionCode": "Version Code value"
  }
}
```



