---
title: Enumerar windowsInformationProtectionNetworkLearningSummaries
description: Enumere las propiedades y las relaciones de los objetos windowsInformationProtectionNetworkLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5100f5f127240214fcb1100891fae4ab6f87858a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970132"
---
# <a name="list-windowsinformationprotectionnetworklearningsummaries"></a><span data-ttu-id="da6ef-103">Enumerar windowsInformationProtectionNetworkLearningSummaries</span><span class="sxs-lookup"><span data-stu-id="da6ef-103">List windowsInformationProtectionNetworkLearningSummaries</span></span>

> <span data-ttu-id="da6ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="da6ef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="da6ef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="da6ef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="da6ef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="da6ef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="da6ef-107">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="da6ef-107">List properties and relationships of the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="da6ef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="da6ef-108">Prerequisites</span></span>
<span data-ttu-id="da6ef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="da6ef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="da6ef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da6ef-111">Permission type</span></span>|<span data-ttu-id="da6ef-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da6ef-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="da6ef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da6ef-113">Delegated (work or school account)</span></span>|<span data-ttu-id="da6ef-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="da6ef-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="da6ef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da6ef-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="da6ef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da6ef-116">Not supported.</span></span>|
|<span data-ttu-id="da6ef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da6ef-117">Application</span></span>|<span data-ttu-id="da6ef-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da6ef-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="da6ef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da6ef-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="da6ef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da6ef-120">Request headers</span></span>
|<span data-ttu-id="da6ef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da6ef-121">Header</span></span>|<span data-ttu-id="da6ef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="da6ef-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="da6ef-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="da6ef-123">Authorization</span></span>|<span data-ttu-id="da6ef-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="da6ef-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="da6ef-125">Accept</span><span class="sxs-lookup"><span data-stu-id="da6ef-125">Accept</span></span>|<span data-ttu-id="da6ef-126">application/json</span><span class="sxs-lookup"><span data-stu-id="da6ef-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="da6ef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da6ef-127">Request body</span></span>
<span data-ttu-id="da6ef-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="da6ef-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="da6ef-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da6ef-129">Response</span></span>
<span data-ttu-id="da6ef-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da6ef-130">If successful, this method returns a `200 OK` response code and a collection of [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da6ef-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da6ef-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="da6ef-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da6ef-132">Request</span></span>
<span data-ttu-id="da6ef-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da6ef-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

### <a name="response"></a><span data-ttu-id="da6ef-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da6ef-134">Response</span></span>
<span data-ttu-id="da6ef-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="da6ef-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





