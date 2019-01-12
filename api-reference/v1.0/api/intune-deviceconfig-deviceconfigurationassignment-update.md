---
title: Actualizar deviceConfigurationAssignment
description: Actualice las propiedades de un objeto deviceConfigurationAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1b3e2931e791c0d7e57e3a9e47896bf1ac7c64f5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947494"
---
# <a name="update-deviceconfigurationassignment"></a><span data-ttu-id="82cfd-103">Actualizar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="82cfd-103">Update deviceConfigurationAssignment</span></span>

> <span data-ttu-id="82cfd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="82cfd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82cfd-105">Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="82cfd-105">Update the properties of a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="82cfd-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="82cfd-106">Prerequisites</span></span>
<span data-ttu-id="82cfd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="82cfd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="82cfd-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="82cfd-109">Permission type</span></span>|<span data-ttu-id="82cfd-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="82cfd-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="82cfd-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="82cfd-111">Delegated (work or school account)</span></span>|<span data-ttu-id="82cfd-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="82cfd-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="82cfd-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="82cfd-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="82cfd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82cfd-114">Not supported.</span></span>|
|<span data-ttu-id="82cfd-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="82cfd-115">Application</span></span>|<span data-ttu-id="82cfd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82cfd-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="82cfd-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="82cfd-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="82cfd-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="82cfd-118">Request headers</span></span>
|<span data-ttu-id="82cfd-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82cfd-119">Header</span></span>|<span data-ttu-id="82cfd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="82cfd-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="82cfd-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="82cfd-121">Authorization</span></span>|<span data-ttu-id="82cfd-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="82cfd-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="82cfd-123">Accept</span><span class="sxs-lookup"><span data-stu-id="82cfd-123">Accept</span></span>|<span data-ttu-id="82cfd-124">application/json</span><span class="sxs-lookup"><span data-stu-id="82cfd-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="82cfd-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="82cfd-125">Request body</span></span>
<span data-ttu-id="82cfd-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="82cfd-126">In the request body, supply a JSON representation for the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>

<span data-ttu-id="82cfd-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="82cfd-127">The following table shows the properties that are required when you create the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span></span>

|<span data-ttu-id="82cfd-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82cfd-128">Property</span></span>|<span data-ttu-id="82cfd-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="82cfd-129">Type</span></span>|<span data-ttu-id="82cfd-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="82cfd-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82cfd-131">id</span><span class="sxs-lookup"><span data-stu-id="82cfd-131">id</span></span>|<span data-ttu-id="82cfd-132">String</span><span class="sxs-lookup"><span data-stu-id="82cfd-132">String</span></span>|<span data-ttu-id="82cfd-133">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="82cfd-133">The key of the assignment.</span></span>|
|<span data-ttu-id="82cfd-134">target</span><span class="sxs-lookup"><span data-stu-id="82cfd-134">target</span></span>|[<span data-ttu-id="82cfd-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="82cfd-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="82cfd-136">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82cfd-136">The assignment target for the device configuration.</span></span>|



## <a name="response"></a><span data-ttu-id="82cfd-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82cfd-137">Response</span></span>
<span data-ttu-id="82cfd-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82cfd-138">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="82cfd-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82cfd-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="82cfd-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="82cfd-140">Request</span></span>
<span data-ttu-id="82cfd-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="82cfd-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
Content-type: application/json
Content-length: 169

{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="82cfd-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82cfd-142">Response</span></span>
<span data-ttu-id="82cfd-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="82cfd-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 218

{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



