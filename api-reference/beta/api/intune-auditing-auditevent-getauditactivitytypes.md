---
title: Función getAuditActivityTypes
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a0a8087b1a1bb61fcbd414da7d1f72bb33caccf9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823109"
---
# <a name="getauditactivitytypes-function"></a><span data-ttu-id="c475b-103">Función getAuditActivityTypes</span><span class="sxs-lookup"><span data-stu-id="c475b-103">getAuditActivityTypes function</span></span>

> <span data-ttu-id="c475b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c475b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c475b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c475b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c475b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c475b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c475b-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c475b-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c475b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c475b-108">Prerequisites</span></span>
<span data-ttu-id="c475b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c475b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c475b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c475b-111">Permission type</span></span>|<span data-ttu-id="c475b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c475b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c475b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c475b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c475b-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="c475b-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="c475b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c475b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c475b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c475b-116">Not supported.</span></span>|
|<span data-ttu-id="c475b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c475b-117">Application</span></span>|<span data-ttu-id="c475b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c475b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c475b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c475b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents/getAuditActivityTypes
```

## <a name="request-headers"></a><span data-ttu-id="c475b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c475b-120">Request headers</span></span>
|<span data-ttu-id="c475b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c475b-121">Header</span></span>|<span data-ttu-id="c475b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c475b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c475b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="c475b-123">Authorization</span></span>|<span data-ttu-id="c475b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c475b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c475b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="c475b-125">Accept</span></span>|<span data-ttu-id="c475b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c475b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c475b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c475b-127">Request body</span></span>
<span data-ttu-id="c475b-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="c475b-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="c475b-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="c475b-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="c475b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c475b-130">Property</span></span>|<span data-ttu-id="c475b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c475b-131">Type</span></span>|<span data-ttu-id="c475b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c475b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c475b-133">categoría</span><span class="sxs-lookup"><span data-stu-id="c475b-133">category</span></span>|<span data-ttu-id="c475b-134">String</span><span class="sxs-lookup"><span data-stu-id="c475b-134">String</span></span>|<span data-ttu-id="c475b-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c475b-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="c475b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c475b-136">Response</span></span>
<span data-ttu-id="c475b-137">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c475b-137">If successful, this function returns a `200 OK` response code and a String collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c475b-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c475b-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="c475b-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c475b-139">Request</span></span>
<span data-ttu-id="c475b-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c475b-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/auditEvents/getAuditActivityTypes(category='parameterValue')
```

### <a name="response"></a><span data-ttu-id="c475b-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c475b-141">Response</span></span>
<span data-ttu-id="c475b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c475b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





