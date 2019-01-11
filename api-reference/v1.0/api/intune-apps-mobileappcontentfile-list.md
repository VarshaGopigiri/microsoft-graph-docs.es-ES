---
title: Enumerar mobileAppContentFiles
description: Enumere las propiedades y las relaciones de los objetos mobileAppContentFile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e4107a0f2f9fc90724df6b2871cbc9b45ec4812e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867511"
---
# <a name="list-mobileappcontentfiles"></a><span data-ttu-id="01d85-103">Enumerar mobileAppContentFiles</span><span class="sxs-lookup"><span data-stu-id="01d85-103">List mobileAppContentFiles</span></span>

> <span data-ttu-id="01d85-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01d85-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01d85-105">Enumere las propiedades y las relaciones de los objetos [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="01d85-105">List properties and relationships of the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="01d85-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01d85-106">Prerequisites</span></span>
<span data-ttu-id="01d85-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01d85-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01d85-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01d85-109">Permission type</span></span>|<span data-ttu-id="01d85-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01d85-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="01d85-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01d85-111">Delegated (work or school account)</span></span>|<span data-ttu-id="01d85-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="01d85-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="01d85-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01d85-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="01d85-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01d85-114">Not supported.</span></span>|
|<span data-ttu-id="01d85-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01d85-115">Application</span></span>|<span data-ttu-id="01d85-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01d85-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="01d85-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01d85-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
```

## <a name="request-headers"></a><span data-ttu-id="01d85-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01d85-118">Request headers</span></span>
|<span data-ttu-id="01d85-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01d85-119">Header</span></span>|<span data-ttu-id="01d85-120">Valor</span><span class="sxs-lookup"><span data-stu-id="01d85-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="01d85-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="01d85-121">Authorization</span></span>|<span data-ttu-id="01d85-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="01d85-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="01d85-123">Accept</span><span class="sxs-lookup"><span data-stu-id="01d85-123">Accept</span></span>|<span data-ttu-id="01d85-124">application/json</span><span class="sxs-lookup"><span data-stu-id="01d85-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="01d85-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01d85-125">Request body</span></span>
<span data-ttu-id="01d85-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="01d85-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="01d85-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01d85-127">Response</span></span>
<span data-ttu-id="01d85-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01d85-128">If successful, this method returns a `200 OK` response code and a collection of [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01d85-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d85-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="01d85-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01d85-130">Request</span></span>
<span data-ttu-id="01d85-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01d85-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
```

### <a name="response"></a><span data-ttu-id="01d85-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01d85-132">Response</span></span>
<span data-ttu-id="01d85-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01d85-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 527

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mobileAppContentFile",
      "azureStorageUri": "Azure Storage Uri value",
      "isCommitted": true,
      "id": "eab2e29b-e29b-eab2-9be2-b2ea9be2b2ea",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "name": "Name value",
      "size": 4,
      "sizeEncrypted": 13,
      "azureStorageUriExpirationDateTime": "2017-01-01T00:00:08.4940464-08:00",
      "manifest": "bWFuaWZlc3Q=",
      "uploadState": "transientError"
    }
  ]
}
```



