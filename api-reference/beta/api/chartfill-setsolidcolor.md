---
title: 'ChartFill: setSolidColor'
description: Establece el formato de relleno de un elemento de gráfico en un color uniforme.
author: lumine2008
ms.openlocfilehash: e33c7a4740b332a8827a4d64a54f2b816c8a1b16
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302810"
---
# <a name="chartfill-setsolidcolor"></a><span data-ttu-id="9db98-103">ChartFill: setSolidColor</span><span class="sxs-lookup"><span data-stu-id="9db98-103">ChartFill: setSolidColor</span></span>

> <span data-ttu-id="9db98-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9db98-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9db98-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9db98-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9db98-106">Establece el formato de relleno de un elemento de gráfico en un color uniforme.</span><span class="sxs-lookup"><span data-stu-id="9db98-106">Sets the fill formatting of a chart element to a uniform color.</span></span>
## <a name="permissions"></a><span data-ttu-id="9db98-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9db98-107">Permissions</span></span>
<span data-ttu-id="9db98-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9db98-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9db98-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9db98-110">Permission type</span></span>      | <span data-ttu-id="9db98-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9db98-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9db98-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9db98-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9db98-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9db98-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9db98-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9db98-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9db98-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9db98-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9db98-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9db98-116">Application</span></span> | <span data-ttu-id="9db98-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9db98-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9db98-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9db98-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/title/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/legend/format/fill/setSolidColor

```
## <a name="request-headers"></a><span data-ttu-id="9db98-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9db98-119">Request headers</span></span>
| <span data-ttu-id="9db98-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9db98-120">Name</span></span>       | <span data-ttu-id="9db98-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9db98-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9db98-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="9db98-122">Authorization</span></span>  | <span data-ttu-id="9db98-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9db98-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9db98-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9db98-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="9db98-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="9db98-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9db98-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9db98-128">Request body</span></span>
<span data-ttu-id="9db98-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9db98-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9db98-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9db98-130">Parameter</span></span>    | <span data-ttu-id="9db98-131">Type</span><span class="sxs-lookup"><span data-stu-id="9db98-131">Type</span></span>   |<span data-ttu-id="9db98-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9db98-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9db98-133">color</span><span class="sxs-lookup"><span data-stu-id="9db98-133">color</span></span>|<span data-ttu-id="9db98-134">string</span><span class="sxs-lookup"><span data-stu-id="9db98-134">string</span></span>|<span data-ttu-id="9db98-135">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="9db98-135">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|

## <a name="response"></a><span data-ttu-id="9db98-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9db98-136">Response</span></span>

<span data-ttu-id="9db98-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9db98-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9db98-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9db98-139">Example</span></span>
<span data-ttu-id="9db98-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9db98-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9db98-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9db98-141">Request</span></span>
<span data-ttu-id="9db98-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9db98-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_setsolidcolor"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```

##### <a name="response"></a><span data-ttu-id="9db98-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9db98-143">Response</span></span>
<span data-ttu-id="9db98-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9db98-144">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
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