---
title: Actualizar targetedManagedAppPolicyAssignment
description: Actualice las propiedades de un objeto targetedManagedAppPolicyAssignment.
author: tfitzmac
ms.openlocfilehash: 5dfe8353658b50a827d4e47d99332117eb3dd57e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334765"
---
# <a name="update-targetedmanagedapppolicyassignment"></a><span data-ttu-id="573b4-103">Actualizar targetedManagedAppPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="573b4-103">Update targetedManagedAppPolicyAssignment</span></span>

> <span data-ttu-id="573b4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="573b4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="573b4-105">Actualice las propiedades de un objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="573b4-105">Update the properties of a [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="573b4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="573b4-106">Prerequisites</span></span>
<span data-ttu-id="573b4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="573b4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="573b4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="573b4-109">Permission type</span></span>|<span data-ttu-id="573b4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="573b4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="573b4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="573b4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="573b4-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="573b4-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="573b4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="573b4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="573b4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="573b4-114">Not supported.</span></span>|
|<span data-ttu-id="573b4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="573b4-115">Application</span></span>|<span data-ttu-id="573b4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="573b4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="573b4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="573b4-117">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="573b4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="573b4-118">Request headers</span></span>
|<span data-ttu-id="573b4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="573b4-119">Header</span></span>|<span data-ttu-id="573b4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="573b4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="573b4-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="573b4-121">Authorization</span></span>|<span data-ttu-id="573b4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="573b4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="573b4-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="573b4-123">Accept</span></span>|<span data-ttu-id="573b4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="573b4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="573b4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="573b4-125">Request body</span></span>
<span data-ttu-id="573b4-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="573b4-126">In the request body, supply a JSON representation for the [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object.</span></span>

<span data-ttu-id="573b4-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="573b4-127">The following table shows the properties that are required when you create the [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span></span>

|<span data-ttu-id="573b4-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="573b4-128">Property</span></span>|<span data-ttu-id="573b4-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="573b4-129">Type</span></span>|<span data-ttu-id="573b4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="573b4-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="573b4-131">id</span><span class="sxs-lookup"><span data-stu-id="573b4-131">id</span></span>|<span data-ttu-id="573b4-132">String</span><span class="sxs-lookup"><span data-stu-id="573b4-132">String</span></span>|<span data-ttu-id="573b4-133">Id</span><span class="sxs-lookup"><span data-stu-id="573b4-133">Id</span></span>|
|<span data-ttu-id="573b4-134">target</span><span class="sxs-lookup"><span data-stu-id="573b4-134">target</span></span>|[<span data-ttu-id="573b4-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="573b4-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="573b4-136">Identificador para la implementación de un grupo o una aplicación</span><span class="sxs-lookup"><span data-stu-id="573b4-136">Identifier for deployment of a group or app</span></span>|



## <a name="response"></a><span data-ttu-id="573b4-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="573b4-137">Response</span></span>
<span data-ttu-id="573b4-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="573b4-138">If successful, this method returns a `200 OK` response code and an updated [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="573b4-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="573b4-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="573b4-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="573b4-140">Request</span></span>
<span data-ttu-id="573b4-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="573b4-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
Content-type: application/json
Content-length: 174

{
  "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="573b4-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="573b4-142">Response</span></span>
<span data-ttu-id="573b4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="573b4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



