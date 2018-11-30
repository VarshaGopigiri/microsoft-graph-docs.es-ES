---
title: 'ChartFill: setSolidColor'
description: Establece el formato de relleno de un elemento de gráfico en un color uniforme.
ms.openlocfilehash: bcb8397217ee6cc574fe08f585d51a6243d83ca9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029181"
---
# <a name="chartfill-setsolidcolor"></a><span data-ttu-id="7aafd-103">ChartFill: setSolidColor</span><span class="sxs-lookup"><span data-stu-id="7aafd-103">ChartFill: setSolidColor</span></span>

<span data-ttu-id="7aafd-104">Establece el formato de relleno de un elemento de gráfico en un color uniforme.</span><span class="sxs-lookup"><span data-stu-id="7aafd-104">Sets the fill formatting of a chart element to a uniform color.</span></span>
## <a name="permissions"></a><span data-ttu-id="7aafd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7aafd-105">Permissions</span></span>
<span data-ttu-id="7aafd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7aafd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7aafd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7aafd-108">Permission type</span></span>      | <span data-ttu-id="7aafd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7aafd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7aafd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7aafd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7aafd-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7aafd-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7aafd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7aafd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7aafd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7aafd-113">Not supported.</span></span>    |
|<span data-ttu-id="7aafd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7aafd-114">Application</span></span> | <span data-ttu-id="7aafd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7aafd-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7aafd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7aafd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts/{name}/title/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts/{name}/legend/format/fill/setSolidColor

```
## <a name="request-headers"></a><span data-ttu-id="7aafd-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7aafd-117">Request headers</span></span>
| <span data-ttu-id="7aafd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="7aafd-118">Name</span></span>       | <span data-ttu-id="7aafd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aafd-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7aafd-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="7aafd-120">Authorization</span></span>  | <span data-ttu-id="7aafd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7aafd-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7aafd-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="7aafd-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="7aafd-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7aafd-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7aafd-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7aafd-126">Request body</span></span>
<span data-ttu-id="7aafd-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7aafd-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7aafd-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7aafd-128">Parameter</span></span>    | <span data-ttu-id="7aafd-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7aafd-129">Type</span></span>   |<span data-ttu-id="7aafd-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aafd-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7aafd-131">color</span><span class="sxs-lookup"><span data-stu-id="7aafd-131">color</span></span>|<span data-ttu-id="7aafd-132">string</span><span class="sxs-lookup"><span data-stu-id="7aafd-132">string</span></span>|<span data-ttu-id="7aafd-133">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="7aafd-133">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|

## <a name="response"></a><span data-ttu-id="7aafd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7aafd-134">Response</span></span>

<span data-ttu-id="7aafd-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7aafd-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7aafd-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7aafd-137">Example</span></span>
<span data-ttu-id="7aafd-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7aafd-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="7aafd-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7aafd-139">Request</span></span>
<span data-ttu-id="7aafd-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7aafd-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_setsolidcolor"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/format/fill/setSolidColor
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```

##### <a name="response"></a><span data-ttu-id="7aafd-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7aafd-141">Response</span></span>
<span data-ttu-id="7aafd-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7aafd-142">Here is an example of the response.</span></span> 
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
  "description": "ChartFill: setSolidColor",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->