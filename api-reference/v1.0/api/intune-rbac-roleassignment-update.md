---
title: Actualizar roleAssignment
description: Actualice las propiedades de un objeto roleAssignment.
ms.openlocfilehash: 0a5c817a2d5f722075976b730c425a62e3670954
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031191"
---
# <a name="update-roleassignment"></a><span data-ttu-id="6cf4d-103">Actualizar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="6cf4d-103">Update roleAssignment</span></span>

> <span data-ttu-id="6cf4d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6cf4d-105">Actualice las propiedades de un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6cf4d-105">Update the properties of a [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6cf4d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6cf4d-106">Prerequisites</span></span>
<span data-ttu-id="6cf4d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6cf4d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6cf4d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6cf4d-109">Permission type</span></span>|<span data-ttu-id="6cf4d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6cf4d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6cf4d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6cf4d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6cf4d-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6cf4d-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="6cf4d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6cf4d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6cf4d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-114">Not supported.</span></span>|
|<span data-ttu-id="6cf4d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6cf4d-115">Application</span></span>|<span data-ttu-id="6cf4d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6cf4d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6cf4d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="6cf4d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6cf4d-118">Request headers</span></span>
|<span data-ttu-id="6cf4d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cf4d-119">Header</span></span>|<span data-ttu-id="6cf4d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6cf4d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6cf4d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6cf4d-121">Authorization</span></span>|<span data-ttu-id="6cf4d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6cf4d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6cf4d-123">Accept</span></span>|<span data-ttu-id="6cf4d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6cf4d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6cf4d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6cf4d-125">Request body</span></span>
<span data-ttu-id="6cf4d-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6cf4d-126">In the request body, supply a JSON representation for the [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>

<span data-ttu-id="6cf4d-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6cf4d-127">The following table shows the properties that are required when you create the [roleAssignment](../resources/intune-rbac-roleassignment.md).</span></span>

|<span data-ttu-id="6cf4d-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6cf4d-128">Property</span></span>|<span data-ttu-id="6cf4d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cf4d-129">Type</span></span>|<span data-ttu-id="6cf4d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cf4d-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6cf4d-131">id</span><span class="sxs-lookup"><span data-stu-id="6cf4d-131">id</span></span>|<span data-ttu-id="6cf4d-132">String</span><span class="sxs-lookup"><span data-stu-id="6cf4d-132">String</span></span>|<span data-ttu-id="6cf4d-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-133">Key of the entity.</span></span> <span data-ttu-id="6cf4d-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-134">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="6cf4d-135">displayName</span><span class="sxs-lookup"><span data-stu-id="6cf4d-135">displayName</span></span>|<span data-ttu-id="6cf4d-136">String</span><span class="sxs-lookup"><span data-stu-id="6cf4d-136">String</span></span>|<span data-ttu-id="6cf4d-137">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-137">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="6cf4d-138">descripción</span><span class="sxs-lookup"><span data-stu-id="6cf4d-138">description</span></span>|<span data-ttu-id="6cf4d-139">String</span><span class="sxs-lookup"><span data-stu-id="6cf4d-139">String</span></span>|<span data-ttu-id="6cf4d-140">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-140">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="6cf4d-141">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="6cf4d-141">resourceScopes</span></span>|<span data-ttu-id="6cf4d-142">Colección string</span><span class="sxs-lookup"><span data-stu-id="6cf4d-142">String collection</span></span>|<span data-ttu-id="6cf4d-143">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-143">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="6cf4d-144">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-144">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="6cf4d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6cf4d-145">Response</span></span>
<span data-ttu-id="6cf4d-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-146">If successful, this method returns a `200 OK` response code and an updated [roleAssignment](../resources/intune-rbac-roleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6cf4d-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6cf4d-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="6cf4d-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6cf4d-148">Request</span></span>
<span data-ttu-id="6cf4d-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-149">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}
Content-type: application/json
Content-length: 193

{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "displayName": "Display Name value",
  "description": "Description value",
  "resourceScopes": [
    "Resource Scopes value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="6cf4d-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6cf4d-150">Response</span></span>
<span data-ttu-id="6cf4d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6cf4d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 242

{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "id": "b3234d24-4d24-b323-244d-23b3244d23b3",
  "displayName": "Display Name value",
  "description": "Description value",
  "resourceScopes": [
    "Resource Scopes value"
  ]
}
```



