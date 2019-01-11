---
title: Función verifyWindowsEnrollmentAutoDiscovery
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 144fb484a9d372c2f3173b300274901c9fdc3dd1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823663"
---
# <a name="verifywindowsenrollmentautodiscovery-function"></a><span data-ttu-id="cf81a-103">Función verifyWindowsEnrollmentAutoDiscovery</span><span class="sxs-lookup"><span data-stu-id="cf81a-103">verifyWindowsEnrollmentAutoDiscovery function</span></span>

> <span data-ttu-id="cf81a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cf81a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cf81a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cf81a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cf81a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf81a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf81a-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf81a-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf81a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf81a-108">Prerequisites</span></span>
<span data-ttu-id="cf81a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cf81a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cf81a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf81a-111">Permission type</span></span>|<span data-ttu-id="cf81a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf81a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf81a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf81a-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="cf81a-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="cf81a-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="cf81a-115">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf81a-115">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="cf81a-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf81a-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf81a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf81a-117">Not supported.</span></span>|
|<span data-ttu-id="cf81a-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf81a-118">Application</span></span>|<span data-ttu-id="cf81a-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf81a-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf81a-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf81a-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/verifyWindowsEnrollmentAutoDiscovery
```

## <a name="request-headers"></a><span data-ttu-id="cf81a-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf81a-121">Request headers</span></span>
|<span data-ttu-id="cf81a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf81a-122">Header</span></span>|<span data-ttu-id="cf81a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="cf81a-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf81a-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="cf81a-124">Authorization</span></span>|<span data-ttu-id="cf81a-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf81a-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cf81a-126">Accept</span><span class="sxs-lookup"><span data-stu-id="cf81a-126">Accept</span></span>|<span data-ttu-id="cf81a-127">application/json</span><span class="sxs-lookup"><span data-stu-id="cf81a-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf81a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf81a-128">Request body</span></span>
<span data-ttu-id="cf81a-129">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="cf81a-129">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="cf81a-130">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="cf81a-130">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="cf81a-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf81a-131">Property</span></span>|<span data-ttu-id="cf81a-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf81a-132">Type</span></span>|<span data-ttu-id="cf81a-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf81a-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf81a-134">domainName</span><span class="sxs-lookup"><span data-stu-id="cf81a-134">domainName</span></span>|<span data-ttu-id="cf81a-135">String</span><span class="sxs-lookup"><span data-stu-id="cf81a-135">String</span></span>|<span data-ttu-id="cf81a-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf81a-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="cf81a-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf81a-137">Response</span></span>
<span data-ttu-id="cf81a-138">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto Boolean en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf81a-138">If successful, this function returns a `200 OK` response code and a Boolean in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf81a-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf81a-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf81a-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf81a-140">Request</span></span>
<span data-ttu-id="cf81a-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf81a-141">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/verifyWindowsEnrollmentAutoDiscovery(domainName='parameterValue')
```

### <a name="response"></a><span data-ttu-id="cf81a-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf81a-142">Response</span></span>
<span data-ttu-id="cf81a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf81a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 21

{
  "value": true
}
```



