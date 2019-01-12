---
title: managedDeviceEnrollmentTopFailures (función)
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b4a21d9fc0b29c63053d184db235a1c44744d8e4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932661"
---
# <a name="manageddeviceenrollmenttopfailures-function"></a><span data-ttu-id="a4c68-103">managedDeviceEnrollmentTopFailures (función)</span><span class="sxs-lookup"><span data-stu-id="a4c68-103">managedDeviceEnrollmentTopFailures function</span></span>

> <span data-ttu-id="a4c68-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4c68-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4c68-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a4c68-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a4c68-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a4c68-106">Prerequisites</span></span>
<span data-ttu-id="a4c68-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4c68-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a4c68-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4c68-109">Permission type</span></span>|<span data-ttu-id="a4c68-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4c68-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a4c68-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4c68-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="a4c68-112">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="a4c68-112">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="a4c68-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4c68-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="a4c68-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4c68-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a4c68-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4c68-115">Not supported.</span></span>|
|<span data-ttu-id="a4c68-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4c68-116">Application</span></span>|<span data-ttu-id="a4c68-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4c68-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a4c68-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4c68-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentTopFailures
```

## <a name="request-headers"></a><span data-ttu-id="a4c68-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4c68-119">Request headers</span></span>
|<span data-ttu-id="a4c68-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4c68-120">Header</span></span>|<span data-ttu-id="a4c68-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c68-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a4c68-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="a4c68-122">Authorization</span></span>|<span data-ttu-id="a4c68-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a4c68-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a4c68-124">Accept</span><span class="sxs-lookup"><span data-stu-id="a4c68-124">Accept</span></span>|<span data-ttu-id="a4c68-125">application/json</span><span class="sxs-lookup"><span data-stu-id="a4c68-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a4c68-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4c68-126">Request body</span></span>
<span data-ttu-id="a4c68-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="a4c68-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="a4c68-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="a4c68-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="a4c68-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4c68-129">Property</span></span>|<span data-ttu-id="a4c68-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4c68-130">Type</span></span>|<span data-ttu-id="a4c68-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4c68-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4c68-132">period</span><span class="sxs-lookup"><span data-stu-id="a4c68-132">period</span></span>|<span data-ttu-id="a4c68-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4c68-133">String</span></span>|<span data-ttu-id="a4c68-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a4c68-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a4c68-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4c68-135">Response</span></span>
<span data-ttu-id="a4c68-136">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4c68-136">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4c68-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4c68-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="a4c68-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4c68-138">Request</span></span>
<span data-ttu-id="a4c68-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4c68-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentTopFailures(period='parameterValue')
```

### <a name="response"></a><span data-ttu-id="a4c68-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4c68-140">Response</span></span>
<span data-ttu-id="a4c68-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4c68-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 123

{
  "value": {
    "@odata.type": "microsoft.graph.report",
    "content": "<Unknown Primitive Type Edm.Stream>"
  }
}
```




