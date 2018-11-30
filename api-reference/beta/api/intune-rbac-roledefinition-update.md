---
title: Actualizar roleDefinition
description: Actualice las propiedades de un objeto roleDefinition.
ms.openlocfilehash: debf63b5d0b7116a1e8d1f9274868d97c3cb8931
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083778"
---
# <a name="update-roledefinition"></a><span data-ttu-id="9927f-103">Actualizar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="9927f-103">Update roleDefinition</span></span>

> <span data-ttu-id="9927f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9927f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9927f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9927f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9927f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9927f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9927f-107">Actualice las propiedades de un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="9927f-107">Update the properties of a [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9927f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9927f-108">Prerequisites</span></span>
<span data-ttu-id="9927f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9927f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9927f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9927f-111">Permission type</span></span>|<span data-ttu-id="9927f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9927f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9927f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9927f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9927f-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9927f-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="9927f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9927f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9927f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9927f-116">Not supported.</span></span>|
|<span data-ttu-id="9927f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9927f-117">Application</span></span>|<span data-ttu-id="9927f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9927f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9927f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9927f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/roleDefinition
```

## <a name="request-headers"></a><span data-ttu-id="9927f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9927f-120">Request headers</span></span>
|<span data-ttu-id="9927f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9927f-121">Header</span></span>|<span data-ttu-id="9927f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9927f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9927f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9927f-123">Authorization</span></span>|<span data-ttu-id="9927f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9927f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9927f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9927f-125">Accept</span></span>|<span data-ttu-id="9927f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9927f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9927f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9927f-127">Request body</span></span>
<span data-ttu-id="9927f-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="9927f-128">In the request body, supply a JSON representation for the [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>

<span data-ttu-id="9927f-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="9927f-129">The following table shows the properties that are required when you create the [roleDefinition](../resources/intune-rbac-roledefinition.md).</span></span>

|<span data-ttu-id="9927f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9927f-130">Property</span></span>|<span data-ttu-id="9927f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9927f-131">Type</span></span>|<span data-ttu-id="9927f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9927f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9927f-133">id</span><span class="sxs-lookup"><span data-stu-id="9927f-133">id</span></span>|<span data-ttu-id="9927f-134">String</span><span class="sxs-lookup"><span data-stu-id="9927f-134">String</span></span>|<span data-ttu-id="9927f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9927f-135">Key of the entity.</span></span> <span data-ttu-id="9927f-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="9927f-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="9927f-137">displayName</span><span class="sxs-lookup"><span data-stu-id="9927f-137">displayName</span></span>|<span data-ttu-id="9927f-138">String</span><span class="sxs-lookup"><span data-stu-id="9927f-138">String</span></span>|<span data-ttu-id="9927f-139">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="9927f-139">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="9927f-140">description</span><span class="sxs-lookup"><span data-stu-id="9927f-140">description</span></span>|<span data-ttu-id="9927f-141">String</span><span class="sxs-lookup"><span data-stu-id="9927f-141">String</span></span>|<span data-ttu-id="9927f-142">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="9927f-142">Description of the Role definition.</span></span>|
|<span data-ttu-id="9927f-143">permissions</span><span class="sxs-lookup"><span data-stu-id="9927f-143">permissions</span></span>|<span data-ttu-id="9927f-144">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="9927f-144">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="9927f-145">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="9927f-145">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="9927f-146">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="9927f-146">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="9927f-147">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="9927f-147">rolePermissions</span></span>|<span data-ttu-id="9927f-148">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="9927f-148">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="9927f-149">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="9927f-149">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="9927f-150">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="9927f-150">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="9927f-151">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9927f-151">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="9927f-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="9927f-152">Boolean</span></span>|<span data-ttu-id="9927f-153">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="9927f-153">Type of Role.</span></span> <span data-ttu-id="9927f-154">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="9927f-154">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|
|<span data-ttu-id="9927f-155">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="9927f-155">isBuiltIn</span></span>|<span data-ttu-id="9927f-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="9927f-156">Boolean</span></span>|<span data-ttu-id="9927f-157">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="9927f-157">Type of Role.</span></span> <span data-ttu-id="9927f-158">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="9927f-158">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|



## <a name="response"></a><span data-ttu-id="9927f-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9927f-159">Response</span></span>
<span data-ttu-id="9927f-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9927f-160">If successful, this method returns a `200 OK` response code and an updated [roleDefinition](../resources/intune-rbac-roledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9927f-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9927f-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="9927f-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9927f-162">Request</span></span>
<span data-ttu-id="9927f-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9927f-163">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="9927f-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9927f-164">Response</span></span>
<span data-ttu-id="9927f-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9927f-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1194

{
  "@odata.type": "#microsoft.graph.roleDefinition",
  "id": "70fdcd08-cd08-70fd-08cd-fd7008cdfd70",
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





