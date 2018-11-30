---
title: 'Table: reapplyFilters'
description: Vuelve a aplicar todos los filtros aplicados actualmente en la tabla.
ms.openlocfilehash: d620eb6840da5e4de2640483bc969d7bd55812f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029548"
---
# <a name="table-reapplyfilters"></a><span data-ttu-id="94dfc-103">Table: reapplyFilters</span><span class="sxs-lookup"><span data-stu-id="94dfc-103">Table: reapplyFilters</span></span>

<span data-ttu-id="94dfc-104">Vuelve a aplicar todos los filtros aplicados actualmente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="94dfc-104">Reapplies all the filters currently on the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="94dfc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="94dfc-105">Permissions</span></span>
<span data-ttu-id="94dfc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="94dfc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="94dfc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="94dfc-108">Permission type</span></span>      | <span data-ttu-id="94dfc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="94dfc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="94dfc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="94dfc-110">Delegated (work or school account)</span></span> | <span data-ttu-id="94dfc-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="94dfc-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="94dfc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="94dfc-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="94dfc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94dfc-113">Not supported.</span></span>    |
|<span data-ttu-id="94dfc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="94dfc-114">Application</span></span> | <span data-ttu-id="94dfc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94dfc-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="94dfc-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="94dfc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/reapplyFilters
POST /workbook/worksheets/{id|name}/tables/{id|name}/reapplyFilters

```
## <a name="request-headers"></a><span data-ttu-id="94dfc-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="94dfc-117">Request headers</span></span>
| <span data-ttu-id="94dfc-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="94dfc-118">Name</span></span>       | <span data-ttu-id="94dfc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="94dfc-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="94dfc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="94dfc-120">Authorization</span></span>  | <span data-ttu-id="94dfc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="94dfc-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="94dfc-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="94dfc-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="94dfc-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="94dfc-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="94dfc-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="94dfc-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="94dfc-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94dfc-127">Response</span></span>

<span data-ttu-id="94dfc-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94dfc-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="94dfc-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94dfc-130">Example</span></span>
<span data-ttu-id="94dfc-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="94dfc-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="94dfc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="94dfc-132">Request</span></span>
<span data-ttu-id="94dfc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="94dfc-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_reapplyfilters"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/reapplyFilters
```

##### <a name="response"></a><span data-ttu-id="94dfc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94dfc-134">Response</span></span>
<span data-ttu-id="94dfc-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94dfc-135">Here is an example of the response.</span></span> 
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
  "description": "Table: reapplyFilters",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->