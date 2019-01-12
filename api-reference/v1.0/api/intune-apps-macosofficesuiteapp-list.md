---
title: Enumerar macOSOfficeSuiteApps
description: Enumere las propiedades y las relaciones de los objetos macOSOfficeSuiteApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cfa1d818714de2b9fcbd3e33460f7c26af0432ed
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949279"
---
# <a name="list-macosofficesuiteapps"></a><span data-ttu-id="68ed9-103">Enumerar macOSOfficeSuiteApps</span><span class="sxs-lookup"><span data-stu-id="68ed9-103">List macOSOfficeSuiteApps</span></span>

> <span data-ttu-id="68ed9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="68ed9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="68ed9-105">Enumere las propiedades y las relaciones de los objetos [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="68ed9-105">List properties and relationships of the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="68ed9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68ed9-106">Prerequisites</span></span>
<span data-ttu-id="68ed9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="68ed9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="68ed9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68ed9-109">Permission type</span></span>|<span data-ttu-id="68ed9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68ed9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="68ed9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68ed9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="68ed9-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="68ed9-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="68ed9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68ed9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="68ed9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68ed9-114">Not supported.</span></span>|
|<span data-ttu-id="68ed9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68ed9-115">Application</span></span>|<span data-ttu-id="68ed9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68ed9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="68ed9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68ed9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="68ed9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68ed9-118">Request headers</span></span>
|<span data-ttu-id="68ed9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68ed9-119">Header</span></span>|<span data-ttu-id="68ed9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="68ed9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="68ed9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="68ed9-121">Authorization</span></span>|<span data-ttu-id="68ed9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="68ed9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="68ed9-123">Accept</span><span class="sxs-lookup"><span data-stu-id="68ed9-123">Accept</span></span>|<span data-ttu-id="68ed9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="68ed9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="68ed9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68ed9-125">Request body</span></span>
<span data-ttu-id="68ed9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="68ed9-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="68ed9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68ed9-127">Response</span></span>
<span data-ttu-id="68ed9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68ed9-128">If successful, this method returns a `200 OK` response code and a collection of [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68ed9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68ed9-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="68ed9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68ed9-130">Request</span></span>
<span data-ttu-id="68ed9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68ed9-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="68ed9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68ed9-132">Response</span></span>
<span data-ttu-id="68ed9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68ed9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 865

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
      "id": "bf39e35d-e35d-bf39-5de3-39bf5de339bf",
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
      "publishingState": "processing"
    }
  ]
}
```



