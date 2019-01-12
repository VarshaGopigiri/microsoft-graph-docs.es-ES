---
title: Enumerar windowsInformationProtectionNetworkLearningSummaries
description: Enumere las propiedades y las relaciones de los objetos windowsInformationProtectionNetworkLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3e99eb8eed2780e2ea57accbd133290b072c167a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972666"
---
# <a name="list-windowsinformationprotectionnetworklearningsummaries"></a><span data-ttu-id="e7745-103">Enumerar windowsInformationProtectionNetworkLearningSummaries</span><span class="sxs-lookup"><span data-stu-id="e7745-103">List windowsInformationProtectionNetworkLearningSummaries</span></span>

> <span data-ttu-id="e7745-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7745-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7745-105">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="e7745-105">List properties and relationships of the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7745-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7745-106">Prerequisites</span></span>
<span data-ttu-id="e7745-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7745-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e7745-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7745-109">Permission type</span></span>|<span data-ttu-id="e7745-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7745-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e7745-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7745-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e7745-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="e7745-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="e7745-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7745-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e7745-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7745-114">Not supported.</span></span>|
|<span data-ttu-id="e7745-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7745-115">Application</span></span>|<span data-ttu-id="e7745-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7745-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e7745-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7745-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="e7745-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7745-118">Request headers</span></span>
|<span data-ttu-id="e7745-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7745-119">Header</span></span>|<span data-ttu-id="e7745-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e7745-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e7745-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e7745-121">Authorization</span></span>|<span data-ttu-id="e7745-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e7745-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e7745-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e7745-123">Accept</span></span>|<span data-ttu-id="e7745-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e7745-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e7745-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7745-125">Request body</span></span>
<span data-ttu-id="e7745-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e7745-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e7745-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7745-127">Response</span></span>
<span data-ttu-id="e7745-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7745-128">If successful, this method returns a `200 OK` response code and a collection of [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e7745-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7745-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e7745-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7745-130">Request</span></span>
<span data-ttu-id="e7745-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7745-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

### <a name="response"></a><span data-ttu-id="e7745-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7745-132">Response</span></span>
<span data-ttu-id="e7745-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7745-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 235

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
      "id": "242108f7-08f7-2421-f708-2124f7082124",
      "url": "Url value",
      "deviceCount": 11
    }
  ]
}
```



