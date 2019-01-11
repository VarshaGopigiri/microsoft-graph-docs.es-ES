---
title: 'Worksheet: Cell'
description: Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.
localization_priority: Normal
ms.openlocfilehash: 94abdb533e64ef1b6fd94e9e7f0b5b149c0c2666
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831384"
---
# <a name="worksheet-cell"></a><span data-ttu-id="73c7a-104">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="73c7a-104">Worksheet: Cell</span></span>

<span data-ttu-id="73c7a-p102">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="73c7a-p102">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="permissions"></a><span data-ttu-id="73c7a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="73c7a-107">Permissions</span></span>
<span data-ttu-id="73c7a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="73c7a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="73c7a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73c7a-110">Permission type</span></span>      | <span data-ttu-id="73c7a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73c7a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="73c7a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73c7a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="73c7a-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="73c7a-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="73c7a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73c7a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="73c7a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73c7a-115">Not supported.</span></span>    |
|<span data-ttu-id="73c7a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73c7a-116">Application</span></span> | <span data-ttu-id="73c7a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73c7a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="73c7a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73c7a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/cell(row={row},column={column})

```

## <a name="function-parameters"></a><span data-ttu-id="73c7a-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="73c7a-119">Function parameters</span></span>
<span data-ttu-id="73c7a-120">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="73c7a-120">In the request path, provide the following parameters.</span></span>

| <span data-ttu-id="73c7a-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="73c7a-121">Parameter</span></span>    | <span data-ttu-id="73c7a-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="73c7a-122">Type</span></span>   |<span data-ttu-id="73c7a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="73c7a-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="73c7a-124">row</span><span class="sxs-lookup"><span data-stu-id="73c7a-124">row</span></span>|<span data-ttu-id="73c7a-125">Int32</span><span class="sxs-lookup"><span data-stu-id="73c7a-125">Int32</span></span>|<span data-ttu-id="73c7a-p104">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="73c7a-p104">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="73c7a-128">column</span><span class="sxs-lookup"><span data-stu-id="73c7a-128">column</span></span>|<span data-ttu-id="73c7a-129">Int32</span><span class="sxs-lookup"><span data-stu-id="73c7a-129">Int32</span></span>|<span data-ttu-id="73c7a-p105">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="73c7a-p105">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="73c7a-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73c7a-132">Request headers</span></span>
| <span data-ttu-id="73c7a-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="73c7a-133">Name</span></span>       | <span data-ttu-id="73c7a-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="73c7a-134">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="73c7a-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="73c7a-135">Authorization</span></span>  | <span data-ttu-id="73c7a-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73c7a-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="73c7a-138">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="73c7a-138">Workbook-Session-Id</span></span>  | <span data-ttu-id="73c7a-p107">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="73c7a-p107">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="73c7a-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73c7a-141">Request body</span></span>
<span data-ttu-id="73c7a-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="73c7a-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="73c7a-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73c7a-143">Response</span></span>

<span data-ttu-id="73c7a-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73c7a-144">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="73c7a-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73c7a-145">Example</span></span>
<span data-ttu-id="73c7a-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="73c7a-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="73c7a-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73c7a-147">Request</span></span>
<span data-ttu-id="73c7a-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73c7a-148">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="73c7a-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73c7a-149">Response</span></span>
<span data-ttu-id="73c7a-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="73c7a-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
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
