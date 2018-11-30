---
title: Actualizar enrollmentConfigurationAssignment
description: Actualice las propiedades de un objeto enrollmentConfigurationAssignment.
ms.openlocfilehash: b23b532ae66f3fe4102ad3e03c2ba6e1aff6daa8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089196"
---
# <a name="update-enrollmentconfigurationassignment"></a><span data-ttu-id="4d2d4-103">Actualizar enrollmentConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="4d2d4-103">Update enrollmentConfigurationAssignment</span></span>

> <span data-ttu-id="4d2d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4d2d4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4d2d4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4d2d4-107">Actualice las propiedades de un objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="4d2d4-107">Update the properties of a [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4d2d4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4d2d4-108">Prerequisites</span></span>
<span data-ttu-id="4d2d4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d2d4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4d2d4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d2d4-111">Permission type</span></span>|<span data-ttu-id="4d2d4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d2d4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4d2d4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d2d4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4d2d4-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d2d4-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="4d2d4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d2d4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4d2d4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-116">Not supported.</span></span>|
|<span data-ttu-id="4d2d4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d2d4-117">Application</span></span>|<span data-ttu-id="4d2d4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4d2d4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d2d4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments/{enrollmentConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="4d2d4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2d4-120">Request headers</span></span>
|<span data-ttu-id="4d2d4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d2d4-121">Header</span></span>|<span data-ttu-id="4d2d4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4d2d4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4d2d4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d2d4-123">Authorization</span></span>|<span data-ttu-id="4d2d4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4d2d4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4d2d4-125">Accept</span></span>|<span data-ttu-id="4d2d4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4d2d4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4d2d4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2d4-127">Request body</span></span>
<span data-ttu-id="4d2d4-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="4d2d4-128">In the request body, supply a JSON representation for the [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) object.</span></span>

<span data-ttu-id="4d2d4-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="4d2d4-129">The following table shows the properties that are required when you create the [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).</span></span>

|<span data-ttu-id="4d2d4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d2d4-130">Property</span></span>|<span data-ttu-id="4d2d4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d2d4-131">Type</span></span>|<span data-ttu-id="4d2d4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d2d4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4d2d4-133">id</span><span class="sxs-lookup"><span data-stu-id="4d2d4-133">id</span></span>|<span data-ttu-id="4d2d4-134">String</span><span class="sxs-lookup"><span data-stu-id="4d2d4-134">String</span></span>|<span data-ttu-id="4d2d4-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4d2d4-135">Not yet documented</span></span>|
|<span data-ttu-id="4d2d4-136">target</span><span class="sxs-lookup"><span data-stu-id="4d2d4-136">target</span></span>|[<span data-ttu-id="4d2d4-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="4d2d4-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="4d2d4-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4d2d4-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="4d2d4-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d2d4-139">Response</span></span>
<span data-ttu-id="4d2d4-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-140">If successful, this method returns a `200 OK` response code and an updated [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d2d4-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d2d4-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="4d2d4-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2d4-142">Request</span></span>
<span data-ttu-id="4d2d4-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments/{enrollmentConfigurationAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="4d2d4-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d2d4-144">Response</span></span>
<span data-ttu-id="4d2d4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d2d4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





