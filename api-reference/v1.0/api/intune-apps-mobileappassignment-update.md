---
title: Actualizar mobileAppAssignment
description: Actualice las propiedades de un objeto mobileAppAssignment.
ms.openlocfilehash: 2fc32dfaee8ca2f8efcc264fef39a20a7d88a77e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032279"
---
# <a name="update-mobileappassignment"></a><span data-ttu-id="e6df5-103">Actualizar mobileAppAssignment</span><span class="sxs-lookup"><span data-stu-id="e6df5-103">Update mobileAppAssignment</span></span>

> <span data-ttu-id="e6df5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6df5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6df5-105">Actualice las propiedades de un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e6df5-105">Update the properties of a [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6df5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6df5-106">Prerequisites</span></span>
<span data-ttu-id="e6df5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6df5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6df5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6df5-109">Permission type</span></span>|<span data-ttu-id="e6df5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6df5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6df5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6df5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e6df5-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6df5-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e6df5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6df5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6df5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6df5-114">Not supported.</span></span>|
|<span data-ttu-id="e6df5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6df5-115">Application</span></span>|<span data-ttu-id="e6df5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6df5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6df5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6df5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/assignments/{mobileAppAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="e6df5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6df5-118">Request headers</span></span>
|<span data-ttu-id="e6df5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6df5-119">Header</span></span>|<span data-ttu-id="e6df5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e6df5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6df5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6df5-121">Authorization</span></span>|<span data-ttu-id="e6df5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6df5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e6df5-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e6df5-123">Accept</span></span>|<span data-ttu-id="e6df5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e6df5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6df5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6df5-125">Request body</span></span>
<span data-ttu-id="e6df5-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e6df5-126">In the request body, supply a JSON representation for the [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object.</span></span>

<span data-ttu-id="e6df5-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e6df5-127">The following table shows the properties that are required when you create the [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span></span>

|<span data-ttu-id="e6df5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6df5-128">Property</span></span>|<span data-ttu-id="e6df5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6df5-129">Type</span></span>|<span data-ttu-id="e6df5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6df5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6df5-131">id</span><span class="sxs-lookup"><span data-stu-id="e6df5-131">id</span></span>|<span data-ttu-id="e6df5-132">String</span><span class="sxs-lookup"><span data-stu-id="e6df5-132">String</span></span>|<span data-ttu-id="e6df5-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e6df5-133">Key of the entity.</span></span>|
|<span data-ttu-id="e6df5-134">objetivo</span><span class="sxs-lookup"><span data-stu-id="e6df5-134">intent</span></span>|[<span data-ttu-id="e6df5-135">installIntent</span><span class="sxs-lookup"><span data-stu-id="e6df5-135">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="e6df5-136">El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="e6df5-136">The install intent defined by the admin. Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|
|<span data-ttu-id="e6df5-137">target</span><span class="sxs-lookup"><span data-stu-id="e6df5-137">target</span></span>|[<span data-ttu-id="e6df5-138">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="e6df5-138">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="e6df5-139">La asignación de grupo de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e6df5-139">The target group assignment defined by the admin.</span></span>|
|<span data-ttu-id="e6df5-140">configuración</span><span class="sxs-lookup"><span data-stu-id="e6df5-140">settings</span></span>|[<span data-ttu-id="e6df5-141">mobileAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="e6df5-141">mobileAppAssignmentSettings</span></span>](../resources/intune-apps-mobileappassignmentsettings.md)|<span data-ttu-id="e6df5-142">La asignación de la configuración para el destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e6df5-142">The settings for target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="e6df5-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6df5-143">Response</span></span>
<span data-ttu-id="e6df5-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6df5-144">If successful, this method returns a `200 OK` response code and an updated [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6df5-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6df5-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6df5-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6df5-146">Request</span></span>
<span data-ttu-id="e6df5-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6df5-147">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/assignments/{mobileAppAssignmentId}
Content-type: application/json
Content-length: 273

{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "intent": "required",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```

### <a name="response"></a><span data-ttu-id="e6df5-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6df5-148">Response</span></span>
<span data-ttu-id="e6df5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6df5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 322

{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "id": "591620b7-20b7-5916-b720-1659b7201659",
  "intent": "required",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```



