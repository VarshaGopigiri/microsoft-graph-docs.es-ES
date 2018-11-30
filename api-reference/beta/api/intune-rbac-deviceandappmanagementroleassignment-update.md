---
title: Actualizar deviceAndAppManagementRoleAssignment
description: Actualice las propiedades de un objeto deviceAndAppManagementRoleAssignment.
ms.openlocfilehash: 4844d13c21e3371385531d43c1160cf34d7a1a50
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085773"
---
# <a name="update-deviceandappmanagementroleassignment"></a><span data-ttu-id="5fd95-103">Actualizar deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5fd95-103">Update deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="5fd95-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5fd95-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5fd95-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5fd95-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5fd95-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5fd95-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5fd95-107">Actualice las propiedades de un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5fd95-107">Update the properties of a [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5fd95-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5fd95-108">Prerequisites</span></span>
<span data-ttu-id="5fd95-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5fd95-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5fd95-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5fd95-111">Permission type</span></span>|<span data-ttu-id="5fd95-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5fd95-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5fd95-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5fd95-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5fd95-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5fd95-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="5fd95-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5fd95-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5fd95-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5fd95-116">Not supported.</span></span>|
|<span data-ttu-id="5fd95-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5fd95-117">Application</span></span>|<span data-ttu-id="5fd95-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5fd95-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5fd95-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5fd95-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="5fd95-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5fd95-120">Request headers</span></span>
|<span data-ttu-id="5fd95-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fd95-121">Header</span></span>|<span data-ttu-id="5fd95-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd95-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5fd95-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5fd95-123">Authorization</span></span>|<span data-ttu-id="5fd95-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5fd95-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5fd95-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5fd95-125">Accept</span></span>|<span data-ttu-id="5fd95-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5fd95-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5fd95-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5fd95-127">Request body</span></span>
<span data-ttu-id="5fd95-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5fd95-128">In the request body, supply a JSON representation for the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>

<span data-ttu-id="5fd95-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5fd95-129">The following table shows the properties that are required when you create the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span></span>

|<span data-ttu-id="5fd95-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5fd95-130">Property</span></span>|<span data-ttu-id="5fd95-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fd95-131">Type</span></span>|<span data-ttu-id="5fd95-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fd95-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5fd95-133">id</span><span class="sxs-lookup"><span data-stu-id="5fd95-133">id</span></span>|<span data-ttu-id="5fd95-134">String</span><span class="sxs-lookup"><span data-stu-id="5fd95-134">String</span></span>|<span data-ttu-id="5fd95-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5fd95-135">Key of the entity.</span></span> <span data-ttu-id="5fd95-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5fd95-136">This is read-only and automatically generated.</span></span> <span data-ttu-id="5fd95-137">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="5fd95-137">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="5fd95-138">displayName</span><span class="sxs-lookup"><span data-stu-id="5fd95-138">displayName</span></span>|<span data-ttu-id="5fd95-139">String</span><span class="sxs-lookup"><span data-stu-id="5fd95-139">String</span></span>|<span data-ttu-id="5fd95-140">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="5fd95-140">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="5fd95-141">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="5fd95-141">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="5fd95-142">descripción</span><span class="sxs-lookup"><span data-stu-id="5fd95-142">description</span></span>|<span data-ttu-id="5fd95-143">String</span><span class="sxs-lookup"><span data-stu-id="5fd95-143">String</span></span>|<span data-ttu-id="5fd95-144">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="5fd95-144">Description of the Role Assignment.</span></span> <span data-ttu-id="5fd95-145">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="5fd95-145">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="5fd95-146">scopeMembers</span><span class="sxs-lookup"><span data-stu-id="5fd95-146">scopeMembers</span></span>|<span data-ttu-id="5fd95-147">Colección string</span><span class="sxs-lookup"><span data-stu-id="5fd95-147">String collection</span></span>|<span data-ttu-id="5fd95-148">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="5fd95-148">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="5fd95-149">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5fd95-149">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="5fd95-150">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="5fd95-150">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="5fd95-151">scopeType</span><span class="sxs-lookup"><span data-stu-id="5fd95-151">scopeType</span></span>|[<span data-ttu-id="5fd95-152">roleAssignmentScopeType</span><span class="sxs-lookup"><span data-stu-id="5fd95-152">roleAssignmentScopeType</span></span>](../resources/intune-rbac-roleassignmentscopetype.md)|<span data-ttu-id="5fd95-153">Especifica el tipo de ámbito para una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="5fd95-153">Specifies the type of scope for a Role Assignment.</span></span> <span data-ttu-id="5fd95-154">El tipo predeterminado 'ResourceScope' permite la asignación de ResourceScopes.</span><span class="sxs-lookup"><span data-stu-id="5fd95-154">Default type 'ResourceScope' allows assignment of ResourceScopes.</span></span> <span data-ttu-id="5fd95-155">Para 'AllDevices', 'AllLicensedUsers' y 'AllDevicesAndLicensedUsers', la propiedad ResourceScopes debería dejarse vacía.</span><span class="sxs-lookup"><span data-stu-id="5fd95-155">For 'AllDevices', 'AllLicensedUsers', and 'AllDevicesAndLicensedUsers', the ResourceScopes property should be left empty.</span></span> <span data-ttu-id="5fd95-156">Se hereda de [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5fd95-156">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md).</span></span> <span data-ttu-id="5fd95-157">Los valores posibles son: `resourceScope`, `allDevices`, `allLicensedUsers` y `allDevicesAndLicensedUsers`.</span><span class="sxs-lookup"><span data-stu-id="5fd95-157">Possible values are: `resourceScope`, `allDevices`, `allLicensedUsers`, `allDevicesAndLicensedUsers`.</span></span>|
|<span data-ttu-id="5fd95-158">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="5fd95-158">resourceScopes</span></span>|<span data-ttu-id="5fd95-159">Colección string</span><span class="sxs-lookup"><span data-stu-id="5fd95-159">String collection</span></span>|<span data-ttu-id="5fd95-160">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="5fd95-160">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="5fd95-161">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5fd95-161">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="5fd95-162">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="5fd95-162">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="5fd95-163">members</span><span class="sxs-lookup"><span data-stu-id="5fd95-163">members</span></span>|<span data-ttu-id="5fd95-164">Colección string</span><span class="sxs-lookup"><span data-stu-id="5fd95-164">String collection</span></span>|<span data-ttu-id="5fd95-165">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="5fd95-165">The list of ids of role member security groups.</span></span> <span data-ttu-id="5fd95-166">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5fd95-166">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="5fd95-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fd95-167">Response</span></span>
<span data-ttu-id="5fd95-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5fd95-168">If successful, this method returns a `200 OK` response code and an updated [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5fd95-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5fd95-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="5fd95-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5fd95-170">Request</span></span>
<span data-ttu-id="5fd95-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5fd95-171">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="5fd95-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fd95-172">Response</span></span>
<span data-ttu-id="5fd95-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5fd95-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





