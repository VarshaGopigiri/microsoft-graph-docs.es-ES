---
title: Lista windowsPhone81AppXs
description: Propiedades de la lista y relaciones de los objetos windowsPhone81AppX.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 470a9c7feaeb133cdb02b452fb587f9e40c2eb36
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939675"
---
# <a name="list-windowsphone81appxs"></a><span data-ttu-id="ae7f2-103">Lista windowsPhone81AppXs</span><span class="sxs-lookup"><span data-stu-id="ae7f2-103">List windowsPhone81AppXs</span></span>

> <span data-ttu-id="ae7f2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ae7f2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ae7f2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ae7f2-107">Propiedades de la lista y relaciones de los objetos [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) .</span><span class="sxs-lookup"><span data-stu-id="ae7f2-107">List properties and relationships of the [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ae7f2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae7f2-108">Prerequisites</span></span>
<span data-ttu-id="ae7f2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ae7f2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ae7f2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ae7f2-111">Permission type</span></span>|<span data-ttu-id="ae7f2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ae7f2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ae7f2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ae7f2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ae7f2-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="ae7f2-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="ae7f2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ae7f2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ae7f2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-116">Not supported.</span></span>|
|<span data-ttu-id="ae7f2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ae7f2-117">Application</span></span>|<span data-ttu-id="ae7f2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ae7f2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae7f2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="ae7f2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae7f2-120">Request headers</span></span>
|<span data-ttu-id="ae7f2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae7f2-121">Header</span></span>|<span data-ttu-id="ae7f2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ae7f2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ae7f2-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ae7f2-123">Authorization</span></span>|<span data-ttu-id="ae7f2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ae7f2-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ae7f2-125">Accept</span></span>|<span data-ttu-id="ae7f2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ae7f2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ae7f2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae7f2-127">Request body</span></span>
<span data-ttu-id="ae7f2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ae7f2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae7f2-129">Response</span></span>
<span data-ttu-id="ae7f2-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-130">If successful, this method returns a `200 OK` response code and a collection of [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ae7f2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae7f2-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ae7f2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae7f2-132">Request</span></span>
<span data-ttu-id="ae7f2-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="ae7f2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae7f2-134">Response</span></span>
<span data-ttu-id="ae7f2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ae7f2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1720

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsPhone81AppX",
      "id": "4ff27f80-7f80-4ff2-807f-f24f807ff24f",
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
      "applicableArchitectures": "x86",
      "identityName": "Identity Name value",
      "identityPublisherHash": "Identity Publisher Hash value",
      "identityResourceIdentifier": "Identity Resource Identifier value",
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
      "phoneProductIdentifier": "Phone Product Identifier value",
      "phonePublisherId": "Phone Publisher Id value",
      "identityVersion": "Identity Version value"
    }
  ]
}
```





