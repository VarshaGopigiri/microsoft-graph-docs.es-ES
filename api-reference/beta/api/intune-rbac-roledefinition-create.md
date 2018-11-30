---
title: Crear roleDefinition
description: Cree un objeto roleDefinition.
ms.openlocfilehash: 6772b065e4d4d73615540667470829b31a2de804
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091184"
---
# <a name="create-roledefinition"></a><span data-ttu-id="bcb89-103">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="bcb89-103">Create roleDefinition</span></span>

> <span data-ttu-id="bcb89-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bcb89-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bcb89-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bcb89-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bcb89-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bcb89-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bcb89-107">Cree un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="bcb89-107">Create a new [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bcb89-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bcb89-108">Prerequisites</span></span>
<span data-ttu-id="bcb89-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bcb89-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bcb89-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bcb89-111">Permission type</span></span>|<span data-ttu-id="bcb89-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bcb89-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bcb89-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bcb89-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bcb89-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bcb89-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="bcb89-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcb89-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bcb89-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcb89-116">Not supported.</span></span>|
|<span data-ttu-id="bcb89-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bcb89-117">Application</span></span>|<span data-ttu-id="bcb89-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcb89-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bcb89-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bcb89-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions
```

## <a name="request-headers"></a><span data-ttu-id="bcb89-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bcb89-120">Request headers</span></span>
|<span data-ttu-id="bcb89-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcb89-121">Header</span></span>|<span data-ttu-id="bcb89-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb89-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bcb89-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bcb89-123">Authorization</span></span>|<span data-ttu-id="bcb89-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bcb89-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bcb89-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bcb89-125">Accept</span></span>|<span data-ttu-id="bcb89-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bcb89-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bcb89-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bcb89-127">Request body</span></span>
<span data-ttu-id="bcb89-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto roleDefinition.</span><span class="sxs-lookup"><span data-stu-id="bcb89-128">In the request body, supply a JSON representation for the roleDefinition object.</span></span>

<span data-ttu-id="bcb89-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto roleDefinition.</span><span class="sxs-lookup"><span data-stu-id="bcb89-129">The following table shows the properties that are required when you create the roleDefinition.</span></span>

|<span data-ttu-id="bcb89-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bcb89-130">Property</span></span>|<span data-ttu-id="bcb89-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bcb89-131">Type</span></span>|<span data-ttu-id="bcb89-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcb89-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bcb89-133">id</span><span class="sxs-lookup"><span data-stu-id="bcb89-133">id</span></span>|<span data-ttu-id="bcb89-134">String</span><span class="sxs-lookup"><span data-stu-id="bcb89-134">String</span></span>|<span data-ttu-id="bcb89-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bcb89-135">Key of the entity.</span></span> <span data-ttu-id="bcb89-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="bcb89-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="bcb89-137">displayName</span><span class="sxs-lookup"><span data-stu-id="bcb89-137">displayName</span></span>|<span data-ttu-id="bcb89-138">String</span><span class="sxs-lookup"><span data-stu-id="bcb89-138">String</span></span>|<span data-ttu-id="bcb89-139">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="bcb89-139">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="bcb89-140">description</span><span class="sxs-lookup"><span data-stu-id="bcb89-140">description</span></span>|<span data-ttu-id="bcb89-141">String</span><span class="sxs-lookup"><span data-stu-id="bcb89-141">String</span></span>|<span data-ttu-id="bcb89-142">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="bcb89-142">Description of the Role definition.</span></span>|
|<span data-ttu-id="bcb89-143">permissions</span><span class="sxs-lookup"><span data-stu-id="bcb89-143">permissions</span></span>|<span data-ttu-id="bcb89-144">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="bcb89-144">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="bcb89-145">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="bcb89-145">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="bcb89-146">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="bcb89-146">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="bcb89-147">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="bcb89-147">rolePermissions</span></span>|<span data-ttu-id="bcb89-148">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="bcb89-148">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="bcb89-149">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="bcb89-149">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="bcb89-150">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="bcb89-150">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="bcb89-151">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bcb89-151">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="bcb89-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="bcb89-152">Boolean</span></span>|<span data-ttu-id="bcb89-153">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="bcb89-153">Type of Role.</span></span> <span data-ttu-id="bcb89-154">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="bcb89-154">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|
|<span data-ttu-id="bcb89-155">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="bcb89-155">isBuiltIn</span></span>|<span data-ttu-id="bcb89-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="bcb89-156">Boolean</span></span>|<span data-ttu-id="bcb89-157">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="bcb89-157">Type of Role.</span></span> <span data-ttu-id="bcb89-158">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="bcb89-158">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|



## <a name="response"></a><span data-ttu-id="bcb89-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcb89-159">Response</span></span>
<span data-ttu-id="bcb89-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcb89-160">If successful, this method returns a `201 Created` response code and a [roleDefinition](../resources/intune-rbac-roledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bcb89-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcb89-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="bcb89-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcb89-162">Request</span></span>
<span data-ttu-id="bcb89-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcb89-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/roleDefinitions
Content-type: application/json
Content-length: 1145

{
  "@odata.type": "#microsoft.graph.roleDefinition",
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

### <a name="response"></a><span data-ttu-id="bcb89-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcb89-164">Response</span></span>
<span data-ttu-id="bcb89-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bcb89-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





