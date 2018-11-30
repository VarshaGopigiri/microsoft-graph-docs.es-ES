---
title: managedDeviceEnrollmentTopFailures (función)
description: Todavía no documentado
ms.openlocfilehash: 455166ddf0e22fc61ad0fab0d64dd2bcfb547a3e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085381"
---
# <a name="manageddeviceenrollmenttopfailures-function"></a><span data-ttu-id="0b94e-103">managedDeviceEnrollmentTopFailures (función)</span><span class="sxs-lookup"><span data-stu-id="0b94e-103">managedDeviceEnrollmentTopFailures function</span></span>

> <span data-ttu-id="0b94e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b94e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b94e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b94e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0b94e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0b94e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0b94e-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0b94e-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0b94e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0b94e-108">Prerequisites</span></span>
<span data-ttu-id="0b94e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0b94e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0b94e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0b94e-111">Permission type</span></span>|<span data-ttu-id="0b94e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0b94e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0b94e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0b94e-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="0b94e-114">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="0b94e-114">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="0b94e-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b94e-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="0b94e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0b94e-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0b94e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b94e-117">Not supported.</span></span>|
|<span data-ttu-id="0b94e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0b94e-118">Application</span></span>|<span data-ttu-id="0b94e-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b94e-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0b94e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b94e-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentTopFailures
```

## <a name="request-headers"></a><span data-ttu-id="0b94e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b94e-121">Request headers</span></span>
|<span data-ttu-id="0b94e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b94e-122">Header</span></span>|<span data-ttu-id="0b94e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0b94e-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0b94e-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="0b94e-124">Authorization</span></span>|<span data-ttu-id="0b94e-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0b94e-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0b94e-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0b94e-126">Accept</span></span>|<span data-ttu-id="0b94e-127">application/json</span><span class="sxs-lookup"><span data-stu-id="0b94e-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0b94e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0b94e-128">Request body</span></span>
<span data-ttu-id="0b94e-129">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="0b94e-129">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="0b94e-130">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="0b94e-130">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="0b94e-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b94e-131">Property</span></span>|<span data-ttu-id="0b94e-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b94e-132">Type</span></span>|<span data-ttu-id="0b94e-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b94e-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0b94e-134">period</span><span class="sxs-lookup"><span data-stu-id="0b94e-134">period</span></span>|<span data-ttu-id="0b94e-135">String</span><span class="sxs-lookup"><span data-stu-id="0b94e-135">String</span></span>|<span data-ttu-id="0b94e-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0b94e-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="0b94e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b94e-137">Response</span></span>
<span data-ttu-id="0b94e-138">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b94e-138">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0b94e-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b94e-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="0b94e-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0b94e-140">Request</span></span>
<span data-ttu-id="0b94e-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b94e-141">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports/managedDeviceEnrollmentTopFailures(period='parameterValue')
```

### <a name="response"></a><span data-ttu-id="0b94e-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b94e-142">Response</span></span>
<span data-ttu-id="0b94e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0b94e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


