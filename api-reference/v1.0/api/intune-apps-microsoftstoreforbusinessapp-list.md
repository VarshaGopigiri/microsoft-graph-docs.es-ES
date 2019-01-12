---
title: Enumerar microsoftStoreForBusinessApps
description: Enumere las propiedades y las relaciones de los objetos microsoftStoreForBusinessApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e03085b793ebdda1ab3b52300d38307c551d908b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956356"
---
# <a name="list-microsoftstoreforbusinessapps"></a><span data-ttu-id="997fb-103">Enumerar microsoftStoreForBusinessApps</span><span class="sxs-lookup"><span data-stu-id="997fb-103">List microsoftStoreForBusinessApps</span></span>

> <span data-ttu-id="997fb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="997fb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="997fb-105">Enumere las propiedades y las relaciones de los objetos [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="997fb-105">List properties and relationships of the [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="997fb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="997fb-106">Prerequisites</span></span>
<span data-ttu-id="997fb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="997fb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="997fb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="997fb-109">Permission type</span></span>|<span data-ttu-id="997fb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="997fb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="997fb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="997fb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="997fb-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="997fb-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="997fb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="997fb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="997fb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="997fb-114">Not supported.</span></span>|
|<span data-ttu-id="997fb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="997fb-115">Application</span></span>|<span data-ttu-id="997fb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="997fb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="997fb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="997fb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="997fb-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="997fb-118">Request headers</span></span>
|<span data-ttu-id="997fb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="997fb-119">Header</span></span>|<span data-ttu-id="997fb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="997fb-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="997fb-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="997fb-121">Authorization</span></span>|<span data-ttu-id="997fb-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="997fb-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="997fb-123">Accept</span><span class="sxs-lookup"><span data-stu-id="997fb-123">Accept</span></span>|<span data-ttu-id="997fb-124">application/json</span><span class="sxs-lookup"><span data-stu-id="997fb-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="997fb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="997fb-125">Request body</span></span>
<span data-ttu-id="997fb-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="997fb-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="997fb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="997fb-127">Response</span></span>
<span data-ttu-id="997fb-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="997fb-128">If successful, this method returns a `200 OK` response code and a collection of [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="997fb-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="997fb-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="997fb-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="997fb-130">Request</span></span>
<span data-ttu-id="997fb-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="997fb-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="997fb-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="997fb-132">Response</span></span>
<span data-ttu-id="997fb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="997fb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1070

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.microsoftStoreForBusinessApp",
      "id": "f33358bc-58bc-f333-bc58-33f3bc5833f3",
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
      "usedLicenseCount": 0,
      "totalLicenseCount": 1,
      "productKey": "Product Key value",
      "licenseType": "online",
      "packageIdentityName": "Package Identity Name value"
    }
  ]
}
```



