---
title: Función getAuditActivityTypes
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dd160f62ef79872cb4540cdeb0993f6bc9f91b79
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919459"
---
# <a name="getauditactivitytypes-function"></a><span data-ttu-id="54932-103">Función getAuditActivityTypes</span><span class="sxs-lookup"><span data-stu-id="54932-103">getAuditActivityTypes function</span></span>

> <span data-ttu-id="54932-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="54932-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="54932-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="54932-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="54932-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54932-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54932-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="54932-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54932-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54932-108">Prerequisites</span></span>
<span data-ttu-id="54932-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54932-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="54932-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54932-111">Permission type</span></span>|<span data-ttu-id="54932-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54932-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54932-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54932-113">Delegated (work or school account)</span></span>|<span data-ttu-id="54932-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="54932-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="54932-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54932-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54932-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54932-116">Not supported.</span></span>|
|<span data-ttu-id="54932-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54932-117">Application</span></span>|<span data-ttu-id="54932-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54932-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54932-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54932-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents/getAuditActivityTypes
```

## <a name="request-headers"></a><span data-ttu-id="54932-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54932-120">Request headers</span></span>
|<span data-ttu-id="54932-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54932-121">Header</span></span>|<span data-ttu-id="54932-122">Valor</span><span class="sxs-lookup"><span data-stu-id="54932-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54932-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="54932-123">Authorization</span></span>|<span data-ttu-id="54932-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54932-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54932-125">Accept</span><span class="sxs-lookup"><span data-stu-id="54932-125">Accept</span></span>|<span data-ttu-id="54932-126">application/json</span><span class="sxs-lookup"><span data-stu-id="54932-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54932-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54932-127">Request body</span></span>
<span data-ttu-id="54932-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="54932-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="54932-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="54932-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="54932-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54932-130">Property</span></span>|<span data-ttu-id="54932-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="54932-131">Type</span></span>|<span data-ttu-id="54932-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="54932-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="54932-133">categoría</span><span class="sxs-lookup"><span data-stu-id="54932-133">category</span></span>|<span data-ttu-id="54932-134">String</span><span class="sxs-lookup"><span data-stu-id="54932-134">String</span></span>|<span data-ttu-id="54932-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="54932-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="54932-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54932-136">Response</span></span>
<span data-ttu-id="54932-137">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54932-137">If successful, this function returns a `200 OK` response code and a String collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54932-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54932-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="54932-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54932-139">Request</span></span>
<span data-ttu-id="54932-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54932-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/auditEvents/getAuditActivityTypes(category='parameterValue')
```

### <a name="response"></a><span data-ttu-id="54932-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54932-141">Response</span></span>
<span data-ttu-id="54932-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54932-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





