---
title: Función verifyWindowsEnrollmentAutoDiscovery
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6090b0a050a493e26a5536f9f04f7c1e448cca98
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918073"
---
# <a name="verifywindowsenrollmentautodiscovery-function"></a><span data-ttu-id="4c508-103">Función verifyWindowsEnrollmentAutoDiscovery</span><span class="sxs-lookup"><span data-stu-id="4c508-103">verifyWindowsEnrollmentAutoDiscovery function</span></span>

> <span data-ttu-id="4c508-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4c508-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4c508-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c508-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4c508-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4c508-106">Prerequisites</span></span>
<span data-ttu-id="4c508-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c508-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c508-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c508-109">Permission type</span></span>|<span data-ttu-id="4c508-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4c508-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4c508-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c508-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="4c508-112">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="4c508-112">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="4c508-113">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4c508-113">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="4c508-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c508-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4c508-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c508-115">Not supported.</span></span>|
|<span data-ttu-id="4c508-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c508-116">Application</span></span>|<span data-ttu-id="4c508-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c508-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4c508-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c508-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/verifyWindowsEnrollmentAutoDiscovery
```

## <a name="request-headers"></a><span data-ttu-id="4c508-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c508-119">Request headers</span></span>
|<span data-ttu-id="4c508-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c508-120">Header</span></span>|<span data-ttu-id="4c508-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4c508-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4c508-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="4c508-122">Authorization</span></span>|<span data-ttu-id="4c508-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4c508-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4c508-124">Accept</span><span class="sxs-lookup"><span data-stu-id="4c508-124">Accept</span></span>|<span data-ttu-id="4c508-125">application/json</span><span class="sxs-lookup"><span data-stu-id="4c508-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c508-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c508-126">Request body</span></span>
<span data-ttu-id="4c508-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="4c508-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="4c508-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="4c508-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="4c508-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c508-129">Property</span></span>|<span data-ttu-id="4c508-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c508-130">Type</span></span>|<span data-ttu-id="4c508-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c508-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4c508-132">domainName</span><span class="sxs-lookup"><span data-stu-id="4c508-132">domainName</span></span>|<span data-ttu-id="4c508-133">String</span><span class="sxs-lookup"><span data-stu-id="4c508-133">String</span></span>|<span data-ttu-id="4c508-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c508-134">Not yet documented</span></span>|

## <a name="response"></a><span data-ttu-id="4c508-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c508-135">Response</span></span>
<span data-ttu-id="4c508-136">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto Boolean en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c508-136">If successful, this function returns a `200 OK` response code and a Boolean in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c508-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c508-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="4c508-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c508-138">Request</span></span>
<span data-ttu-id="4c508-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c508-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/verifyWindowsEnrollmentAutoDiscovery(domainName='parameterValue')
```

### <a name="response"></a><span data-ttu-id="4c508-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c508-140">Response</span></span>
<span data-ttu-id="4c508-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4c508-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 21

{
  "value": true
}
```



