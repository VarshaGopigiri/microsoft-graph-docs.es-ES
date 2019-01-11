---
title: Enumerar deviceCompliancePolicyAssignments
description: Enumere las propiedades y las relaciones de los objetos deviceCompliancePolicyAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a300fae9d8e6a39557b9da39ca33fdd0aa5c046c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839350"
---
# <a name="list-devicecompliancepolicyassignments"></a><span data-ttu-id="585de-103">Enumerar deviceCompliancePolicyAssignments</span><span class="sxs-lookup"><span data-stu-id="585de-103">List deviceCompliancePolicyAssignments</span></span>

> <span data-ttu-id="585de-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="585de-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="585de-105">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="585de-105">List properties and relationships of the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="585de-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="585de-106">Prerequisites</span></span>
<span data-ttu-id="585de-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="585de-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="585de-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="585de-109">Permission type</span></span>|<span data-ttu-id="585de-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="585de-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="585de-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="585de-111">Delegated (work or school account)</span></span>|<span data-ttu-id="585de-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="585de-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="585de-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="585de-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="585de-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="585de-114">Not supported.</span></span>|
|<span data-ttu-id="585de-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="585de-115">Application</span></span>|<span data-ttu-id="585de-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="585de-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="585de-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="585de-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="585de-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="585de-118">Request headers</span></span>
|<span data-ttu-id="585de-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="585de-119">Header</span></span>|<span data-ttu-id="585de-120">Valor</span><span class="sxs-lookup"><span data-stu-id="585de-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="585de-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="585de-121">Authorization</span></span>|<span data-ttu-id="585de-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="585de-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="585de-123">Accept</span><span class="sxs-lookup"><span data-stu-id="585de-123">Accept</span></span>|<span data-ttu-id="585de-124">application/json</span><span class="sxs-lookup"><span data-stu-id="585de-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="585de-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="585de-125">Request body</span></span>
<span data-ttu-id="585de-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="585de-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="585de-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="585de-127">Response</span></span>
<span data-ttu-id="585de-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="585de-128">If successful, this method returns a `200 OK` response code and a collection of [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="585de-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="585de-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="585de-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="585de-130">Request</span></span>
<span data-ttu-id="585de-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="585de-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

### <a name="response"></a><span data-ttu-id="585de-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="585de-132">Response</span></span>
<span data-ttu-id="585de-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="585de-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



