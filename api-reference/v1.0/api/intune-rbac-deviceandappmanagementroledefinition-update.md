---
title: Actualizar deviceAndAppManagementRoleDefinition
description: Actualice las propiedades de un objeto deviceAndAppManagementRoleDefinition.
ms.openlocfilehash: 37492fe897baef448d0589fcbd1d1d1c1b51f3db
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032656"
---
# <a name="update-deviceandappmanagementroledefinition"></a><span data-ttu-id="2b9c4-103">Actualizar deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2b9c4-103">Update deviceAndAppManagementRoleDefinition</span></span>

> <span data-ttu-id="2b9c4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2b9c4-105">Actualice las propiedades de un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="2b9c4-105">Update the properties of a [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2b9c4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2b9c4-106">Prerequisites</span></span>
<span data-ttu-id="2b9c4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2b9c4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2b9c4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b9c4-109">Permission type</span></span>|<span data-ttu-id="2b9c4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2b9c4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2b9c4-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2b9c4-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="2b9c4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2b9c4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-114">Not supported.</span></span>|
|<span data-ttu-id="2b9c4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b9c4-115">Application</span></span>|<span data-ttu-id="2b9c4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2b9c4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b9c4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/roleDefinition
```

## <a name="request-headers"></a><span data-ttu-id="2b9c4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b9c4-118">Request headers</span></span>
|<span data-ttu-id="2b9c4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b9c4-119">Header</span></span>|<span data-ttu-id="2b9c4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2b9c4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2b9c4-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="2b9c4-121">Authorization</span></span>|<span data-ttu-id="2b9c4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2b9c4-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2b9c4-123">Accept</span></span>|<span data-ttu-id="2b9c4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2b9c4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2b9c4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b9c4-125">Request body</span></span>
<span data-ttu-id="2b9c4-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="2b9c4-126">In the request body, supply a JSON representation for the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>

<span data-ttu-id="2b9c4-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="2b9c4-127">The following table shows the properties that are required when you create the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span></span>

|<span data-ttu-id="2b9c4-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b9c4-128">Property</span></span>|<span data-ttu-id="2b9c4-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b9c4-129">Type</span></span>|<span data-ttu-id="2b9c4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b9c4-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2b9c4-131">id</span><span class="sxs-lookup"><span data-stu-id="2b9c4-131">id</span></span>|<span data-ttu-id="2b9c4-132">String</span><span class="sxs-lookup"><span data-stu-id="2b9c4-132">String</span></span>|<span data-ttu-id="2b9c4-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-133">Key of the entity.</span></span> <span data-ttu-id="2b9c4-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-134">This is read-only and automatically generated.</span></span> <span data-ttu-id="2b9c4-135">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-135">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="2b9c4-136">displayName</span><span class="sxs-lookup"><span data-stu-id="2b9c4-136">displayName</span></span>|<span data-ttu-id="2b9c4-137">String</span><span class="sxs-lookup"><span data-stu-id="2b9c4-137">String</span></span>|<span data-ttu-id="2b9c4-138">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-138">Display Name of the Role definition.</span></span> <span data-ttu-id="2b9c4-139">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-139">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="2b9c4-140">descripción</span><span class="sxs-lookup"><span data-stu-id="2b9c4-140">description</span></span>|<span data-ttu-id="2b9c4-141">String</span><span class="sxs-lookup"><span data-stu-id="2b9c4-141">String</span></span>|<span data-ttu-id="2b9c4-142">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-142">Description of the Role definition.</span></span> <span data-ttu-id="2b9c4-143">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-143">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="2b9c4-144">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="2b9c4-144">rolePermissions</span></span>|<span data-ttu-id="2b9c4-145">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-145">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="2b9c4-146">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-146">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="2b9c4-147">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-147">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="2b9c4-148">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-148">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="2b9c4-149">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="2b9c4-149">isBuiltIn</span></span>|<span data-ttu-id="2b9c4-150">Booleano</span><span class="sxs-lookup"><span data-stu-id="2b9c4-150">Boolean</span></span>|<span data-ttu-id="2b9c4-151">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-151">Type of Role.</span></span> <span data-ttu-id="2b9c4-152">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-152">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="2b9c4-153">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="2b9c4-153">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|



## <a name="response"></a><span data-ttu-id="2b9c4-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b9c4-154">Response</span></span>
<span data-ttu-id="2b9c4-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-155">If successful, this method returns a `200 OK` response code and an updated [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2b9c4-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b9c4-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="2b9c4-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b9c4-157">Request</span></span>
<span data-ttu-id="2b9c4-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-158">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}
Content-type: application/json
Content-length: 602

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
  "displayName": "Display Name value",
  "description": "Description value",
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "resourceActions": [
        {
          "@odata.type": "microsoft.graph.resourceAction",
          "allowedResourceActions": [
            "Allowed Resource Actions value"
          ],
          "notAllowedResourceActions": [
            "Not Allowed Resource Actions value"
          ]
        }
      ]
    }
  ],
  "isBuiltIn": true
}
```

### <a name="response"></a><span data-ttu-id="2b9c4-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b9c4-159">Response</span></span>
<span data-ttu-id="2b9c4-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b9c4-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 651

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
  "id": "bca1dfb5-dfb5-bca1-b5df-a1bcb5dfa1bc",
  "displayName": "Display Name value",
  "description": "Description value",
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "resourceActions": [
        {
          "@odata.type": "microsoft.graph.resourceAction",
          "allowedResourceActions": [
            "Allowed Resource Actions value"
          ],
          "notAllowedResourceActions": [
            "Not Allowed Resource Actions value"
          ]
        }
      ]
    }
  ],
  "isBuiltIn": true
}
```



