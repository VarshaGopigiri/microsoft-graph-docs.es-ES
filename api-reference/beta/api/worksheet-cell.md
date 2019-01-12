---
title: 'Worksheet: Cell'
description: Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 5b4771283922c4c41aeb3210040b3e95823cad81
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976068"
---
# <a name="worksheet-cell"></a><span data-ttu-id="a0964-104">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="a0964-104">Worksheet: Cell</span></span>

> <span data-ttu-id="a0964-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a0964-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a0964-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a0964-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a0964-p103">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a0964-p103">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="permissions"></a><span data-ttu-id="a0964-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0964-109">Permissions</span></span>
<span data-ttu-id="a0964-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0964-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0964-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0964-112">Permission type</span></span>      | <span data-ttu-id="a0964-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0964-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0964-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0964-114">Delegated (work or school account)</span></span> | <span data-ttu-id="a0964-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0964-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a0964-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0964-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0964-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0964-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a0964-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0964-118">Application</span></span> | <span data-ttu-id="a0964-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0964-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0964-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0964-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/Cell(row={row},column={column})

```

## <a name="function-parameters"></a><span data-ttu-id="a0964-121">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="a0964-121">Function parameters</span></span>
<span data-ttu-id="a0964-122">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="a0964-122">In the request path, provide the following parameters.</span></span>

| <span data-ttu-id="a0964-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a0964-123">Parameter</span></span>    | <span data-ttu-id="a0964-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0964-124">Type</span></span>   |<span data-ttu-id="a0964-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0964-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a0964-126">row</span><span class="sxs-lookup"><span data-stu-id="a0964-126">row</span></span>|<span data-ttu-id="a0964-127">Int32</span><span class="sxs-lookup"><span data-stu-id="a0964-127">Int32</span></span>|<span data-ttu-id="a0964-p105">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="a0964-p105">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="a0964-130">column</span><span class="sxs-lookup"><span data-stu-id="a0964-130">column</span></span>|<span data-ttu-id="a0964-131">Int32</span><span class="sxs-lookup"><span data-stu-id="a0964-131">Int32</span></span>|<span data-ttu-id="a0964-p106">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="a0964-p106">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="a0964-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0964-134">Request headers</span></span>
| <span data-ttu-id="a0964-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0964-135">Name</span></span>       | <span data-ttu-id="a0964-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0964-136">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a0964-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0964-137">Authorization</span></span>  | <span data-ttu-id="a0964-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0964-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a0964-140">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="a0964-140">Workbook-Session-Id</span></span>  | <span data-ttu-id="a0964-p108">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="a0964-p108">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a0964-143">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0964-143">Request body</span></span>
<span data-ttu-id="a0964-144">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a0964-144">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a0964-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0964-145">Response</span></span>

<span data-ttu-id="a0964-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0964-146">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0964-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0964-147">Example</span></span>
<span data-ttu-id="a0964-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a0964-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a0964-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0964-149">Request</span></span>
<span data-ttu-id="a0964-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0964-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/Cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="a0964-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0964-151">Response</span></span>
<span data-ttu-id="a0964-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0964-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 1,
  "columnCount": 1,
  "columnIndex": 3,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet: Cell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
