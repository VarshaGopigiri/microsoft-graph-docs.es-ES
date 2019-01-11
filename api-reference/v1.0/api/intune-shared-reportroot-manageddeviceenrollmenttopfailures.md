---
title: managedDeviceEnrollmentTopFailures (función)
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4e9ff98c2ddc55110026153c854d91901ffd2335
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882974"
---
# <a name="manageddeviceenrollmenttopfailures-function"></a><span data-ttu-id="c06cc-103">managedDeviceEnrollmentTopFailures (función)</span><span class="sxs-lookup"><span data-stu-id="c06cc-103">managedDeviceEnrollmentTopFailures function</span></span>

> <span data-ttu-id="c06cc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c06cc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c06cc-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c06cc-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c06cc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c06cc-106">Prerequisites</span></span>
<span data-ttu-id="c06cc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c06cc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c06cc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c06cc-109">Permission type</span></span>|<span data-ttu-id="c06cc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c06cc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c06cc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c06cc-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="c06cc-112">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="c06cc-112">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="c06cc-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c06cc-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="c06cc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c06cc-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c06cc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c06cc-115">Not supported.</span></span>|
|<span data-ttu-id="c06cc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c06cc-116">Application</span></span>|<span data-ttu-id="c06cc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c06cc-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c06cc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c06cc-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentTopFailures
```

## <a name="request-headers"></a><span data-ttu-id="c06cc-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c06cc-119">Request headers</span></span>
|<span data-ttu-id="c06cc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c06cc-120">Header</span></span>|<span data-ttu-id="c06cc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c06cc-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c06cc-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="c06cc-122">Authorization</span></span>|<span data-ttu-id="c06cc-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c06cc-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c06cc-124">Accept</span><span class="sxs-lookup"><span data-stu-id="c06cc-124">Accept</span></span>|<span data-ttu-id="c06cc-125">application/json</span><span class="sxs-lookup"><span data-stu-id="c06cc-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c06cc-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c06cc-126">Request body</span></span>
<span data-ttu-id="c06cc-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="c06cc-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="c06cc-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="c06cc-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="c06cc-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c06cc-129">Property</span></span>|<span data-ttu-id="c06cc-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c06cc-130">Type</span></span>|<span data-ttu-id="c06cc-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="c06cc-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c06cc-132">period</span><span class="sxs-lookup"><span data-stu-id="c06cc-132">period</span></span>|<span data-ttu-id="c06cc-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="c06cc-133">String</span></span>|<span data-ttu-id="c06cc-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c06cc-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="c06cc-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c06cc-135">Response</span></span>
<span data-ttu-id="c06cc-136">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c06cc-136">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c06cc-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c06cc-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="c06cc-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c06cc-138">Request</span></span>
<span data-ttu-id="c06cc-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c06cc-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentTopFailures(period='parameterValue')
```

### <a name="response"></a><span data-ttu-id="c06cc-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c06cc-140">Response</span></span>
<span data-ttu-id="c06cc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c06cc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




