---
title: Crear deviceAndAppManagementRoleAssignment
description: Cree un objeto deviceAndAppManagementRoleAssignment.
ms.openlocfilehash: bdfb17c1f6e1bc9ea75c6ee72e0277efd5295035
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030803"
---
# <a name="create-deviceandappmanagementroleassignment"></a><span data-ttu-id="d249b-103">Crear deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d249b-103">Create deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="d249b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d249b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d249b-105">Cree un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d249b-105">Create a new [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d249b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d249b-106">Prerequisites</span></span>
<span data-ttu-id="d249b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d249b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d249b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d249b-109">Permission type</span></span>|<span data-ttu-id="d249b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d249b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d249b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d249b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d249b-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d249b-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="d249b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d249b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d249b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d249b-114">Not supported.</span></span>|
|<span data-ttu-id="d249b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d249b-115">Application</span></span>|<span data-ttu-id="d249b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d249b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d249b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d249b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="d249b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d249b-118">Request headers</span></span>
|<span data-ttu-id="d249b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d249b-119">Header</span></span>|<span data-ttu-id="d249b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d249b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d249b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d249b-121">Authorization</span></span>|<span data-ttu-id="d249b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d249b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d249b-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d249b-123">Accept</span></span>|<span data-ttu-id="d249b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d249b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d249b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d249b-125">Request body</span></span>
<span data-ttu-id="d249b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceAndAppManagementRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="d249b-126">In the request body, supply a JSON representation for the deviceAndAppManagementRoleAssignment object.</span></span>

<span data-ttu-id="d249b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceAndAppManagementRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="d249b-127">The following table shows the properties that are required when you create the deviceAndAppManagementRoleAssignment.</span></span>

|<span data-ttu-id="d249b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d249b-128">Property</span></span>|<span data-ttu-id="d249b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d249b-129">Type</span></span>|<span data-ttu-id="d249b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d249b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d249b-131">id</span><span class="sxs-lookup"><span data-stu-id="d249b-131">id</span></span>|<span data-ttu-id="d249b-132">String</span><span class="sxs-lookup"><span data-stu-id="d249b-132">String</span></span>|<span data-ttu-id="d249b-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d249b-133">Key of the entity.</span></span> <span data-ttu-id="d249b-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d249b-134">This is read-only and automatically generated.</span></span> <span data-ttu-id="d249b-135">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d249b-135">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d249b-136">displayName</span><span class="sxs-lookup"><span data-stu-id="d249b-136">displayName</span></span>|<span data-ttu-id="d249b-137">String</span><span class="sxs-lookup"><span data-stu-id="d249b-137">String</span></span>|<span data-ttu-id="d249b-138">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="d249b-138">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="d249b-139">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d249b-139">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d249b-140">descripción</span><span class="sxs-lookup"><span data-stu-id="d249b-140">description</span></span>|<span data-ttu-id="d249b-141">String</span><span class="sxs-lookup"><span data-stu-id="d249b-141">String</span></span>|<span data-ttu-id="d249b-142">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="d249b-142">Description of the Role Assignment.</span></span> <span data-ttu-id="d249b-143">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d249b-143">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d249b-144">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="d249b-144">resourceScopes</span></span>|<span data-ttu-id="d249b-145">Colección string</span><span class="sxs-lookup"><span data-stu-id="d249b-145">String collection</span></span>|<span data-ttu-id="d249b-146">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="d249b-146">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="d249b-147">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d249b-147">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="d249b-148">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d249b-148">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="d249b-149">members</span><span class="sxs-lookup"><span data-stu-id="d249b-149">members</span></span>|<span data-ttu-id="d249b-150">Colección string</span><span class="sxs-lookup"><span data-stu-id="d249b-150">String collection</span></span>|<span data-ttu-id="d249b-151">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="d249b-151">The list of ids of role member security groups.</span></span> <span data-ttu-id="d249b-152">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d249b-152">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="d249b-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d249b-153">Response</span></span>
<span data-ttu-id="d249b-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d249b-154">If successful, this method returns a `201 Created` response code and a [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d249b-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d249b-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="d249b-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d249b-156">Request</span></span>
<span data-ttu-id="d249b-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d249b-157">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/roleAssignments
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

### <a name="response"></a><span data-ttu-id="d249b-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d249b-158">Response</span></span>
<span data-ttu-id="d249b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d249b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



