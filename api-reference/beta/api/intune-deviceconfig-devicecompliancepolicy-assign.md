---
title: asignar acción
description: Todavía no documentado
ms.openlocfilehash: 9cca8b47cd857bce017858d24375b77ea822980d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084255"
---
# <a name="assign-action"></a><span data-ttu-id="45b18-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="45b18-103">assign action</span></span>

> <span data-ttu-id="45b18-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45b18-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45b18-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45b18-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="45b18-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="45b18-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="45b18-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="45b18-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="45b18-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="45b18-108">Prerequisites</span></span>
<span data-ttu-id="45b18-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="45b18-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45b18-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45b18-111">Permission type</span></span>|<span data-ttu-id="45b18-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45b18-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="45b18-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45b18-113">Delegated (work or school account)</span></span>|<span data-ttu-id="45b18-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="45b18-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="45b18-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45b18-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="45b18-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45b18-116">Not supported.</span></span>|
|<span data-ttu-id="45b18-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45b18-117">Application</span></span>|<span data-ttu-id="45b18-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45b18-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="45b18-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45b18-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="45b18-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45b18-120">Request headers</span></span>
|<span data-ttu-id="45b18-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45b18-121">Header</span></span>|<span data-ttu-id="45b18-122">Valor</span><span class="sxs-lookup"><span data-stu-id="45b18-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="45b18-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="45b18-123">Authorization</span></span>|<span data-ttu-id="45b18-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="45b18-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="45b18-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="45b18-125">Accept</span></span>|<span data-ttu-id="45b18-126">application/json</span><span class="sxs-lookup"><span data-stu-id="45b18-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="45b18-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45b18-127">Request body</span></span>
<span data-ttu-id="45b18-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="45b18-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="45b18-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="45b18-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="45b18-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="45b18-130">Property</span></span>|<span data-ttu-id="45b18-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="45b18-131">Type</span></span>|<span data-ttu-id="45b18-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="45b18-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="45b18-133">asignaciones</span><span class="sxs-lookup"><span data-stu-id="45b18-133">assignments</span></span>|<span data-ttu-id="45b18-134">Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="45b18-134">[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection</span></span>|<span data-ttu-id="45b18-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="45b18-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="45b18-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45b18-136">Response</span></span>
<span data-ttu-id="45b18-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y una colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45b18-137">If successful, this action returns a `200 OK` response code and a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="45b18-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45b18-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="45b18-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45b18-139">Request</span></span>
<span data-ttu-id="45b18-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45b18-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assign

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

### <a name="response"></a><span data-ttu-id="45b18-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45b18-141">Response</span></span>
<span data-ttu-id="45b18-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="45b18-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





