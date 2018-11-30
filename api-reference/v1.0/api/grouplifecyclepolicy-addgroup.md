---
title: 'groupLifecyclePolicy: addGroup'
description: Agrega un grupo a una directiva de ciclo de vida.
ms.openlocfilehash: efcb7a29814049ba6e7c5d063c6744e5a3646b67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030724"
---
# <a name="grouplifecyclepolicy-addgroup"></a><span data-ttu-id="e6c02-103">groupLifecyclePolicy: addGroup</span><span class="sxs-lookup"><span data-stu-id="e6c02-103">groupLifecyclePolicy: addGroup</span></span>

<span data-ttu-id="e6c02-104">Agrega un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="e6c02-104">Adds a group to a lifecycle policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="e6c02-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e6c02-105">Permissions</span></span>

<span data-ttu-id="e6c02-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6c02-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="e6c02-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6c02-108">Permission type</span></span>      | <span data-ttu-id="e6c02-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6c02-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e6c02-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6c02-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e6c02-111">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6c02-111">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="e6c02-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6c02-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e6c02-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6c02-113">Not supported.</span></span>    |
|<span data-ttu-id="e6c02-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6c02-114">Application</span></span> | <span data-ttu-id="e6c02-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6c02-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e6c02-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6c02-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/addGroup
```

## <a name="request-headers"></a><span data-ttu-id="e6c02-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c02-117">Request headers</span></span>

| <span data-ttu-id="e6c02-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6c02-118">Name</span></span> | <span data-ttu-id="e6c02-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6c02-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="e6c02-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6c02-120">Authorization</span></span> | <span data-ttu-id="e6c02-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e6c02-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e6c02-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e6c02-123">Content-Type</span></span>  | <span data-ttu-id="e6c02-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e6c02-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="e6c02-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c02-125">Request body</span></span>
<span data-ttu-id="e6c02-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e6c02-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e6c02-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e6c02-127">Parameter</span></span> | <span data-ttu-id="e6c02-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6c02-128">Type</span></span> | <span data-ttu-id="e6c02-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6c02-129">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="e6c02-130">groupId</span><span class="sxs-lookup"><span data-stu-id="e6c02-130">groupId</span></span>|<span data-ttu-id="e6c02-131">Guid</span><span class="sxs-lookup"><span data-stu-id="e6c02-131">Guid</span></span>| <span data-ttu-id="e6c02-132">El id. del grupo para agregar a la directiva.</span><span class="sxs-lookup"><span data-stu-id="e6c02-132">The id of the group to add to the policy.</span></span> |

## <a name="response"></a><span data-ttu-id="e6c02-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6c02-133">Response</span></span>

<span data-ttu-id="e6c02-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="e6c02-134">If successful, this method returns `200 OK` response code.</span></span> <span data-ttu-id="e6c02-135">Si el grupo se agrega a la directiva, se devuelve un valor **true** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6c02-135">If the group is added to the policy, a **true** value is returned in the response body.</span></span> <span data-ttu-id="e6c02-136">En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6c02-136">Otherwise, a **false** value is returned in the reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="e6c02-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6c02-137">Example</span></span>

#### <a name="request"></a><span data-ttu-id="e6c02-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c02-138">Request</span></span>

<!-- {
  "blockType": "ignored",
  "name": "grouplifecyclepolicy_addgroup"
} -->
```http
POST https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}/addGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

#### <a name="response"></a><span data-ttu-id="e6c02-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6c02-139">Response</span></span>
<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 21

{
  "value": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy: addgroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->