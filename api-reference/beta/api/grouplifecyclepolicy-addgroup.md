---
title: 'groupLifecyclePolicy: addGroup'
description: Agrega un grupo a una directiva de ciclo de vida.
author: dkershaw10
ms.openlocfilehash: 57af4383c471832acbffb4136a057c91a1d061d0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327912"
---
# <a name="grouplifecyclepolicy-addgroup"></a><span data-ttu-id="f4e62-103">groupLifecyclePolicy: addGroup</span><span class="sxs-lookup"><span data-stu-id="f4e62-103">groupLifecyclePolicy: addGroup</span></span>

> <span data-ttu-id="f4e62-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4e62-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4e62-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4e62-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f4e62-106">Agrega un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="f4e62-106">Adds a group to a lifecycle policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="f4e62-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f4e62-107">Permissions</span></span>

<span data-ttu-id="f4e62-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4e62-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="f4e62-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4e62-110">Permission type</span></span>      | <span data-ttu-id="f4e62-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4e62-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f4e62-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4e62-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f4e62-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4e62-113">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="f4e62-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4e62-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f4e62-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="f4e62-115">Not supported</span></span> |
|<span data-ttu-id="f4e62-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4e62-116">Application</span></span> | <span data-ttu-id="f4e62-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4e62-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f4e62-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4e62-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/addGroup
```

## <a name="request-headers"></a><span data-ttu-id="f4e62-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4e62-119">Request headers</span></span>

| <span data-ttu-id="f4e62-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4e62-120">Name</span></span> | <span data-ttu-id="f4e62-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4e62-121">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="f4e62-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f4e62-122">Authorization</span></span> | <span data-ttu-id="f4e62-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f4e62-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f4e62-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f4e62-125">Content-Type</span></span>  | <span data-ttu-id="f4e62-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f4e62-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f4e62-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4e62-127">Request body</span></span>
<span data-ttu-id="f4e62-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f4e62-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f4e62-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f4e62-129">Parameter</span></span> | <span data-ttu-id="f4e62-130">Type</span><span class="sxs-lookup"><span data-stu-id="f4e62-130">Type</span></span> | <span data-ttu-id="f4e62-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4e62-131">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="f4e62-132">groupId</span><span class="sxs-lookup"><span data-stu-id="f4e62-132">groupId</span></span>|<span data-ttu-id="f4e62-133">Guid</span><span class="sxs-lookup"><span data-stu-id="f4e62-133">Guid</span></span>| <span data-ttu-id="f4e62-134">El id. del grupo para agregar a la directiva.</span><span class="sxs-lookup"><span data-stu-id="f4e62-134">The id of the group to add to the policy.</span></span> |

## <a name="response"></a><span data-ttu-id="f4e62-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4e62-135">Response</span></span>

<span data-ttu-id="f4e62-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="f4e62-136">If successful, this method returns `200 OK` response code.</span></span> <span data-ttu-id="f4e62-137">Si el grupo se agrega a la directiva, se devuelve un valor **true** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4e62-137">If the group is added to the policy, a **true** value is returned in the response body.</span></span> <span data-ttu-id="f4e62-138">En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4e62-138">Otherwise, a **false** value is returned in the reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="f4e62-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4e62-139">Example</span></span>

#### <a name="request"></a><span data-ttu-id="f4e62-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4e62-140">Request</span></span>

<!-- {
  "blockType": "ignored",
  "name": "grouplifecyclepolicy_addgroup"
} -->
```http
POST https://graph.microsoft.com/beta/groupLifecyclePolicies/{id}/addGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

#### <a name="response"></a><span data-ttu-id="f4e62-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4e62-141">Response</span></span>
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