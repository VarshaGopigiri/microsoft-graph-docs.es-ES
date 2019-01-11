---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 29da35a7ea8f3da144543b6064a3252ab58daf95
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819960"
---
# <a name="assign-action"></a><span data-ttu-id="fb27e-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="fb27e-103">assign action</span></span>

> <span data-ttu-id="fb27e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb27e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb27e-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fb27e-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fb27e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fb27e-106">Prerequisites</span></span>
<span data-ttu-id="fb27e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb27e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb27e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb27e-109">Permission type</span></span>|<span data-ttu-id="fb27e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb27e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fb27e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb27e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fb27e-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fb27e-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="fb27e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb27e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fb27e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb27e-114">Not supported.</span></span>|
|<span data-ttu-id="fb27e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb27e-115">Application</span></span>|<span data-ttu-id="fb27e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb27e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fb27e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb27e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="fb27e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb27e-118">Request headers</span></span>
|<span data-ttu-id="fb27e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb27e-119">Header</span></span>|<span data-ttu-id="fb27e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fb27e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fb27e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fb27e-121">Authorization</span></span>|<span data-ttu-id="fb27e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fb27e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fb27e-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fb27e-123">Accept</span></span>|<span data-ttu-id="fb27e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fb27e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fb27e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb27e-125">Request body</span></span>
<span data-ttu-id="fb27e-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb27e-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="fb27e-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="fb27e-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="fb27e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb27e-128">Property</span></span>|<span data-ttu-id="fb27e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb27e-129">Type</span></span>|<span data-ttu-id="fb27e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb27e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb27e-131">asignaciones</span><span class="sxs-lookup"><span data-stu-id="fb27e-131">assignments</span></span>|<span data-ttu-id="fb27e-132">Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="fb27e-132">[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection</span></span>|<span data-ttu-id="fb27e-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fb27e-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="fb27e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb27e-134">Response</span></span>
<span data-ttu-id="fb27e-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y una colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb27e-135">If successful, this action returns a `200 OK` response code and a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb27e-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb27e-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="fb27e-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb27e-137">Request</span></span>
<span data-ttu-id="fb27e-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb27e-138">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="fb27e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb27e-139">Response</span></span>
<span data-ttu-id="fb27e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb27e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



