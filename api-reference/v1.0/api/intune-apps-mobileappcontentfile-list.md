---
title: Enumerar mobileAppContentFiles
description: Enumere las propiedades y las relaciones de los objetos mobileAppContentFile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dbcc2263b92d2b7c0a996944730b71f75e1a5c08
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961816"
---
# <a name="list-mobileappcontentfiles"></a><span data-ttu-id="ebdd4-103">Enumerar mobileAppContentFiles</span><span class="sxs-lookup"><span data-stu-id="ebdd4-103">List mobileAppContentFiles</span></span>

> <span data-ttu-id="ebdd4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ebdd4-105">Enumere las propiedades y las relaciones de los objetos [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="ebdd4-105">List properties and relationships of the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ebdd4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ebdd4-106">Prerequisites</span></span>
<span data-ttu-id="ebdd4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ebdd4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ebdd4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebdd4-109">Permission type</span></span>|<span data-ttu-id="ebdd4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebdd4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ebdd4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebdd4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ebdd4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="ebdd4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="ebdd4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebdd4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ebdd4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-114">Not supported.</span></span>|
|<span data-ttu-id="ebdd4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebdd4-115">Application</span></span>|<span data-ttu-id="ebdd4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ebdd4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebdd4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
```

## <a name="request-headers"></a><span data-ttu-id="ebdd4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebdd4-118">Request headers</span></span>
|<span data-ttu-id="ebdd4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebdd4-119">Header</span></span>|<span data-ttu-id="ebdd4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ebdd4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ebdd4-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ebdd4-121">Authorization</span></span>|<span data-ttu-id="ebdd4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ebdd4-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ebdd4-123">Accept</span></span>|<span data-ttu-id="ebdd4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ebdd4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ebdd4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebdd4-125">Request body</span></span>
<span data-ttu-id="ebdd4-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ebdd4-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebdd4-127">Response</span></span>
<span data-ttu-id="ebdd4-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-128">If successful, this method returns a `200 OK` response code and a collection of [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ebdd4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebdd4-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="ebdd4-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebdd4-130">Request</span></span>
<span data-ttu-id="ebdd4-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
```

### <a name="response"></a><span data-ttu-id="ebdd4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebdd4-132">Response</span></span>
<span data-ttu-id="ebdd4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ebdd4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



