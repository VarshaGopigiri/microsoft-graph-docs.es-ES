---
title: managedDeviceEnrollmentFailureDetails (función)
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 128ad6e3985649b3dbaffa101c19f0b2440b0838
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980380"
---
# <a name="manageddeviceenrollmentfailuredetails-function"></a><span data-ttu-id="cb7f4-103">managedDeviceEnrollmentFailureDetails (función)</span><span class="sxs-lookup"><span data-stu-id="cb7f4-103">managedDeviceEnrollmentFailureDetails function</span></span>

> <span data-ttu-id="cb7f4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cb7f4-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cb7f4-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cb7f4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cb7f4-106">Prerequisites</span></span>
<span data-ttu-id="cb7f4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cb7f4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cb7f4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cb7f4-109">Permission type</span></span>|<span data-ttu-id="cb7f4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cb7f4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cb7f4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cb7f4-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="cb7f4-112">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="cb7f4-112">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="cb7f4-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cb7f4-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="cb7f4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cb7f4-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cb7f4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-115">Not supported.</span></span>|
|<span data-ttu-id="cb7f4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cb7f4-116">Application</span></span>|<span data-ttu-id="cb7f4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cb7f4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cb7f4-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentFailureDetails
```

## <a name="request-headers"></a><span data-ttu-id="cb7f4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cb7f4-119">Request headers</span></span>
|<span data-ttu-id="cb7f4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb7f4-120">Header</span></span>|<span data-ttu-id="cb7f4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cb7f4-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cb7f4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="cb7f4-122">Authorization</span></span>|<span data-ttu-id="cb7f4-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cb7f4-124">Accept</span><span class="sxs-lookup"><span data-stu-id="cb7f4-124">Accept</span></span>|<span data-ttu-id="cb7f4-125">application/json</span><span class="sxs-lookup"><span data-stu-id="cb7f4-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cb7f4-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cb7f4-126">Request body</span></span>
<span data-ttu-id="cb7f4-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="cb7f4-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="cb7f4-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb7f4-129">Property</span></span>|<span data-ttu-id="cb7f4-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb7f4-130">Type</span></span>|<span data-ttu-id="cb7f4-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb7f4-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cb7f4-132">skip</span><span class="sxs-lookup"><span data-stu-id="cb7f4-132">skip</span></span>|<span data-ttu-id="cb7f4-133">Int32</span><span class="sxs-lookup"><span data-stu-id="cb7f4-133">Int32</span></span>|<span data-ttu-id="cb7f4-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cb7f4-134">Not yet documented</span></span>|
|<span data-ttu-id="cb7f4-135">top</span><span class="sxs-lookup"><span data-stu-id="cb7f4-135">top</span></span>|<span data-ttu-id="cb7f4-136">Int32</span><span class="sxs-lookup"><span data-stu-id="cb7f4-136">Int32</span></span>|<span data-ttu-id="cb7f4-137">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cb7f4-137">Not yet documented</span></span>|
|<span data-ttu-id="cb7f4-138">filter</span><span class="sxs-lookup"><span data-stu-id="cb7f4-138">filter</span></span>|<span data-ttu-id="cb7f4-139">String</span><span class="sxs-lookup"><span data-stu-id="cb7f4-139">String</span></span>|<span data-ttu-id="cb7f4-140">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cb7f4-140">Not yet documented</span></span>|
|<span data-ttu-id="cb7f4-141">skipToken</span><span class="sxs-lookup"><span data-stu-id="cb7f4-141">skipToken</span></span>|<span data-ttu-id="cb7f4-142">String</span><span class="sxs-lookup"><span data-stu-id="cb7f4-142">String</span></span>|<span data-ttu-id="cb7f4-143">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cb7f4-143">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="cb7f4-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb7f4-144">Response</span></span>
<span data-ttu-id="cb7f4-145">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-145">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cb7f4-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb7f4-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="cb7f4-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb7f4-147">Request</span></span>
<span data-ttu-id="cb7f4-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-148">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentFailureDetails(skip=4,top=3,filter='parameterValue',skipToken='parameterValue')
```

### <a name="response"></a><span data-ttu-id="cb7f4-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb7f4-149">Response</span></span>
<span data-ttu-id="cb7f4-150">El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-150">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="cb7f4-151">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cb7f4-151">All of the properties will be returned from an actual call.</span></span>

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




