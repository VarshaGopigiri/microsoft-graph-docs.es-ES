---
title: 'groupLifecyclePolicy: addGroup'
description: Agrega un grupo a una directiva de ciclo de vida.
author: dkershaw10
ms.openlocfilehash: 1ee36dd824d41c0a37c818d1e42e29a912857d20
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321150"
---
# <a name="grouplifecyclepolicy-addgroup"></a><span data-ttu-id="d41e8-103">groupLifecyclePolicy: addGroup</span><span class="sxs-lookup"><span data-stu-id="d41e8-103">groupLifecyclePolicy: addGroup</span></span>

<span data-ttu-id="d41e8-104">Agrega un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="d41e8-104">Adds a group to a lifecycle policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="d41e8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d41e8-105">Permissions</span></span>

<span data-ttu-id="d41e8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d41e8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="d41e8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d41e8-108">Permission type</span></span>      | <span data-ttu-id="d41e8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d41e8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d41e8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d41e8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d41e8-111">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d41e8-111">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="d41e8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d41e8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d41e8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d41e8-113">Not supported.</span></span>    |
|<span data-ttu-id="d41e8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d41e8-114">Application</span></span> | <span data-ttu-id="d41e8-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d41e8-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d41e8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d41e8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/addGroup
```

## <a name="request-headers"></a><span data-ttu-id="d41e8-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d41e8-117">Request headers</span></span>

| <span data-ttu-id="d41e8-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d41e8-118">Name</span></span> | <span data-ttu-id="d41e8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d41e8-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d41e8-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d41e8-120">Authorization</span></span> | <span data-ttu-id="d41e8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d41e8-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d41e8-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d41e8-123">Content-Type</span></span>  | <span data-ttu-id="d41e8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d41e8-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d41e8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d41e8-125">Request body</span></span>
<span data-ttu-id="d41e8-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d41e8-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d41e8-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d41e8-127">Parameter</span></span> | <span data-ttu-id="d41e8-128">Type</span><span class="sxs-lookup"><span data-stu-id="d41e8-128">Type</span></span> | <span data-ttu-id="d41e8-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="d41e8-129">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="d41e8-130">groupId</span><span class="sxs-lookup"><span data-stu-id="d41e8-130">groupId</span></span>|<span data-ttu-id="d41e8-131">Guid</span><span class="sxs-lookup"><span data-stu-id="d41e8-131">Guid</span></span>| <span data-ttu-id="d41e8-132">El id. del grupo para agregar a la directiva.</span><span class="sxs-lookup"><span data-stu-id="d41e8-132">The id of the group to add to the policy.</span></span> |

## <a name="response"></a><span data-ttu-id="d41e8-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d41e8-133">Response</span></span>

<span data-ttu-id="d41e8-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="d41e8-134">If successful, this method returns `200 OK` response code.</span></span> <span data-ttu-id="d41e8-135">Si el grupo se agrega a la directiva, se devuelve un valor **true** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d41e8-135">If the group is added to the policy, a **true** value is returned in the response body.</span></span> <span data-ttu-id="d41e8-136">En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d41e8-136">Otherwise, a **false** value is returned in the reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="d41e8-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d41e8-137">Example</span></span>

#### <a name="request"></a><span data-ttu-id="d41e8-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d41e8-138">Request</span></span>

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

#### <a name="response"></a><span data-ttu-id="d41e8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d41e8-139">Response</span></span>
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