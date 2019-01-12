---
title: 'groupLifecyclePolicy: removeGroup'
description: Quita un grupo de una directiva de ciclo de vida.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 7affc1af4fcee76cfa4ff044bc11604247d46762
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919542"
---
# <a name="grouplifecyclepolicy-removegroup"></a><span data-ttu-id="9c0db-103">groupLifecyclePolicy: removeGroup</span><span class="sxs-lookup"><span data-stu-id="9c0db-103">groupLifecyclePolicy: removeGroup</span></span>

<span data-ttu-id="9c0db-104">Quita un grupo de una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="9c0db-104">Removes a group from a lifecycle policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="9c0db-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9c0db-105">Permissions</span></span>

<span data-ttu-id="9c0db-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9c0db-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9c0db-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c0db-108">Permission type</span></span>      | <span data-ttu-id="9c0db-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9c0db-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9c0db-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9c0db-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9c0db-111">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9c0db-111">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="9c0db-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9c0db-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9c0db-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c0db-113">Not supported.</span></span>    |
|<span data-ttu-id="9c0db-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c0db-114">Application</span></span> | <span data-ttu-id="9c0db-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9c0db-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9c0db-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c0db-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/removeGroup
```

## <a name="request-headers"></a><span data-ttu-id="9c0db-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9c0db-117">Request headers</span></span>

| <span data-ttu-id="9c0db-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9c0db-118">Name</span></span> | <span data-ttu-id="9c0db-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c0db-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="9c0db-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="9c0db-120">Authorization</span></span> | <span data-ttu-id="9c0db-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9c0db-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9c0db-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9c0db-123">Content-Type</span></span>  | <span data-ttu-id="9c0db-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9c0db-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="9c0db-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c0db-125">Request body</span></span>
<span data-ttu-id="9c0db-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9c0db-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9c0db-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9c0db-127">Parameter</span></span> | <span data-ttu-id="9c0db-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c0db-128">Type</span></span> | <span data-ttu-id="9c0db-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c0db-129">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="9c0db-130">groupId</span><span class="sxs-lookup"><span data-stu-id="9c0db-130">groupId</span></span>|<span data-ttu-id="9c0db-131">Guid</span><span class="sxs-lookup"><span data-stu-id="9c0db-131">Guid</span></span>| <span data-ttu-id="9c0db-132">El id. del grupo para quitar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="9c0db-132">The id of the group to remove from the policy.</span></span>|

## <a name="response"></a><span data-ttu-id="9c0db-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c0db-133">Response</span></span>

<span data-ttu-id="9c0db-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="9c0db-134">If successful, this method returns `200 OK` response code.</span></span> <span data-ttu-id="9c0db-135">Si el grupo se quita de la directiva, se devuelve un valor **true** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c0db-135">If the group is removed from the policy, a **true** value is returned in the response body.</span></span> <span data-ttu-id="9c0db-136">En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c0db-136">Otherwise, a **false** value is returned in the reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="9c0db-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c0db-137">Example</span></span>

##### <a name="request"></a><span data-ttu-id="9c0db-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c0db-138">Request</span></span>

<!-- {
  "blockType": "ignored",
  "name": "grouplifecyclepolicy_removegroup"
} -->
```http
POST https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}/removeGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

##### <a name="response"></a><span data-ttu-id="9c0db-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c0db-139">Response</span></span>
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
  "description": "groupLifecyclePolicy: removegroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
