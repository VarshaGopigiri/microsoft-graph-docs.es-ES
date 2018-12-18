---
title: Actualizar deviceAndAppManagementRoleDefinition
description: Actualice las propiedades de un objeto deviceAndAppManagementRoleDefinition.
author: tfitzmac
ms.openlocfilehash: ee118a2593a968557f8ccf9103d6f50af014a491
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362807"
---
# <a name="update-deviceandappmanagementroledefinition"></a><span data-ttu-id="0aa7d-103">Actualizar deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0aa7d-103">Update deviceAndAppManagementRoleDefinition</span></span>

> <span data-ttu-id="0aa7d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0aa7d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0aa7d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0aa7d-107">Actualice las propiedades de un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="0aa7d-107">Update the properties of a [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0aa7d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0aa7d-108">Prerequisites</span></span>
<span data-ttu-id="0aa7d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0aa7d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0aa7d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0aa7d-111">Permission type</span></span>|<span data-ttu-id="0aa7d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0aa7d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0aa7d-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0aa7d-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="0aa7d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0aa7d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-116">Not supported.</span></span>|
|<span data-ttu-id="0aa7d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0aa7d-117">Application</span></span>|<span data-ttu-id="0aa7d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0aa7d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0aa7d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/roleDefinition
```

## <a name="request-headers"></a><span data-ttu-id="0aa7d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0aa7d-120">Request headers</span></span>
|<span data-ttu-id="0aa7d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa7d-121">Header</span></span>|<span data-ttu-id="0aa7d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0aa7d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0aa7d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0aa7d-123">Authorization</span></span>|<span data-ttu-id="0aa7d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0aa7d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0aa7d-125">Accept</span></span>|<span data-ttu-id="0aa7d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0aa7d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0aa7d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0aa7d-127">Request body</span></span>
<span data-ttu-id="0aa7d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="0aa7d-128">In the request body, supply a JSON representation for the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>

<span data-ttu-id="0aa7d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="0aa7d-129">The following table shows the properties that are required when you create the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span></span>

|<span data-ttu-id="0aa7d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0aa7d-130">Property</span></span>|<span data-ttu-id="0aa7d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0aa7d-131">Type</span></span>|<span data-ttu-id="0aa7d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0aa7d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0aa7d-133">id</span><span class="sxs-lookup"><span data-stu-id="0aa7d-133">id</span></span>|<span data-ttu-id="0aa7d-134">String</span><span class="sxs-lookup"><span data-stu-id="0aa7d-134">String</span></span>|<span data-ttu-id="0aa7d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-135">Key of the entity.</span></span> <span data-ttu-id="0aa7d-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-136">This is read-only and automatically generated.</span></span> <span data-ttu-id="0aa7d-137">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-137">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="0aa7d-138">displayName</span><span class="sxs-lookup"><span data-stu-id="0aa7d-138">displayName</span></span>|<span data-ttu-id="0aa7d-139">String</span><span class="sxs-lookup"><span data-stu-id="0aa7d-139">String</span></span>|<span data-ttu-id="0aa7d-140">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-140">Display Name of the Role definition.</span></span> <span data-ttu-id="0aa7d-141">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-141">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="0aa7d-142">descripción</span><span class="sxs-lookup"><span data-stu-id="0aa7d-142">description</span></span>|<span data-ttu-id="0aa7d-143">String</span><span class="sxs-lookup"><span data-stu-id="0aa7d-143">String</span></span>|<span data-ttu-id="0aa7d-144">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-144">Description of the Role definition.</span></span> <span data-ttu-id="0aa7d-145">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-145">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="0aa7d-146">permissions</span><span class="sxs-lookup"><span data-stu-id="0aa7d-146">permissions</span></span>|<span data-ttu-id="0aa7d-147">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-147">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="0aa7d-148">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-148">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="0aa7d-149">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-149">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="0aa7d-150">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-150">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="0aa7d-151">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="0aa7d-151">rolePermissions</span></span>|<span data-ttu-id="0aa7d-152">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-152">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="0aa7d-153">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-153">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="0aa7d-154">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-154">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="0aa7d-155">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-155">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="0aa7d-156">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0aa7d-156">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="0aa7d-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="0aa7d-157">Boolean</span></span>|<span data-ttu-id="0aa7d-158">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-158">Type of Role.</span></span> <span data-ttu-id="0aa7d-159">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-159">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="0aa7d-160">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-160">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="0aa7d-161">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="0aa7d-161">isBuiltIn</span></span>|<span data-ttu-id="0aa7d-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="0aa7d-162">Boolean</span></span>|<span data-ttu-id="0aa7d-163">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-163">Type of Role.</span></span> <span data-ttu-id="0aa7d-164">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-164">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="0aa7d-165">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-165">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|



## <a name="response"></a><span data-ttu-id="0aa7d-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0aa7d-166">Response</span></span>
<span data-ttu-id="0aa7d-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-167">If successful, this method returns a `200 OK` response code and an updated [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0aa7d-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0aa7d-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="0aa7d-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0aa7d-169">Request</span></span>
<span data-ttu-id="0aa7d-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/roleDefinitions/{roleDefinitionId}
Content-type: application/json
Content-length: 1092

{
  "displayName": "Display Name value",
  "description": "Description value",
  "permissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "Actions value"
      ],
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
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "Actions value"
      ],
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
  "isBuiltInRoleDefinition": true,
  "isBuiltIn": true
}
```

### <a name="response"></a><span data-ttu-id="0aa7d-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0aa7d-171">Response</span></span>
<span data-ttu-id="0aa7d-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1216

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
  "id": "bca1dfb5-dfb5-bca1-b5df-a1bcb5dfa1bc",
  "displayName": "Display Name value",
  "description": "Description value",
  "permissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "Actions value"
      ],
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
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "Actions value"
      ],
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
  "isBuiltInRoleDefinition": true,
  "isBuiltIn": true
}
```





