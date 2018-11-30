---
title: Función verifyWindowsEnrollmentAutoDiscovery
description: Todavía no documentado
ms.openlocfilehash: ecccb32089a2547d4b130943e9afc8c6d7caebf6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088810"
---
# <a name="verifywindowsenrollmentautodiscovery-function"></a><span data-ttu-id="82660-103">Función verifyWindowsEnrollmentAutoDiscovery</span><span class="sxs-lookup"><span data-stu-id="82660-103">verifyWindowsEnrollmentAutoDiscovery function</span></span>

> <span data-ttu-id="82660-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="82660-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="82660-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="82660-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="82660-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="82660-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82660-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="82660-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="82660-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="82660-108">Prerequisites</span></span>
<span data-ttu-id="82660-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="82660-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="82660-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="82660-111">Permission type</span></span>|<span data-ttu-id="82660-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="82660-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="82660-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="82660-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="82660-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="82660-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="82660-115">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="82660-115">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="82660-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="82660-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="82660-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82660-117">Not supported.</span></span>|
|<span data-ttu-id="82660-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="82660-118">Application</span></span>|<span data-ttu-id="82660-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82660-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="82660-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="82660-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/verifyWindowsEnrollmentAutoDiscovery
```

## <a name="request-headers"></a><span data-ttu-id="82660-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="82660-121">Request headers</span></span>
|<span data-ttu-id="82660-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82660-122">Header</span></span>|<span data-ttu-id="82660-123">Valor</span><span class="sxs-lookup"><span data-stu-id="82660-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="82660-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="82660-124">Authorization</span></span>|<span data-ttu-id="82660-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="82660-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="82660-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="82660-126">Accept</span></span>|<span data-ttu-id="82660-127">application/json</span><span class="sxs-lookup"><span data-stu-id="82660-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="82660-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="82660-128">Request body</span></span>
<span data-ttu-id="82660-129">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="82660-129">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="82660-130">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="82660-130">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="82660-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82660-131">Property</span></span>|<span data-ttu-id="82660-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="82660-132">Type</span></span>|<span data-ttu-id="82660-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="82660-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82660-134">domainName</span><span class="sxs-lookup"><span data-stu-id="82660-134">domainName</span></span>|<span data-ttu-id="82660-135">String</span><span class="sxs-lookup"><span data-stu-id="82660-135">String</span></span>|<span data-ttu-id="82660-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="82660-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="82660-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82660-137">Response</span></span>
<span data-ttu-id="82660-138">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto Boolean en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82660-138">If successful, this function returns a `200 OK` response code and a Boolean in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="82660-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82660-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="82660-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="82660-140">Request</span></span>
<span data-ttu-id="82660-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="82660-141">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/verifyWindowsEnrollmentAutoDiscovery(domainName='parameterValue')
```

### <a name="response"></a><span data-ttu-id="82660-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82660-142">Response</span></span>
<span data-ttu-id="82660-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="82660-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 21

{
  "value": true
}
```



