---
title: 'TableSort: reapply'
description: Vuelve a aplicar los parámetros de ordenación actuales a la tabla.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: f23f0eebbc3354d066b465e8edeaa37be5e5e90d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883730"
---
# <a name="tablesort-reapply"></a><span data-ttu-id="1f94c-103">TableSort: reapply</span><span class="sxs-lookup"><span data-stu-id="1f94c-103">TableSort: reapply</span></span>

<span data-ttu-id="1f94c-104">Vuelve a aplicar los parámetros de ordenación actuales a la tabla.</span><span class="sxs-lookup"><span data-stu-id="1f94c-104">Reapplies the current sorting parameters to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="1f94c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1f94c-105">Permissions</span></span>
<span data-ttu-id="1f94c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1f94c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1f94c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1f94c-108">Permission type</span></span>      | <span data-ttu-id="1f94c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1f94c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1f94c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1f94c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1f94c-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f94c-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1f94c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1f94c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1f94c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f94c-113">Not supported.</span></span>    |
|<span data-ttu-id="1f94c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1f94c-114">Application</span></span> | <span data-ttu-id="1f94c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f94c-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1f94c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1f94c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/reapply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/reapply

```
## <a name="request-headers"></a><span data-ttu-id="1f94c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1f94c-117">Request headers</span></span>
| <span data-ttu-id="1f94c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f94c-118">Name</span></span>       | <span data-ttu-id="1f94c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f94c-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1f94c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1f94c-120">Authorization</span></span>  | <span data-ttu-id="1f94c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f94c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1f94c-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1f94c-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="1f94c-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f94c-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1f94c-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1f94c-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="1f94c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f94c-127">Response</span></span>

<span data-ttu-id="1f94c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f94c-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1f94c-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1f94c-130">Example</span></span>
<span data-ttu-id="1f94c-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1f94c-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1f94c-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1f94c-132">Request</span></span>
<span data-ttu-id="1f94c-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1f94c-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_reapply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/reapply
```

##### <a name="response"></a><span data-ttu-id="1f94c-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f94c-134">Response</span></span>
<span data-ttu-id="1f94c-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f94c-135">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort: reapply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
