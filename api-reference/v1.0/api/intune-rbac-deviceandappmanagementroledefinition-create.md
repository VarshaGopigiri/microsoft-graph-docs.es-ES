---
title: Crear deviceAndAppManagementRoleDefinition
description: Cree un objeto deviceAndAppManagementRoleDefinition.
ms.openlocfilehash: 71ac4a42dcf0795ad9e1e26d20be5be09fbf0705
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031965"
---
# <a name="create-deviceandappmanagementroledefinition"></a><span data-ttu-id="04bef-103">Crear deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="04bef-103">Create deviceAndAppManagementRoleDefinition</span></span>

> <span data-ttu-id="04bef-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="04bef-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="04bef-105">Cree un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="04bef-105">Create a new [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="04bef-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="04bef-106">Prerequisites</span></span>
<span data-ttu-id="04bef-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="04bef-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="04bef-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04bef-109">Permission type</span></span>|<span data-ttu-id="04bef-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04bef-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="04bef-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04bef-111">Delegated (work or school account)</span></span>|<span data-ttu-id="04bef-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04bef-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="04bef-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04bef-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="04bef-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04bef-114">Not supported.</span></span>|
|<span data-ttu-id="04bef-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04bef-115">Application</span></span>|<span data-ttu-id="04bef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04bef-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="04bef-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04bef-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions
```

## <a name="request-headers"></a><span data-ttu-id="04bef-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04bef-118">Request headers</span></span>
|<span data-ttu-id="04bef-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04bef-119">Header</span></span>|<span data-ttu-id="04bef-120">Valor</span><span class="sxs-lookup"><span data-stu-id="04bef-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="04bef-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="04bef-121">Authorization</span></span>|<span data-ttu-id="04bef-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="04bef-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="04bef-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="04bef-123">Accept</span></span>|<span data-ttu-id="04bef-124">application/json</span><span class="sxs-lookup"><span data-stu-id="04bef-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="04bef-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04bef-125">Request body</span></span>
<span data-ttu-id="04bef-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceAndAppManagementRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="04bef-126">In the request body, supply a JSON representation for the deviceAndAppManagementRoleDefinition object.</span></span>

<span data-ttu-id="04bef-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceAndAppManagementRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="04bef-127">The following table shows the properties that are required when you create the deviceAndAppManagementRoleDefinition.</span></span>

|<span data-ttu-id="04bef-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04bef-128">Property</span></span>|<span data-ttu-id="04bef-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="04bef-129">Type</span></span>|<span data-ttu-id="04bef-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="04bef-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04bef-131">id</span><span class="sxs-lookup"><span data-stu-id="04bef-131">id</span></span>|<span data-ttu-id="04bef-132">String</span><span class="sxs-lookup"><span data-stu-id="04bef-132">String</span></span>|<span data-ttu-id="04bef-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="04bef-133">Key of the entity.</span></span> <span data-ttu-id="04bef-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="04bef-134">This is read-only and automatically generated.</span></span> <span data-ttu-id="04bef-135">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="04bef-135">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="04bef-136">displayName</span><span class="sxs-lookup"><span data-stu-id="04bef-136">displayName</span></span>|<span data-ttu-id="04bef-137">String</span><span class="sxs-lookup"><span data-stu-id="04bef-137">String</span></span>|<span data-ttu-id="04bef-138">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="04bef-138">Display Name of the Role definition.</span></span> <span data-ttu-id="04bef-139">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="04bef-139">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="04bef-140">descripción</span><span class="sxs-lookup"><span data-stu-id="04bef-140">description</span></span>|<span data-ttu-id="04bef-141">String</span><span class="sxs-lookup"><span data-stu-id="04bef-141">String</span></span>|<span data-ttu-id="04bef-142">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="04bef-142">Description of the Role definition.</span></span> <span data-ttu-id="04bef-143">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="04bef-143">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="04bef-144">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="04bef-144">rolePermissions</span></span>|<span data-ttu-id="04bef-145">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="04bef-145">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="04bef-146">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="04bef-146">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="04bef-147">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="04bef-147">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="04bef-148">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="04bef-148">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="04bef-149">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="04bef-149">isBuiltIn</span></span>|<span data-ttu-id="04bef-150">Booleano</span><span class="sxs-lookup"><span data-stu-id="04bef-150">Boolean</span></span>|<span data-ttu-id="04bef-151">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="04bef-151">Type of Role.</span></span> <span data-ttu-id="04bef-152">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="04bef-152">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="04bef-153">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="04bef-153">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|



## <a name="response"></a><span data-ttu-id="04bef-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04bef-154">Response</span></span>
<span data-ttu-id="04bef-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04bef-155">If successful, this method returns a `201 Created` response code and a [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04bef-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04bef-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="04bef-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04bef-157">Request</span></span>
<span data-ttu-id="04bef-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04bef-158">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions
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

### <a name="response"></a><span data-ttu-id="04bef-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04bef-159">Response</span></span>
<span data-ttu-id="04bef-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04bef-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



