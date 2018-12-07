---
title: Actualizar governanceRoleSetting
description: Actualizar las propiedades de governanceRoleSetting.
ms.openlocfilehash: 2d9417c99e63b1b4c7302c2afdda4c272b2fce82
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27191119"
---
# <a name="update-governancerolesetting"></a><span data-ttu-id="a6620-103">Actualizar governanceRoleSetting</span><span class="sxs-lookup"><span data-stu-id="a6620-103">Update governanceRoleSetting</span></span>

> <span data-ttu-id="a6620-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6620-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6620-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6620-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a6620-106">Actualizar las propiedades de [governanceRoleSetting](../resources/governancerolesetting.md).</span><span class="sxs-lookup"><span data-stu-id="a6620-106">Update the properties of [governanceRoleSetting](../resources/governancerolesetting.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a6620-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6620-107">Permissions</span></span>
<span data-ttu-id="a6620-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a6620-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

><span data-ttu-id="a6620-110">**Nota:** Esta API también requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="a6620-110">**Note:** This API also requires that the requester have at least one `Active` administrator role assignment (`owner` or `user access administrator`) on the resource.</span></span>

|<span data-ttu-id="a6620-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6620-111">Permission type</span></span>      | <span data-ttu-id="a6620-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6620-112">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a6620-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6620-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a6620-114">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="a6620-114">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="a6620-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6620-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a6620-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6620-116">Not supported.</span></span>    |
|<span data-ttu-id="a6620-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6620-117">Application</span></span> | <span data-ttu-id="a6620-118">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="a6620-118">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="a6620-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6620-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /privilegedAccess/azureResources/roleSettings/{id}
```
## <a name="request-headers"></a><span data-ttu-id="a6620-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6620-120">Request headers</span></span>
| <span data-ttu-id="a6620-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6620-121">Name</span></span>       | <span data-ttu-id="a6620-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6620-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="a6620-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a6620-123">Authorization</span></span>  | <span data-ttu-id="a6620-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="a6620-124">Bearer {code}</span></span>|
| <span data-ttu-id="a6620-125">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="a6620-125">Content-type</span></span>  | <span data-ttu-id="a6620-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a6620-126">application/json</span></span>|


## <a name="request-body"></a><span data-ttu-id="a6620-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6620-127">Request body</span></span>
<span data-ttu-id="a6620-128">En el cuerpo de la solicitud, proporciona los valores para [governanceRuleSettings](../resources/governancerulesetting.md) que necesitan actualizarse.</span><span class="sxs-lookup"><span data-stu-id="a6620-128">In the request body, supply the values for [governanceRuleSettings](../resources/governancerulesetting.md) that need to be updated.</span></span> 

| <span data-ttu-id="a6620-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6620-129">Property</span></span>     | <span data-ttu-id="a6620-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6620-130">Type</span></span>   |<span data-ttu-id="a6620-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6620-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a6620-132">adminEligibleSettings</span><span class="sxs-lookup"><span data-stu-id="a6620-132">adminEligibleSettings</span></span>|[<span data-ttu-id="a6620-133">governanceRuleSetting</span><span class="sxs-lookup"><span data-stu-id="a6620-133">governanceRuleSetting</span></span>](../resources/governancerulesetting.md)|<span data-ttu-id="a6620-134">La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol aptos.</span><span class="sxs-lookup"><span data-stu-id="a6620-134">The rule settings that are evaluated when an administrator tries to add an eligible role assignment.</span></span>|
|<span data-ttu-id="a6620-135">adminMemberSettings</span><span class="sxs-lookup"><span data-stu-id="a6620-135">adminMemberSettings</span></span>|[<span data-ttu-id="a6620-136">governanceRuleSetting</span><span class="sxs-lookup"><span data-stu-id="a6620-136">governanceRuleSetting</span></span>](../resources/governancerulesetting.md)|<span data-ttu-id="a6620-137">La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol miembro directo.</span><span class="sxs-lookup"><span data-stu-id="a6620-137">The rule settings that are evaluated when an administrator tries to add a direct member role assignment.</span></span>|
|<span data-ttu-id="a6620-138">userEligibleSettings</span><span class="sxs-lookup"><span data-stu-id="a6620-138">userEligibleSettings</span></span>|[<span data-ttu-id="a6620-139">governanceRuleSetting</span><span class="sxs-lookup"><span data-stu-id="a6620-139">governanceRuleSetting</span></span>](../resources/governancerulesetting.md)|<span data-ttu-id="a6620-140">La configuración de la regla que se evalúa cuando un usuario intenta agregar una asignación de rol optan.</span><span class="sxs-lookup"><span data-stu-id="a6620-140">The rule settings that are evaluated when a user tries to add an eligible role assignment.</span></span> <span data-ttu-id="a6620-141">Esto no es compatible con `pimforazurerbac` escenario por ahora y pueden estar disponibles en las situaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="a6620-141">This is not supported for `pimforazurerbac` scenario for now, and may be available in the future scenarios.</span></span>|
|<span data-ttu-id="a6620-142">userMemberSettings</span><span class="sxs-lookup"><span data-stu-id="a6620-142">userMemberSettings</span></span>|[<span data-ttu-id="a6620-143">governanceRuleSetting</span><span class="sxs-lookup"><span data-stu-id="a6620-143">governanceRuleSetting</span></span>](../resources/governancerulesetting.md)|<span data-ttu-id="a6620-144">La configuración de la regla que se evalúa cuando un usuario intenta activar su asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="a6620-144">The rule settings that are evaluated when a user tries to activate his role assignment.</span></span>|

## <a name="response"></a><span data-ttu-id="a6620-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6620-145">Response</span></span>
<span data-ttu-id="a6620-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 NoContent`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6620-p104">If successful, this method returns a `204 NoContent` response code. It does not return anything in the response body.</span></span> 

### <a name="error-codes"></a><span data-ttu-id="a6620-148">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a6620-148">Error codes</span></span>
<span data-ttu-id="a6620-149">Esta API devuelve los códigos de error HTTP estándares.</span><span class="sxs-lookup"><span data-stu-id="a6620-149">This API returns the standard HTTP error codes.</span></span> <span data-ttu-id="a6620-150">Además, devuelve los siguientes códigos de error personalizado.</span><span class="sxs-lookup"><span data-stu-id="a6620-150">In addition, it returns the following custom error codes.</span></span>

|<span data-ttu-id="a6620-151">Código de error</span><span class="sxs-lookup"><span data-stu-id="a6620-151">Error code</span></span>     | <span data-ttu-id="a6620-152">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="a6620-152">Error message</span></span>         | <span data-ttu-id="a6620-153">Detalles</span><span class="sxs-lookup"><span data-stu-id="a6620-153">Details</span></span>             |
|:--------------| :---------------------|:--------------------|
| <span data-ttu-id="a6620-154">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="a6620-154">400 BadRequest</span></span>| <span data-ttu-id="a6620-155">RoleSettingNotFound</span><span class="sxs-lookup"><span data-stu-id="a6620-155">RoleSettingNotFound</span></span>   | <span data-ttu-id="a6620-156">La [governanceRoleSetting](../resources/governancerolesetting.md) no existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a6620-156">The [governanceRoleSetting](../resources/governancerolesetting.md) does not exist in system.</span></span>
| <span data-ttu-id="a6620-157">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="a6620-157">400 BadRequest</span></span>| <span data-ttu-id="a6620-158">InvalidRoleSetting</span><span class="sxs-lookup"><span data-stu-id="a6620-158">InvalidRoleSetting</span></span>    | <span data-ttu-id="a6620-159">Los valores de [governanceRuleSettings](../resources/governancerulesetting.md) proporcionados en el cuerpo de la solicitud no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a6620-159">The [governanceRuleSettings](../resources/governancerulesetting.md) values provided in the request body are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="a6620-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6620-160">Example</span></span> 
<span data-ttu-id="a6620-161">En este ejemplo se actualiza la configuración de rol para 3 de rol personalizada en la suscripción Wingtip Toys - Prod.</span><span class="sxs-lookup"><span data-stu-id="a6620-161">This example updates the role setting for Custom Role 3 in the subscription Wingtip Toys - Prod.</span></span>
##### <a name="request"></a><span data-ttu-id="a6620-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6620-162">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "update_governancerolesetting"
}-->
```http
PATCH https://graph.microsoft.com/beta/privilegedAccess/pimforazurerbac/roleSettings/5fb5aef8-1081-4b8e-bb16-9d5d0385bab5
Content-type: application/json
Content-length: 350

{
  "adminEligibleSettings":[{"ruleIdentifier":"ExpirationRule","setting":"{\"permanentAssignment\":false,\"maximumGrantPeriodInMinutes\":129600}"}]
}
```
##### <a name="response"></a><span data-ttu-id="a6620-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6620-163">Response</span></span>
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update governanceRoleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
