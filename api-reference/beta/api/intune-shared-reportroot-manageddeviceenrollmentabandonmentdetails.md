---
title: managedDeviceEnrollmentAbandonmentDetails (función)
description: Informe detallan de metadatos por abandono de inscripción
ms.openlocfilehash: 53096db451630240c7d87f40250a8c55aec9618d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083773"
---
# <a name="manageddeviceenrollmentabandonmentdetails-function"></a><span data-ttu-id="049d5-103">managedDeviceEnrollmentAbandonmentDetails (función)</span><span class="sxs-lookup"><span data-stu-id="049d5-103">managedDeviceEnrollmentAbandonmentDetails function</span></span>

> <span data-ttu-id="049d5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="049d5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="049d5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="049d5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="049d5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="049d5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="049d5-107">Informe detallan de metadatos por abandono de inscripción</span><span class="sxs-lookup"><span data-stu-id="049d5-107">Metadata for Enrollment abandonment details report</span></span>
## <a name="prerequisites"></a><span data-ttu-id="049d5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="049d5-108">Prerequisites</span></span>
<span data-ttu-id="049d5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="049d5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="049d5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="049d5-111">Permission type</span></span>|<span data-ttu-id="049d5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="049d5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="049d5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="049d5-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="049d5-114">&nbsp;&nbsp; **Troublshooting**</span><span class="sxs-lookup"><span data-stu-id="049d5-114">&nbsp; &nbsp; **Troublshooting**</span></span> | <span data-ttu-id="049d5-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="049d5-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="049d5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="049d5-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="049d5-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="049d5-117">Not supported.</span></span>|
|<span data-ttu-id="049d5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="049d5-118">Application</span></span>|<span data-ttu-id="049d5-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="049d5-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="049d5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="049d5-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentAbandonmentDetails
```

## <a name="request-headers"></a><span data-ttu-id="049d5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="049d5-121">Request headers</span></span>
|<span data-ttu-id="049d5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="049d5-122">Header</span></span>|<span data-ttu-id="049d5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="049d5-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="049d5-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="049d5-124">Authorization</span></span>|<span data-ttu-id="049d5-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="049d5-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="049d5-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="049d5-126">Accept</span></span>|<span data-ttu-id="049d5-127">application/json</span><span class="sxs-lookup"><span data-stu-id="049d5-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="049d5-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="049d5-128">Request body</span></span>
<span data-ttu-id="049d5-129">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="049d5-129">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="049d5-130">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="049d5-130">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="049d5-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="049d5-131">Property</span></span>|<span data-ttu-id="049d5-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="049d5-132">Type</span></span>|<span data-ttu-id="049d5-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="049d5-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="049d5-134">skip</span><span class="sxs-lookup"><span data-stu-id="049d5-134">skip</span></span>|<span data-ttu-id="049d5-135">Int32</span><span class="sxs-lookup"><span data-stu-id="049d5-135">Int32</span></span>|<span data-ttu-id="049d5-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="049d5-136">Not yet documented</span></span>|
|<span data-ttu-id="049d5-137">top</span><span class="sxs-lookup"><span data-stu-id="049d5-137">top</span></span>|<span data-ttu-id="049d5-138">Int32</span><span class="sxs-lookup"><span data-stu-id="049d5-138">Int32</span></span>|<span data-ttu-id="049d5-139">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="049d5-139">Not yet documented</span></span>|
|<span data-ttu-id="049d5-140">filter</span><span class="sxs-lookup"><span data-stu-id="049d5-140">filter</span></span>|<span data-ttu-id="049d5-141">String</span><span class="sxs-lookup"><span data-stu-id="049d5-141">String</span></span>|<span data-ttu-id="049d5-142">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="049d5-142">Not yet documented</span></span>|
|<span data-ttu-id="049d5-143">skipToken</span><span class="sxs-lookup"><span data-stu-id="049d5-143">skipToken</span></span>|<span data-ttu-id="049d5-144">String</span><span class="sxs-lookup"><span data-stu-id="049d5-144">String</span></span>|<span data-ttu-id="049d5-145">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="049d5-145">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="049d5-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="049d5-146">Response</span></span>
<span data-ttu-id="049d5-147">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="049d5-147">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="049d5-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="049d5-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="049d5-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="049d5-149">Request</span></span>
<span data-ttu-id="049d5-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="049d5-150">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports/managedDeviceEnrollmentAbandonmentDetails(skip=4,top=3,filter='parameterValue',skipToken='parameterValue')
```

### <a name="response"></a><span data-ttu-id="049d5-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="049d5-151">Response</span></span>
<span data-ttu-id="049d5-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="049d5-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





