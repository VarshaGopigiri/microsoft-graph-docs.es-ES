---
title: Actualizar managedDeviceMobileAppConfigurationAssignment
description: Actualice las propiedades de un objeto managedDeviceMobileAppConfigurationAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c9098a17def65d4eeeab4638a1b0625c33b04dc7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960794"
---
# <a name="update-manageddevicemobileappconfigurationassignment"></a><span data-ttu-id="2b2f1-103">Actualizar managedDeviceMobileAppConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="2b2f1-103">Update managedDeviceMobileAppConfigurationAssignment</span></span>

> <span data-ttu-id="2b2f1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2b2f1-105">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f1-105">Update the properties of a [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2b2f1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2b2f1-106">Prerequisites</span></span>
<span data-ttu-id="2b2f1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2b2f1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2b2f1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b2f1-109">Permission type</span></span>|<span data-ttu-id="2b2f1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b2f1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2b2f1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b2f1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2b2f1-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2b2f1-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2b2f1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b2f1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2b2f1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-114">Not supported.</span></span>|
|<span data-ttu-id="2b2f1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b2f1-115">Application</span></span>|<span data-ttu-id="2b2f1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2b2f1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b2f1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments/{managedDeviceMobileAppConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="2b2f1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b2f1-118">Request headers</span></span>
|<span data-ttu-id="2b2f1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b2f1-119">Header</span></span>|<span data-ttu-id="2b2f1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2b2f1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2b2f1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2b2f1-121">Authorization</span></span>|<span data-ttu-id="2b2f1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2b2f1-123">Accept</span><span class="sxs-lookup"><span data-stu-id="2b2f1-123">Accept</span></span>|<span data-ttu-id="2b2f1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2b2f1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2b2f1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b2f1-125">Request body</span></span>
<span data-ttu-id="2b2f1-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f1-126">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object.</span></span>

<span data-ttu-id="2b2f1-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f1-127">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span></span>

|<span data-ttu-id="2b2f1-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b2f1-128">Property</span></span>|<span data-ttu-id="2b2f1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b2f1-129">Type</span></span>|<span data-ttu-id="2b2f1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b2f1-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2b2f1-131">id</span><span class="sxs-lookup"><span data-stu-id="2b2f1-131">id</span></span>|<span data-ttu-id="2b2f1-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="2b2f1-132">String</span></span>|<span data-ttu-id="2b2f1-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="2b2f1-134">target</span><span class="sxs-lookup"><span data-stu-id="2b2f1-134">target</span></span>|[<span data-ttu-id="2b2f1-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="2b2f1-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="2b2f1-136">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-136">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="2b2f1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b2f1-137">Response</span></span>
<span data-ttu-id="2b2f1-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-138">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2b2f1-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b2f1-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="2b2f1-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b2f1-140">Request</span></span>
<span data-ttu-id="2b2f1-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments/{managedDeviceMobileAppConfigurationAssignmentId}
Content-type: application/json
Content-length: 185

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="2b2f1-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b2f1-142">Response</span></span>
<span data-ttu-id="2b2f1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b2f1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



