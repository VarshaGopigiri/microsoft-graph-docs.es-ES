---
title: Crear windowsAutopilotDeploymentProfileAssignment
description: Crear un nuevo objeto windowsAutopilotDeploymentProfileAssignment.
author: tfitzmac
ms.openlocfilehash: c73cd0c8f32ea5b5e84afb5873700a6523186059
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338853"
---
# <a name="create-windowsautopilotdeploymentprofileassignment"></a><span data-ttu-id="3f985-103">Crear windowsAutopilotDeploymentProfileAssignment</span><span class="sxs-lookup"><span data-stu-id="3f985-103">Create windowsAutopilotDeploymentProfileAssignment</span></span>

> <span data-ttu-id="3f985-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f985-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f985-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f985-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3f985-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3f985-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3f985-107">Crear un nuevo objeto [windowsAutopilotDeploymentProfileAssignment](../resources/intune-enrollment-windowsautopilotdeploymentprofileassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="3f985-107">Create a new [windowsAutopilotDeploymentProfileAssignment](../resources/intune-enrollment-windowsautopilotdeploymentprofileassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3f985-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3f985-108">Prerequisites</span></span>
<span data-ttu-id="3f985-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f985-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f985-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f985-111">Permission type</span></span>|<span data-ttu-id="3f985-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f985-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3f985-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f985-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3f985-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f985-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="3f985-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f985-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3f985-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f985-116">Not supported.</span></span>|
|<span data-ttu-id="3f985-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f985-117">Application</span></span>|<span data-ttu-id="3f985-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f985-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3f985-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f985-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignments
```

## <a name="request-headers"></a><span data-ttu-id="3f985-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f985-120">Request headers</span></span>
|<span data-ttu-id="3f985-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f985-121">Header</span></span>|<span data-ttu-id="3f985-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3f985-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3f985-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3f985-123">Authorization</span></span>|<span data-ttu-id="3f985-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3f985-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3f985-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3f985-125">Accept</span></span>|<span data-ttu-id="3f985-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3f985-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f985-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f985-127">Request body</span></span>
<span data-ttu-id="3f985-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsAutopilotDeploymentProfileAssignment.</span><span class="sxs-lookup"><span data-stu-id="3f985-128">In the request body, supply a JSON representation for the windowsAutopilotDeploymentProfileAssignment object.</span></span>

<span data-ttu-id="3f985-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsAutopilotDeploymentProfileAssignment.</span><span class="sxs-lookup"><span data-stu-id="3f985-129">The following table shows the properties that are required when you create the windowsAutopilotDeploymentProfileAssignment.</span></span>

|<span data-ttu-id="3f985-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f985-130">Property</span></span>|<span data-ttu-id="3f985-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f985-131">Type</span></span>|<span data-ttu-id="3f985-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f985-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3f985-133">id</span><span class="sxs-lookup"><span data-stu-id="3f985-133">id</span></span>|<span data-ttu-id="3f985-134">String</span><span class="sxs-lookup"><span data-stu-id="3f985-134">String</span></span>|<span data-ttu-id="3f985-135">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="3f985-135">The key of the assignment.</span></span>|
|<span data-ttu-id="3f985-136">target</span><span class="sxs-lookup"><span data-stu-id="3f985-136">target</span></span>|[<span data-ttu-id="3f985-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="3f985-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="3f985-138">El destino de la asignación para el perfil de la implementación piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="3f985-138">The assignment target for the Windows Autopilot deployment profile.</span></span>|



## <a name="response"></a><span data-ttu-id="3f985-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f985-139">Response</span></span>
<span data-ttu-id="3f985-140">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsAutopilotDeploymentProfileAssignment](../resources/intune-enrollment-windowsautopilotdeploymentprofileassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f985-140">If successful, this method returns a `201 Created` response code and a [windowsAutopilotDeploymentProfileAssignment](../resources/intune-enrollment-windowsautopilotdeploymentprofileassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f985-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f985-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="3f985-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f985-142">Request</span></span>
<span data-ttu-id="3f985-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f985-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignments
Content-type: application/json
Content-length: 183

{
  "@odata.type": "#microsoft.graph.windowsAutopilotDeploymentProfileAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="3f985-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f985-144">Response</span></span>
<span data-ttu-id="3f985-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f985-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 232

{
  "@odata.type": "#microsoft.graph.windowsAutopilotDeploymentProfileAssignment",
  "id": "de7e1e1e-1e1e-de7e-1e1e-7ede1e1e7ede",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





