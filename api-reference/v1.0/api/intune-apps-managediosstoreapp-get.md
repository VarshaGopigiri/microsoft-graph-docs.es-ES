---
title: Obtener managedIOSStoreApp
description: Lea las propiedades y las relaciones del objeto managedIOSStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 714d095744132dfc11ee7e7b1d0a6a9150983e4e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967605"
---
# <a name="get-managediosstoreapp"></a><span data-ttu-id="79afa-103">Obtener managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="79afa-103">Get managedIOSStoreApp</span></span>

> <span data-ttu-id="79afa-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="79afa-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="79afa-105">Lea las propiedades y las relaciones del objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="79afa-105">Read properties and relationships of the [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="79afa-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="79afa-106">Prerequisites</span></span>
<span data-ttu-id="79afa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="79afa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="79afa-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79afa-109">Permission type</span></span>|<span data-ttu-id="79afa-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79afa-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="79afa-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79afa-111">Delegated (work or school account)</span></span>|<span data-ttu-id="79afa-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="79afa-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="79afa-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79afa-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="79afa-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79afa-114">Not supported.</span></span>|
|<span data-ttu-id="79afa-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79afa-115">Application</span></span>|<span data-ttu-id="79afa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79afa-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="79afa-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79afa-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="79afa-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="79afa-118">Optional query parameters</span></span>
<span data-ttu-id="79afa-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79afa-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="79afa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79afa-120">Request headers</span></span>
|<span data-ttu-id="79afa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79afa-121">Header</span></span>|<span data-ttu-id="79afa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="79afa-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="79afa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="79afa-123">Authorization</span></span>|<span data-ttu-id="79afa-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="79afa-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="79afa-125">Accept</span><span class="sxs-lookup"><span data-stu-id="79afa-125">Accept</span></span>|<span data-ttu-id="79afa-126">application/json</span><span class="sxs-lookup"><span data-stu-id="79afa-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="79afa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79afa-127">Request body</span></span>
<span data-ttu-id="79afa-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79afa-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="79afa-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79afa-129">Response</span></span>
<span data-ttu-id="79afa-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79afa-130">If successful, this method returns a `200 OK` response code and [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="79afa-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79afa-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="79afa-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79afa-132">Request</span></span>
<span data-ttu-id="79afa-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79afa-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="79afa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79afa-134">Response</span></span>
<span data-ttu-id="79afa-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="79afa-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1347

{
  "value": {
    "@odata.type": "#microsoft.graph.managedIOSStoreApp",
    "id": "51b9830f-830f-51b9-0f83-b9510f83b951",
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
    "appAvailability": "lineOfBusiness",
    "version": "Version value",
    "bundleId": "Bundle Id value",
    "appStoreUrl": "https://example.com/appStoreUrl/",
    "applicableDeviceType": {
      "@odata.type": "microsoft.graph.iosDeviceType",
      "iPad": true,
      "iPhoneAndIPod": true
    },
    "minimumSupportedOperatingSystem": {
      "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
      "v8_0": true,
      "v9_0": true,
      "v10_0": true,
      "v11_0": true,
      "v12_0": true
    }
  }
}
```



