---
title: Crear deviceCompliancePolicyAssignment
description: Cree un objeto deviceCompliancePolicyAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3c181e7362528fe0231e2e744f59ac82d7ee333e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847960"
---
# <a name="create-devicecompliancepolicyassignment"></a><span data-ttu-id="30cb5-103">Crear deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="30cb5-103">Create deviceCompliancePolicyAssignment</span></span>

> <span data-ttu-id="30cb5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30cb5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30cb5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30cb5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="30cb5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="30cb5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="30cb5-107">Cree un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="30cb5-107">Create a new [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="30cb5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="30cb5-108">Prerequisites</span></span>
<span data-ttu-id="30cb5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30cb5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30cb5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30cb5-111">Permission type</span></span>|<span data-ttu-id="30cb5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30cb5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="30cb5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30cb5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="30cb5-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="30cb5-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="30cb5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30cb5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="30cb5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30cb5-116">Not supported.</span></span>|
|<span data-ttu-id="30cb5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30cb5-117">Application</span></span>|<span data-ttu-id="30cb5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30cb5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="30cb5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30cb5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="30cb5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30cb5-120">Request headers</span></span>
|<span data-ttu-id="30cb5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30cb5-121">Header</span></span>|<span data-ttu-id="30cb5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="30cb5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="30cb5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="30cb5-123">Authorization</span></span>|<span data-ttu-id="30cb5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="30cb5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="30cb5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="30cb5-125">Accept</span></span>|<span data-ttu-id="30cb5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="30cb5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="30cb5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30cb5-127">Request body</span></span>
<span data-ttu-id="30cb5-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="30cb5-128">In the request body, supply a JSON representation for the deviceCompliancePolicyAssignment object.</span></span>

<span data-ttu-id="30cb5-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="30cb5-129">The following table shows the properties that are required when you create the deviceCompliancePolicyAssignment.</span></span>

|<span data-ttu-id="30cb5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="30cb5-130">Property</span></span>|<span data-ttu-id="30cb5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="30cb5-131">Type</span></span>|<span data-ttu-id="30cb5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="30cb5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="30cb5-133">id</span><span class="sxs-lookup"><span data-stu-id="30cb5-133">id</span></span>|<span data-ttu-id="30cb5-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="30cb5-134">String</span></span>|<span data-ttu-id="30cb5-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="30cb5-135">Key of the entity.</span></span>|
|<span data-ttu-id="30cb5-136">target</span><span class="sxs-lookup"><span data-stu-id="30cb5-136">target</span></span>|[<span data-ttu-id="30cb5-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="30cb5-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="30cb5-138">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="30cb5-138">Target for the compliance policy assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="30cb5-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30cb5-139">Response</span></span>
<span data-ttu-id="30cb5-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30cb5-140">If successful, this method returns a `201 Created` response code and a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="30cb5-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30cb5-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="30cb5-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30cb5-142">Request</span></span>
<span data-ttu-id="30cb5-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30cb5-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="30cb5-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30cb5-144">Response</span></span>
<span data-ttu-id="30cb5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30cb5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





