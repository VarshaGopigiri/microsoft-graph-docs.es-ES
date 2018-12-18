---
title: 'Chart: setPosition'
description: Coloca el gráfico con respecto a las celdas de la hoja de cálculo.
author: lumine2008
ms.openlocfilehash: a83657a4654099dc1b52e55e2e627d14ef8c7aff
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324594"
---
# <a name="chart-setposition"></a><span data-ttu-id="c0884-103">Chart: setPosition</span><span class="sxs-lookup"><span data-stu-id="c0884-103">Chart: setPosition</span></span>

<span data-ttu-id="c0884-104">Coloca el gráfico con respecto a las celdas de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c0884-104">Positions the chart relative to cells on the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="c0884-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0884-105">Permissions</span></span>
<span data-ttu-id="c0884-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0884-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0884-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0884-108">Permission type</span></span>      | <span data-ttu-id="c0884-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0884-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0884-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0884-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c0884-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0884-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c0884-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0884-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0884-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0884-113">Not supported.</span></span>    |
|<span data-ttu-id="c0884-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0884-114">Application</span></span> | <span data-ttu-id="c0884-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0884-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0884-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0884-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/setPosition

```
## <a name="request-headers"></a><span data-ttu-id="c0884-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0884-117">Request headers</span></span>
| <span data-ttu-id="c0884-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0884-118">Name</span></span>       | <span data-ttu-id="c0884-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0884-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c0884-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0884-120">Authorization</span></span>  | <span data-ttu-id="c0884-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0884-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c0884-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c0884-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="c0884-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c0884-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c0884-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0884-126">Request body</span></span>
<span data-ttu-id="c0884-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c0884-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c0884-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0884-128">Parameter</span></span>    | <span data-ttu-id="c0884-129">Type</span><span class="sxs-lookup"><span data-stu-id="c0884-129">Type</span></span>   |<span data-ttu-id="c0884-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0884-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0884-131">startCell</span><span class="sxs-lookup"><span data-stu-id="c0884-131">startCell</span></span>|<span data-ttu-id="c0884-132">Json</span><span class="sxs-lookup"><span data-stu-id="c0884-132">Json</span></span>|<span data-ttu-id="c0884-p104">Celda de inicio. Aquí es adonde se moverá el gráfico. La celda de inicio es la celda superior izquierda o superior derecha, en función de la configuración del usuario de la presentación de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="c0884-p104">The start cell. This is where the chart will be moved to. The start cell is the top-left or top-right cell, depending on the user's right-to-left display settings.</span></span>|
|<span data-ttu-id="c0884-136">endCell</span><span class="sxs-lookup"><span data-stu-id="c0884-136">endCell</span></span>|<span data-ttu-id="c0884-137">Json</span><span class="sxs-lookup"><span data-stu-id="c0884-137">Json</span></span>|<span data-ttu-id="c0884-p105">Opcional. Última celda. Si se especifica, el ancho y el alto del gráfico se establecerán de modo que cubran totalmente esta celda o rango.</span><span class="sxs-lookup"><span data-stu-id="c0884-p105">Optional. The end cell. If specified, the chart's width and height will be set to fully cover up this cell/range.</span></span>|

## <a name="response"></a><span data-ttu-id="c0884-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0884-141">Response</span></span>

<span data-ttu-id="c0884-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0884-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c0884-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0884-144">Example</span></span>
<span data-ttu-id="c0884-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c0884-145">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c0884-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0884-146">Request</span></span>
<span data-ttu-id="c0884-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0884-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setposition"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setPosition
Content-type: application/json
Content-length: 66

{
  "startCell": "startCell-value",
  "endCell": "endCell-value"
}
```

##### <a name="response"></a><span data-ttu-id="c0884-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0884-148">Response</span></span>
<span data-ttu-id="c0884-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0884-149">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
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