---
title: Función verifyWindowsEnrollmentAutoDiscovery
description: Todavía no documentado
ms.openlocfilehash: bfc4967bb95b5aa76a827e7c8438ac60845d7445
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029625"
---
# <a name="verifywindowsenrollmentautodiscovery-function"></a><span data-ttu-id="3bc45-103">Función verifyWindowsEnrollmentAutoDiscovery</span><span class="sxs-lookup"><span data-stu-id="3bc45-103">verifyWindowsEnrollmentAutoDiscovery function</span></span>

> <span data-ttu-id="3bc45-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3bc45-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3bc45-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3bc45-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3bc45-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3bc45-106">Prerequisites</span></span>
<span data-ttu-id="3bc45-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3bc45-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3bc45-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3bc45-109">Permission type</span></span>|<span data-ttu-id="3bc45-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3bc45-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3bc45-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3bc45-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="3bc45-112">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="3bc45-112">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="3bc45-113">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3bc45-113">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="3bc45-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3bc45-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3bc45-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bc45-115">Not supported.</span></span>|
|<span data-ttu-id="3bc45-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3bc45-116">Application</span></span>|<span data-ttu-id="3bc45-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bc45-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3bc45-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3bc45-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/verifyWindowsEnrollmentAutoDiscovery
```

## <a name="request-headers"></a><span data-ttu-id="3bc45-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3bc45-119">Request headers</span></span>
|<span data-ttu-id="3bc45-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bc45-120">Header</span></span>|<span data-ttu-id="3bc45-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3bc45-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3bc45-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3bc45-122">Authorization</span></span>|<span data-ttu-id="3bc45-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3bc45-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3bc45-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3bc45-124">Accept</span></span>|<span data-ttu-id="3bc45-125">application/json</span><span class="sxs-lookup"><span data-stu-id="3bc45-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3bc45-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3bc45-126">Request body</span></span>
<span data-ttu-id="3bc45-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="3bc45-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="3bc45-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="3bc45-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="3bc45-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3bc45-129">Property</span></span>|<span data-ttu-id="3bc45-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bc45-130">Type</span></span>|<span data-ttu-id="3bc45-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bc45-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3bc45-132">domainName</span><span class="sxs-lookup"><span data-stu-id="3bc45-132">domainName</span></span>|<span data-ttu-id="3bc45-133">String</span><span class="sxs-lookup"><span data-stu-id="3bc45-133">String</span></span>|<span data-ttu-id="3bc45-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3bc45-134">Not yet documented</span></span>|

## <a name="response"></a><span data-ttu-id="3bc45-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bc45-135">Response</span></span>
<span data-ttu-id="3bc45-136">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto Boolean en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3bc45-136">If successful, this function returns a `200 OK` response code and a Boolean in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3bc45-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bc45-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="3bc45-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3bc45-138">Request</span></span>
<span data-ttu-id="3bc45-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3bc45-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/verifyWindowsEnrollmentAutoDiscovery(domainName='parameterValue')
```

### <a name="response"></a><span data-ttu-id="3bc45-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bc45-140">Response</span></span>
<span data-ttu-id="3bc45-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3bc45-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 21

{
  "value": true
}
```



