---
title: Actualizar deviceConfigurationAssignment
description: Actualice las propiedades de un objeto deviceConfigurationAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c39a50f5cfba40cf4b41f654e75cd84e69b7f8cb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894358"
---
# <a name="update-deviceconfigurationassignment"></a><span data-ttu-id="ac26e-103">Actualizar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ac26e-103">Update deviceConfigurationAssignment</span></span>

> <span data-ttu-id="ac26e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ac26e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ac26e-105">Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ac26e-105">Update the properties of a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ac26e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ac26e-106">Prerequisites</span></span>
<span data-ttu-id="ac26e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ac26e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ac26e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac26e-109">Permission type</span></span>|<span data-ttu-id="ac26e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac26e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ac26e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac26e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ac26e-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ac26e-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ac26e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac26e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ac26e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac26e-114">Not supported.</span></span>|
|<span data-ttu-id="ac26e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac26e-115">Application</span></span>|<span data-ttu-id="ac26e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac26e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ac26e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac26e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="ac26e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac26e-118">Request headers</span></span>
|<span data-ttu-id="ac26e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac26e-119">Header</span></span>|<span data-ttu-id="ac26e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ac26e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ac26e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ac26e-121">Authorization</span></span>|<span data-ttu-id="ac26e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ac26e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ac26e-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ac26e-123">Accept</span></span>|<span data-ttu-id="ac26e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ac26e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ac26e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac26e-125">Request body</span></span>
<span data-ttu-id="ac26e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ac26e-126">In the request body, supply a JSON representation for the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>

<span data-ttu-id="ac26e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ac26e-127">The following table shows the properties that are required when you create the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span></span>

|<span data-ttu-id="ac26e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac26e-128">Property</span></span>|<span data-ttu-id="ac26e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac26e-129">Type</span></span>|<span data-ttu-id="ac26e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac26e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ac26e-131">id</span><span class="sxs-lookup"><span data-stu-id="ac26e-131">id</span></span>|<span data-ttu-id="ac26e-132">String</span><span class="sxs-lookup"><span data-stu-id="ac26e-132">String</span></span>|<span data-ttu-id="ac26e-133">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="ac26e-133">The key of the assignment.</span></span>|
|<span data-ttu-id="ac26e-134">target</span><span class="sxs-lookup"><span data-stu-id="ac26e-134">target</span></span>|[<span data-ttu-id="ac26e-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="ac26e-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="ac26e-136">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac26e-136">The assignment target for the device configuration.</span></span>|



## <a name="response"></a><span data-ttu-id="ac26e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac26e-137">Response</span></span>
<span data-ttu-id="ac26e-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac26e-138">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ac26e-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac26e-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="ac26e-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac26e-140">Request</span></span>
<span data-ttu-id="ac26e-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac26e-141">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ac26e-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac26e-142">Response</span></span>
<span data-ttu-id="ac26e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ac26e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



