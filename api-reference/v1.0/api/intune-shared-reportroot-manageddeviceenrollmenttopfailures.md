---
title: managedDeviceEnrollmentTopFailures (función)
description: Todavía no documentado
ms.openlocfilehash: 2fb1fc9d611f4a61cf243de0d1c44fa2a3da889e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032521"
---
# <a name="manageddeviceenrollmenttopfailures-function"></a><span data-ttu-id="f6612-103">managedDeviceEnrollmentTopFailures (función)</span><span class="sxs-lookup"><span data-stu-id="f6612-103">managedDeviceEnrollmentTopFailures function</span></span>

> <span data-ttu-id="f6612-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6612-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6612-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f6612-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f6612-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f6612-106">Prerequisites</span></span>
<span data-ttu-id="f6612-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6612-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f6612-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6612-109">Permission type</span></span>|<span data-ttu-id="f6612-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6612-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f6612-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6612-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="f6612-112">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="f6612-112">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="f6612-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f6612-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="f6612-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6612-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f6612-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6612-115">Not supported.</span></span>|
|<span data-ttu-id="f6612-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6612-116">Application</span></span>|<span data-ttu-id="f6612-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6612-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f6612-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6612-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentTopFailures
```

## <a name="request-headers"></a><span data-ttu-id="f6612-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6612-119">Request headers</span></span>
|<span data-ttu-id="f6612-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6612-120">Header</span></span>|<span data-ttu-id="f6612-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f6612-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f6612-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f6612-122">Authorization</span></span>|<span data-ttu-id="f6612-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f6612-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f6612-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f6612-124">Accept</span></span>|<span data-ttu-id="f6612-125">application/json</span><span class="sxs-lookup"><span data-stu-id="f6612-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f6612-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6612-126">Request body</span></span>
<span data-ttu-id="f6612-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="f6612-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="f6612-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="f6612-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="f6612-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6612-129">Property</span></span>|<span data-ttu-id="f6612-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6612-130">Type</span></span>|<span data-ttu-id="f6612-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6612-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6612-132">period</span><span class="sxs-lookup"><span data-stu-id="f6612-132">period</span></span>|<span data-ttu-id="f6612-133">String</span><span class="sxs-lookup"><span data-stu-id="f6612-133">String</span></span>|<span data-ttu-id="f6612-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f6612-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="f6612-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6612-135">Response</span></span>
<span data-ttu-id="f6612-136">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6612-136">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f6612-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6612-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="f6612-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6612-138">Request</span></span>
<span data-ttu-id="f6612-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6612-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentTopFailures(period='parameterValue')
```

### <a name="response"></a><span data-ttu-id="f6612-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6612-140">Response</span></span>
<span data-ttu-id="f6612-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f6612-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



