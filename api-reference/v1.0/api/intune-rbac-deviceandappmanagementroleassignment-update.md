---
title: Actualizar deviceAndAppManagementRoleAssignment
description: Actualice las propiedades de un objeto deviceAndAppManagementRoleAssignment.
author: tfitzmac
ms.openlocfilehash: d701d859798095442b3ba0e0ee0287e8afced8cf
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331804"
---
# <a name="update-deviceandappmanagementroleassignment"></a><span data-ttu-id="dc970-103">Actualizar deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dc970-103">Update deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="dc970-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dc970-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dc970-105">Actualice las propiedades de un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="dc970-105">Update the properties of a [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dc970-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dc970-106">Prerequisites</span></span>
<span data-ttu-id="dc970-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc970-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc970-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc970-109">Permission type</span></span>|<span data-ttu-id="dc970-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc970-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dc970-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc970-111">Delegated (work or school account)</span></span>|<span data-ttu-id="dc970-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dc970-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="dc970-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc970-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dc970-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc970-114">Not supported.</span></span>|
|<span data-ttu-id="dc970-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc970-115">Application</span></span>|<span data-ttu-id="dc970-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc970-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dc970-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc970-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="dc970-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc970-118">Request headers</span></span>
|<span data-ttu-id="dc970-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc970-119">Header</span></span>|<span data-ttu-id="dc970-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dc970-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dc970-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="dc970-121">Authorization</span></span>|<span data-ttu-id="dc970-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dc970-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dc970-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dc970-123">Accept</span></span>|<span data-ttu-id="dc970-124">application/json</span><span class="sxs-lookup"><span data-stu-id="dc970-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dc970-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc970-125">Request body</span></span>
<span data-ttu-id="dc970-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="dc970-126">In the request body, supply a JSON representation for the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object.</span></span>

<span data-ttu-id="dc970-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="dc970-127">The following table shows the properties that are required when you create the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span></span>

|<span data-ttu-id="dc970-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc970-128">Property</span></span>|<span data-ttu-id="dc970-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc970-129">Type</span></span>|<span data-ttu-id="dc970-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc970-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dc970-131">id</span><span class="sxs-lookup"><span data-stu-id="dc970-131">id</span></span>|<span data-ttu-id="dc970-132">String</span><span class="sxs-lookup"><span data-stu-id="dc970-132">String</span></span>|<span data-ttu-id="dc970-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="dc970-133">Key of the entity.</span></span> <span data-ttu-id="dc970-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="dc970-134">This is read-only and automatically generated.</span></span> <span data-ttu-id="dc970-135">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="dc970-135">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="dc970-136">displayName</span><span class="sxs-lookup"><span data-stu-id="dc970-136">displayName</span></span>|<span data-ttu-id="dc970-137">String</span><span class="sxs-lookup"><span data-stu-id="dc970-137">String</span></span>|<span data-ttu-id="dc970-138">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="dc970-138">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="dc970-139">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="dc970-139">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="dc970-140">descripción</span><span class="sxs-lookup"><span data-stu-id="dc970-140">description</span></span>|<span data-ttu-id="dc970-141">String</span><span class="sxs-lookup"><span data-stu-id="dc970-141">String</span></span>|<span data-ttu-id="dc970-142">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="dc970-142">Description of the Role Assignment.</span></span> <span data-ttu-id="dc970-143">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="dc970-143">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="dc970-144">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="dc970-144">resourceScopes</span></span>|<span data-ttu-id="dc970-145">Colección string</span><span class="sxs-lookup"><span data-stu-id="dc970-145">String collection</span></span>|<span data-ttu-id="dc970-146">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="dc970-146">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="dc970-147">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc970-147">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="dc970-148">Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="dc970-148">Inherited from [roleAssignment](../resources/intune-rbac-roleassignment.md)</span></span>|
|<span data-ttu-id="dc970-149">members</span><span class="sxs-lookup"><span data-stu-id="dc970-149">members</span></span>|<span data-ttu-id="dc970-150">Colección string</span><span class="sxs-lookup"><span data-stu-id="dc970-150">String collection</span></span>|<span data-ttu-id="dc970-151">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="dc970-151">The list of ids of role member security groups.</span></span> <span data-ttu-id="dc970-152">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc970-152">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="dc970-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc970-153">Response</span></span>
<span data-ttu-id="dc970-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc970-154">If successful, this method returns a `200 OK` response code and an updated [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dc970-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc970-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="dc970-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc970-156">Request</span></span>
<span data-ttu-id="dc970-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc970-157">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="dc970-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc970-158">Response</span></span>
<span data-ttu-id="dc970-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc970-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



