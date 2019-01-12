---
title: Eliminar una configuración de grupo
description: Elimina una configuración de grupo.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 32bdd6b2856a96377859d523767f198779d23497
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936112"
---
# <a name="delete-a-group-setting"></a><span data-ttu-id="ebb5d-103">Eliminar una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="ebb5d-103">Delete a group setting</span></span>

<span data-ttu-id="ebb5d-104">Elimina una configuración de grupo.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-104">Delete a group setting.</span></span>

## <a name="permissions"></a><span data-ttu-id="ebb5d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ebb5d-105">Permissions</span></span>

<span data-ttu-id="ebb5d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ebb5d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="ebb5d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebb5d-108">Permission type</span></span>      | <span data-ttu-id="ebb5d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebb5d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ebb5d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebb5d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ebb5d-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ebb5d-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ebb5d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebb5d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ebb5d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-113">Not supported.</span></span>    |
|<span data-ttu-id="ebb5d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebb5d-114">Application</span></span> | <span data-ttu-id="ebb5d-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ebb5d-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ebb5d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebb5d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groupSettings/{id}
DELETE /groups/{id}/settings/{id}

```

## <a name="request-headers"></a><span data-ttu-id="ebb5d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebb5d-117">Request headers</span></span>

| <span data-ttu-id="ebb5d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ebb5d-118">Name</span></span> | <span data-ttu-id="ebb5d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebb5d-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="ebb5d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ebb5d-120">Authorization</span></span>  | <span data-ttu-id="ebb5d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ebb5d-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ebb5d-123">Content-Type</span></span>  | <span data-ttu-id="ebb5d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ebb5d-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="ebb5d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebb5d-125">Request body</span></span>
<span data-ttu-id="ebb5d-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ebb5d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebb5d-127">Response</span></span>

<span data-ttu-id="ebb5d-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebb5d-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ebb5d-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebb5d-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ebb5d-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebb5d-131">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_groupsetting"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groupSettings/{id}
```
##### <a name="response"></a><span data-ttu-id="ebb5d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebb5d-132">Response</span></span>
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
