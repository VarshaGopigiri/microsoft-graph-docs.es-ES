---
title: managedDeviceEnrollmentFailureDetails (función)
description: Todavía no documentado
ms.openlocfilehash: 92a06a4fae5d469759f633698abcf7bff2bfb322
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087397"
---
# <a name="manageddeviceenrollmentfailuredetails-function"></a><span data-ttu-id="3355e-103">managedDeviceEnrollmentFailureDetails (función)</span><span class="sxs-lookup"><span data-stu-id="3355e-103">managedDeviceEnrollmentFailureDetails function</span></span>

> <span data-ttu-id="3355e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3355e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3355e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3355e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3355e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3355e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3355e-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3355e-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3355e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3355e-108">Prerequisites</span></span>
<span data-ttu-id="3355e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3355e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3355e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3355e-111">Permission type</span></span>|<span data-ttu-id="3355e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3355e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3355e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3355e-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="3355e-114">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="3355e-114">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="3355e-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3355e-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="3355e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3355e-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3355e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3355e-117">Not supported.</span></span>|
|<span data-ttu-id="3355e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3355e-118">Application</span></span>|<span data-ttu-id="3355e-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3355e-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3355e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3355e-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentFailureDetails
```

## <a name="request-headers"></a><span data-ttu-id="3355e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3355e-121">Request headers</span></span>
|<span data-ttu-id="3355e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3355e-122">Header</span></span>|<span data-ttu-id="3355e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3355e-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3355e-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="3355e-124">Authorization</span></span>|<span data-ttu-id="3355e-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3355e-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3355e-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3355e-126">Accept</span></span>|<span data-ttu-id="3355e-127">application/json</span><span class="sxs-lookup"><span data-stu-id="3355e-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3355e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3355e-128">Request body</span></span>
<span data-ttu-id="3355e-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="3355e-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="3355e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3355e-130">Property</span></span>|<span data-ttu-id="3355e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3355e-131">Type</span></span>|<span data-ttu-id="3355e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3355e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3355e-133">filter</span><span class="sxs-lookup"><span data-stu-id="3355e-133">filter</span></span>|<span data-ttu-id="3355e-134">String</span><span class="sxs-lookup"><span data-stu-id="3355e-134">String</span></span>|<span data-ttu-id="3355e-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3355e-135">Not yet documented</span></span>|
|<span data-ttu-id="3355e-136">skipToken</span><span class="sxs-lookup"><span data-stu-id="3355e-136">skipToken</span></span>|<span data-ttu-id="3355e-137">String</span><span class="sxs-lookup"><span data-stu-id="3355e-137">String</span></span>|<span data-ttu-id="3355e-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3355e-138">Not yet documented</span></span>|
|<span data-ttu-id="3355e-139">skip</span><span class="sxs-lookup"><span data-stu-id="3355e-139">skip</span></span>|<span data-ttu-id="3355e-140">Int32</span><span class="sxs-lookup"><span data-stu-id="3355e-140">Int32</span></span>|<span data-ttu-id="3355e-141">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3355e-141">Not yet documented</span></span>|
|<span data-ttu-id="3355e-142">top</span><span class="sxs-lookup"><span data-stu-id="3355e-142">top</span></span>|<span data-ttu-id="3355e-143">Int32</span><span class="sxs-lookup"><span data-stu-id="3355e-143">Int32</span></span>|<span data-ttu-id="3355e-144">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3355e-144">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="3355e-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3355e-145">Response</span></span>
<span data-ttu-id="3355e-146">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3355e-146">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3355e-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3355e-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="3355e-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3355e-148">Request</span></span>
<span data-ttu-id="3355e-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3355e-149">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports/managedDeviceEnrollmentFailureDetails(skip=4,top=3,filter='parameterValue',skipToken='parameterValue')
```

### <a name="response"></a><span data-ttu-id="3355e-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3355e-150">Response</span></span>
<span data-ttu-id="3355e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3355e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



