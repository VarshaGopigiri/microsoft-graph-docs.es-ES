---
title: 'privilegedRole: selfActivate'
description: Activar la función que se asigna al solicitante.
ms.openlocfilehash: bff445bf1fa5d7c0dfbce080b4361b0479b7dcb7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089166"
---
# <a name="privilegedrole-selfactivate"></a><span data-ttu-id="3a7c3-103">privilegedRole: selfActivate</span><span class="sxs-lookup"><span data-stu-id="3a7c3-103">privilegedRole: selfActivate</span></span>

><span data-ttu-id="3a7c3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3a7c3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3a7c3-106">Activar la función que se asigna al solicitante.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-106">Activate the role that is assigned to the requester.</span></span>

><span data-ttu-id="3a7c3-107">**Nota:** De 2018 eficaz de diciembre, esta API ya no se admite y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-107">**Note:** Effective December 2018, this API will no longer be supported and should not be used.</span></span> <span data-ttu-id="3a7c3-108">Utilice la [PrivilegedRoleAssignmentRequest crear](privilegedroleassignmentrequest-post.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-108">Use the [Create PrivilegedRoleAssignmentRequest](privilegedroleassignmentrequest-post.md) instead.</span></span>


## <a name="permissions"></a><span data-ttu-id="3a7c3-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="3a7c3-109">Permissions</span></span>
<span data-ttu-id="3a7c3-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3a7c3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="3a7c3-112">El solicitante sólo puede llamar a ```selfActivate``` para la función que se asigna a él.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-112">The requestor can only call ```selfActivate``` for the role that is assigned to him.</span></span>
 

|<span data-ttu-id="3a7c3-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a7c3-113">Permission type</span></span>      | <span data-ttu-id="3a7c3-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a7c3-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3a7c3-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a7c3-115">Delegated (work or school account)</span></span> | <span data-ttu-id="3a7c3-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3a7c3-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="3a7c3-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a7c3-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3a7c3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-118">Not supported.</span></span>    |
|<span data-ttu-id="3a7c3-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a7c3-119">Application</span></span> | <span data-ttu-id="3a7c3-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3a7c3-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a7c3-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoles/{id}/selfActivate
```

<span data-ttu-id="3a7c3-122">Tenga en cuenta que ``<id>`` es el identificador de rol de destino.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-122">Note that ``<id>`` is the target role ID.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3a7c3-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a7c3-123">Request headers</span></span>
| <span data-ttu-id="3a7c3-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="3a7c3-124">Name</span></span>       | <span data-ttu-id="3a7c3-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a7c3-125">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3a7c3-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="3a7c3-126">Authorization</span></span>  | <span data-ttu-id="3a7c3-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3a7c3-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a7c3-129">Request body</span></span>
<span data-ttu-id="3a7c3-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3a7c3-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3a7c3-131">Parameter</span></span>    | <span data-ttu-id="3a7c3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a7c3-132">Type</span></span>   |<span data-ttu-id="3a7c3-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a7c3-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3a7c3-134">motivo</span><span class="sxs-lookup"><span data-stu-id="3a7c3-134">reason</span></span>|<span data-ttu-id="3a7c3-135">string</span><span class="sxs-lookup"><span data-stu-id="3a7c3-135">string</span></span>|<span data-ttu-id="3a7c3-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-136">Optional.</span></span> <span data-ttu-id="3a7c3-137">Descripción sobre el motivo de la activación de este rol.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-137">Description about the reason for this role activation.</span></span>|
|<span data-ttu-id="3a7c3-138">duration</span><span class="sxs-lookup"><span data-stu-id="3a7c3-138">duration</span></span>|<span data-ttu-id="3a7c3-139">string</span><span class="sxs-lookup"><span data-stu-id="3a7c3-139">string</span></span>|<span data-ttu-id="3a7c3-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-140">Optional.</span></span> <span data-ttu-id="3a7c3-141">Los valores válidos podrían ser ```min``` (duración de activación mínimo), ```default``` (duración predeterminada de activación para el rol), o un valor de tipo double para especificar cuántas horas es la activación.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-141">Valid values could be ```min``` (minimal activation duration), ```default``` (default activation duration for the role), or a double value to specify how many hours is the activation.</span></span> <span data-ttu-id="3a7c3-142">La duración especificada no se puede tener más de duración de activación de la función de la configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-142">The specified duration cannot be longer than the role's activation duration from the role setting.</span></span> |
|<span data-ttu-id="3a7c3-143">ticketNumber</span><span class="sxs-lookup"><span data-stu-id="3a7c3-143">ticketNumber</span></span>|<span data-ttu-id="3a7c3-144">string</span><span class="sxs-lookup"><span data-stu-id="3a7c3-144">string</span></span>|<span data-ttu-id="3a7c3-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-145">Optional.</span></span> <span data-ttu-id="3a7c3-146">El número de vale que se usa para realizar un seguimiento de la activación de este rol.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-146">The ticket number that is used to tracking this role activation.</span></span>|
|<span data-ttu-id="3a7c3-147">ticketSystem</span><span class="sxs-lookup"><span data-stu-id="3a7c3-147">ticketSystem</span></span>|<span data-ttu-id="3a7c3-148">string</span><span class="sxs-lookup"><span data-stu-id="3a7c3-148">string</span></span>|<span data-ttu-id="3a7c3-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-149">Optional.</span></span> <span data-ttu-id="3a7c3-150">El sistema de vale.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-150">The ticket system.</span></span>|

## <a name="response"></a><span data-ttu-id="3a7c3-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a7c3-151">Response</span></span>

<span data-ttu-id="3a7c3-152">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [privilegedRoleAssignment](../resources/privilegedroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-152">If successful, this method returns a `200 OK` response code and a [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object in the response body.</span></span>

<span data-ttu-id="3a7c3-153">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-153">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="3a7c3-154">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-154">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="3a7c3-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a7c3-155">Example</span></span>
<span data-ttu-id="3a7c3-156">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-156">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3a7c3-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a7c3-157">Request</span></span>
<span data-ttu-id="3a7c3-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-158">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "privilegedrole_selfactivate"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoles/{id}/selfActivate
Content-type: application/json
Content-length: 142

{
  "reason": "reason-value",
  "duration": "duration-value",
  "ticketNumber": "ticketNumber-value",
  "ticketSystem": "ticketSystem-value"
}
```

##### <a name="response"></a><span data-ttu-id="3a7c3-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a7c3-159">Response</span></span>
<span data-ttu-id="3a7c3-160">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-160">Here is an example of the response.</span></span> 

><span data-ttu-id="3a7c3-p110">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a7c3-p110">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 184

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "isElevated": true,
  "expirationDateTime": "2016-10-19T10:37:00Z",
  "resultMessage": "resultMessage-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRole: selfActivate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
