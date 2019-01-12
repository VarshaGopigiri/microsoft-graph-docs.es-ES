---
title: 'Chart: setPosition'
description: Coloca el gráfico con respecto a las celdas de la hoja de cálculo.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: dae44414db5a095c4cf12506582a9533972a0373
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941222"
---
# <a name="chart-setposition"></a><span data-ttu-id="22013-103">Chart: setPosition</span><span class="sxs-lookup"><span data-stu-id="22013-103">Chart: setPosition</span></span>

> <span data-ttu-id="22013-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="22013-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="22013-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="22013-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="22013-106">Coloca el gráfico con respecto a las celdas de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="22013-106">Positions the chart relative to cells on the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="22013-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="22013-107">Permissions</span></span>
<span data-ttu-id="22013-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22013-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="22013-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22013-110">Permission type</span></span>      | <span data-ttu-id="22013-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22013-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="22013-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22013-112">Delegated (work or school account)</span></span> | <span data-ttu-id="22013-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="22013-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="22013-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22013-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22013-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="22013-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="22013-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22013-116">Application</span></span> | <span data-ttu-id="22013-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22013-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="22013-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22013-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/setPosition

```
## <a name="request-headers"></a><span data-ttu-id="22013-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="22013-119">Request headers</span></span>
| <span data-ttu-id="22013-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="22013-120">Name</span></span>       | <span data-ttu-id="22013-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="22013-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="22013-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="22013-122">Authorization</span></span>  | <span data-ttu-id="22013-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="22013-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="22013-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="22013-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="22013-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="22013-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="22013-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="22013-128">Request body</span></span>
<span data-ttu-id="22013-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="22013-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="22013-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="22013-130">Parameter</span></span>    | <span data-ttu-id="22013-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="22013-131">Type</span></span>   |<span data-ttu-id="22013-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="22013-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="22013-133">startCell</span><span class="sxs-lookup"><span data-stu-id="22013-133">startCell</span></span>|<span data-ttu-id="22013-134">string</span><span class="sxs-lookup"><span data-stu-id="22013-134">string</span></span>|<span data-ttu-id="22013-p105">Celda de inicio. Aquí es adonde se moverá el gráfico. La celda de inicio es la celda superior izquierda o superior derecha, en función de la configuración del usuario de la presentación de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="22013-p105">The start cell. This is where the chart will be moved to. The start cell is the top-left or top-right cell, depending on the user's right-to-left display settings.</span></span>|
|<span data-ttu-id="22013-138">endCell</span><span class="sxs-lookup"><span data-stu-id="22013-138">endCell</span></span>|<span data-ttu-id="22013-139">string</span><span class="sxs-lookup"><span data-stu-id="22013-139">string</span></span>|<span data-ttu-id="22013-p106">Opcional. Última celda. Si se especifica, el ancho y el alto del gráfico se establecerán de modo que cubran totalmente esta celda o rango.</span><span class="sxs-lookup"><span data-stu-id="22013-p106">Optional. The end cell. If specified, the chart's width and height will be set to fully cover up this cell/range.</span></span>|

## <a name="response"></a><span data-ttu-id="22013-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22013-143">Response</span></span>

<span data-ttu-id="22013-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22013-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="22013-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22013-146">Example</span></span>
<span data-ttu-id="22013-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="22013-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="22013-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22013-148">Request</span></span>
<span data-ttu-id="22013-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22013-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setposition"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/setPosition
Content-type: application/json
Content-length: 66

{
  "startCell": "startCell-value",
  "endCell": "endCell-value"
}
```

##### <a name="response"></a><span data-ttu-id="22013-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22013-150">Response</span></span>
<span data-ttu-id="22013-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22013-151">Here is an example of the response.</span></span> 
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
  "description": "Chart: setPosition",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
