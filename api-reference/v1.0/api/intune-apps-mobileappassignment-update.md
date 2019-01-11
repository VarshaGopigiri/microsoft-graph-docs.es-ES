---
title: Actualizar mobileAppAssignment
description: Actualice las propiedades de un objeto mobileAppAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e46df43d27e35d4d9c88a6520761d737b8bf720c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887272"
---
# <a name="update-mobileappassignment"></a><span data-ttu-id="abb96-103">Actualizar mobileAppAssignment</span><span class="sxs-lookup"><span data-stu-id="abb96-103">Update mobileAppAssignment</span></span>

> <span data-ttu-id="abb96-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abb96-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abb96-105">Actualice las propiedades de un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="abb96-105">Update the properties of a [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="abb96-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="abb96-106">Prerequisites</span></span>
<span data-ttu-id="abb96-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="abb96-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="abb96-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="abb96-109">Permission type</span></span>|<span data-ttu-id="abb96-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="abb96-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="abb96-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="abb96-111">Delegated (work or school account)</span></span>|<span data-ttu-id="abb96-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="abb96-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="abb96-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="abb96-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="abb96-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abb96-114">Not supported.</span></span>|
|<span data-ttu-id="abb96-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="abb96-115">Application</span></span>|<span data-ttu-id="abb96-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abb96-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="abb96-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="abb96-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/assignments/{mobileAppAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="abb96-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="abb96-118">Request headers</span></span>
|<span data-ttu-id="abb96-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abb96-119">Header</span></span>|<span data-ttu-id="abb96-120">Valor</span><span class="sxs-lookup"><span data-stu-id="abb96-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="abb96-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="abb96-121">Authorization</span></span>|<span data-ttu-id="abb96-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="abb96-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="abb96-123">Accept</span><span class="sxs-lookup"><span data-stu-id="abb96-123">Accept</span></span>|<span data-ttu-id="abb96-124">application/json</span><span class="sxs-lookup"><span data-stu-id="abb96-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="abb96-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="abb96-125">Request body</span></span>
<span data-ttu-id="abb96-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="abb96-126">In the request body, supply a JSON representation for the [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object.</span></span>

<span data-ttu-id="abb96-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="abb96-127">The following table shows the properties that are required when you create the [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span></span>

|<span data-ttu-id="abb96-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abb96-128">Property</span></span>|<span data-ttu-id="abb96-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="abb96-129">Type</span></span>|<span data-ttu-id="abb96-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="abb96-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abb96-131">id</span><span class="sxs-lookup"><span data-stu-id="abb96-131">id</span></span>|<span data-ttu-id="abb96-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="abb96-132">String</span></span>|<span data-ttu-id="abb96-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="abb96-133">Key of the entity.</span></span>|
|<span data-ttu-id="abb96-134">objetivo</span><span class="sxs-lookup"><span data-stu-id="abb96-134">intent</span></span>|[<span data-ttu-id="abb96-135">installIntent</span><span class="sxs-lookup"><span data-stu-id="abb96-135">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="abb96-136">El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="abb96-136">The install intent defined by the admin. Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|
|<span data-ttu-id="abb96-137">target</span><span class="sxs-lookup"><span data-stu-id="abb96-137">target</span></span>|[<span data-ttu-id="abb96-138">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="abb96-138">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="abb96-139">La asignación de grupo de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="abb96-139">The target group assignment defined by the admin.</span></span>|
|<span data-ttu-id="abb96-140">configuración</span><span class="sxs-lookup"><span data-stu-id="abb96-140">settings</span></span>|[<span data-ttu-id="abb96-141">mobileAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="abb96-141">mobileAppAssignmentSettings</span></span>](../resources/intune-apps-mobileappassignmentsettings.md)|<span data-ttu-id="abb96-142">La asignación de la configuración para el destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="abb96-142">The settings for target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="abb96-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abb96-143">Response</span></span>
<span data-ttu-id="abb96-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abb96-144">If successful, this method returns a `200 OK` response code and an updated [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="abb96-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="abb96-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="abb96-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="abb96-146">Request</span></span>
<span data-ttu-id="abb96-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="abb96-147">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="abb96-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abb96-148">Response</span></span>
<span data-ttu-id="abb96-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="abb96-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



