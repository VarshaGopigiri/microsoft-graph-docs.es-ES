---
title: Crear deviceAndAppManagementRoleAssignment
description: Cree un objeto deviceAndAppManagementRoleAssignment.
ms.openlocfilehash: ec8c641ca9d3d4d4f42cfe71f44bcb6f216be273
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091211"
---
# <a name="create-deviceandappmanagementroleassignment"></a><span data-ttu-id="ebbbe-103">Crear deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ebbbe-103">Create deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="ebbbe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ebbbe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ebbbe-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ebbbe-107">Cree un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ebbbe-107">Create a new [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ebbbe-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ebbbe-108">Prerequisites</span></span>
<span data-ttu-id="ebbbe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ebbbe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ebbbe-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebbbe-111">Permission type</span></span>|<span data-ttu-id="ebbbe-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ebbbe-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ebbbe-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ebbbe-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="ebbbe-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ebbbe-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-116">Not supported.</span></span>|
|<span data-ttu-id="ebbbe-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebbbe-117">Application</span></span>|<span data-ttu-id="ebbbe-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ebbbe-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebbbe-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="ebbbe-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebbbe-120">Request headers</span></span>
|<span data-ttu-id="ebbbe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebbbe-121">Header</span></span>|<span data-ttu-id="ebbbe-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ebbbe-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ebbbe-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ebbbe-123">Authorization</span></span>|<span data-ttu-id="ebbbe-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ebbbe-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ebbbe-125">Accept</span></span>|<span data-ttu-id="ebbbe-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ebbbe-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ebbbe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebbbe-127">Request body</span></span>
<span data-ttu-id="ebbbe-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceAndAppManagementRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-128">In the request body, supply a JSON representation for the deviceAndAppManagementRoleAssignment object.</span></span>

<span data-ttu-id="ebbbe-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceAndAppManagementRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-129">The following table shows the properties that are required when you create the deviceAndAppManagementRoleAssignment.</span></span>

|<span data-ttu-id="ebbbe-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebbbe-130">Property</span></span>|<span data-ttu-id="ebbbe-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebbbe-131">Type</span></span>|<span data-ttu-id="ebbbe-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebbbe-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ebbbe-133">id</span><span class="sxs-lookup"><span data-stu-id="ebbbe-133">id</span></span>|<span data-ttu-id="ebbbe-134">String</span><span class="sxs-lookup"><span data-stu-id="ebbbe-134">String</span></span>|<span data-ttu-id="ebbbe-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-135">Key of the entity.</span></span> <span data-ttu-id="ebbbe-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-136">This is read-only and automatically generated.</span></span> <span data-ttu-id="ebbbe-137">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-137">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="ebbbe-138">displayName</span><span class="sxs-lookup"><span data-stu-id="ebbbe-138">displayName</span></span>|<span data-ttu-id="ebbbe-139">String</span><span class="sxs-lookup"><span data-stu-id="ebbbe-139">String</span></span>|<span data-ttu-id="ebbbe-140">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-140">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="ebbbe-141">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-141">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="ebbbe-142">descripción</span><span class="sxs-lookup"><span data-stu-id="ebbbe-142">description</span></span>|<span data-ttu-id="ebbbe-143">String</span><span class="sxs-lookup"><span data-stu-id="ebbbe-143">String</span></span>|<span data-ttu-id="ebbbe-144">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-144">Description of the Role Assignment.</span></span> <span data-ttu-id="ebbbe-145">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-145">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="ebbbe-146">scopeMembers</span><span class="sxs-lookup"><span data-stu-id="ebbbe-146">scopeMembers</span></span>|<span data-ttu-id="ebbbe-147">Colección string</span><span class="sxs-lookup"><span data-stu-id="ebbbe-147">String collection</span></span>|<span data-ttu-id="ebbbe-148">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-148">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="ebbbe-149">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-149">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="ebbbe-150">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-150">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="ebbbe-151">scopeType</span><span class="sxs-lookup"><span data-stu-id="ebbbe-151">scopeType</span></span>|[<span data-ttu-id="ebbbe-152">roleAssignmentScopeType</span><span class="sxs-lookup"><span data-stu-id="ebbbe-152">roleAssignmentScopeType</span></span>](../resources/intune-rbac-roleassignmentscopetype.md)|<span data-ttu-id="ebbbe-153">Especifica el tipo de ámbito para una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-153">Specifies the type of scope for a Role Assignment.</span></span> <span data-ttu-id="ebbbe-154">El tipo predeterminado 'ResourceScope' permite la asignación de ResourceScopes.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-154">Default type 'ResourceScope' allows assignment of ResourceScopes.</span></span> <span data-ttu-id="ebbbe-155">Para 'AllDevices', 'AllLicensedUsers' y 'AllDevicesAndLicensedUsers', la propiedad ResourceScopes debería dejarse vacía.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-155">For 'AllDevices', 'AllLicensedUsers', and 'AllDevicesAndLicensedUsers', the ResourceScopes property should be left empty.</span></span> <span data-ttu-id="ebbbe-156">Se hereda de [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ebbbe-156">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md).</span></span> <span data-ttu-id="ebbbe-157">Los valores posibles son: `resourceScope`, `allDevices`, `allLicensedUsers` y `allDevicesAndLicensedUsers`.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-157">Possible values are: `resourceScope`, `allDevices`, `allLicensedUsers`, `allDevicesAndLicensedUsers`.</span></span>|
|<span data-ttu-id="ebbbe-158">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="ebbbe-158">resourceScopes</span></span>|<span data-ttu-id="ebbbe-159">Colección string</span><span class="sxs-lookup"><span data-stu-id="ebbbe-159">String collection</span></span>|<span data-ttu-id="ebbbe-160">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-160">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="ebbbe-161">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-161">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="ebbbe-162">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ebbbe-162">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="ebbbe-163">members</span><span class="sxs-lookup"><span data-stu-id="ebbbe-163">members</span></span>|<span data-ttu-id="ebbbe-164">Colección string</span><span class="sxs-lookup"><span data-stu-id="ebbbe-164">String collection</span></span>|<span data-ttu-id="ebbbe-165">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-165">The list of ids of role member security groups.</span></span> <span data-ttu-id="ebbbe-166">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-166">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="ebbbe-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebbbe-167">Response</span></span>
<span data-ttu-id="ebbbe-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-168">If successful, this method returns a `201 Created` response code and a [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ebbbe-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebbbe-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="ebbbe-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebbbe-170">Request</span></span>
<span data-ttu-id="ebbbe-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-171">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/roleAssignments
Content-type: application/json
Content-length: 342

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
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

### <a name="response"></a><span data-ttu-id="ebbbe-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebbbe-172">Response</span></span>
<span data-ttu-id="ebbbe-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ebbbe-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




