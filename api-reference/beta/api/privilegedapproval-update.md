---
title: Actualizar privilegedapproval
description: Actualizar las propiedades del objeto privilegedapproval.
ms.openlocfilehash: 566351ba89d0173718320640e6fa45b0650aaf0e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084331"
---
# <a name="update-privilegedapproval"></a><span data-ttu-id="be342-103">Actualizar privilegedapproval</span><span class="sxs-lookup"><span data-stu-id="be342-103">Update privilegedapproval</span></span>

> <span data-ttu-id="be342-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="be342-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="be342-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="be342-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="be342-106">Actualizar las propiedades del objeto privilegedapproval.</span><span class="sxs-lookup"><span data-stu-id="be342-106">Update the properties of privilegedapproval object.</span></span>
## <a name="permissions"></a><span data-ttu-id="be342-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="be342-107">Permissions</span></span>
<span data-ttu-id="be342-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="be342-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="be342-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="be342-110">Permission type</span></span>      | <span data-ttu-id="be342-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="be342-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="be342-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="be342-112">Delegated (work or school account)</span></span> | <span data-ttu-id="be342-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="be342-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="be342-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="be342-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="be342-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be342-115">Not supported.</span></span>    |
|<span data-ttu-id="be342-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="be342-116">Application</span></span> | <span data-ttu-id="be342-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be342-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="be342-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="be342-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /privilegedApproval/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="be342-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="be342-119">Optional request headers</span></span>
| <span data-ttu-id="be342-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="be342-120">Name</span></span>       | <span data-ttu-id="be342-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="be342-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="be342-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="be342-122">Authorization</span></span>  | <span data-ttu-id="be342-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="be342-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="be342-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="be342-125">Request body</span></span>
<span data-ttu-id="be342-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="be342-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="be342-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be342-129">Property</span></span>     | <span data-ttu-id="be342-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="be342-130">Type</span></span>   |<span data-ttu-id="be342-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="be342-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="be342-132">approvalDuration</span><span class="sxs-lookup"><span data-stu-id="be342-132">approvalDuration</span></span>|<span data-ttu-id="be342-133">Duración</span><span class="sxs-lookup"><span data-stu-id="be342-133">Duration</span></span>||
|<span data-ttu-id="be342-134">approvalState</span><span class="sxs-lookup"><span data-stu-id="be342-134">approvalState</span></span>|<span data-ttu-id="be342-135">string</span><span class="sxs-lookup"><span data-stu-id="be342-135">string</span></span>| <span data-ttu-id="be342-136">Los valores posibles son: `pending`, `approved`, `denied`, `aborted` y `canceled`.</span><span class="sxs-lookup"><span data-stu-id="be342-136">Possible values are: `pending`, `approved`, `denied`, `aborted`, `canceled`.</span></span>|
|<span data-ttu-id="be342-137">approvalType</span><span class="sxs-lookup"><span data-stu-id="be342-137">approvalType</span></span>|<span data-ttu-id="be342-138">String</span><span class="sxs-lookup"><span data-stu-id="be342-138">String</span></span>||
|<span data-ttu-id="be342-139">approverReason</span><span class="sxs-lookup"><span data-stu-id="be342-139">approverReason</span></span>|<span data-ttu-id="be342-140">String</span><span class="sxs-lookup"><span data-stu-id="be342-140">String</span></span>||
|<span data-ttu-id="be342-141">endDateTime</span><span class="sxs-lookup"><span data-stu-id="be342-141">endDateTime</span></span>|<span data-ttu-id="be342-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be342-142">DateTimeOffset</span></span>||
|<span data-ttu-id="be342-143">requestorReason</span><span class="sxs-lookup"><span data-stu-id="be342-143">requestorReason</span></span>|<span data-ttu-id="be342-144">String</span><span class="sxs-lookup"><span data-stu-id="be342-144">String</span></span>||
|<span data-ttu-id="be342-145">identificador de función</span><span class="sxs-lookup"><span data-stu-id="be342-145">roleId</span></span>|<span data-ttu-id="be342-146">String</span><span class="sxs-lookup"><span data-stu-id="be342-146">String</span></span>||
|<span data-ttu-id="be342-147">startDateTime</span><span class="sxs-lookup"><span data-stu-id="be342-147">startDateTime</span></span>|<span data-ttu-id="be342-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be342-148">DateTimeOffset</span></span>||
|<span data-ttu-id="be342-149">userId</span><span class="sxs-lookup"><span data-stu-id="be342-149">userId</span></span>|<span data-ttu-id="be342-150">String</span><span class="sxs-lookup"><span data-stu-id="be342-150">String</span></span>||

## <a name="response"></a><span data-ttu-id="be342-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be342-151">Response</span></span>

<span data-ttu-id="be342-152">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [privilegedApproval](../resources/privilegedapproval.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be342-152">If successful, this method returns a `200 OK` response code and updated [privilegedApproval](../resources/privilegedapproval.md) object in the response body.</span></span>

<span data-ttu-id="be342-153">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="be342-153">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="be342-154">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="be342-154">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>

## <a name="example"></a><span data-ttu-id="be342-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be342-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="be342-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be342-156">Request</span></span>
<span data-ttu-id="be342-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="be342-157">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_privilegedapproval"
}-->
```http
PATCH https://graph.microsoft.com/beta/privilegedApproval/<id>
Content-type: application/json
Content-length: 180

{
  "userId": "userId-value",
  "roleId": "roleId-value",
  "approvalType": "approvalType-value",
  "approvalState": "approvalState-value",
  "approvalDuration": "datetime-value"
}
```
##### <a name="response"></a><span data-ttu-id="be342-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be342-158">Response</span></span>
<span data-ttu-id="be342-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="be342-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedApproval"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 200

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "approvalType": "approvalType-value",
  "approvalState": "approvalState-value",
  "approvalDuration": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update privilegedapproval",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
