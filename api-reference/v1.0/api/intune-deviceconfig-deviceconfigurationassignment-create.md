---
title: Crear deviceConfigurationAssignment
description: Cree un objeto deviceConfigurationAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d81f8f5618b9582b40bfbccbb4c6c0fb50c2c11c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961564"
---
# <a name="create-deviceconfigurationassignment"></a><span data-ttu-id="c1b67-103">Crear deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="c1b67-103">Create deviceConfigurationAssignment</span></span>

> <span data-ttu-id="c1b67-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c1b67-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c1b67-105">Cree un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c1b67-105">Create a new [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c1b67-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c1b67-106">Prerequisites</span></span>
<span data-ttu-id="c1b67-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c1b67-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c1b67-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c1b67-109">Permission type</span></span>|<span data-ttu-id="c1b67-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c1b67-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c1b67-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c1b67-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c1b67-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1b67-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c1b67-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c1b67-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c1b67-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c1b67-114">Not supported.</span></span>|
|<span data-ttu-id="c1b67-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c1b67-115">Application</span></span>|<span data-ttu-id="c1b67-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c1b67-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c1b67-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c1b67-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="c1b67-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c1b67-118">Request headers</span></span>
|<span data-ttu-id="c1b67-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1b67-119">Header</span></span>|<span data-ttu-id="c1b67-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c1b67-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c1b67-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c1b67-121">Authorization</span></span>|<span data-ttu-id="c1b67-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c1b67-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c1b67-123">Accept</span><span class="sxs-lookup"><span data-stu-id="c1b67-123">Accept</span></span>|<span data-ttu-id="c1b67-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c1b67-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c1b67-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c1b67-125">Request body</span></span>
<span data-ttu-id="c1b67-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="c1b67-126">In the request body, supply a JSON representation for the deviceConfigurationAssignment object.</span></span>

<span data-ttu-id="c1b67-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="c1b67-127">The following table shows the properties that are required when you create the deviceConfigurationAssignment.</span></span>

|<span data-ttu-id="c1b67-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c1b67-128">Property</span></span>|<span data-ttu-id="c1b67-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1b67-129">Type</span></span>|<span data-ttu-id="c1b67-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1b67-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c1b67-131">id</span><span class="sxs-lookup"><span data-stu-id="c1b67-131">id</span></span>|<span data-ttu-id="c1b67-132">String</span><span class="sxs-lookup"><span data-stu-id="c1b67-132">String</span></span>|<span data-ttu-id="c1b67-133">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="c1b67-133">The key of the assignment.</span></span>|
|<span data-ttu-id="c1b67-134">target</span><span class="sxs-lookup"><span data-stu-id="c1b67-134">target</span></span>|[<span data-ttu-id="c1b67-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="c1b67-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="c1b67-136">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1b67-136">The assignment target for the device configuration.</span></span>|



## <a name="response"></a><span data-ttu-id="c1b67-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1b67-137">Response</span></span>
<span data-ttu-id="c1b67-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1b67-138">If successful, this method returns a `201 Created` response code and a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c1b67-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c1b67-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="c1b67-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c1b67-140">Request</span></span>
<span data-ttu-id="c1b67-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c1b67-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments
Content-type: application/json
Content-length: 169

{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="c1b67-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1b67-142">Response</span></span>
<span data-ttu-id="c1b67-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c1b67-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



