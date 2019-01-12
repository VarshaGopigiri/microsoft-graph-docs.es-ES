---
title: Actualizar deviceManagementScriptGroupAssignment
description: Actualizar las propiedades de un objeto deviceManagementScriptGroupAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d1509b232e77178f6b992772507712cb050a6c06
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990232"
---
# <a name="update-devicemanagementscriptgroupassignment"></a><span data-ttu-id="84acd-103">Actualizar deviceManagementScriptGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="84acd-103">Update deviceManagementScriptGroupAssignment</span></span>

> <span data-ttu-id="84acd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="84acd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="84acd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="84acd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="84acd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84acd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84acd-107">Actualizar las propiedades de un objeto [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="84acd-107">Update the properties of a [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="84acd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="84acd-108">Prerequisites</span></span>
<span data-ttu-id="84acd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="84acd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="84acd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="84acd-111">Permission type</span></span>|<span data-ttu-id="84acd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="84acd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="84acd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="84acd-113">Delegated (work or school account)</span></span>|<span data-ttu-id="84acd-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="84acd-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="84acd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="84acd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="84acd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84acd-116">Not supported.</span></span>|
|<span data-ttu-id="84acd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="84acd-117">Application</span></span>|<span data-ttu-id="84acd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84acd-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="84acd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84acd-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/groupAssignments/{deviceManagementScriptGroupAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="84acd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="84acd-120">Request headers</span></span>
|<span data-ttu-id="84acd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84acd-121">Header</span></span>|<span data-ttu-id="84acd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="84acd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="84acd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="84acd-123">Authorization</span></span>|<span data-ttu-id="84acd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="84acd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="84acd-125">Accept</span><span class="sxs-lookup"><span data-stu-id="84acd-125">Accept</span></span>|<span data-ttu-id="84acd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="84acd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="84acd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="84acd-127">Request body</span></span>
<span data-ttu-id="84acd-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="84acd-128">In the request body, supply a JSON representation for the [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) object.</span></span>

<span data-ttu-id="84acd-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md).</span><span class="sxs-lookup"><span data-stu-id="84acd-129">The following table shows the properties that are required when you create the [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md).</span></span>

|<span data-ttu-id="84acd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84acd-130">Property</span></span>|<span data-ttu-id="84acd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="84acd-131">Type</span></span>|<span data-ttu-id="84acd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="84acd-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84acd-133">id</span><span class="sxs-lookup"><span data-stu-id="84acd-133">id</span></span>|<span data-ttu-id="84acd-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="84acd-134">String</span></span>|<span data-ttu-id="84acd-135">Clave de la entidad de asignación de grupo de secuencia de comandos de dispositivo administración.</span><span class="sxs-lookup"><span data-stu-id="84acd-135">Key of the device management script group assignment entity.</span></span>|
|<span data-ttu-id="84acd-136">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="84acd-136">targetGroupId</span></span>|<span data-ttu-id="84acd-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="84acd-137">String</span></span>|<span data-ttu-id="84acd-138">El identificador de grupo de Active Directory de Azure, nuestro destino son la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="84acd-138">The Id of the Azure Active Directory group we are targeting the script to.</span></span>|



## <a name="response"></a><span data-ttu-id="84acd-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84acd-139">Response</span></span>
<span data-ttu-id="84acd-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="84acd-140">If successful, this method returns a `200 OK` response code and an updated [deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="84acd-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84acd-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="84acd-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="84acd-142">Request</span></span>
<span data-ttu-id="84acd-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84acd-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/groupAssignments/{deviceManagementScriptGroupAssignmentId}
Content-type: application/json
Content-length: 48

{
  "targetGroupId": "Target Group Id value"
}
```

### <a name="response"></a><span data-ttu-id="84acd-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84acd-144">Response</span></span>
<span data-ttu-id="84acd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="84acd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 173

{
  "@odata.type": "#microsoft.graph.deviceManagementScriptGroupAssignment",
  "id": "ecd2357d-357d-ecd2-7d35-d2ec7d35d2ec",
  "targetGroupId": "Target Group Id value"
}
```





