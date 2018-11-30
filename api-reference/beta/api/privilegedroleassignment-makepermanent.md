---
title: 'privilegedRoleAssignment: makePermanent'
description: Hacer que la asignación de rol como permanente.
ms.openlocfilehash: 06875fc62539598a5e1e806714fcae3d973ba29c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090832"
---
# <a name="privilegedroleassignment-makepermanent"></a><span data-ttu-id="9f88f-103">privilegedRoleAssignment: makePermanent</span><span class="sxs-lookup"><span data-stu-id="9f88f-103">privilegedRoleAssignment: makePermanent</span></span>

> <span data-ttu-id="9f88f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9f88f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9f88f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9f88f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9f88f-106">Hacer que la asignación de rol como permanente.</span><span class="sxs-lookup"><span data-stu-id="9f88f-106">Make the role assignment as permanent.</span></span>

## <a name="permissions"></a><span data-ttu-id="9f88f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9f88f-107">Permissions</span></span>
<span data-ttu-id="9f88f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9f88f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="9f88f-110">El inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="9f88f-110">The tenant needs to be registered to PIM.</span></span> <span data-ttu-id="9f88f-111">De lo contrario, se devolverá error HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="9f88f-111">Otherwise, HTTP 403 Forbidden error will be returned.</span></span>

<span data-ttu-id="9f88f-112">El solicitante debe tener el rol de _Administrador de roles con privilegios_ .</span><span class="sxs-lookup"><span data-stu-id="9f88f-112">The requestor needs to have _Privileged Role Administrator_ role.</span></span> 

|<span data-ttu-id="9f88f-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f88f-113">Permission type</span></span>      | <span data-ttu-id="9f88f-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f88f-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9f88f-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f88f-115">Delegated (work or school account)</span></span> | <span data-ttu-id="9f88f-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9f88f-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9f88f-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f88f-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9f88f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f88f-118">Not supported.</span></span>    |
|<span data-ttu-id="9f88f-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f88f-119">Application</span></span> | <span data-ttu-id="9f88f-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f88f-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9f88f-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f88f-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignments/{id}/makePermanent
```
## <a name="request-headers"></a><span data-ttu-id="9f88f-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f88f-122">Request headers</span></span>
| <span data-ttu-id="9f88f-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9f88f-123">Name</span></span>       | <span data-ttu-id="9f88f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f88f-124">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9f88f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="9f88f-125">Authorization</span></span>  | <span data-ttu-id="9f88f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9f88f-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9f88f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f88f-128">Request body</span></span>
<span data-ttu-id="9f88f-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9f88f-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9f88f-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9f88f-130">Parameter</span></span>    | <span data-ttu-id="9f88f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f88f-131">Type</span></span>   |<span data-ttu-id="9f88f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f88f-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9f88f-133">motivo</span><span class="sxs-lookup"><span data-stu-id="9f88f-133">reason</span></span>|<span data-ttu-id="9f88f-134">string</span><span class="sxs-lookup"><span data-stu-id="9f88f-134">string</span></span>|<span data-ttu-id="9f88f-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9f88f-135">Optional.</span></span> <span data-ttu-id="9f88f-136">La razón para realizar esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9f88f-136">The reason to make this call.</span></span>|
|<span data-ttu-id="9f88f-137">ticketNumber</span><span class="sxs-lookup"><span data-stu-id="9f88f-137">ticketNumber</span></span>|<span data-ttu-id="9f88f-138">string</span><span class="sxs-lookup"><span data-stu-id="9f88f-138">string</span></span>|<span data-ttu-id="9f88f-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9f88f-139">Optional.</span></span> <span data-ttu-id="9f88f-140">El número de vale que está asociado con esta acción.</span><span class="sxs-lookup"><span data-stu-id="9f88f-140">The ticket number that is associated with this action.</span></span>|
|<span data-ttu-id="9f88f-141">ticketSystem</span><span class="sxs-lookup"><span data-stu-id="9f88f-141">ticketSystem</span></span>|<span data-ttu-id="9f88f-142">string</span><span class="sxs-lookup"><span data-stu-id="9f88f-142">string</span></span>|<span data-ttu-id="9f88f-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9f88f-143">Optional.</span></span> <span data-ttu-id="9f88f-144">El sistema de vale.</span><span class="sxs-lookup"><span data-stu-id="9f88f-144">The ticket system.</span></span>|

## <a name="response"></a><span data-ttu-id="9f88f-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f88f-145">Response</span></span>

<span data-ttu-id="9f88f-146">Si tiene éxito, este método devuelve `200 OK` objeto de código y [privilegedRoleAssignment](../resources/privilegedroleassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f88f-146">If successful, this method returns `200 OK` response code and [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f88f-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f88f-147">Example</span></span>
<span data-ttu-id="9f88f-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9f88f-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9f88f-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f88f-149">Request</span></span>
<span data-ttu-id="9f88f-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9f88f-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "privilegedroleassignment_makepermanent"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignments/{id}/makePermanent
Content-type: application/json
Content-length: 110

{
  "reason": "reason-value",
  "ticketNumber": "ticketNumber-value",
  "ticketSystem": "ticketSystem-value"
}
```

##### <a name="response"></a><span data-ttu-id="9f88f-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f88f-151">Response</span></span>
<span data-ttu-id="9f88f-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f88f-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "privilegedRoleAssignment: makePermanent",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->