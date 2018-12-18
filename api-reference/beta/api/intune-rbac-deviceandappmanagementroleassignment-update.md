---
title: Actualizar deviceAndAppManagementRoleAssignment
description: Actualice las propiedades de un objeto deviceAndAppManagementRoleAssignment.
author: tfitzmac
ms.openlocfilehash: 79c7f35a52f7d0d853a77ec4186a957a287ec3ed
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357256"
---
# <a name="update-deviceandappmanagementroleassignment"></a><span data-ttu-id="8046e-103">Actualizar deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8046e-103">Update deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="8046e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8046e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8046e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8046e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8046e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8046e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8046e-107">Actualice las propiedades de un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8046e-107">Update the properties of a [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8046e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8046e-108">Prerequisites</span></span>
<span data-ttu-id="8046e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8046e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8046e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8046e-111">Permission type</span></span>|<span data-ttu-id="8046e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8046e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8046e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8046e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8046e-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8046e-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="8046e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8046e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8046e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8046e-116">Not supported.</span></span>|
|<span data-ttu-id="8046e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8046e-117">Application</span></span>|<span data-ttu-id="8046e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8046e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8046e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8046e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="8046e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8046e-120">Request headers</span></span>
|<span data-ttu-id="8046e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8046e-121">Header</span></span>|<span data-ttu-id="8046e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8046e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8046e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8046e-123">Authorization</span></span>|<span data-ttu-id="8046e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8046e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8046e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8046e-125">Accept</span></span>|<span data-ttu-id="8046e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8046e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8046e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8046e-127">Request body</span></span>
<span data-ttu-id="8046e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8046e-128">In the request body, supply a JSON representation for the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>

<span data-ttu-id="8046e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8046e-129">The following table shows the properties that are required when you create the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span></span>

|<span data-ttu-id="8046e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8046e-130">Property</span></span>|<span data-ttu-id="8046e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8046e-131">Type</span></span>|<span data-ttu-id="8046e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8046e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8046e-133">id</span><span class="sxs-lookup"><span data-stu-id="8046e-133">id</span></span>|<span data-ttu-id="8046e-134">String</span><span class="sxs-lookup"><span data-stu-id="8046e-134">String</span></span>|<span data-ttu-id="8046e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8046e-135">Key of the entity.</span></span> <span data-ttu-id="8046e-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8046e-136">This is read-only and automatically generated.</span></span> <span data-ttu-id="8046e-137">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8046e-137">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="8046e-138">displayName</span><span class="sxs-lookup"><span data-stu-id="8046e-138">displayName</span></span>|<span data-ttu-id="8046e-139">String</span><span class="sxs-lookup"><span data-stu-id="8046e-139">String</span></span>|<span data-ttu-id="8046e-140">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="8046e-140">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="8046e-141">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8046e-141">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="8046e-142">descripción</span><span class="sxs-lookup"><span data-stu-id="8046e-142">description</span></span>|<span data-ttu-id="8046e-143">String</span><span class="sxs-lookup"><span data-stu-id="8046e-143">String</span></span>|<span data-ttu-id="8046e-144">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="8046e-144">Description of the Role Assignment.</span></span> <span data-ttu-id="8046e-145">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8046e-145">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="8046e-146">scopeMembers</span><span class="sxs-lookup"><span data-stu-id="8046e-146">scopeMembers</span></span>|<span data-ttu-id="8046e-147">Colección string</span><span class="sxs-lookup"><span data-stu-id="8046e-147">String collection</span></span>|<span data-ttu-id="8046e-148">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="8046e-148">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="8046e-149">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8046e-149">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="8046e-150">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8046e-150">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="8046e-151">scopeType</span><span class="sxs-lookup"><span data-stu-id="8046e-151">scopeType</span></span>|[<span data-ttu-id="8046e-152">roleAssignmentScopeType</span><span class="sxs-lookup"><span data-stu-id="8046e-152">roleAssignmentScopeType</span></span>](../resources/intune-rbac-roleassignmentscopetype.md)|<span data-ttu-id="8046e-153">Especifica el tipo de ámbito para una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="8046e-153">Specifies the type of scope for a Role Assignment.</span></span> <span data-ttu-id="8046e-154">El tipo predeterminado 'ResourceScope' permite la asignación de ResourceScopes.</span><span class="sxs-lookup"><span data-stu-id="8046e-154">Default type 'ResourceScope' allows assignment of ResourceScopes.</span></span> <span data-ttu-id="8046e-155">Para 'AllDevices', 'AllLicensedUsers' y 'AllDevicesAndLicensedUsers', la propiedad ResourceScopes debería dejarse vacía.</span><span class="sxs-lookup"><span data-stu-id="8046e-155">For 'AllDevices', 'AllLicensedUsers', and 'AllDevicesAndLicensedUsers', the ResourceScopes property should be left empty.</span></span> <span data-ttu-id="8046e-156">Se hereda de [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8046e-156">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md).</span></span> <span data-ttu-id="8046e-157">Los valores posibles son: `resourceScope`, `allDevices`, `allLicensedUsers` y `allDevicesAndLicensedUsers`.</span><span class="sxs-lookup"><span data-stu-id="8046e-157">Possible values are: `resourceScope`, `allDevices`, `allLicensedUsers`, `allDevicesAndLicensedUsers`.</span></span>|
|<span data-ttu-id="8046e-158">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="8046e-158">resourceScopes</span></span>|<span data-ttu-id="8046e-159">Colección string</span><span class="sxs-lookup"><span data-stu-id="8046e-159">String collection</span></span>|<span data-ttu-id="8046e-160">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="8046e-160">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="8046e-161">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8046e-161">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="8046e-162">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8046e-162">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="8046e-163">members</span><span class="sxs-lookup"><span data-stu-id="8046e-163">members</span></span>|<span data-ttu-id="8046e-164">Colección string</span><span class="sxs-lookup"><span data-stu-id="8046e-164">String collection</span></span>|<span data-ttu-id="8046e-165">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="8046e-165">The list of ids of role member security groups.</span></span> <span data-ttu-id="8046e-166">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8046e-166">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="8046e-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8046e-167">Response</span></span>
<span data-ttu-id="8046e-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8046e-168">If successful, this method returns a `200 OK` response code and an updated [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8046e-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8046e-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="8046e-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8046e-170">Request</span></span>
<span data-ttu-id="8046e-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8046e-171">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
Content-type: application/json
Content-length: 267

{
  "displayName": "Display Name value",
  "description": "Description value",
  "scopeMembers": [
    "Scope Members value"
  ],
  "scopeType": "allDevices",
  "resourceScopes": [
    "Resource Scopes value"
  ],
  "members": [
    "Members value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="8046e-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8046e-172">Response</span></span>
<span data-ttu-id="8046e-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8046e-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 391

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
  "id": "a12e8ebb-8ebb-a12e-bb8e-2ea1bb8e2ea1",
  "displayName": "Display Name value",
  "description": "Description value",
  "scopeMembers": [
    "Scope Members value"
  ],
  "scopeType": "allDevices",
  "resourceScopes": [
    "Resource Scopes value"
  ],
  "members": [
    "Members value"
  ]
}
```





