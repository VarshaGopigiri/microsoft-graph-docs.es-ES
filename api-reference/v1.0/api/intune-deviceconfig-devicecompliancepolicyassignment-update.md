---
title: Actualizar deviceCompliancePolicyAssignment
description: Actualice las propiedades de un objeto deviceCompliancePolicyAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 31fb66288f2c7706115b9d1ab52efa652b0b98ec
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968648"
---
# <a name="update-devicecompliancepolicyassignment"></a><span data-ttu-id="38941-103">Actualizar deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="38941-103">Update deviceCompliancePolicyAssignment</span></span>

> <span data-ttu-id="38941-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="38941-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="38941-105">Actualice las propiedades de un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="38941-105">Update the properties of a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="38941-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="38941-106">Prerequisites</span></span>
<span data-ttu-id="38941-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38941-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38941-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38941-109">Permission type</span></span>|<span data-ttu-id="38941-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38941-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="38941-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38941-111">Delegated (work or school account)</span></span>|<span data-ttu-id="38941-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="38941-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="38941-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38941-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="38941-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38941-114">Not supported.</span></span>|
|<span data-ttu-id="38941-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38941-115">Application</span></span>|<span data-ttu-id="38941-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38941-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="38941-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38941-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments/{deviceCompliancePolicyAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="38941-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38941-118">Request headers</span></span>
|<span data-ttu-id="38941-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38941-119">Header</span></span>|<span data-ttu-id="38941-120">Valor</span><span class="sxs-lookup"><span data-stu-id="38941-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="38941-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="38941-121">Authorization</span></span>|<span data-ttu-id="38941-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="38941-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="38941-123">Accept</span><span class="sxs-lookup"><span data-stu-id="38941-123">Accept</span></span>|<span data-ttu-id="38941-124">application/json</span><span class="sxs-lookup"><span data-stu-id="38941-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="38941-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38941-125">Request body</span></span>
<span data-ttu-id="38941-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="38941-126">In the request body, supply a JSON representation for the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>

<span data-ttu-id="38941-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="38941-127">The following table shows the properties that are required when you create the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span></span>

|<span data-ttu-id="38941-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38941-128">Property</span></span>|<span data-ttu-id="38941-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="38941-129">Type</span></span>|<span data-ttu-id="38941-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="38941-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="38941-131">id</span><span class="sxs-lookup"><span data-stu-id="38941-131">id</span></span>|<span data-ttu-id="38941-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="38941-132">String</span></span>|<span data-ttu-id="38941-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="38941-133">Key of the entity.</span></span>|
|<span data-ttu-id="38941-134">target</span><span class="sxs-lookup"><span data-stu-id="38941-134">target</span></span>|[<span data-ttu-id="38941-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="38941-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="38941-136">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="38941-136">Target for the compliance policy assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="38941-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38941-137">Response</span></span>
<span data-ttu-id="38941-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38941-138">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38941-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38941-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="38941-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38941-140">Request</span></span>
<span data-ttu-id="38941-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38941-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments/{deviceCompliancePolicyAssignmentId}
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="38941-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38941-142">Response</span></span>
<span data-ttu-id="38941-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38941-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "id": "92dc3fef-3fef-92dc-ef3f-dc92ef3fdc92",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



