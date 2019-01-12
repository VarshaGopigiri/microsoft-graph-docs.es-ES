---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a3a54693fcb2c689827e41d811cd616d428dc83f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934397"
---
# <a name="assign-action"></a><span data-ttu-id="f55b3-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="f55b3-103">assign action</span></span>

> <span data-ttu-id="f55b3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f55b3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f55b3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f55b3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f55b3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f55b3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f55b3-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f55b3-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f55b3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f55b3-108">Prerequisites</span></span>
<span data-ttu-id="f55b3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f55b3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f55b3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f55b3-111">Permission type</span></span>|<span data-ttu-id="f55b3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f55b3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f55b3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f55b3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f55b3-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f55b3-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="f55b3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f55b3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f55b3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f55b3-116">Not supported.</span></span>|
|<span data-ttu-id="f55b3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f55b3-117">Application</span></span>|<span data-ttu-id="f55b3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f55b3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f55b3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f55b3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="f55b3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f55b3-120">Request headers</span></span>
|<span data-ttu-id="f55b3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f55b3-121">Header</span></span>|<span data-ttu-id="f55b3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f55b3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f55b3-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f55b3-123">Authorization</span></span>|<span data-ttu-id="f55b3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f55b3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f55b3-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f55b3-125">Accept</span></span>|<span data-ttu-id="f55b3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f55b3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f55b3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f55b3-127">Request body</span></span>
<span data-ttu-id="f55b3-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="f55b3-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="f55b3-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="f55b3-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="f55b3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f55b3-130">Property</span></span>|<span data-ttu-id="f55b3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f55b3-131">Type</span></span>|<span data-ttu-id="f55b3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f55b3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f55b3-133">deviceManagementScriptGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="f55b3-133">deviceManagementScriptGroupAssignments</span></span>|<span data-ttu-id="f55b3-134">colección de [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="f55b3-134">[deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) collection</span></span>|<span data-ttu-id="f55b3-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f55b3-135">Not yet documented</span></span>|
|<span data-ttu-id="f55b3-136">deviceManagementScriptAssignments</span><span class="sxs-lookup"><span data-stu-id="f55b3-136">deviceManagementScriptAssignments</span></span>|<span data-ttu-id="f55b3-137">colección de [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)</span><span class="sxs-lookup"><span data-stu-id="f55b3-137">[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) collection</span></span>|<span data-ttu-id="f55b3-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f55b3-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="f55b3-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f55b3-139">Response</span></span>
<span data-ttu-id="f55b3-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f55b3-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f55b3-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f55b3-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="f55b3-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f55b3-142">Request</span></span>
<span data-ttu-id="f55b3-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f55b3-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/assign

Content-type: application/json
Content-length: 550

{
  "deviceManagementScriptGroupAssignments": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementScriptGroupAssignment",
      "id": "ecd2357d-357d-ecd2-7d35-d2ec7d35d2ec",
      "targetGroupId": "Target Group Id value"
    }
  ],
  "deviceManagementScriptAssignments": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementScriptAssignment",
      "id": "a87a601e-601e-a87a-1e60-7aa81e607aa8",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="f55b3-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f55b3-144">Response</span></span>
<span data-ttu-id="f55b3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f55b3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





