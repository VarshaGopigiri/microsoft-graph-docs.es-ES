---
title: 'groupLifecyclePolicy: renewGroup'
description: Renueva la expiración de un grupo. Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.
ms.openlocfilehash: 13e1713d3d00e7feac0b23eae8a314e55341e20e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085927"
---
# <a name="grouplifecyclepolicy-renewgroup"></a><span data-ttu-id="ae209-104">groupLifecyclePolicy: renewGroup</span><span class="sxs-lookup"><span data-stu-id="ae209-104">groupLifecyclePolicy: renewGroup</span></span>

> <span data-ttu-id="ae209-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ae209-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ae209-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ae209-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ae209-107">Renueva la expiración de un grupo.</span><span class="sxs-lookup"><span data-stu-id="ae209-107">Renews a group's expiration.</span></span> <span data-ttu-id="ae209-108">Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="ae209-108">When a group is renewed, the group expiration is extended by the number of days defined in the policy.</span></span>

> <span data-ttu-id="ae209-109">**Nota:** En la V1.0, [use el recurso de grupo para hacer que las solicitudes de renovar](/graph/api/group-renew?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="ae209-109">**Note:** In V1.0, [use the group resource to make renew requests](/graph/api/group-renew?view=graph-rest-1.0).</span></span>

## <a name="permissions"></a><span data-ttu-id="ae209-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="ae209-110">Permissions</span></span>

<span data-ttu-id="ae209-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ae209-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>
 

|<span data-ttu-id="ae209-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ae209-113">Permission type</span></span>      | <span data-ttu-id="ae209-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ae209-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ae209-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ae209-115">Delegated (work or school account)</span></span> | <span data-ttu-id="ae209-116">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ae209-116">Group.ReadWrite.All or Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="ae209-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ae209-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ae209-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="ae209-118">Not supported</span></span> |
|<span data-ttu-id="ae209-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ae209-119">Application</span></span> | <span data-ttu-id="ae209-120">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ae209-120">Group.ReadWrite.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ae209-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae209-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/renewGroup

```

## <a name="request-headers"></a><span data-ttu-id="ae209-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae209-122">Request headers</span></span>

| <span data-ttu-id="ae209-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae209-123">Name</span></span> | <span data-ttu-id="ae209-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae209-124">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="ae209-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae209-125">Authorization</span></span> | <span data-ttu-id="ae209-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae209-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ae209-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ae209-128">Content-Type</span></span>  | <span data-ttu-id="ae209-129">application/json</span><span class="sxs-lookup"><span data-stu-id="ae209-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="ae209-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae209-130">Request body</span></span>
<span data-ttu-id="ae209-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ae209-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ae209-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ae209-132">Parameter</span></span> | <span data-ttu-id="ae209-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae209-133">Type</span></span> | <span data-ttu-id="ae209-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae209-134">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="ae209-135">groupId</span><span class="sxs-lookup"><span data-stu-id="ae209-135">groupId</span></span>|<span data-ttu-id="ae209-136">Guid</span><span class="sxs-lookup"><span data-stu-id="ae209-136">Guid</span></span>| <span data-ttu-id="ae209-137">El identificador del grupo renovar.</span><span class="sxs-lookup"><span data-stu-id="ae209-137">The id of the group to renew.</span></span> |

## <a name="response"></a><span data-ttu-id="ae209-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae209-138">Response</span></span>

<span data-ttu-id="ae209-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae209-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ae209-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae209-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ae209-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae209-142">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "grouplifecyclepolicy_renewgroup"
}-->
```http
POST https://graph.microsoft.com/beta/groupLifecyclePolicies/renewGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

##### <a name="response"></a><span data-ttu-id="ae209-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae209-143">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy: renewgroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->