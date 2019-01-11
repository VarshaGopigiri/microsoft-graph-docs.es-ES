---
title: Actualizar approleassignment
description: Actualizar las propiedades del objeto approleassignment.
localization_priority: Normal
ms.openlocfilehash: 3d0f95e5413354a28e7b9b26e9b440f147c45931
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809635"
---
# <a name="update-approleassignment"></a><span data-ttu-id="891e1-103">Actualizar approleassignment</span><span class="sxs-lookup"><span data-stu-id="891e1-103">Update approleassignment</span></span>

> <span data-ttu-id="891e1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="891e1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="891e1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="891e1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="891e1-106">Actualizar las propiedades del objeto approleassignment.</span><span class="sxs-lookup"><span data-stu-id="891e1-106">Update the properties of approleassignment object.</span></span>
## <a name="permissions"></a><span data-ttu-id="891e1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="891e1-107">Permissions</span></span>
<span data-ttu-id="891e1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="891e1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="891e1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="891e1-110">Permission type</span></span>      | <span data-ttu-id="891e1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="891e1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="891e1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="891e1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="891e1-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="891e1-113">Directory.AccessAsUser.All</span></span>   |
|<span data-ttu-id="891e1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="891e1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="891e1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="891e1-115">Not supported.</span></span>    |
|<span data-ttu-id="891e1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="891e1-116">Application</span></span> | <span data-ttu-id="891e1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="891e1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="891e1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="891e1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}/appRoleAssignments/{id}
PATCH /servicePrincipals/{id}/appRoleAssignedTo
PATCH /groups/{id}/appRoleAssignments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="891e1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="891e1-119">Request headers</span></span>
| <span data-ttu-id="891e1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="891e1-120">Name</span></span>       | <span data-ttu-id="891e1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="891e1-121">Type</span></span> | <span data-ttu-id="891e1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="891e1-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="891e1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="891e1-123">Authorization</span></span>  | <span data-ttu-id="891e1-124">string</span><span class="sxs-lookup"><span data-stu-id="891e1-124">string</span></span>  | <span data-ttu-id="891e1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="891e1-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="891e1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="891e1-127">Request body</span></span>
<span data-ttu-id="891e1-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="891e1-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="891e1-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="891e1-131">Property</span></span>     | <span data-ttu-id="891e1-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="891e1-132">Type</span></span>   |<span data-ttu-id="891e1-133">Description</span><span class="sxs-lookup"><span data-stu-id="891e1-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="891e1-134">creationTimestamp</span><span class="sxs-lookup"><span data-stu-id="891e1-134">creationTimestamp</span></span>|<span data-ttu-id="891e1-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="891e1-135">DateTimeOffset</span></span>|<span data-ttu-id="891e1-136">La hora de creación de la concesión.</span><span class="sxs-lookup"><span data-stu-id="891e1-136">The time when the grant was created.</span></span>|
|<span data-ttu-id="891e1-137">id</span><span class="sxs-lookup"><span data-stu-id="891e1-137">id</span></span>|<span data-ttu-id="891e1-138">Guid</span><span class="sxs-lookup"><span data-stu-id="891e1-138">Guid</span></span>|<span data-ttu-id="891e1-139">El identificador de rol que se asignó a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="891e1-139">The role id that was assigned to the principal.</span></span>  <span data-ttu-id="891e1-140">Esta función se debe declarar por el de aplicación de destino recursos **resourceId** en su propiedad **appRoles** .</span><span class="sxs-lookup"><span data-stu-id="891e1-140">This role must be declared by the target resource application **resourceId** in its **appRoles** property.</span></span> <span data-ttu-id="891e1-141">Donde el recurso no declarar los permisos, debe especificarse un identificador predeterminado (identificador GUID cero).</span><span class="sxs-lookup"><span data-stu-id="891e1-141">Where the resource does not declare any permissions, a default id (zero GUID) must be specified.</span></span>                            <span data-ttu-id="891e1-142">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="891e1-142">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="891e1-143">principalDisplayName</span><span class="sxs-lookup"><span data-stu-id="891e1-143">principalDisplayName</span></span>|<span data-ttu-id="891e1-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="891e1-144">String</span></span>|<span data-ttu-id="891e1-145">El nombre para mostrar de la entidad de seguridad que se ha concedido el acceso.</span><span class="sxs-lookup"><span data-stu-id="891e1-145">The display name of the principal that was granted the access.</span></span>|
|<span data-ttu-id="891e1-146">principalId</span><span class="sxs-lookup"><span data-stu-id="891e1-146">principalId</span></span>|<span data-ttu-id="891e1-147">Guid</span><span class="sxs-lookup"><span data-stu-id="891e1-147">Guid</span></span>|<span data-ttu-id="891e1-148">El identificador único (**objectId**) para la entidad de seguridad que se van a conceder el acceso.</span><span class="sxs-lookup"><span data-stu-id="891e1-148">The unique identifier (**objectId**) for the principal being granted the access.</span></span>                            <span data-ttu-id="891e1-149">**Notas**: necesarios.</span><span class="sxs-lookup"><span data-stu-id="891e1-149">**Notes**: required.</span></span>            |
|<span data-ttu-id="891e1-150">principalType</span><span class="sxs-lookup"><span data-stu-id="891e1-150">principalType</span></span>|<span data-ttu-id="891e1-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="891e1-151">String</span></span>|<span data-ttu-id="891e1-152">El tipo de entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="891e1-152">The type of principal.</span></span>  <span data-ttu-id="891e1-153">Esto puede ser "User", "ServicePrincipal" o "Grupo".</span><span class="sxs-lookup"><span data-stu-id="891e1-153">This can either be "User", "Group" or "ServicePrincipal".</span></span>|
|<span data-ttu-id="891e1-154">resourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="891e1-154">resourceDisplayName</span></span>|<span data-ttu-id="891e1-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="891e1-155">String</span></span>|<span data-ttu-id="891e1-156">El nombre para mostrar del recurso al que se realizó la asignación.</span><span class="sxs-lookup"><span data-stu-id="891e1-156">The display name of the resource to which the assignment was made.</span></span>|
|<span data-ttu-id="891e1-157">resourceId</span><span class="sxs-lookup"><span data-stu-id="891e1-157">resourceId</span></span>|<span data-ttu-id="891e1-158">Guid</span><span class="sxs-lookup"><span data-stu-id="891e1-158">Guid</span></span>|<span data-ttu-id="891e1-159">El identificador único (**objectId**) para el recurso de destino (entidad de seguridad de servicio) para el que se realizó la asignación.</span><span class="sxs-lookup"><span data-stu-id="891e1-159">The unique identifier (**objectId**) for the target resource (service principal) for which the assignment was made.</span></span>|

## <a name="response"></a><span data-ttu-id="891e1-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="891e1-160">Response</span></span>

<span data-ttu-id="891e1-161">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [appRoleAssignment](../resources/approleassignment.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="891e1-161">If successful, this method returns a `200 OK` response code and updated [appRoleAssignment](../resources/approleassignment.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="891e1-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="891e1-162">Example</span></span>
##### <a name="request"></a><span data-ttu-id="891e1-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="891e1-163">Request</span></span>
<span data-ttu-id="891e1-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="891e1-164">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_approleassignment"
}-->
```http
PATCH https://graph.microsoft.com/beta/appRoleAssignments/{id}
Content-type: application/json
Content-length: 233

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```
##### <a name="response"></a><span data-ttu-id="891e1-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="891e1-165">Response</span></span>
<span data-ttu-id="891e1-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="891e1-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.approleassignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 253

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "id": "id-value",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update approleassignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
