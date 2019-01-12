---
title: Actualizar deviceCompliancePolicyAssignment
description: Actualice las propiedades de un objeto deviceCompliancePolicyAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2e71f053d48ad4931d5858075409436e72dae12d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938898"
---
# <a name="update-devicecompliancepolicyassignment"></a><span data-ttu-id="e3e8b-103">Actualizar deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e3e8b-103">Update deviceCompliancePolicyAssignment</span></span>

> <span data-ttu-id="e3e8b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e3e8b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e3e8b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e3e8b-107">Actualice las propiedades de un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e3e8b-107">Update the properties of a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e3e8b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e3e8b-108">Prerequisites</span></span>
<span data-ttu-id="e3e8b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3e8b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e3e8b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3e8b-111">Permission type</span></span>|<span data-ttu-id="e3e8b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3e8b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e3e8b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3e8b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e3e8b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3e8b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e3e8b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3e8b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e3e8b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-116">Not supported.</span></span>|
|<span data-ttu-id="e3e8b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3e8b-117">Application</span></span>|<span data-ttu-id="e3e8b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e3e8b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3e8b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments/{deviceCompliancePolicyAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="e3e8b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3e8b-120">Request headers</span></span>
|<span data-ttu-id="e3e8b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3e8b-121">Header</span></span>|<span data-ttu-id="e3e8b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e3e8b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e3e8b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e3e8b-123">Authorization</span></span>|<span data-ttu-id="e3e8b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e3e8b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e3e8b-125">Accept</span></span>|<span data-ttu-id="e3e8b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e3e8b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e3e8b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3e8b-127">Request body</span></span>
<span data-ttu-id="e3e8b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e3e8b-128">In the request body, supply a JSON representation for the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>

<span data-ttu-id="e3e8b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e3e8b-129">The following table shows the properties that are required when you create the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span></span>

|<span data-ttu-id="e3e8b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3e8b-130">Property</span></span>|<span data-ttu-id="e3e8b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3e8b-131">Type</span></span>|<span data-ttu-id="e3e8b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3e8b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e3e8b-133">id</span><span class="sxs-lookup"><span data-stu-id="e3e8b-133">id</span></span>|<span data-ttu-id="e3e8b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e3e8b-134">String</span></span>|<span data-ttu-id="e3e8b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-135">Key of the entity.</span></span>|
|<span data-ttu-id="e3e8b-136">target</span><span class="sxs-lookup"><span data-stu-id="e3e8b-136">target</span></span>|[<span data-ttu-id="e3e8b-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="e3e8b-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="e3e8b-138">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="e3e8b-138">Target for the compliance policy assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="e3e8b-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3e8b-139">Response</span></span>
<span data-ttu-id="e3e8b-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-140">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3e8b-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3e8b-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="e3e8b-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3e8b-142">Request</span></span>
<span data-ttu-id="e3e8b-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments/{deviceCompliancePolicyAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="e3e8b-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3e8b-144">Response</span></span>
<span data-ttu-id="e3e8b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e3e8b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





