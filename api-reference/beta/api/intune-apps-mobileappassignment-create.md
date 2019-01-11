---
title: Crear mobileAppAssignment
description: Cree un objeto mobileAppAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8ceae2f0bacac3d83532a6aa9b338c32573d6332
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874658"
---
# <a name="create-mobileappassignment"></a><span data-ttu-id="8ca07-103">Crear mobileAppAssignment</span><span class="sxs-lookup"><span data-stu-id="8ca07-103">Create mobileAppAssignment</span></span>

> <span data-ttu-id="8ca07-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ca07-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ca07-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ca07-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8ca07-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ca07-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ca07-107">Cree un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8ca07-107">Create a new [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8ca07-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8ca07-108">Prerequisites</span></span>
<span data-ttu-id="8ca07-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8ca07-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8ca07-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ca07-111">Permission type</span></span>|<span data-ttu-id="8ca07-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ca07-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8ca07-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ca07-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8ca07-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8ca07-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8ca07-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ca07-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8ca07-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ca07-116">Not supported.</span></span>|
|<span data-ttu-id="8ca07-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ca07-117">Application</span></span>|<span data-ttu-id="8ca07-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ca07-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8ca07-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ca07-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="8ca07-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ca07-120">Request headers</span></span>
|<span data-ttu-id="8ca07-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ca07-121">Header</span></span>|<span data-ttu-id="8ca07-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8ca07-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8ca07-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8ca07-123">Authorization</span></span>|<span data-ttu-id="8ca07-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8ca07-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8ca07-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8ca07-125">Accept</span></span>|<span data-ttu-id="8ca07-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8ca07-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8ca07-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ca07-127">Request body</span></span>
<span data-ttu-id="8ca07-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ca07-128">In the request body, supply a JSON representation for the mobileAppAssignment object.</span></span>

<span data-ttu-id="8ca07-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ca07-129">The following table shows the properties that are required when you create the mobileAppAssignment.</span></span>

|<span data-ttu-id="8ca07-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ca07-130">Property</span></span>|<span data-ttu-id="8ca07-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ca07-131">Type</span></span>|<span data-ttu-id="8ca07-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ca07-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8ca07-133">id</span><span class="sxs-lookup"><span data-stu-id="8ca07-133">id</span></span>|<span data-ttu-id="8ca07-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8ca07-134">String</span></span>|<span data-ttu-id="8ca07-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8ca07-135">Key of the entity.</span></span>|
|<span data-ttu-id="8ca07-136">objetivo</span><span class="sxs-lookup"><span data-stu-id="8ca07-136">intent</span></span>|[<span data-ttu-id="8ca07-137">installIntent</span><span class="sxs-lookup"><span data-stu-id="8ca07-137">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="8ca07-138">El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="8ca07-138">The install intent defined by the admin. Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|
|<span data-ttu-id="8ca07-139">target</span><span class="sxs-lookup"><span data-stu-id="8ca07-139">target</span></span>|[<span data-ttu-id="8ca07-140">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="8ca07-140">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="8ca07-141">La asignación de grupo de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="8ca07-141">The target group assignment defined by the admin.</span></span>|
|<span data-ttu-id="8ca07-142">configuración</span><span class="sxs-lookup"><span data-stu-id="8ca07-142">settings</span></span>|[<span data-ttu-id="8ca07-143">mobileAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="8ca07-143">mobileAppAssignmentSettings</span></span>](../resources/intune-apps-mobileappassignmentsettings.md)|<span data-ttu-id="8ca07-144">La asignación de la configuración para el destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="8ca07-144">The settings for target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="8ca07-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ca07-145">Response</span></span>
<span data-ttu-id="8ca07-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ca07-146">If successful, this method returns a `201 Created` response code and a [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8ca07-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ca07-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="8ca07-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ca07-148">Request</span></span>
<span data-ttu-id="8ca07-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ca07-149">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/assignments
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

### <a name="response"></a><span data-ttu-id="8ca07-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ca07-150">Response</span></span>
<span data-ttu-id="8ca07-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ca07-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





