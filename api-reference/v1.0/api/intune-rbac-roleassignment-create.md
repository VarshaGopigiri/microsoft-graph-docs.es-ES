---
title: Crear roleAssignment
description: Cree un objeto roleAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0cb60cad1785de83c44772d6f1cbc00c9129861f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973786"
---
# <a name="create-roleassignment"></a><span data-ttu-id="8b668-103">Crear roleAssignment</span><span class="sxs-lookup"><span data-stu-id="8b668-103">Create roleAssignment</span></span>

> <span data-ttu-id="8b668-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8b668-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8b668-105">Cree un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8b668-105">Create a new [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8b668-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8b668-106">Prerequisites</span></span>
<span data-ttu-id="8b668-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8b668-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8b668-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8b668-109">Permission type</span></span>|<span data-ttu-id="8b668-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8b668-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8b668-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8b668-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8b668-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b668-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="8b668-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8b668-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8b668-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b668-114">Not supported.</span></span>|
|<span data-ttu-id="8b668-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8b668-115">Application</span></span>|<span data-ttu-id="8b668-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b668-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8b668-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8b668-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="8b668-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8b668-118">Request headers</span></span>
|<span data-ttu-id="8b668-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b668-119">Header</span></span>|<span data-ttu-id="8b668-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8b668-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8b668-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8b668-121">Authorization</span></span>|<span data-ttu-id="8b668-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8b668-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8b668-123">Accept</span><span class="sxs-lookup"><span data-stu-id="8b668-123">Accept</span></span>|<span data-ttu-id="8b668-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8b668-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8b668-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8b668-125">Request body</span></span>
<span data-ttu-id="8b668-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto roleAssignment.</span><span class="sxs-lookup"><span data-stu-id="8b668-126">In the request body, supply a JSON representation for the roleAssignment object.</span></span>

<span data-ttu-id="8b668-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto roleAssignment.</span><span class="sxs-lookup"><span data-stu-id="8b668-127">The following table shows the properties that are required when you create the roleAssignment.</span></span>

|<span data-ttu-id="8b668-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8b668-128">Property</span></span>|<span data-ttu-id="8b668-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b668-129">Type</span></span>|<span data-ttu-id="8b668-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b668-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8b668-131">id</span><span class="sxs-lookup"><span data-stu-id="8b668-131">id</span></span>|<span data-ttu-id="8b668-132">String</span><span class="sxs-lookup"><span data-stu-id="8b668-132">String</span></span>|<span data-ttu-id="8b668-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8b668-133">Key of the entity.</span></span> <span data-ttu-id="8b668-134">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8b668-134">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="8b668-135">displayName</span><span class="sxs-lookup"><span data-stu-id="8b668-135">displayName</span></span>|<span data-ttu-id="8b668-136">String</span><span class="sxs-lookup"><span data-stu-id="8b668-136">String</span></span>|<span data-ttu-id="8b668-137">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="8b668-137">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="8b668-138">descripción</span><span class="sxs-lookup"><span data-stu-id="8b668-138">description</span></span>|<span data-ttu-id="8b668-139">String</span><span class="sxs-lookup"><span data-stu-id="8b668-139">String</span></span>|<span data-ttu-id="8b668-140">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="8b668-140">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="8b668-141">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="8b668-141">resourceScopes</span></span>|<span data-ttu-id="8b668-142">Colección string</span><span class="sxs-lookup"><span data-stu-id="8b668-142">String collection</span></span>|<span data-ttu-id="8b668-143">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="8b668-143">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="8b668-144">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8b668-144">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="8b668-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b668-145">Response</span></span>
<span data-ttu-id="8b668-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b668-146">If successful, this method returns a `201 Created` response code and a [roleAssignment](../resources/intune-rbac-roleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8b668-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b668-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="8b668-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8b668-148">Request</span></span>
<span data-ttu-id="8b668-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b668-149">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
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

### <a name="response"></a><span data-ttu-id="8b668-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b668-150">Response</span></span>
<span data-ttu-id="8b668-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8b668-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



