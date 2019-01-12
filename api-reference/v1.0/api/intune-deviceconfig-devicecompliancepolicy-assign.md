---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ad8c2097f599dfe3d8beef145efdaeda51b6467b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959940"
---
# <a name="assign-action"></a><span data-ttu-id="223ea-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="223ea-103">assign action</span></span>

> <span data-ttu-id="223ea-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="223ea-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="223ea-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="223ea-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="223ea-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="223ea-106">Prerequisites</span></span>
<span data-ttu-id="223ea-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="223ea-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="223ea-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="223ea-109">Permission type</span></span>|<span data-ttu-id="223ea-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="223ea-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="223ea-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="223ea-111">Delegated (work or school account)</span></span>|<span data-ttu-id="223ea-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="223ea-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="223ea-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="223ea-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="223ea-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="223ea-114">Not supported.</span></span>|
|<span data-ttu-id="223ea-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="223ea-115">Application</span></span>|<span data-ttu-id="223ea-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="223ea-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="223ea-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="223ea-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="223ea-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="223ea-118">Request headers</span></span>
|<span data-ttu-id="223ea-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="223ea-119">Header</span></span>|<span data-ttu-id="223ea-120">Valor</span><span class="sxs-lookup"><span data-stu-id="223ea-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="223ea-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="223ea-121">Authorization</span></span>|<span data-ttu-id="223ea-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="223ea-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="223ea-123">Accept</span><span class="sxs-lookup"><span data-stu-id="223ea-123">Accept</span></span>|<span data-ttu-id="223ea-124">application/json</span><span class="sxs-lookup"><span data-stu-id="223ea-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="223ea-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="223ea-125">Request body</span></span>
<span data-ttu-id="223ea-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="223ea-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="223ea-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="223ea-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="223ea-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="223ea-128">Property</span></span>|<span data-ttu-id="223ea-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="223ea-129">Type</span></span>|<span data-ttu-id="223ea-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="223ea-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="223ea-131">asignaciones</span><span class="sxs-lookup"><span data-stu-id="223ea-131">assignments</span></span>|<span data-ttu-id="223ea-132">Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="223ea-132">[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection</span></span>|<span data-ttu-id="223ea-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="223ea-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="223ea-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="223ea-134">Response</span></span>
<span data-ttu-id="223ea-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y una colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="223ea-135">If successful, this action returns a `200 OK` response code and a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="223ea-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="223ea-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="223ea-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="223ea-137">Request</span></span>
<span data-ttu-id="223ea-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="223ea-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assign

Content-type: application/json
Content-length: 280

{
  "assignments": [
    {
      "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
      "id": "92dc3fef-3fef-92dc-ef3f-dc92ef3fdc92",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="223ea-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="223ea-139">Response</span></span>
<span data-ttu-id="223ea-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="223ea-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 274

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
      "id": "92dc3fef-3fef-92dc-ef3f-dc92ef3fdc92",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```



