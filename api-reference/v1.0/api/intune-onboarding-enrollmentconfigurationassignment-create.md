---
title: Crear enrollmentConfigurationAssignment
description: Cree un objeto enrollmentConfigurationAssignment.
author: tfitzmac
ms.openlocfilehash: e2677c6a1ecabe71a0ff46c8e11e2e8d4515f786
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301620"
---
# <a name="create-enrollmentconfigurationassignment"></a><span data-ttu-id="b3d92-103">Crear enrollmentConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b3d92-103">Create enrollmentConfigurationAssignment</span></span>

> <span data-ttu-id="b3d92-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3d92-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3d92-105">Cree un objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b3d92-105">Create a new [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b3d92-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b3d92-106">Prerequisites</span></span>
<span data-ttu-id="b3d92-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3d92-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b3d92-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3d92-109">Permission type</span></span>|<span data-ttu-id="b3d92-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3d92-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b3d92-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3d92-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b3d92-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b3d92-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="b3d92-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3d92-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b3d92-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3d92-114">Not supported.</span></span>|
|<span data-ttu-id="b3d92-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3d92-115">Application</span></span>|<span data-ttu-id="b3d92-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3d92-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b3d92-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3d92-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="b3d92-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3d92-118">Request headers</span></span>
|<span data-ttu-id="b3d92-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3d92-119">Header</span></span>|<span data-ttu-id="b3d92-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b3d92-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b3d92-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b3d92-121">Authorization</span></span>|<span data-ttu-id="b3d92-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b3d92-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b3d92-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b3d92-123">Accept</span></span>|<span data-ttu-id="b3d92-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b3d92-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b3d92-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3d92-125">Request body</span></span>
<span data-ttu-id="b3d92-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto enrollmentConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="b3d92-126">In the request body, supply a JSON representation for the enrollmentConfigurationAssignment object.</span></span>

<span data-ttu-id="b3d92-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto enrollmentConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="b3d92-127">The following table shows the properties that are required when you create the enrollmentConfigurationAssignment.</span></span>

|<span data-ttu-id="b3d92-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3d92-128">Property</span></span>|<span data-ttu-id="b3d92-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3d92-129">Type</span></span>|<span data-ttu-id="b3d92-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3d92-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b3d92-131">id</span><span class="sxs-lookup"><span data-stu-id="b3d92-131">id</span></span>|<span data-ttu-id="b3d92-132">String</span><span class="sxs-lookup"><span data-stu-id="b3d92-132">String</span></span>|<span data-ttu-id="b3d92-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b3d92-133">Not yet documented</span></span>|
|<span data-ttu-id="b3d92-134">target</span><span class="sxs-lookup"><span data-stu-id="b3d92-134">target</span></span>|[<span data-ttu-id="b3d92-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="b3d92-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="b3d92-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b3d92-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="b3d92-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3d92-137">Response</span></span>
<span data-ttu-id="b3d92-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3d92-138">If successful, this method returns a `201 Created` response code and a [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3d92-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3d92-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="b3d92-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3d92-140">Request</span></span>
<span data-ttu-id="b3d92-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3d92-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
Content-type: application/json
Content-length: 173

{
  "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="b3d92-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3d92-142">Response</span></span>
<span data-ttu-id="b3d92-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b3d92-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 222

{
  "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
  "id": "705b021c-021c-705b-1c02-5b701c025b70",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



