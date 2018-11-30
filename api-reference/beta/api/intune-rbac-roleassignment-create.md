---
title: Crear roleAssignment
description: Cree un objeto roleAssignment.
ms.openlocfilehash: f8dca67aad606f1e5a653e0bdf05eb87fbb6b28c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087373"
---
# <a name="create-roleassignment"></a><span data-ttu-id="974f8-103">Crear roleAssignment</span><span class="sxs-lookup"><span data-stu-id="974f8-103">Create roleAssignment</span></span>

> <span data-ttu-id="974f8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="974f8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="974f8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="974f8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="974f8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="974f8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="974f8-107">Cree un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="974f8-107">Create a new [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="974f8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="974f8-108">Prerequisites</span></span>
<span data-ttu-id="974f8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="974f8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="974f8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="974f8-111">Permission type</span></span>|<span data-ttu-id="974f8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="974f8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="974f8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="974f8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="974f8-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="974f8-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="974f8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="974f8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="974f8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="974f8-116">Not supported.</span></span>|
|<span data-ttu-id="974f8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="974f8-117">Application</span></span>|<span data-ttu-id="974f8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="974f8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="974f8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="974f8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="974f8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="974f8-120">Request headers</span></span>
|<span data-ttu-id="974f8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="974f8-121">Header</span></span>|<span data-ttu-id="974f8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="974f8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="974f8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="974f8-123">Authorization</span></span>|<span data-ttu-id="974f8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="974f8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="974f8-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="974f8-125">Accept</span></span>|<span data-ttu-id="974f8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="974f8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="974f8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="974f8-127">Request body</span></span>
<span data-ttu-id="974f8-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto roleAssignment.</span><span class="sxs-lookup"><span data-stu-id="974f8-128">In the request body, supply a JSON representation for the roleAssignment object.</span></span>

<span data-ttu-id="974f8-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto roleAssignment.</span><span class="sxs-lookup"><span data-stu-id="974f8-129">The following table shows the properties that are required when you create the roleAssignment.</span></span>

|<span data-ttu-id="974f8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="974f8-130">Property</span></span>|<span data-ttu-id="974f8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="974f8-131">Type</span></span>|<span data-ttu-id="974f8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="974f8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="974f8-133">id</span><span class="sxs-lookup"><span data-stu-id="974f8-133">id</span></span>|<span data-ttu-id="974f8-134">String</span><span class="sxs-lookup"><span data-stu-id="974f8-134">String</span></span>|<span data-ttu-id="974f8-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="974f8-135">Key of the entity.</span></span> <span data-ttu-id="974f8-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="974f8-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="974f8-137">displayName</span><span class="sxs-lookup"><span data-stu-id="974f8-137">displayName</span></span>|<span data-ttu-id="974f8-138">String</span><span class="sxs-lookup"><span data-stu-id="974f8-138">String</span></span>|<span data-ttu-id="974f8-139">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="974f8-139">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="974f8-140">descripción</span><span class="sxs-lookup"><span data-stu-id="974f8-140">description</span></span>|<span data-ttu-id="974f8-141">String</span><span class="sxs-lookup"><span data-stu-id="974f8-141">String</span></span>|<span data-ttu-id="974f8-142">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="974f8-142">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="974f8-143">scopeMembers</span><span class="sxs-lookup"><span data-stu-id="974f8-143">scopeMembers</span></span>|<span data-ttu-id="974f8-144">Colección string</span><span class="sxs-lookup"><span data-stu-id="974f8-144">String collection</span></span>|<span data-ttu-id="974f8-145">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="974f8-145">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="974f8-146">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="974f8-146">These are IDs from Azure Active Directory.</span></span>|
|<span data-ttu-id="974f8-147">scopeType</span><span class="sxs-lookup"><span data-stu-id="974f8-147">scopeType</span></span>|[<span data-ttu-id="974f8-148">roleAssignmentScopeType</span><span class="sxs-lookup"><span data-stu-id="974f8-148">roleAssignmentScopeType</span></span>](../resources/intune-rbac-roleassignmentscopetype.md)|<span data-ttu-id="974f8-149">Especifica el tipo de ámbito para una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="974f8-149">Specifies the type of scope for a Role Assignment.</span></span> <span data-ttu-id="974f8-150">El tipo predeterminado 'ResourceScope' permite la asignación de ResourceScopes.</span><span class="sxs-lookup"><span data-stu-id="974f8-150">Default type 'ResourceScope' allows assignment of ResourceScopes.</span></span> <span data-ttu-id="974f8-151">Para 'AllDevices', 'AllLicensedUsers' y 'AllDevicesAndLicensedUsers', la propiedad ResourceScopes debería dejarse vacía.</span><span class="sxs-lookup"><span data-stu-id="974f8-151">For 'AllDevices', 'AllLicensedUsers', and 'AllDevicesAndLicensedUsers', the ResourceScopes property should be left empty.</span></span> <span data-ttu-id="974f8-152">Los valores posibles son: `resourceScope`, `allDevices`, `allLicensedUsers` y `allDevicesAndLicensedUsers`.</span><span class="sxs-lookup"><span data-stu-id="974f8-152">Possible values are: `resourceScope`, `allDevices`, `allLicensedUsers`, `allDevicesAndLicensedUsers`.</span></span>|
|<span data-ttu-id="974f8-153">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="974f8-153">resourceScopes</span></span>|<span data-ttu-id="974f8-154">Colección string</span><span class="sxs-lookup"><span data-stu-id="974f8-154">String collection</span></span>|<span data-ttu-id="974f8-155">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="974f8-155">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="974f8-156">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="974f8-156">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="974f8-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="974f8-157">Response</span></span>
<span data-ttu-id="974f8-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="974f8-158">If successful, this method returns a `201 Created` response code and a [roleAssignment](../resources/intune-rbac-roleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="974f8-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="974f8-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="974f8-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="974f8-160">Request</span></span>
<span data-ttu-id="974f8-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="974f8-161">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
Content-type: application/json
Content-length: 277

{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "displayName": "Display Name value",
  "description": "Description value",
  "scopeMembers": [
    "Scope Members value"
  ],
  "scopeType": "allDevices",
  "resourceScopes": [
    "Resource Scopes value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="974f8-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="974f8-162">Response</span></span>
<span data-ttu-id="974f8-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="974f8-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 326

{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "id": "b3234d24-4d24-b323-244d-23b3244d23b3",
  "displayName": "Display Name value",
  "description": "Description value",
  "scopeMembers": [
    "Scope Members value"
  ],
  "scopeType": "allDevices",
  "resourceScopes": [
    "Resource Scopes value"
  ]
}
```




