---
title: 'Range: clear'
description: Borrar valores de rango, formato, relleno, borde, etc.
localization_priority: Normal
ms.openlocfilehash: 8bf7bafd42947528c98a83819afd7b16f49d2e7d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861918"
---
# <a name="range-clear"></a><span data-ttu-id="af2e6-103">Range: clear</span><span class="sxs-lookup"><span data-stu-id="af2e6-103">Range: clear</span></span>

<span data-ttu-id="af2e6-104">Borrar valores de rango, formato, relleno, borde, etc.</span><span class="sxs-lookup"><span data-stu-id="af2e6-104">Clear range values, format, fill, border, etc.</span></span>
## <a name="permissions"></a><span data-ttu-id="af2e6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="af2e6-105">Permissions</span></span>
<span data-ttu-id="af2e6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="af2e6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="af2e6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="af2e6-108">Permission type</span></span>      | <span data-ttu-id="af2e6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="af2e6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="af2e6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="af2e6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="af2e6-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="af2e6-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="af2e6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="af2e6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="af2e6-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="af2e6-113">Not supported.</span></span>    |
|<span data-ttu-id="af2e6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="af2e6-114">Application</span></span> | <span data-ttu-id="af2e6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="af2e6-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="af2e6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="af2e6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/clear
POST /workbook/worksheets/{id|name}/range(address='<address>')/clear
POST /workbook/tables/{id|name}/columns/{id|name}/range/clear

```
## <a name="request-headers"></a><span data-ttu-id="af2e6-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="af2e6-117">Request headers</span></span>
| <span data-ttu-id="af2e6-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="af2e6-118">Name</span></span>       | <span data-ttu-id="af2e6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="af2e6-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="af2e6-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="af2e6-120">Authorization</span></span>  | <span data-ttu-id="af2e6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="af2e6-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="af2e6-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="af2e6-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="af2e6-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="af2e6-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="af2e6-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="af2e6-126">Request body</span></span>
<span data-ttu-id="af2e6-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="af2e6-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="af2e6-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="af2e6-128">Parameter</span></span>    | <span data-ttu-id="af2e6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="af2e6-129">Type</span></span>   |<span data-ttu-id="af2e6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="af2e6-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="af2e6-131">applyTo</span><span class="sxs-lookup"><span data-stu-id="af2e6-131">applyTo</span></span>|<span data-ttu-id="af2e6-132">string</span><span class="sxs-lookup"><span data-stu-id="af2e6-132">string</span></span>|<span data-ttu-id="af2e6-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="af2e6-133">Optional.</span></span> <span data-ttu-id="af2e6-134">Determina el tipo de acción Borrar.</span><span class="sxs-lookup"><span data-stu-id="af2e6-134">Determines the type of clear action.</span></span>  <span data-ttu-id="af2e6-135">Los valores posibles son: `All`, `Formats`, `Contents`.</span><span class="sxs-lookup"><span data-stu-id="af2e6-135">The possible values are: `All`, `Formats`, `Contents`.</span></span>|

## <a name="response"></a><span data-ttu-id="af2e6-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af2e6-136">Response</span></span>

<span data-ttu-id="af2e6-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="af2e6-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="af2e6-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af2e6-139">Example</span></span>
<span data-ttu-id="af2e6-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="af2e6-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="af2e6-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="af2e6-141">Request</span></span>
<span data-ttu-id="af2e6-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="af2e6-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="af2e6-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af2e6-143">Response</span></span>
<span data-ttu-id="af2e6-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="af2e6-144">Here is an example of the response.</span></span> 
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
