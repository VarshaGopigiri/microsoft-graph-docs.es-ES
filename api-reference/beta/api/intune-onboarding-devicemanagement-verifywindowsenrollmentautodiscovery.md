---
title: Función verifyWindowsEnrollmentAutoDiscovery
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: c093490b27db844db434b05725e48464d9792cb7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344810"
---
# <a name="verifywindowsenrollmentautodiscovery-function"></a><span data-ttu-id="517d2-103">Función verifyWindowsEnrollmentAutoDiscovery</span><span class="sxs-lookup"><span data-stu-id="517d2-103">verifyWindowsEnrollmentAutoDiscovery function</span></span>

> <span data-ttu-id="517d2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="517d2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="517d2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="517d2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="517d2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="517d2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="517d2-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="517d2-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="517d2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="517d2-108">Prerequisites</span></span>
<span data-ttu-id="517d2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="517d2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="517d2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="517d2-111">Permission type</span></span>|<span data-ttu-id="517d2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="517d2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="517d2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="517d2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="517d2-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="517d2-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="517d2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="517d2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="517d2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="517d2-116">Not supported.</span></span>|
|<span data-ttu-id="517d2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="517d2-117">Application</span></span>|<span data-ttu-id="517d2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="517d2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="517d2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="517d2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/verifyWindowsEnrollmentAutoDiscovery
```

## <a name="request-headers"></a><span data-ttu-id="517d2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="517d2-120">Request headers</span></span>
|<span data-ttu-id="517d2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="517d2-121">Header</span></span>|<span data-ttu-id="517d2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="517d2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="517d2-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="517d2-123">Authorization</span></span>|<span data-ttu-id="517d2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="517d2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="517d2-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="517d2-125">Accept</span></span>|<span data-ttu-id="517d2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="517d2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="517d2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="517d2-127">Request body</span></span>
<span data-ttu-id="517d2-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="517d2-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="517d2-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="517d2-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="517d2-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="517d2-130">Property</span></span>|<span data-ttu-id="517d2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="517d2-131">Type</span></span>|<span data-ttu-id="517d2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="517d2-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="517d2-133">domainName</span><span class="sxs-lookup"><span data-stu-id="517d2-133">domainName</span></span>|<span data-ttu-id="517d2-134">String</span><span class="sxs-lookup"><span data-stu-id="517d2-134">String</span></span>|<span data-ttu-id="517d2-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="517d2-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="517d2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="517d2-136">Response</span></span>
<span data-ttu-id="517d2-137">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto Boolean en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="517d2-137">If successful, this function returns a `200 OK` response code and a Boolean in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="517d2-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="517d2-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="517d2-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="517d2-139">Request</span></span>
<span data-ttu-id="517d2-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="517d2-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/verifyWindowsEnrollmentAutoDiscovery(domainName='parameterValue')
```

### <a name="response"></a><span data-ttu-id="517d2-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="517d2-141">Response</span></span>
<span data-ttu-id="517d2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="517d2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 21

{
  "value": true
}
```





