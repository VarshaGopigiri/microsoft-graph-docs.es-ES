---
title: Actualizar roleAssignment
description: Actualice las propiedades de un objeto roleAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: edcfa7d06cbe4348835109c2adc3a48d9f24fe7d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816215"
---
# <a name="update-roleassignment"></a><span data-ttu-id="36d1e-103">Actualizar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="36d1e-103">Update roleAssignment</span></span>

> <span data-ttu-id="36d1e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="36d1e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="36d1e-105">Actualice las propiedades de un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="36d1e-105">Update the properties of a [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="36d1e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="36d1e-106">Prerequisites</span></span>
<span data-ttu-id="36d1e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="36d1e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="36d1e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="36d1e-109">Permission type</span></span>|<span data-ttu-id="36d1e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="36d1e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="36d1e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="36d1e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="36d1e-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36d1e-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="36d1e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="36d1e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="36d1e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36d1e-114">Not supported.</span></span>|
|<span data-ttu-id="36d1e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="36d1e-115">Application</span></span>|<span data-ttu-id="36d1e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36d1e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="36d1e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="36d1e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="36d1e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="36d1e-118">Request headers</span></span>
|<span data-ttu-id="36d1e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36d1e-119">Header</span></span>|<span data-ttu-id="36d1e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="36d1e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="36d1e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="36d1e-121">Authorization</span></span>|<span data-ttu-id="36d1e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="36d1e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="36d1e-123">Accept</span><span class="sxs-lookup"><span data-stu-id="36d1e-123">Accept</span></span>|<span data-ttu-id="36d1e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="36d1e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="36d1e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="36d1e-125">Request body</span></span>
<span data-ttu-id="36d1e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="36d1e-126">In the request body, supply a JSON representation for the [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>

<span data-ttu-id="36d1e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="36d1e-127">The following table shows the properties that are required when you create the [roleAssignment](../resources/intune-rbac-roleassignment.md).</span></span>

|<span data-ttu-id="36d1e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36d1e-128">Property</span></span>|<span data-ttu-id="36d1e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="36d1e-129">Type</span></span>|<span data-ttu-id="36d1e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="36d1e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="36d1e-131">id</span><span class="sxs-lookup"><span data-stu-id="36d1e-131">id</span></span>|<span data-ttu-id="36d1e-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="36d1e-132">String</span></span>|<span data-ttu-id="36d1e-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="36d1e-133">Key of the entity.</span></span> <span data-ttu-id="36d1e-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="36d1e-134">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="36d1e-135">displayName</span><span class="sxs-lookup"><span data-stu-id="36d1e-135">displayName</span></span>|<span data-ttu-id="36d1e-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="36d1e-136">String</span></span>|<span data-ttu-id="36d1e-137">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="36d1e-137">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="36d1e-138">descripción</span><span class="sxs-lookup"><span data-stu-id="36d1e-138">description</span></span>|<span data-ttu-id="36d1e-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="36d1e-139">String</span></span>|<span data-ttu-id="36d1e-140">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="36d1e-140">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="36d1e-141">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="36d1e-141">resourceScopes</span></span>|<span data-ttu-id="36d1e-142">Colección string</span><span class="sxs-lookup"><span data-stu-id="36d1e-142">String collection</span></span>|<span data-ttu-id="36d1e-143">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="36d1e-143">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="36d1e-144">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="36d1e-144">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="36d1e-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36d1e-145">Response</span></span>
<span data-ttu-id="36d1e-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36d1e-146">If successful, this method returns a `200 OK` response code and an updated [roleAssignment](../resources/intune-rbac-roleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="36d1e-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36d1e-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="36d1e-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="36d1e-148">Request</span></span>
<span data-ttu-id="36d1e-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="36d1e-149">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="36d1e-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36d1e-150">Response</span></span>
<span data-ttu-id="36d1e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="36d1e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



