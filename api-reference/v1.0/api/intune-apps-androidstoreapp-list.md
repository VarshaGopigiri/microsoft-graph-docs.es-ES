---
title: Enumerar androidStoreApps
description: Enumere las propiedades y las relaciones de los objetos androidStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cd1911d1c372fe6e01e8ef00eaecf66d43101202
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957322"
---
# <a name="list-androidstoreapps"></a><span data-ttu-id="fc430-103">Enumerar androidStoreApps</span><span class="sxs-lookup"><span data-stu-id="fc430-103">List androidStoreApps</span></span>

> <span data-ttu-id="fc430-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fc430-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc430-105">Enumere las propiedades y las relaciones de los objetos [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="fc430-105">List properties and relationships of the [androidStoreApp](../resources/intune-apps-androidstoreapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fc430-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fc430-106">Prerequisites</span></span>
<span data-ttu-id="fc430-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc430-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc430-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc430-109">Permission type</span></span>|<span data-ttu-id="fc430-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc430-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fc430-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc430-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fc430-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="fc430-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="fc430-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc430-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fc430-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc430-114">Not supported.</span></span>|
|<span data-ttu-id="fc430-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc430-115">Application</span></span>|<span data-ttu-id="fc430-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc430-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fc430-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc430-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="fc430-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc430-118">Request headers</span></span>
|<span data-ttu-id="fc430-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc430-119">Header</span></span>|<span data-ttu-id="fc430-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fc430-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fc430-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fc430-121">Authorization</span></span>|<span data-ttu-id="fc430-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fc430-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fc430-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fc430-123">Accept</span></span>|<span data-ttu-id="fc430-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fc430-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fc430-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc430-125">Request body</span></span>
<span data-ttu-id="fc430-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fc430-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fc430-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc430-127">Response</span></span>
<span data-ttu-id="fc430-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidStoreApp](../resources/intune-apps-androidstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc430-128">If successful, this method returns a `200 OK` response code and a collection of [androidStoreApp](../resources/intune-apps-androidstoreapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc430-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc430-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="fc430-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc430-130">Request</span></span>
<span data-ttu-id="fc430-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc430-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="fc430-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc430-132">Response</span></span>
<span data-ttu-id="fc430-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc430-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1271

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidStoreApp",
      "id": "1f2b7654-7654-1f2b-5476-2b1f54762b1f",
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
      "packageId": "Package Id value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
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
      }
    }
  ]
}
```



