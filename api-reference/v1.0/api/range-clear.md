---
title: 'Range: clear'
description: Borrar valores de rango, formato, relleno, borde, etc.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 00dfabae88554d94d068fcb81f74601583e817a7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926368"
---
# <a name="range-clear"></a><span data-ttu-id="f6048-103">Range: clear</span><span class="sxs-lookup"><span data-stu-id="f6048-103">Range: clear</span></span>

<span data-ttu-id="f6048-104">Borrar valores de rango, formato, relleno, borde, etc.</span><span class="sxs-lookup"><span data-stu-id="f6048-104">Clear range values, format, fill, border, etc.</span></span>
## <a name="permissions"></a><span data-ttu-id="f6048-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f6048-105">Permissions</span></span>
<span data-ttu-id="f6048-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6048-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f6048-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6048-108">Permission type</span></span>      | <span data-ttu-id="f6048-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6048-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f6048-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6048-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f6048-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f6048-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f6048-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6048-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f6048-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6048-113">Not supported.</span></span>    |
|<span data-ttu-id="f6048-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6048-114">Application</span></span> | <span data-ttu-id="f6048-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6048-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f6048-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6048-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/clear
POST /workbook/worksheets/{id|name}/range(address='<address>')/clear
POST /workbook/tables/{id|name}/columns/{id|name}/range/clear

```
## <a name="request-headers"></a><span data-ttu-id="f6048-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6048-117">Request headers</span></span>
| <span data-ttu-id="f6048-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f6048-118">Name</span></span>       | <span data-ttu-id="f6048-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6048-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f6048-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f6048-120">Authorization</span></span>  | <span data-ttu-id="f6048-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6048-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f6048-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f6048-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="f6048-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f6048-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f6048-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6048-126">Request body</span></span>
<span data-ttu-id="f6048-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f6048-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f6048-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f6048-128">Parameter</span></span>    | <span data-ttu-id="f6048-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6048-129">Type</span></span>   |<span data-ttu-id="f6048-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6048-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f6048-131">applyTo</span><span class="sxs-lookup"><span data-stu-id="f6048-131">applyTo</span></span>|<span data-ttu-id="f6048-132">string</span><span class="sxs-lookup"><span data-stu-id="f6048-132">string</span></span>|<span data-ttu-id="f6048-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f6048-133">Optional.</span></span> <span data-ttu-id="f6048-134">Determina el tipo de acción Borrar.</span><span class="sxs-lookup"><span data-stu-id="f6048-134">Determines the type of clear action.</span></span>  <span data-ttu-id="f6048-135">Los valores posibles son: `All`, `Formats`, `Contents`.</span><span class="sxs-lookup"><span data-stu-id="f6048-135">The possible values are: `All`, `Formats`, `Contents`.</span></span>|

## <a name="response"></a><span data-ttu-id="f6048-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6048-136">Response</span></span>

<span data-ttu-id="f6048-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6048-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f6048-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6048-139">Example</span></span>
<span data-ttu-id="f6048-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f6048-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f6048-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6048-141">Request</span></span>
<span data-ttu-id="f6048-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6048-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/clear
Content-type: application/json
Content-length: 32

{
  "applyTo": "applyTo-value"
}
```

##### <a name="response"></a><span data-ttu-id="f6048-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6048-143">Response</span></span>
<span data-ttu-id="f6048-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6048-144">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
