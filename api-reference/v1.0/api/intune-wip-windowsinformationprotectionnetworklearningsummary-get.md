---
title: Obtener windowsInformationProtectionNetworkLearningSummary
description: Lea las propiedades y las relaciones del objeto windowsInformationProtectionNetworkLearningSummary.
ms.openlocfilehash: 7dc5fafb725048016339332f7076a3a518fa0936
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031321"
---
# <a name="get-windowsinformationprotectionnetworklearningsummary"></a><span data-ttu-id="39e0f-103">Obtener windowsInformationProtectionNetworkLearningSummary</span><span class="sxs-lookup"><span data-stu-id="39e0f-103">Get windowsInformationProtectionNetworkLearningSummary</span></span>

> <span data-ttu-id="39e0f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39e0f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39e0f-105">Lea las propiedades y las relaciones del objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="39e0f-105">Read properties and relationships of the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39e0f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39e0f-106">Prerequisites</span></span>
<span data-ttu-id="39e0f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39e0f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39e0f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39e0f-109">Permission type</span></span>|<span data-ttu-id="39e0f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39e0f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39e0f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39e0f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="39e0f-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="39e0f-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="39e0f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39e0f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39e0f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39e0f-114">Not supported.</span></span>|
|<span data-ttu-id="39e0f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39e0f-115">Application</span></span>|<span data-ttu-id="39e0f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39e0f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="39e0f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39e0f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsInformationProtectionNetworkLearningSummaries/{windowsInformationProtectionNetworkLearningSummaryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="39e0f-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="39e0f-118">Optional query parameters</span></span>
<span data-ttu-id="39e0f-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39e0f-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="39e0f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39e0f-120">Request headers</span></span>
|<span data-ttu-id="39e0f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39e0f-121">Header</span></span>|<span data-ttu-id="39e0f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="39e0f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39e0f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="39e0f-123">Authorization</span></span>|<span data-ttu-id="39e0f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="39e0f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39e0f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="39e0f-125">Accept</span></span>|<span data-ttu-id="39e0f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="39e0f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39e0f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39e0f-127">Request body</span></span>
<span data-ttu-id="39e0f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="39e0f-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="39e0f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39e0f-129">Response</span></span>
<span data-ttu-id="39e0f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39e0f-130">If successful, this method returns a `200 OK` response code and [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39e0f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39e0f-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="39e0f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39e0f-132">Request</span></span>
<span data-ttu-id="39e0f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39e0f-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionNetworkLearningSummaries/{windowsInformationProtectionNetworkLearningSummaryId}
```

### <a name="response"></a><span data-ttu-id="39e0f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39e0f-134">Response</span></span>
<span data-ttu-id="39e0f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39e0f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 213

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
    "id": "242108f7-08f7-2421-f708-2124f7082124",
    "url": "Url value",
    "deviceCount": 11
  }
}
```



