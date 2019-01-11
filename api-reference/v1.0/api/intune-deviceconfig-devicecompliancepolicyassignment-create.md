---
title: Crear deviceCompliancePolicyAssignment
description: Cree un objeto deviceCompliancePolicyAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 752d90ce8f98b69e3f7a429880589f74bccaa82b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805008"
---
# <a name="create-devicecompliancepolicyassignment"></a><span data-ttu-id="90e64-103">Crear deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="90e64-103">Create deviceCompliancePolicyAssignment</span></span>

> <span data-ttu-id="90e64-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="90e64-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="90e64-105">Cree un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="90e64-105">Create a new [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="90e64-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="90e64-106">Prerequisites</span></span>
<span data-ttu-id="90e64-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90e64-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90e64-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90e64-109">Permission type</span></span>|<span data-ttu-id="90e64-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90e64-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="90e64-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90e64-111">Delegated (work or school account)</span></span>|<span data-ttu-id="90e64-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="90e64-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="90e64-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90e64-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="90e64-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90e64-114">Not supported.</span></span>|
|<span data-ttu-id="90e64-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90e64-115">Application</span></span>|<span data-ttu-id="90e64-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90e64-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="90e64-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90e64-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="90e64-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90e64-118">Request headers</span></span>
|<span data-ttu-id="90e64-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90e64-119">Header</span></span>|<span data-ttu-id="90e64-120">Valor</span><span class="sxs-lookup"><span data-stu-id="90e64-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="90e64-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="90e64-121">Authorization</span></span>|<span data-ttu-id="90e64-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="90e64-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="90e64-123">Accept</span><span class="sxs-lookup"><span data-stu-id="90e64-123">Accept</span></span>|<span data-ttu-id="90e64-124">application/json</span><span class="sxs-lookup"><span data-stu-id="90e64-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="90e64-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90e64-125">Request body</span></span>
<span data-ttu-id="90e64-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="90e64-126">In the request body, supply a JSON representation for the deviceCompliancePolicyAssignment object.</span></span>

<span data-ttu-id="90e64-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="90e64-127">The following table shows the properties that are required when you create the deviceCompliancePolicyAssignment.</span></span>

|<span data-ttu-id="90e64-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90e64-128">Property</span></span>|<span data-ttu-id="90e64-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="90e64-129">Type</span></span>|<span data-ttu-id="90e64-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="90e64-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="90e64-131">id</span><span class="sxs-lookup"><span data-stu-id="90e64-131">id</span></span>|<span data-ttu-id="90e64-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="90e64-132">String</span></span>|<span data-ttu-id="90e64-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="90e64-133">Key of the entity.</span></span>|
|<span data-ttu-id="90e64-134">target</span><span class="sxs-lookup"><span data-stu-id="90e64-134">target</span></span>|[<span data-ttu-id="90e64-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="90e64-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="90e64-136">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="90e64-136">Target for the compliance policy assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="90e64-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90e64-137">Response</span></span>
<span data-ttu-id="90e64-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90e64-138">If successful, this method returns a `201 Created` response code and a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90e64-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90e64-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="90e64-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90e64-140">Request</span></span>
<span data-ttu-id="90e64-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90e64-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="90e64-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90e64-142">Response</span></span>
<span data-ttu-id="90e64-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90e64-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



