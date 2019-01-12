---
title: 'groupLifecyclePolicy: renewGroup'
description: Renueva la expiración de un grupo. Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 8facbd22887e99fc3b7edcdcb17940d0845cd31d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960410"
---
# <a name="grouplifecyclepolicy-renewgroup"></a><span data-ttu-id="d9475-104">groupLifecyclePolicy: renewGroup</span><span class="sxs-lookup"><span data-stu-id="d9475-104">groupLifecyclePolicy: renewGroup</span></span>

> <span data-ttu-id="d9475-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9475-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9475-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9475-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d9475-107">Renueva la expiración de un grupo.</span><span class="sxs-lookup"><span data-stu-id="d9475-107">Renews a group's expiration.</span></span> <span data-ttu-id="d9475-108">Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="d9475-108">When a group is renewed, the group expiration is extended by the number of days defined in the policy.</span></span>

> <span data-ttu-id="d9475-109">**Nota:** En la V1.0, [use el recurso de grupo para hacer que las solicitudes de renovar](/graph/api/group-renew?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="d9475-109">**Note:** In V1.0, [use the group resource to make renew requests](/graph/api/group-renew?view=graph-rest-1.0).</span></span>

## <a name="permissions"></a><span data-ttu-id="d9475-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="d9475-110">Permissions</span></span>

<span data-ttu-id="d9475-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d9475-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>
 

|<span data-ttu-id="d9475-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d9475-113">Permission type</span></span>      | <span data-ttu-id="d9475-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d9475-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d9475-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d9475-115">Delegated (work or school account)</span></span> | <span data-ttu-id="d9475-116">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9475-116">Group.ReadWrite.All or Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="d9475-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d9475-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d9475-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9475-118">Not supported</span></span> |
|<span data-ttu-id="d9475-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d9475-119">Application</span></span> | <span data-ttu-id="d9475-120">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9475-120">Group.ReadWrite.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9475-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9475-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/renewGroup

```

## <a name="request-headers"></a><span data-ttu-id="d9475-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9475-122">Request headers</span></span>

| <span data-ttu-id="d9475-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9475-123">Name</span></span> | <span data-ttu-id="d9475-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9475-124">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d9475-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9475-125">Authorization</span></span> | <span data-ttu-id="d9475-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9475-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d9475-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d9475-128">Content-Type</span></span>  | <span data-ttu-id="d9475-129">application/json</span><span class="sxs-lookup"><span data-stu-id="d9475-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d9475-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9475-130">Request body</span></span>
<span data-ttu-id="d9475-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d9475-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d9475-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d9475-132">Parameter</span></span> | <span data-ttu-id="d9475-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9475-133">Type</span></span> | <span data-ttu-id="d9475-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9475-134">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="d9475-135">groupId</span><span class="sxs-lookup"><span data-stu-id="d9475-135">groupId</span></span>|<span data-ttu-id="d9475-136">Guid</span><span class="sxs-lookup"><span data-stu-id="d9475-136">Guid</span></span>| <span data-ttu-id="d9475-137">El identificador del grupo renovar.</span><span class="sxs-lookup"><span data-stu-id="d9475-137">The id of the group to renew.</span></span> |

## <a name="response"></a><span data-ttu-id="d9475-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9475-138">Response</span></span>

<span data-ttu-id="d9475-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9475-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9475-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9475-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d9475-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9475-142">Request</span></span>

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

##### <a name="response"></a><span data-ttu-id="d9475-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9475-143">Response</span></span>

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
