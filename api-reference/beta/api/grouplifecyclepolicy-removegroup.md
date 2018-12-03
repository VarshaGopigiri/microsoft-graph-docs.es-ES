---
title: 'groupLifecyclePolicy: removeGroup'
description: Quita un grupo de una directiva de ciclo de vida.
ms.openlocfilehash: 0f136adc35c9dd80c392ce6dabacdb725f245247
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083938"
---
# <a name="grouplifecyclepolicy-removegroup"></a><span data-ttu-id="2ef55-103">groupLifecyclePolicy: removeGroup</span><span class="sxs-lookup"><span data-stu-id="2ef55-103">groupLifecyclePolicy: removeGroup</span></span>

> <span data-ttu-id="2ef55-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ef55-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ef55-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ef55-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2ef55-106">Quita un grupo de una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="2ef55-106">Removes a group from a lifecycle policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="2ef55-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2ef55-107">Permissions</span></span>

<span data-ttu-id="2ef55-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ef55-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2ef55-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ef55-110">Permission type</span></span>      | <span data-ttu-id="2ef55-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ef55-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2ef55-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ef55-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2ef55-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ef55-113">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="2ef55-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ef55-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2ef55-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="2ef55-115">Not supported</span></span> |
|<span data-ttu-id="2ef55-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ef55-116">Application</span></span> |  <span data-ttu-id="2ef55-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ef55-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2ef55-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ef55-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/removeGroup
```

## <a name="request-headers"></a><span data-ttu-id="2ef55-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ef55-119">Request headers</span></span>

| <span data-ttu-id="2ef55-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ef55-120">Name</span></span> | <span data-ttu-id="2ef55-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ef55-121">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="2ef55-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2ef55-122">Authorization</span></span> | <span data-ttu-id="2ef55-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ef55-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2ef55-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2ef55-125">Content-Type</span></span>  | <span data-ttu-id="2ef55-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2ef55-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="2ef55-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ef55-127">Request body</span></span>
<span data-ttu-id="2ef55-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2ef55-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2ef55-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2ef55-129">Parameter</span></span> | <span data-ttu-id="2ef55-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ef55-130">Type</span></span> | <span data-ttu-id="2ef55-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ef55-131">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="2ef55-132">groupId</span><span class="sxs-lookup"><span data-stu-id="2ef55-132">groupId</span></span>|<span data-ttu-id="2ef55-133">Guid</span><span class="sxs-lookup"><span data-stu-id="2ef55-133">Guid</span></span>| <span data-ttu-id="2ef55-134">El id. del grupo para quitar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2ef55-134">The id of the group to remove from the policy.</span></span>|

## <a name="response"></a><span data-ttu-id="2ef55-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ef55-135">Response</span></span>

<span data-ttu-id="2ef55-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="2ef55-136">If successful, this method returns `200 OK` response code.</span></span> <span data-ttu-id="2ef55-137">Si el grupo se quita de la directiva, se devuelve un valor **true** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ef55-137">If the group is removed from the policy, a **true** value is returned in the response body.</span></span> <span data-ttu-id="2ef55-138">En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ef55-138">Otherwise, a **false** value is returned in the reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="2ef55-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ef55-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="2ef55-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ef55-140">Request</span></span>

<!-- {
  "blockType": "ignored",
  "name": "grouplifecyclepolicy_removegroup"
} -->
```http
POST https://graph.microsoft.com/beta/groupLifecyclePolicies/{id}/removeGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

##### <a name="response"></a><span data-ttu-id="2ef55-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ef55-141">Response</span></span>
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