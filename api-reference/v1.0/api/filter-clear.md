---
title: 'Filter: clear'
description: Borrar el filtro de la columna especificada.
ms.openlocfilehash: 85a9249cf70ffdd44b8b84e0d28bec63ca743ca1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030540"
---
# <a name="filter-clear"></a><span data-ttu-id="72c8f-103">Filter: clear</span><span class="sxs-lookup"><span data-stu-id="72c8f-103">Filter: clear</span></span>

<span data-ttu-id="72c8f-104">Borrar el filtro de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="72c8f-104">Clear the filter on the given column.</span></span>
## <a name="permissions"></a><span data-ttu-id="72c8f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="72c8f-105">Permissions</span></span>
<span data-ttu-id="72c8f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="72c8f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="72c8f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72c8f-108">Permission type</span></span>      | <span data-ttu-id="72c8f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72c8f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="72c8f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72c8f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="72c8f-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72c8f-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="72c8f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72c8f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="72c8f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72c8f-113">Not supported.</span></span>    |
|<span data-ttu-id="72c8f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72c8f-114">Application</span></span> | <span data-ttu-id="72c8f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72c8f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="72c8f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72c8f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/filter/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/filter/clear

```
## <a name="request-headers"></a><span data-ttu-id="72c8f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="72c8f-117">Request headers</span></span>
| <span data-ttu-id="72c8f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="72c8f-118">Name</span></span>       | <span data-ttu-id="72c8f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="72c8f-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="72c8f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="72c8f-120">Authorization</span></span>  | <span data-ttu-id="72c8f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="72c8f-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="72c8f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72c8f-123">Request body</span></span>
<span data-ttu-id="72c8f-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="72c8f-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="72c8f-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72c8f-125">Response</span></span>

<span data-ttu-id="72c8f-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72c8f-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="72c8f-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72c8f-128">Example</span></span>
<span data-ttu-id="72c8f-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="72c8f-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="72c8f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72c8f-130">Request</span></span>
<span data-ttu-id="72c8f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="72c8f-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "filter_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/clear
```

##### <a name="response"></a><span data-ttu-id="72c8f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72c8f-132">Response</span></span>
<span data-ttu-id="72c8f-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72c8f-133">Here is an example of the response.</span></span> 
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
  "description": "Filter: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->