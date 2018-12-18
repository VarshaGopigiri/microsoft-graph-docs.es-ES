---
title: managedDeviceEnrollmentTopFailures (función)
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: dd62bffa153d56c279644eeaa99763c4220f27b1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337824"
---
# <a name="manageddeviceenrollmenttopfailures-function"></a><span data-ttu-id="16d65-103">managedDeviceEnrollmentTopFailures (función)</span><span class="sxs-lookup"><span data-stu-id="16d65-103">managedDeviceEnrollmentTopFailures function</span></span>

> <span data-ttu-id="16d65-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16d65-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16d65-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16d65-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="16d65-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16d65-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16d65-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="16d65-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="16d65-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16d65-108">Prerequisites</span></span>
<span data-ttu-id="16d65-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16d65-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16d65-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16d65-111">Permission type</span></span>|<span data-ttu-id="16d65-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16d65-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="16d65-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16d65-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="16d65-114">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="16d65-114">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="16d65-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="16d65-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="16d65-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16d65-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="16d65-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16d65-117">Not supported.</span></span>|
|<span data-ttu-id="16d65-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16d65-118">Application</span></span>|<span data-ttu-id="16d65-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16d65-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="16d65-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16d65-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentTopFailures
```

## <a name="request-headers"></a><span data-ttu-id="16d65-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16d65-121">Request headers</span></span>
|<span data-ttu-id="16d65-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16d65-122">Header</span></span>|<span data-ttu-id="16d65-123">Valor</span><span class="sxs-lookup"><span data-stu-id="16d65-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="16d65-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="16d65-124">Authorization</span></span>|<span data-ttu-id="16d65-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="16d65-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="16d65-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="16d65-126">Accept</span></span>|<span data-ttu-id="16d65-127">application/json</span><span class="sxs-lookup"><span data-stu-id="16d65-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="16d65-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16d65-128">Request body</span></span>
<span data-ttu-id="16d65-129">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="16d65-129">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="16d65-130">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="16d65-130">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="16d65-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16d65-131">Property</span></span>|<span data-ttu-id="16d65-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="16d65-132">Type</span></span>|<span data-ttu-id="16d65-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="16d65-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16d65-134">period</span><span class="sxs-lookup"><span data-stu-id="16d65-134">period</span></span>|<span data-ttu-id="16d65-135">String</span><span class="sxs-lookup"><span data-stu-id="16d65-135">String</span></span>|<span data-ttu-id="16d65-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="16d65-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="16d65-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16d65-137">Response</span></span>
<span data-ttu-id="16d65-138">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16d65-138">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="16d65-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16d65-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="16d65-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16d65-140">Request</span></span>
<span data-ttu-id="16d65-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16d65-141">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports/managedDeviceEnrollmentTopFailures(period='parameterValue')
```

### <a name="response"></a><span data-ttu-id="16d65-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16d65-142">Response</span></span>
<span data-ttu-id="16d65-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16d65-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



