---
title: managedDeviceEnrollmentFailureDetails (función)
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: e95a0590ee08fb29d2ae95cb68f0bded658ecf18
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357060"
---
# <a name="manageddeviceenrollmentfailuredetails-function"></a><span data-ttu-id="b2091-103">managedDeviceEnrollmentFailureDetails (función)</span><span class="sxs-lookup"><span data-stu-id="b2091-103">managedDeviceEnrollmentFailureDetails function</span></span>

> <span data-ttu-id="b2091-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2091-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2091-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b2091-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b2091-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b2091-106">Prerequisites</span></span>
<span data-ttu-id="b2091-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b2091-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b2091-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2091-109">Permission type</span></span>|<span data-ttu-id="b2091-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2091-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b2091-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2091-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="b2091-112">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="b2091-112">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="b2091-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b2091-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="b2091-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2091-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b2091-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2091-115">Not supported.</span></span>|
|<span data-ttu-id="b2091-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2091-116">Application</span></span>|<span data-ttu-id="b2091-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2091-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b2091-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2091-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentFailureDetails
```

## <a name="request-headers"></a><span data-ttu-id="b2091-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2091-119">Request headers</span></span>
|<span data-ttu-id="b2091-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2091-120">Header</span></span>|<span data-ttu-id="b2091-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b2091-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b2091-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="b2091-122">Authorization</span></span>|<span data-ttu-id="b2091-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b2091-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b2091-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b2091-124">Accept</span></span>|<span data-ttu-id="b2091-125">application/json</span><span class="sxs-lookup"><span data-stu-id="b2091-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b2091-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2091-126">Request body</span></span>
<span data-ttu-id="b2091-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="b2091-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="b2091-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="b2091-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="b2091-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2091-129">Property</span></span>|<span data-ttu-id="b2091-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2091-130">Type</span></span>|<span data-ttu-id="b2091-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2091-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b2091-132">skip</span><span class="sxs-lookup"><span data-stu-id="b2091-132">skip</span></span>|<span data-ttu-id="b2091-133">Int32</span><span class="sxs-lookup"><span data-stu-id="b2091-133">Int32</span></span>|<span data-ttu-id="b2091-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b2091-134">Not yet documented</span></span>|
|<span data-ttu-id="b2091-135">top</span><span class="sxs-lookup"><span data-stu-id="b2091-135">top</span></span>|<span data-ttu-id="b2091-136">Int32</span><span class="sxs-lookup"><span data-stu-id="b2091-136">Int32</span></span>|<span data-ttu-id="b2091-137">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b2091-137">Not yet documented</span></span>|
|<span data-ttu-id="b2091-138">filter</span><span class="sxs-lookup"><span data-stu-id="b2091-138">filter</span></span>|<span data-ttu-id="b2091-139">String</span><span class="sxs-lookup"><span data-stu-id="b2091-139">String</span></span>|<span data-ttu-id="b2091-140">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b2091-140">Not yet documented</span></span>|
|<span data-ttu-id="b2091-141">skipToken</span><span class="sxs-lookup"><span data-stu-id="b2091-141">skipToken</span></span>|<span data-ttu-id="b2091-142">String</span><span class="sxs-lookup"><span data-stu-id="b2091-142">String</span></span>|<span data-ttu-id="b2091-143">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b2091-143">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="b2091-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2091-144">Response</span></span>
<span data-ttu-id="b2091-145">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2091-145">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b2091-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2091-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="b2091-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2091-147">Request</span></span>
<span data-ttu-id="b2091-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2091-148">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentFailureDetails(skip=4,top=3,filter='parameterValue',skipToken='parameterValue')
```

### <a name="response"></a><span data-ttu-id="b2091-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2091-149">Response</span></span>
<span data-ttu-id="b2091-150">El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="b2091-150">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="b2091-151">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2091-151">All of the properties will be returned from an actual call.</span></span>

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




