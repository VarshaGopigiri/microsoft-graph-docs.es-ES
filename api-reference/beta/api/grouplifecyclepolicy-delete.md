---
title: Eliminar groupLifecyclePolicy
description: Elimina un objeto groupLifecyclePolicy
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: f92a8fbfd0a45abfdfbb1705f99eaa2d7335bc08
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882582"
---
# <a name="delete-grouplifecyclepolicy"></a><span data-ttu-id="222e2-103">Eliminar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="222e2-103">Delete groupLifecyclePolicy</span></span>

> <span data-ttu-id="222e2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="222e2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="222e2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="222e2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="222e2-106">Elimina un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md)</span><span class="sxs-lookup"><span data-stu-id="222e2-106">Deletes a [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="222e2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="222e2-107">Permissions</span></span>

<span data-ttu-id="222e2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="222e2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="222e2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="222e2-110">Permission type</span></span>      | <span data-ttu-id="222e2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="222e2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="222e2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="222e2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="222e2-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="222e2-113">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="222e2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="222e2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="222e2-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="222e2-115">Not supported</span></span> |
|<span data-ttu-id="222e2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="222e2-116">Application</span></span> | <span data-ttu-id="222e2-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="222e2-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="222e2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="222e2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groupLifecyclePolicies/{id}

```

## <a name="request-headers"></a><span data-ttu-id="222e2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="222e2-119">Request headers</span></span>

| <span data-ttu-id="222e2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="222e2-120">Name</span></span> | <span data-ttu-id="222e2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="222e2-121">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="222e2-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="222e2-122">Authorization</span></span> | <span data-ttu-id="222e2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="222e2-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="222e2-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="222e2-125">Content-Type</span></span>  | <span data-ttu-id="222e2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="222e2-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="222e2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="222e2-127">Request body</span></span>
<span data-ttu-id="222e2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="222e2-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="222e2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="222e2-129">Response</span></span>

<span data-ttu-id="222e2-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="222e2-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="222e2-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="222e2-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="222e2-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="222e2-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_grouplifecyclepolicy"
}-->
```http
DELETE https://graph.microsoft.com/beta/groupLifecyclePolicies/{id}
```
##### <a name="response"></a><span data-ttu-id="222e2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="222e2-134">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
