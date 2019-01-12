---
title: Crear mobileAppAssignment
description: Cree un objeto mobileAppAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0d163d3d13b69cd536ad7ef99a2a9bab54baa366
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987842"
---
# <a name="create-mobileappassignment"></a><span data-ttu-id="89767-103">Crear mobileAppAssignment</span><span class="sxs-lookup"><span data-stu-id="89767-103">Create mobileAppAssignment</span></span>

> <span data-ttu-id="89767-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="89767-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="89767-105">Cree un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="89767-105">Create a new [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="89767-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="89767-106">Prerequisites</span></span>
<span data-ttu-id="89767-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="89767-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="89767-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89767-109">Permission type</span></span>|<span data-ttu-id="89767-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89767-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="89767-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89767-111">Delegated (work or school account)</span></span>|<span data-ttu-id="89767-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="89767-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="89767-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89767-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="89767-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89767-114">Not supported.</span></span>|
|<span data-ttu-id="89767-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89767-115">Application</span></span>|<span data-ttu-id="89767-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89767-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="89767-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89767-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="89767-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89767-118">Request headers</span></span>
|<span data-ttu-id="89767-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89767-119">Header</span></span>|<span data-ttu-id="89767-120">Valor</span><span class="sxs-lookup"><span data-stu-id="89767-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="89767-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="89767-121">Authorization</span></span>|<span data-ttu-id="89767-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="89767-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="89767-123">Accept</span><span class="sxs-lookup"><span data-stu-id="89767-123">Accept</span></span>|<span data-ttu-id="89767-124">application/json</span><span class="sxs-lookup"><span data-stu-id="89767-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="89767-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89767-125">Request body</span></span>
<span data-ttu-id="89767-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppAssignment.</span><span class="sxs-lookup"><span data-stu-id="89767-126">In the request body, supply a JSON representation for the mobileAppAssignment object.</span></span>

<span data-ttu-id="89767-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppAssignment.</span><span class="sxs-lookup"><span data-stu-id="89767-127">The following table shows the properties that are required when you create the mobileAppAssignment.</span></span>

|<span data-ttu-id="89767-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89767-128">Property</span></span>|<span data-ttu-id="89767-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="89767-129">Type</span></span>|<span data-ttu-id="89767-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="89767-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="89767-131">id</span><span class="sxs-lookup"><span data-stu-id="89767-131">id</span></span>|<span data-ttu-id="89767-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="89767-132">String</span></span>|<span data-ttu-id="89767-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="89767-133">Key of the entity.</span></span>|
|<span data-ttu-id="89767-134">objetivo</span><span class="sxs-lookup"><span data-stu-id="89767-134">intent</span></span>|[<span data-ttu-id="89767-135">installIntent</span><span class="sxs-lookup"><span data-stu-id="89767-135">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="89767-136">El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="89767-136">The install intent defined by the admin. Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|
|<span data-ttu-id="89767-137">target</span><span class="sxs-lookup"><span data-stu-id="89767-137">target</span></span>|[<span data-ttu-id="89767-138">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="89767-138">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="89767-139">La asignación de grupo de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="89767-139">The target group assignment defined by the admin.</span></span>|
|<span data-ttu-id="89767-140">configuración</span><span class="sxs-lookup"><span data-stu-id="89767-140">settings</span></span>|[<span data-ttu-id="89767-141">mobileAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="89767-141">mobileAppAssignmentSettings</span></span>](../resources/intune-apps-mobileappassignmentsettings.md)|<span data-ttu-id="89767-142">La asignación de la configuración para el destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="89767-142">The settings for target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="89767-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89767-143">Response</span></span>
<span data-ttu-id="89767-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89767-144">If successful, this method returns a `201 Created` response code and a [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="89767-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89767-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="89767-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89767-146">Request</span></span>
<span data-ttu-id="89767-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89767-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/assignments
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

### <a name="response"></a><span data-ttu-id="89767-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89767-148">Response</span></span>
<span data-ttu-id="89767-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="89767-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



