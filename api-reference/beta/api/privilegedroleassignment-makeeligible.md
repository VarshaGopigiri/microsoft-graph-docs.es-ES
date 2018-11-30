---
title: 'privilegedRoleAssignment: makeEligible'
description: Hacer que la asignación de rol como elegibles. Si la asignación de rol ya tiene derecho a antes de la llamada, no hace nada. Si la asignación de rol es permanente y el solicitante es distinto del usuario de destino, la asignación de roles se convertirán en elegible y se desactivará la función para el usuario de destino. Si el solicitante es el usuario de destino y el rol de administrador de seguridad o con privilegios de administrador de roles, se activará la función de la expiración de forma predeterminada.
ms.openlocfilehash: f39f508c7aeae4d85db92b43f406cd3497533e38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083779"
---
# <a name="privilegedroleassignment-makeeligible"></a><span data-ttu-id="e96fa-106">privilegedRoleAssignment: makeEligible</span><span class="sxs-lookup"><span data-stu-id="e96fa-106">privilegedRoleAssignment: makeEligible</span></span>

> <span data-ttu-id="e96fa-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e96fa-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e96fa-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e96fa-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e96fa-109">Hacer que la asignación de rol como elegibles.</span><span class="sxs-lookup"><span data-stu-id="e96fa-109">Make the role assignment as eligible.</span></span> <span data-ttu-id="e96fa-110">Si la asignación de rol ya tiene derecho a antes de la llamada, no hace nada.</span><span class="sxs-lookup"><span data-stu-id="e96fa-110">If the role assignment is already eligible before the call, it does nothing.</span></span> <span data-ttu-id="e96fa-111">Si la asignación de rol es permanente y el solicitante es distinto del usuario de destino, la asignación de roles se convertirán en elegible y se desactivará la función para el usuario de destino.</span><span class="sxs-lookup"><span data-stu-id="e96fa-111">If the role assignment is permanent and the requestor is different from the target user, the role assignment will become eligible and the role will be deactivated for the target user.</span></span> <span data-ttu-id="e96fa-112">Si el solicitante es el usuario de destino y el rol de administrador de seguridad o con privilegios de administrador de roles, se activará la función de la expiración de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e96fa-112">If the requestor is the target user and the role is Security Administrator or Privileged Role Administrator, the role will be activated with the default expiration.</span></span>

## <a name="permissions"></a><span data-ttu-id="e96fa-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="e96fa-113">Permissions</span></span>
<span data-ttu-id="e96fa-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e96fa-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="e96fa-116">El solicitante debe tener el rol de _Administrador de roles con privilegios_ .</span><span class="sxs-lookup"><span data-stu-id="e96fa-116">The requestor needs to have _Privileged Role Administrator_ role.</span></span> 

|<span data-ttu-id="e96fa-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e96fa-117">Permission type</span></span>      | <span data-ttu-id="e96fa-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e96fa-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e96fa-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e96fa-119">Delegated (work or school account)</span></span> | <span data-ttu-id="e96fa-120">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e96fa-120">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="e96fa-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e96fa-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e96fa-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e96fa-122">Not supported.</span></span>    |
|<span data-ttu-id="e96fa-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e96fa-123">Application</span></span> | <span data-ttu-id="e96fa-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e96fa-124">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e96fa-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e96fa-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignments/{id}/makeEligible
```
## <a name="request-headers"></a><span data-ttu-id="e96fa-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e96fa-126">Request headers</span></span>
| <span data-ttu-id="e96fa-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e96fa-127">Name</span></span>       | <span data-ttu-id="e96fa-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e96fa-128">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e96fa-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="e96fa-129">Authorization</span></span>  | <span data-ttu-id="e96fa-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e96fa-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e96fa-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e96fa-132">Request body</span></span>
<span data-ttu-id="e96fa-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e96fa-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e96fa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e96fa-134">Response</span></span>

<span data-ttu-id="e96fa-135">Si tiene éxito, este método devuelve `200 OK` objeto de código y [privilegedRoleAssignment](../resources/privilegedroleassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e96fa-135">If successful, this method returns `200 OK` response code and [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object in the response body.</span></span>

<span data-ttu-id="e96fa-136">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="e96fa-136">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="e96fa-137">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="e96fa-137">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="e96fa-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e96fa-138">Example</span></span>
<span data-ttu-id="e96fa-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e96fa-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e96fa-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e96fa-140">Request</span></span>
<span data-ttu-id="e96fa-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e96fa-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "privilegedroleassignment_makeeligible"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignments/{id}/makeEligible
```

##### <a name="response"></a><span data-ttu-id="e96fa-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e96fa-142">Response</span></span>
<span data-ttu-id="e96fa-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e96fa-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "privilegedRoleAssignment: makeEligible",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->