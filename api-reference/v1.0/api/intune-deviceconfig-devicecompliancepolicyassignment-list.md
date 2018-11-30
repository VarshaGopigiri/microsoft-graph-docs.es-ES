---
title: Enumerar deviceCompliancePolicyAssignments
description: Enumere las propiedades y las relaciones de los objetos deviceCompliancePolicyAssignment.
ms.openlocfilehash: daa23abeef6d55f59c9bc8b51cd44554b221e67f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031962"
---
# <a name="list-devicecompliancepolicyassignments"></a><span data-ttu-id="d8023-103">Enumerar deviceCompliancePolicyAssignments</span><span class="sxs-lookup"><span data-stu-id="d8023-103">List deviceCompliancePolicyAssignments</span></span>

> <span data-ttu-id="d8023-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d8023-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d8023-105">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d8023-105">List properties and relationships of the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d8023-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d8023-106">Prerequisites</span></span>
<span data-ttu-id="d8023-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d8023-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d8023-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d8023-109">Permission type</span></span>|<span data-ttu-id="d8023-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d8023-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d8023-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d8023-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d8023-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="d8023-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="d8023-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d8023-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d8023-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8023-114">Not supported.</span></span>|
|<span data-ttu-id="d8023-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d8023-115">Application</span></span>|<span data-ttu-id="d8023-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8023-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d8023-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d8023-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="d8023-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d8023-118">Request headers</span></span>
|<span data-ttu-id="d8023-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8023-119">Header</span></span>|<span data-ttu-id="d8023-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d8023-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d8023-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d8023-121">Authorization</span></span>|<span data-ttu-id="d8023-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d8023-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d8023-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d8023-123">Accept</span></span>|<span data-ttu-id="d8023-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d8023-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d8023-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d8023-125">Request body</span></span>
<span data-ttu-id="d8023-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d8023-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d8023-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8023-127">Response</span></span>
<span data-ttu-id="d8023-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8023-128">If successful, this method returns a `200 OK` response code and a collection of [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d8023-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8023-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="d8023-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d8023-130">Request</span></span>
<span data-ttu-id="d8023-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8023-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

### <a name="response"></a><span data-ttu-id="d8023-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8023-132">Response</span></span>
<span data-ttu-id="d8023-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d8023-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



