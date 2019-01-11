---
title: Enumerar macOSOfficeSuiteApps
description: Enumere las propiedades y las relaciones de los objetos macOSOfficeSuiteApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6c109d56c5f1365a5e2f61022f568ab422b91281
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824314"
---
# <a name="list-macosofficesuiteapps"></a><span data-ttu-id="8d7ed-103">Enumerar macOSOfficeSuiteApps</span><span class="sxs-lookup"><span data-stu-id="8d7ed-103">List macOSOfficeSuiteApps</span></span>

> <span data-ttu-id="8d7ed-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d7ed-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8d7ed-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d7ed-107">Enumere las propiedades y las relaciones de los objetos [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="8d7ed-107">List properties and relationships of the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8d7ed-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8d7ed-108">Prerequisites</span></span>
<span data-ttu-id="8d7ed-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8d7ed-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8d7ed-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8d7ed-111">Permission type</span></span>|<span data-ttu-id="8d7ed-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8d7ed-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8d7ed-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8d7ed-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8d7ed-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d7ed-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="8d7ed-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8d7ed-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8d7ed-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-116">Not supported.</span></span>|
|<span data-ttu-id="8d7ed-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8d7ed-117">Application</span></span>|<span data-ttu-id="8d7ed-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8d7ed-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8d7ed-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="8d7ed-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8d7ed-120">Request headers</span></span>
|<span data-ttu-id="8d7ed-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d7ed-121">Header</span></span>|<span data-ttu-id="8d7ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8d7ed-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8d7ed-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8d7ed-123">Authorization</span></span>|<span data-ttu-id="8d7ed-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8d7ed-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8d7ed-125">Accept</span></span>|<span data-ttu-id="8d7ed-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8d7ed-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8d7ed-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8d7ed-127">Request body</span></span>
<span data-ttu-id="8d7ed-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8d7ed-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d7ed-129">Response</span></span>
<span data-ttu-id="8d7ed-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-130">If successful, this method returns a `200 OK` response code and a collection of [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8d7ed-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d7ed-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="8d7ed-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8d7ed-132">Request</span></span>
<span data-ttu-id="8d7ed-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="8d7ed-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d7ed-134">Response</span></span>
<span data-ttu-id="8d7ed-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8d7ed-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 891

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
      "uploadState": 11,
      "publishingState": "processing"
    }
  ]
}
```





