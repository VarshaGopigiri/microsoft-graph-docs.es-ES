---
title: Obtener androidLobApp
description: Lea las propiedades y las relaciones del objeto androidLobApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4ae34e9d632b7112e9709136a3eff6cacc11e19d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956510"
---
# <a name="get-androidlobapp"></a><span data-ttu-id="abf01-103">Obtener androidLobApp</span><span class="sxs-lookup"><span data-stu-id="abf01-103">Get androidLobApp</span></span>

> <span data-ttu-id="abf01-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="abf01-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="abf01-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="abf01-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="abf01-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abf01-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abf01-107">Lea las propiedades y las relaciones del objeto [androidLobApp](../resources/intune-apps-androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="abf01-107">Read properties and relationships of the [androidLobApp](../resources/intune-apps-androidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="abf01-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="abf01-108">Prerequisites</span></span>
<span data-ttu-id="abf01-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="abf01-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="abf01-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="abf01-111">Permission type</span></span>|<span data-ttu-id="abf01-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="abf01-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="abf01-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="abf01-113">Delegated (work or school account)</span></span>|<span data-ttu-id="abf01-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="abf01-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="abf01-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="abf01-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="abf01-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abf01-116">Not supported.</span></span>|
|<span data-ttu-id="abf01-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="abf01-117">Application</span></span>|<span data-ttu-id="abf01-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abf01-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="abf01-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="abf01-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
GET /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="optional-query-parameters"></a><span data-ttu-id="abf01-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="abf01-120">Optional query parameters</span></span>
<span data-ttu-id="abf01-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abf01-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="abf01-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="abf01-122">Request headers</span></span>
|<span data-ttu-id="abf01-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abf01-123">Header</span></span>|<span data-ttu-id="abf01-124">Valor</span><span class="sxs-lookup"><span data-stu-id="abf01-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="abf01-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="abf01-125">Authorization</span></span>|<span data-ttu-id="abf01-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="abf01-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="abf01-127">Accept</span><span class="sxs-lookup"><span data-stu-id="abf01-127">Accept</span></span>|<span data-ttu-id="abf01-128">application/json</span><span class="sxs-lookup"><span data-stu-id="abf01-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="abf01-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="abf01-129">Request body</span></span>
<span data-ttu-id="abf01-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="abf01-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="abf01-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abf01-131">Response</span></span>
<span data-ttu-id="abf01-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidLobApp](../resources/intune-apps-androidlobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abf01-132">If successful, this method returns a `200 OK` response code and [androidLobApp](../resources/intune-apps-androidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="abf01-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="abf01-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="abf01-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="abf01-134">Request</span></span>
<span data-ttu-id="abf01-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="abf01-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="abf01-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abf01-136">Response</span></span>
<span data-ttu-id="abf01-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="abf01-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1582

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
    "uploadState": 11,
    "publishingState": "processing",
    "committedContentVersion": "Committed Content Version value",
    "fileName": "File Name value",
    "size": 4,
    "packageId": "Package Id value",
    "identityName": "Identity Name value",
    "minimumSupportedOperatingSystem": {
      "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
      "v4_0": true,
      "v4_0_3": true,
      "v4_1": true,
      "v4_2": true,
      "v4_3": true,
      "v4_4": true,
      "v5_0": true,
      "v5_1": true,
      "v6_0": true,
      "v7_0": true,
      "v7_1": true,
      "v8_0": true,
      "v8_1": true,
      "v9_0": true
    },
    "versionName": "Version Name value",
    "versionCode": "Version Code value",
    "identityVersion": "Identity Version value"
  }
}
```





