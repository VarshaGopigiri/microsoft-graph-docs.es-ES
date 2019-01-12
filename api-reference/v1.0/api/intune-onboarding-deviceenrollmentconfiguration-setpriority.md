---
title: Acción setPriority
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 405c7094e0513d5162eb2120a73892904dbf8b6d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954739"
---
# <a name="setpriority-action"></a><span data-ttu-id="d021a-103">Acción setPriority</span><span class="sxs-lookup"><span data-stu-id="d021a-103">setPriority action</span></span>

> <span data-ttu-id="d021a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d021a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d021a-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d021a-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d021a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d021a-106">Prerequisites</span></span>
<span data-ttu-id="d021a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d021a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d021a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d021a-109">Permission type</span></span>|<span data-ttu-id="d021a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d021a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d021a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d021a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d021a-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d021a-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="d021a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d021a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d021a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d021a-114">Not supported.</span></span>|
|<span data-ttu-id="d021a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d021a-115">Application</span></span>|<span data-ttu-id="d021a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d021a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d021a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d021a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/setPriority
```

## <a name="request-headers"></a><span data-ttu-id="d021a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d021a-118">Request headers</span></span>
|<span data-ttu-id="d021a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d021a-119">Header</span></span>|<span data-ttu-id="d021a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d021a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d021a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d021a-121">Authorization</span></span>|<span data-ttu-id="d021a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d021a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d021a-123">Accept</span><span class="sxs-lookup"><span data-stu-id="d021a-123">Accept</span></span>|<span data-ttu-id="d021a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d021a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d021a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d021a-125">Request body</span></span>
<span data-ttu-id="d021a-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="d021a-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="d021a-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="d021a-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="d021a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d021a-128">Property</span></span>|<span data-ttu-id="d021a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d021a-129">Type</span></span>|<span data-ttu-id="d021a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d021a-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d021a-131">prioridad</span><span class="sxs-lookup"><span data-stu-id="d021a-131">priority</span></span>|<span data-ttu-id="d021a-132">Int32</span><span class="sxs-lookup"><span data-stu-id="d021a-132">Int32</span></span>|<span data-ttu-id="d021a-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d021a-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="d021a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d021a-134">Response</span></span>
<span data-ttu-id="d021a-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d021a-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="d021a-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d021a-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="d021a-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d021a-137">Request</span></span>
<span data-ttu-id="d021a-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d021a-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/setPriority

Content-type: application/json
Content-length: 21

{
  "priority": 8
}
```

### <a name="response"></a><span data-ttu-id="d021a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d021a-139">Response</span></span>
<span data-ttu-id="d021a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d021a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



