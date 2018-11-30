---
title: Actualizar deviceAndAppManagementRoleAssignment
description: Actualice las propiedades de un objeto deviceAndAppManagementRoleAssignment.
ms.openlocfilehash: e5bf6040ce08a62ae557c8f137e0bd14c8b0b9a5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031349"
---
# <a name="update-deviceandappmanagementroleassignment"></a><span data-ttu-id="d4e0d-103">Actualizar deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d4e0d-103">Update deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="d4e0d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d4e0d-105">Actualice las propiedades de un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d4e0d-105">Update the properties of a [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d4e0d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d4e0d-106">Prerequisites</span></span>
<span data-ttu-id="d4e0d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d4e0d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d4e0d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4e0d-109">Permission type</span></span>|<span data-ttu-id="d4e0d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4e0d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d4e0d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4e0d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d4e0d-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4e0d-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="d4e0d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4e0d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d4e0d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-114">Not supported.</span></span>|
|<span data-ttu-id="d4e0d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4e0d-115">Application</span></span>|<span data-ttu-id="d4e0d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d4e0d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4e0d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="d4e0d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d4e0d-118">Request headers</span></span>
|<span data-ttu-id="d4e0d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4e0d-119">Header</span></span>|<span data-ttu-id="d4e0d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d4e0d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d4e0d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d4e0d-121">Authorization</span></span>|<span data-ttu-id="d4e0d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d4e0d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d4e0d-123">Accept</span></span>|<span data-ttu-id="d4e0d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d4e0d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d4e0d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d4e0d-125">Request body</span></span>
<span data-ttu-id="d4e0d-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d4e0d-126">In the request body, supply a JSON representation for the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>

<span data-ttu-id="d4e0d-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d4e0d-127">The following table shows the properties that are required when you create the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span></span>

|<span data-ttu-id="d4e0d-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4e0d-128">Property</span></span>|<span data-ttu-id="d4e0d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4e0d-129">Type</span></span>|<span data-ttu-id="d4e0d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4e0d-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d4e0d-131">id</span><span class="sxs-lookup"><span data-stu-id="d4e0d-131">id</span></span>|<span data-ttu-id="d4e0d-132">String</span><span class="sxs-lookup"><span data-stu-id="d4e0d-132">String</span></span>|<span data-ttu-id="d4e0d-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-133">Key of the entity.</span></span> <span data-ttu-id="d4e0d-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-134">This is read-only and automatically generated.</span></span> <span data-ttu-id="d4e0d-135">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d4e0d-135">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d4e0d-136">displayName</span><span class="sxs-lookup"><span data-stu-id="d4e0d-136">displayName</span></span>|<span data-ttu-id="d4e0d-137">String</span><span class="sxs-lookup"><span data-stu-id="d4e0d-137">String</span></span>|<span data-ttu-id="d4e0d-138">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-138">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="d4e0d-139">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d4e0d-139">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d4e0d-140">descripción</span><span class="sxs-lookup"><span data-stu-id="d4e0d-140">description</span></span>|<span data-ttu-id="d4e0d-141">String</span><span class="sxs-lookup"><span data-stu-id="d4e0d-141">String</span></span>|<span data-ttu-id="d4e0d-142">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-142">Description of the Role Assignment.</span></span> <span data-ttu-id="d4e0d-143">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d4e0d-143">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d4e0d-144">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="d4e0d-144">resourceScopes</span></span>|<span data-ttu-id="d4e0d-145">Colección string</span><span class="sxs-lookup"><span data-stu-id="d4e0d-145">String collection</span></span>|<span data-ttu-id="d4e0d-146">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-146">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="d4e0d-147">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-147">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="d4e0d-148">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d4e0d-148">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d4e0d-149">members</span><span class="sxs-lookup"><span data-stu-id="d4e0d-149">members</span></span>|<span data-ttu-id="d4e0d-150">Colección string</span><span class="sxs-lookup"><span data-stu-id="d4e0d-150">String collection</span></span>|<span data-ttu-id="d4e0d-151">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-151">The list of ids of role member security groups.</span></span> <span data-ttu-id="d4e0d-152">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-152">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="d4e0d-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4e0d-153">Response</span></span>
<span data-ttu-id="d4e0d-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-154">If successful, this method returns a `200 OK` response code and an updated [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4e0d-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4e0d-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="d4e0d-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d4e0d-156">Request</span></span>
<span data-ttu-id="d4e0d-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
Content-type: application/json
Content-length: 258

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
  "displayName": "Display Name value",
  "description": "Description value",
  "resourceScopes": [
    "Resource Scopes value"
  ],
  "members": [
    "Members value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="d4e0d-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4e0d-158">Response</span></span>
<span data-ttu-id="d4e0d-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d4e0d-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 307

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
  "id": "a12e8ebb-8ebb-a12e-bb8e-2ea1bb8e2ea1",
  "displayName": "Display Name value",
  "description": "Description value",
  "resourceScopes": [
    "Resource Scopes value"
  ],
  "members": [
    "Members value"
  ]
}
```



