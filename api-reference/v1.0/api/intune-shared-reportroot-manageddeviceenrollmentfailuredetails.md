---
title: managedDeviceEnrollmentFailureDetails (función)
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d7e3ad342ad19314e10ae5e2987143646e5796c3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840372"
---
# <a name="manageddeviceenrollmentfailuredetails-function"></a><span data-ttu-id="d49e1-103">managedDeviceEnrollmentFailureDetails (función)</span><span class="sxs-lookup"><span data-stu-id="d49e1-103">managedDeviceEnrollmentFailureDetails function</span></span>

> <span data-ttu-id="d49e1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d49e1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d49e1-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d49e1-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d49e1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d49e1-106">Prerequisites</span></span>
<span data-ttu-id="d49e1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d49e1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d49e1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d49e1-109">Permission type</span></span>|<span data-ttu-id="d49e1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d49e1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d49e1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d49e1-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="d49e1-112">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="d49e1-112">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="d49e1-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d49e1-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="d49e1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d49e1-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d49e1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d49e1-115">Not supported.</span></span>|
|<span data-ttu-id="d49e1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d49e1-116">Application</span></span>|<span data-ttu-id="d49e1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d49e1-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d49e1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d49e1-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentFailureDetails
```

## <a name="request-headers"></a><span data-ttu-id="d49e1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d49e1-119">Request headers</span></span>
|<span data-ttu-id="d49e1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d49e1-120">Header</span></span>|<span data-ttu-id="d49e1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d49e1-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d49e1-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="d49e1-122">Authorization</span></span>|<span data-ttu-id="d49e1-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d49e1-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d49e1-124">Accept</span><span class="sxs-lookup"><span data-stu-id="d49e1-124">Accept</span></span>|<span data-ttu-id="d49e1-125">application/json</span><span class="sxs-lookup"><span data-stu-id="d49e1-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d49e1-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d49e1-126">Request body</span></span>
<span data-ttu-id="d49e1-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="d49e1-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="d49e1-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="d49e1-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="d49e1-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d49e1-129">Property</span></span>|<span data-ttu-id="d49e1-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="d49e1-130">Type</span></span>|<span data-ttu-id="d49e1-131">Description</span><span class="sxs-lookup"><span data-stu-id="d49e1-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d49e1-132">skip</span><span class="sxs-lookup"><span data-stu-id="d49e1-132">skip</span></span>|<span data-ttu-id="d49e1-133">Int32</span><span class="sxs-lookup"><span data-stu-id="d49e1-133">Int32</span></span>|<span data-ttu-id="d49e1-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d49e1-134">Not yet documented</span></span>|
|<span data-ttu-id="d49e1-135">top</span><span class="sxs-lookup"><span data-stu-id="d49e1-135">top</span></span>|<span data-ttu-id="d49e1-136">Int32</span><span class="sxs-lookup"><span data-stu-id="d49e1-136">Int32</span></span>|<span data-ttu-id="d49e1-137">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d49e1-137">Not yet documented</span></span>|
|<span data-ttu-id="d49e1-138">filter</span><span class="sxs-lookup"><span data-stu-id="d49e1-138">filter</span></span>|<span data-ttu-id="d49e1-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="d49e1-139">String</span></span>|<span data-ttu-id="d49e1-140">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d49e1-140">Not yet documented</span></span>|
|<span data-ttu-id="d49e1-141">skipToken</span><span class="sxs-lookup"><span data-stu-id="d49e1-141">skipToken</span></span>|<span data-ttu-id="d49e1-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="d49e1-142">String</span></span>|<span data-ttu-id="d49e1-143">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d49e1-143">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="d49e1-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d49e1-144">Response</span></span>
<span data-ttu-id="d49e1-145">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d49e1-145">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d49e1-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d49e1-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="d49e1-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d49e1-147">Request</span></span>
<span data-ttu-id="d49e1-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d49e1-148">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentFailureDetails(skip=4,top=3,filter='parameterValue',skipToken='parameterValue')
```

### <a name="response"></a><span data-ttu-id="d49e1-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d49e1-149">Response</span></span>
<span data-ttu-id="d49e1-150">El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="d49e1-150">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="d49e1-151">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d49e1-151">All of the properties will be returned from an actual call.</span></span>

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




