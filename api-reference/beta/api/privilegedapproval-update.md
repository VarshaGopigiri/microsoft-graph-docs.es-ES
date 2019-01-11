---
title: Actualizar privilegedapproval
description: Actualizar las propiedades del objeto privilegedapproval.
localization_priority: Normal
ms.openlocfilehash: 0ddab7d7a628be8513c27114e1e4ec3d13477784
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866888"
---
# <a name="update-privilegedapproval"></a><span data-ttu-id="6c958-103">Actualizar privilegedapproval</span><span class="sxs-lookup"><span data-stu-id="6c958-103">Update privilegedapproval</span></span>

> <span data-ttu-id="6c958-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6c958-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6c958-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6c958-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6c958-106">Actualizar las propiedades del objeto privilegedapproval.</span><span class="sxs-lookup"><span data-stu-id="6c958-106">Update the properties of privilegedapproval object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6c958-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6c958-107">Permissions</span></span>
<span data-ttu-id="6c958-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6c958-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="6c958-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c958-110">Permission type</span></span>      | <span data-ttu-id="6c958-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c958-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6c958-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c958-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6c958-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6c958-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6c958-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c958-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6c958-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c958-115">Not supported.</span></span>    |
|<span data-ttu-id="6c958-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c958-116">Application</span></span> | <span data-ttu-id="6c958-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c958-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6c958-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c958-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /privilegedApproval/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="6c958-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="6c958-119">Optional request headers</span></span>
| <span data-ttu-id="6c958-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c958-120">Name</span></span>       | <span data-ttu-id="6c958-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c958-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="6c958-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="6c958-122">Authorization</span></span>  | <span data-ttu-id="6c958-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c958-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6c958-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c958-125">Request body</span></span>
<span data-ttu-id="6c958-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6c958-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6c958-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c958-129">Property</span></span>     | <span data-ttu-id="6c958-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c958-130">Type</span></span>   |<span data-ttu-id="6c958-131">Description</span><span class="sxs-lookup"><span data-stu-id="6c958-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6c958-132">approvalDuration</span><span class="sxs-lookup"><span data-stu-id="6c958-132">approvalDuration</span></span>|<span data-ttu-id="6c958-133">Duración</span><span class="sxs-lookup"><span data-stu-id="6c958-133">Duration</span></span>||
|<span data-ttu-id="6c958-134">approvalState</span><span class="sxs-lookup"><span data-stu-id="6c958-134">approvalState</span></span>|<span data-ttu-id="6c958-135">string</span><span class="sxs-lookup"><span data-stu-id="6c958-135">string</span></span>| <span data-ttu-id="6c958-136">Los valores posibles son: `pending`, `approved`, `denied`, `aborted` y `canceled`.</span><span class="sxs-lookup"><span data-stu-id="6c958-136">Possible values are: `pending`, `approved`, `denied`, `aborted`, `canceled`.</span></span>|
|<span data-ttu-id="6c958-137">approvalType</span><span class="sxs-lookup"><span data-stu-id="6c958-137">approvalType</span></span>|<span data-ttu-id="6c958-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c958-138">String</span></span>||
|<span data-ttu-id="6c958-139">approverReason</span><span class="sxs-lookup"><span data-stu-id="6c958-139">approverReason</span></span>|<span data-ttu-id="6c958-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c958-140">String</span></span>||
|<span data-ttu-id="6c958-141">endDateTime</span><span class="sxs-lookup"><span data-stu-id="6c958-141">endDateTime</span></span>|<span data-ttu-id="6c958-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6c958-142">DateTimeOffset</span></span>||
|<span data-ttu-id="6c958-143">requestorReason</span><span class="sxs-lookup"><span data-stu-id="6c958-143">requestorReason</span></span>|<span data-ttu-id="6c958-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c958-144">String</span></span>||
|<span data-ttu-id="6c958-145">identificador de función</span><span class="sxs-lookup"><span data-stu-id="6c958-145">roleId</span></span>|<span data-ttu-id="6c958-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c958-146">String</span></span>||
|<span data-ttu-id="6c958-147">startDateTime</span><span class="sxs-lookup"><span data-stu-id="6c958-147">startDateTime</span></span>|<span data-ttu-id="6c958-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6c958-148">DateTimeOffset</span></span>||
|<span data-ttu-id="6c958-149">userId</span><span class="sxs-lookup"><span data-stu-id="6c958-149">userId</span></span>|<span data-ttu-id="6c958-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c958-150">String</span></span>||

## <a name="response"></a><span data-ttu-id="6c958-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c958-151">Response</span></span>

<span data-ttu-id="6c958-152">Si tiene éxito, este método devuelve una `204 No Content` código de respuesta</span><span class="sxs-lookup"><span data-stu-id="6c958-152">If successful, this method returns a `204 No Content` response code</span></span>

<span data-ttu-id="6c958-153">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="6c958-153">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="6c958-154">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="6c958-154">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>

## <a name="example"></a><span data-ttu-id="6c958-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c958-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6c958-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c958-156">Request</span></span>
<span data-ttu-id="6c958-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c958-157">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_privilegedapproval"
}-->
```http
PATCH https://graph.microsoft.com/beta/privilegedApproval{request-id}
Content-type: application/json
Content-length: 180

{
  "approvalState": "approvalState-value",
  "approverReason": "approverReason-value"
}
```
##### <a name="response"></a><span data-ttu-id="6c958-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c958-158">Response</span></span>
<span data-ttu-id="6c958-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c958-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedApproval"
} -->
```http
HTTP/1.1 204 No Content
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
