---
title: Eliminar una configuración de grupo
description: Elimina una configuración de grupo.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 55a9c1d51e03eaea785d351c0700803915b2fe33
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839070"
---
# <a name="delete-a-group-setting"></a><span data-ttu-id="6507f-103">Eliminar una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="6507f-103">Delete a group setting</span></span>

<span data-ttu-id="6507f-104">Elimina una configuración de grupo.</span><span class="sxs-lookup"><span data-stu-id="6507f-104">Delete a group setting.</span></span>

## <a name="permissions"></a><span data-ttu-id="6507f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6507f-105">Permissions</span></span>

<span data-ttu-id="6507f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6507f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="6507f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6507f-108">Permission type</span></span>      | <span data-ttu-id="6507f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6507f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6507f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6507f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="6507f-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6507f-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6507f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6507f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6507f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6507f-113">Not supported.</span></span>    |
|<span data-ttu-id="6507f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6507f-114">Application</span></span> | <span data-ttu-id="6507f-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6507f-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6507f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6507f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groupSettings/{id}
DELETE /groups/{id}/settings/{id}

```

## <a name="request-headers"></a><span data-ttu-id="6507f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6507f-117">Request headers</span></span>

| <span data-ttu-id="6507f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6507f-118">Name</span></span> | <span data-ttu-id="6507f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6507f-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="6507f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6507f-120">Authorization</span></span>  | <span data-ttu-id="6507f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6507f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6507f-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6507f-123">Content-Type</span></span>  | <span data-ttu-id="6507f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6507f-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="6507f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6507f-125">Request body</span></span>
<span data-ttu-id="6507f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6507f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6507f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6507f-127">Response</span></span>

<span data-ttu-id="6507f-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6507f-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6507f-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6507f-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6507f-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6507f-131">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_groupsetting"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groupSettings/{id}
```
##### <a name="response"></a><span data-ttu-id="6507f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6507f-132">Response</span></span>
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
  "description": "Delete groupSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
