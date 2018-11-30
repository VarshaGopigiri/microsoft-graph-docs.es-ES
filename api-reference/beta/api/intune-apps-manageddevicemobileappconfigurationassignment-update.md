---
title: Actualizar managedDeviceMobileAppConfigurationAssignment
description: Actualice las propiedades de un objeto managedDeviceMobileAppConfigurationAssignment.
ms.openlocfilehash: 552c4a7e4dc68bfc7f1f4b0fb82173c0fcb16769
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086484"
---
# <a name="update-manageddevicemobileappconfigurationassignment"></a><span data-ttu-id="0e0e8-103">Actualizar managedDeviceMobileAppConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="0e0e8-103">Update managedDeviceMobileAppConfigurationAssignment</span></span>

> <span data-ttu-id="0e0e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0e0e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0e0e8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e0e8-107">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="0e0e8-107">Update the properties of a [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0e0e8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0e0e8-108">Prerequisites</span></span>
<span data-ttu-id="0e0e8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e0e8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e0e8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e0e8-111">Permission type</span></span>|<span data-ttu-id="0e0e8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e0e8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0e0e8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e0e8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0e0e8-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e0e8-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0e0e8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e0e8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0e0e8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-116">Not supported.</span></span>|
|<span data-ttu-id="0e0e8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e0e8-117">Application</span></span>|<span data-ttu-id="0e0e8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0e0e8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e0e8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments/{managedDeviceMobileAppConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="0e0e8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e0e8-120">Request headers</span></span>
|<span data-ttu-id="0e0e8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e0e8-121">Header</span></span>|<span data-ttu-id="0e0e8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0e0e8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0e0e8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e0e8-123">Authorization</span></span>|<span data-ttu-id="0e0e8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0e0e8-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0e0e8-125">Accept</span></span>|<span data-ttu-id="0e0e8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0e0e8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0e0e8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e0e8-127">Request body</span></span>
<span data-ttu-id="0e0e8-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="0e0e8-128">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object.</span></span>

<span data-ttu-id="0e0e8-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="0e0e8-129">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span></span>

|<span data-ttu-id="0e0e8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e0e8-130">Property</span></span>|<span data-ttu-id="0e0e8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e0e8-131">Type</span></span>|<span data-ttu-id="0e0e8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e0e8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e0e8-133">id</span><span class="sxs-lookup"><span data-stu-id="0e0e8-133">id</span></span>|<span data-ttu-id="0e0e8-134">String</span><span class="sxs-lookup"><span data-stu-id="0e0e8-134">String</span></span>|<span data-ttu-id="0e0e8-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="0e0e8-136">target</span><span class="sxs-lookup"><span data-stu-id="0e0e8-136">target</span></span>|[<span data-ttu-id="0e0e8-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="0e0e8-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="0e0e8-138">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-138">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="0e0e8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e0e8-139">Response</span></span>
<span data-ttu-id="0e0e8-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-140">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e0e8-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e0e8-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="0e0e8-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e0e8-142">Request</span></span>
<span data-ttu-id="0e0e8-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments/{managedDeviceMobileAppConfigurationAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="0e0e8-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e0e8-144">Response</span></span>
<span data-ttu-id="0e0e8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 234

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationAssignment",
  "id": "4df81c9c-1c9c-4df8-9c1c-f84d9c1cf84d",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





