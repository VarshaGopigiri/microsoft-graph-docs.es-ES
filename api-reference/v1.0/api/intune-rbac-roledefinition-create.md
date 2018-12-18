---
title: Crear roleDefinition
description: Cree un objeto roleDefinition.
author: tfitzmac
ms.openlocfilehash: 0ad52c78b6b414fc0419078cd44bcbca2b82ed83
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322403"
---
# <a name="create-roledefinition"></a><span data-ttu-id="a85d8-103">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="a85d8-103">Create roleDefinition</span></span>

> <span data-ttu-id="a85d8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a85d8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a85d8-105">Cree un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="a85d8-105">Create a new [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a85d8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a85d8-106">Prerequisites</span></span>
<span data-ttu-id="a85d8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a85d8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a85d8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a85d8-109">Permission type</span></span>|<span data-ttu-id="a85d8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a85d8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a85d8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a85d8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a85d8-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a85d8-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="a85d8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a85d8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a85d8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a85d8-114">Not supported.</span></span>|
|<span data-ttu-id="a85d8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a85d8-115">Application</span></span>|<span data-ttu-id="a85d8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a85d8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a85d8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a85d8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions
```

## <a name="request-headers"></a><span data-ttu-id="a85d8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a85d8-118">Request headers</span></span>
|<span data-ttu-id="a85d8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a85d8-119">Header</span></span>|<span data-ttu-id="a85d8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a85d8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a85d8-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a85d8-121">Authorization</span></span>|<span data-ttu-id="a85d8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a85d8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a85d8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a85d8-123">Accept</span></span>|<span data-ttu-id="a85d8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a85d8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a85d8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a85d8-125">Request body</span></span>
<span data-ttu-id="a85d8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto roleDefinition.</span><span class="sxs-lookup"><span data-stu-id="a85d8-126">In the request body, supply a JSON representation for the roleDefinition object.</span></span>

<span data-ttu-id="a85d8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto roleDefinition.</span><span class="sxs-lookup"><span data-stu-id="a85d8-127">The following table shows the properties that are required when you create the roleDefinition.</span></span>

|<span data-ttu-id="a85d8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a85d8-128">Property</span></span>|<span data-ttu-id="a85d8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a85d8-129">Type</span></span>|<span data-ttu-id="a85d8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a85d8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a85d8-131">id</span><span class="sxs-lookup"><span data-stu-id="a85d8-131">id</span></span>|<span data-ttu-id="a85d8-132">String</span><span class="sxs-lookup"><span data-stu-id="a85d8-132">String</span></span>|<span data-ttu-id="a85d8-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a85d8-133">Key of the entity.</span></span> <span data-ttu-id="a85d8-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a85d8-134">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="a85d8-135">displayName</span><span class="sxs-lookup"><span data-stu-id="a85d8-135">displayName</span></span>|<span data-ttu-id="a85d8-136">String</span><span class="sxs-lookup"><span data-stu-id="a85d8-136">String</span></span>|<span data-ttu-id="a85d8-137">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="a85d8-137">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="a85d8-138">description</span><span class="sxs-lookup"><span data-stu-id="a85d8-138">description</span></span>|<span data-ttu-id="a85d8-139">String</span><span class="sxs-lookup"><span data-stu-id="a85d8-139">String</span></span>|<span data-ttu-id="a85d8-140">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="a85d8-140">Description of the Role definition.</span></span>|
|<span data-ttu-id="a85d8-141">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="a85d8-141">rolePermissions</span></span>|<span data-ttu-id="a85d8-142">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="a85d8-142">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="a85d8-143">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="a85d8-143">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="a85d8-144">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="a85d8-144">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="a85d8-145">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="a85d8-145">isBuiltIn</span></span>|<span data-ttu-id="a85d8-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="a85d8-146">Boolean</span></span>|<span data-ttu-id="a85d8-147">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="a85d8-147">Type of Role.</span></span> <span data-ttu-id="a85d8-148">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="a85d8-148">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|



## <a name="response"></a><span data-ttu-id="a85d8-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a85d8-149">Response</span></span>
<span data-ttu-id="a85d8-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a85d8-150">If successful, this method returns a `201 Created` response code and a [roleDefinition](../resources/intune-rbac-roledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a85d8-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a85d8-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="a85d8-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a85d8-152">Request</span></span>
<span data-ttu-id="a85d8-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a85d8-153">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions
Content-type: application/json
Content-length: 580

{
  "@odata.type": "#microsoft.graph.roleDefinition",
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

### <a name="response"></a><span data-ttu-id="a85d8-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a85d8-154">Response</span></span>
<span data-ttu-id="a85d8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a85d8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 629

{
  "@odata.type": "#microsoft.graph.roleDefinition",
  "id": "70fdcd08-cd08-70fd-08cd-fd7008cdfd70",
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



