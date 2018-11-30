---
title: managedDeviceEnrollmentFailureTrends (función)
description: Metadatos para el informe de tendencias de errores de inscripción
ms.openlocfilehash: bebbebfff3b37ef940e55583e859736f6caf92cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090886"
---
# <a name="manageddeviceenrollmentfailuretrends-function"></a><span data-ttu-id="eea87-103">managedDeviceEnrollmentFailureTrends (función)</span><span class="sxs-lookup"><span data-stu-id="eea87-103">managedDeviceEnrollmentFailureTrends function</span></span>

> <span data-ttu-id="eea87-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eea87-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eea87-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eea87-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eea87-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eea87-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eea87-107">Metadatos para el informe de tendencias de errores de inscripción</span><span class="sxs-lookup"><span data-stu-id="eea87-107">Metadata for the enrollment failure trends report</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eea87-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eea87-108">Prerequisites</span></span>
<span data-ttu-id="eea87-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eea87-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eea87-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eea87-111">Permission type</span></span>|<span data-ttu-id="eea87-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eea87-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eea87-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eea87-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="eea87-114">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="eea87-114">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="eea87-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eea87-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="eea87-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eea87-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eea87-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eea87-117">Not supported.</span></span>|
|<span data-ttu-id="eea87-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eea87-118">Application</span></span>|<span data-ttu-id="eea87-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eea87-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eea87-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eea87-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentFailureTrends
```

## <a name="request-headers"></a><span data-ttu-id="eea87-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eea87-121">Request headers</span></span>
|<span data-ttu-id="eea87-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eea87-122">Header</span></span>|<span data-ttu-id="eea87-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eea87-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eea87-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="eea87-124">Authorization</span></span>|<span data-ttu-id="eea87-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eea87-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eea87-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eea87-126">Accept</span></span>|<span data-ttu-id="eea87-127">application/json</span><span class="sxs-lookup"><span data-stu-id="eea87-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eea87-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eea87-128">Request body</span></span>
<span data-ttu-id="eea87-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eea87-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eea87-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eea87-130">Response</span></span>
<span data-ttu-id="eea87-131">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eea87-131">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eea87-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eea87-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="eea87-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eea87-133">Request</span></span>
<span data-ttu-id="eea87-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eea87-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports/managedDeviceEnrollmentFailureTrends
```

### <a name="response"></a><span data-ttu-id="eea87-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eea87-135">Response</span></span>
<span data-ttu-id="eea87-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eea87-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



