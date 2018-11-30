---
title: Función getAuditActivityTypes
description: Todavía no documentado
ms.openlocfilehash: 957ad384cf49ffbd361ed2e8904d66f94b75c8f8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031472"
---
# <a name="getauditactivitytypes-function"></a><span data-ttu-id="a2ce8-103">Función getAuditActivityTypes</span><span class="sxs-lookup"><span data-stu-id="a2ce8-103">getAuditActivityTypes function</span></span>

> <span data-ttu-id="a2ce8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2ce8-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a2ce8-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a2ce8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a2ce8-106">Prerequisites</span></span>
<span data-ttu-id="a2ce8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2ce8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2ce8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2ce8-109">Permission type</span></span>|<span data-ttu-id="a2ce8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2ce8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a2ce8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2ce8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a2ce8-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="a2ce8-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="a2ce8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2ce8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a2ce8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-114">Not supported.</span></span>|
|<span data-ttu-id="a2ce8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2ce8-115">Application</span></span>|<span data-ttu-id="a2ce8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a2ce8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2ce8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents/getAuditActivityTypes
```

## <a name="request-headers"></a><span data-ttu-id="a2ce8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2ce8-118">Request headers</span></span>
|<span data-ttu-id="a2ce8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2ce8-119">Header</span></span>|<span data-ttu-id="a2ce8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ce8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a2ce8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2ce8-121">Authorization</span></span>|<span data-ttu-id="a2ce8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a2ce8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a2ce8-123">Accept</span></span>|<span data-ttu-id="a2ce8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a2ce8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a2ce8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2ce8-125">Request body</span></span>
<span data-ttu-id="a2ce8-126">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-126">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="a2ce8-127">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-127">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="a2ce8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2ce8-128">Property</span></span>|<span data-ttu-id="a2ce8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2ce8-129">Type</span></span>|<span data-ttu-id="a2ce8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2ce8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2ce8-131">categoría</span><span class="sxs-lookup"><span data-stu-id="a2ce8-131">category</span></span>|<span data-ttu-id="a2ce8-132">String</span><span class="sxs-lookup"><span data-stu-id="a2ce8-132">String</span></span>|<span data-ttu-id="a2ce8-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a2ce8-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a2ce8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2ce8-134">Response</span></span>
<span data-ttu-id="a2ce8-135">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-135">If successful, this function returns a `200 OK` response code and a String collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2ce8-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2ce8-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="a2ce8-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2ce8-137">Request</span></span>
<span data-ttu-id="a2ce8-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-138">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/auditEvents/getAuditActivityTypes(category='parameterValue')
```

### <a name="response"></a><span data-ttu-id="a2ce8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2ce8-139">Response</span></span>
<span data-ttu-id="a2ce8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 61

{
  "value": [
    "Get Audit Activity Types value"
  ]
}
```


