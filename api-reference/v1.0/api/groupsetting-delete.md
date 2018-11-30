---
title: Eliminar una configuración de grupo
description: Elimina una configuración de grupo.
ms.openlocfilehash: 1c8a62225497aed066a2a25630103b0ee46b3963
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030025"
---
# <a name="delete-a-group-setting"></a><span data-ttu-id="1ad6b-103">Eliminar una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="1ad6b-103">Delete a group setting</span></span>

<span data-ttu-id="1ad6b-104">Elimina una configuración de grupo.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-104">Delete a group setting.</span></span>

## <a name="permissions"></a><span data-ttu-id="1ad6b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1ad6b-105">Permissions</span></span>

<span data-ttu-id="1ad6b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1ad6b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="1ad6b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ad6b-108">Permission type</span></span>      | <span data-ttu-id="1ad6b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ad6b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1ad6b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ad6b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1ad6b-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="1ad6b-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="1ad6b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ad6b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1ad6b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-113">Not supported.</span></span>    |
|<span data-ttu-id="1ad6b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ad6b-114">Application</span></span> | <span data-ttu-id="1ad6b-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1ad6b-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1ad6b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ad6b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groupSettings/{id}
DELETE /groups/{id}/settings/{id}

```

## <a name="request-headers"></a><span data-ttu-id="1ad6b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ad6b-117">Request headers</span></span>

| <span data-ttu-id="1ad6b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ad6b-118">Name</span></span> | <span data-ttu-id="1ad6b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ad6b-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="1ad6b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1ad6b-120">Authorization</span></span>  | <span data-ttu-id="1ad6b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1ad6b-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1ad6b-123">Content-Type</span></span>  | <span data-ttu-id="1ad6b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1ad6b-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="1ad6b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ad6b-125">Request body</span></span>
<span data-ttu-id="1ad6b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1ad6b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ad6b-127">Response</span></span>

<span data-ttu-id="1ad6b-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1ad6b-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ad6b-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1ad6b-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ad6b-131">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_groupsetting"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groupSettings/{id}
```
##### <a name="response"></a><span data-ttu-id="1ad6b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ad6b-132">Response</span></span>
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