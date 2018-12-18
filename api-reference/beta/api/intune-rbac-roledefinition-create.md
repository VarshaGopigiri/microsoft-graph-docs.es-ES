---
title: Crear roleDefinition
description: Cree un objeto roleDefinition.
author: tfitzmac
ms.openlocfilehash: 03134f270d49002c5882a1e65cb0c4454684cd4a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337348"
---
# <a name="create-roledefinition"></a><span data-ttu-id="1f41b-103">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="1f41b-103">Create roleDefinition</span></span>

> <span data-ttu-id="1f41b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1f41b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1f41b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1f41b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1f41b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1f41b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1f41b-107">Cree un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="1f41b-107">Create a new [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1f41b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1f41b-108">Prerequisites</span></span>
<span data-ttu-id="1f41b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1f41b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1f41b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1f41b-111">Permission type</span></span>|<span data-ttu-id="1f41b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1f41b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1f41b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1f41b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1f41b-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1f41b-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="1f41b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1f41b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1f41b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f41b-116">Not supported.</span></span>|
|<span data-ttu-id="1f41b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1f41b-117">Application</span></span>|<span data-ttu-id="1f41b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f41b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1f41b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1f41b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions
```

## <a name="request-headers"></a><span data-ttu-id="1f41b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1f41b-120">Request headers</span></span>
|<span data-ttu-id="1f41b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f41b-121">Header</span></span>|<span data-ttu-id="1f41b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1f41b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1f41b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1f41b-123">Authorization</span></span>|<span data-ttu-id="1f41b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1f41b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1f41b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1f41b-125">Accept</span></span>|<span data-ttu-id="1f41b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1f41b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1f41b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1f41b-127">Request body</span></span>
<span data-ttu-id="1f41b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto roleDefinition.</span><span class="sxs-lookup"><span data-stu-id="1f41b-128">In the request body, supply a JSON representation for the roleDefinition object.</span></span>

<span data-ttu-id="1f41b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto roleDefinition.</span><span class="sxs-lookup"><span data-stu-id="1f41b-129">The following table shows the properties that are required when you create the roleDefinition.</span></span>

|<span data-ttu-id="1f41b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f41b-130">Property</span></span>|<span data-ttu-id="1f41b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f41b-131">Type</span></span>|<span data-ttu-id="1f41b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f41b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1f41b-133">id</span><span class="sxs-lookup"><span data-stu-id="1f41b-133">id</span></span>|<span data-ttu-id="1f41b-134">String</span><span class="sxs-lookup"><span data-stu-id="1f41b-134">String</span></span>|<span data-ttu-id="1f41b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1f41b-135">Key of the entity.</span></span> <span data-ttu-id="1f41b-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1f41b-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="1f41b-137">displayName</span><span class="sxs-lookup"><span data-stu-id="1f41b-137">displayName</span></span>|<span data-ttu-id="1f41b-138">String</span><span class="sxs-lookup"><span data-stu-id="1f41b-138">String</span></span>|<span data-ttu-id="1f41b-139">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="1f41b-139">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="1f41b-140">description</span><span class="sxs-lookup"><span data-stu-id="1f41b-140">description</span></span>|<span data-ttu-id="1f41b-141">String</span><span class="sxs-lookup"><span data-stu-id="1f41b-141">String</span></span>|<span data-ttu-id="1f41b-142">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="1f41b-142">Description of the Role definition.</span></span>|
|<span data-ttu-id="1f41b-143">permissions</span><span class="sxs-lookup"><span data-stu-id="1f41b-143">permissions</span></span>|<span data-ttu-id="1f41b-144">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="1f41b-144">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="1f41b-145">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="1f41b-145">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="1f41b-146">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="1f41b-146">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="1f41b-147">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="1f41b-147">rolePermissions</span></span>|<span data-ttu-id="1f41b-148">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="1f41b-148">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="1f41b-149">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="1f41b-149">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="1f41b-150">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="1f41b-150">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="1f41b-151">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1f41b-151">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="1f41b-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f41b-152">Boolean</span></span>|<span data-ttu-id="1f41b-153">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="1f41b-153">Type of Role.</span></span> <span data-ttu-id="1f41b-154">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="1f41b-154">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|
|<span data-ttu-id="1f41b-155">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="1f41b-155">isBuiltIn</span></span>|<span data-ttu-id="1f41b-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f41b-156">Boolean</span></span>|<span data-ttu-id="1f41b-157">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="1f41b-157">Type of Role.</span></span> <span data-ttu-id="1f41b-158">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="1f41b-158">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|



## <a name="response"></a><span data-ttu-id="1f41b-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f41b-159">Response</span></span>
<span data-ttu-id="1f41b-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f41b-160">If successful, this method returns a `201 Created` response code and a [roleDefinition](../resources/intune-rbac-roledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1f41b-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1f41b-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="1f41b-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1f41b-162">Request</span></span>
<span data-ttu-id="1f41b-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1f41b-163">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="1f41b-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f41b-164">Response</span></span>
<span data-ttu-id="1f41b-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1f41b-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





