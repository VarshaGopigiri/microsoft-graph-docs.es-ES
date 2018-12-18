---
title: Actualizar targetedManagedAppPolicyAssignment
description: Actualice las propiedades de un objeto targetedManagedAppPolicyAssignment.
author: tfitzmac
ms.openlocfilehash: 4c0343d1790cf457dba5a28a999af5cc91eca66c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358929"
---
# <a name="update-targetedmanagedapppolicyassignment"></a><span data-ttu-id="d8817-103">Actualizar targetedManagedAppPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d8817-103">Update targetedManagedAppPolicyAssignment</span></span>

> <span data-ttu-id="d8817-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d8817-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d8817-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d8817-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d8817-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d8817-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d8817-107">Actualice las propiedades de un objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d8817-107">Update the properties of a [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d8817-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d8817-108">Prerequisites</span></span>
<span data-ttu-id="d8817-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d8817-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d8817-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d8817-111">Permission type</span></span>|<span data-ttu-id="d8817-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d8817-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d8817-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d8817-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d8817-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d8817-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d8817-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d8817-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d8817-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8817-116">Not supported.</span></span>|
|<span data-ttu-id="d8817-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d8817-117">Application</span></span>|<span data-ttu-id="d8817-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8817-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d8817-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d8817-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/assignments/{targetedManagedAppPolicyAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="d8817-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d8817-120">Request headers</span></span>
|<span data-ttu-id="d8817-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8817-121">Header</span></span>|<span data-ttu-id="d8817-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d8817-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d8817-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d8817-123">Authorization</span></span>|<span data-ttu-id="d8817-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d8817-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d8817-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d8817-125">Accept</span></span>|<span data-ttu-id="d8817-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d8817-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d8817-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d8817-127">Request body</span></span>
<span data-ttu-id="d8817-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d8817-128">In the request body, supply a JSON representation for the [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object.</span></span>

<span data-ttu-id="d8817-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d8817-129">The following table shows the properties that are required when you create the [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span></span>

|<span data-ttu-id="d8817-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8817-130">Property</span></span>|<span data-ttu-id="d8817-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8817-131">Type</span></span>|<span data-ttu-id="d8817-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8817-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d8817-133">id</span><span class="sxs-lookup"><span data-stu-id="d8817-133">id</span></span>|<span data-ttu-id="d8817-134">String</span><span class="sxs-lookup"><span data-stu-id="d8817-134">String</span></span>|<span data-ttu-id="d8817-135">Id</span><span class="sxs-lookup"><span data-stu-id="d8817-135">Id</span></span>|
|<span data-ttu-id="d8817-136">target</span><span class="sxs-lookup"><span data-stu-id="d8817-136">target</span></span>|[<span data-ttu-id="d8817-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="d8817-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="d8817-138">Identificador para la implementación de un grupo o una aplicación</span><span class="sxs-lookup"><span data-stu-id="d8817-138">Identifier for deployment of a group or app</span></span>|



## <a name="response"></a><span data-ttu-id="d8817-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8817-139">Response</span></span>
<span data-ttu-id="d8817-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8817-140">If successful, this method returns a `200 OK` response code and an updated [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d8817-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8817-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="d8817-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d8817-142">Request</span></span>
<span data-ttu-id="d8817-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8817-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="d8817-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8817-144">Response</span></span>
<span data-ttu-id="d8817-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d8817-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 223

{
  "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
  "id": "8b68c4a6-c4a6-8b68-a6c4-688ba6c4688b",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





