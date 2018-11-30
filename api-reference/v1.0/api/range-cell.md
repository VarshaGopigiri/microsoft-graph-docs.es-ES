---
title: 'Range: Cell'
description: Obtiene el objeto de intervalo que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del intervalo principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del intervalo.
ms.openlocfilehash: cbf44d75ee6d6599e9a8ff924f5dee40936d4431
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029561"
---
# <a name="range-cell"></a><span data-ttu-id="693b4-105">Range: Cell</span><span class="sxs-lookup"><span data-stu-id="693b4-105">Range: Cell</span></span>

<span data-ttu-id="693b4-p102">Obtiene el objeto de intervalo que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del intervalo principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del intervalo.</span><span class="sxs-lookup"><span data-stu-id="693b4-p102">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid. The returned cell is located relative to the top left cell of the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="693b4-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="693b4-109">Permissions</span></span>
<span data-ttu-id="693b4-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="693b4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="693b4-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="693b4-112">Permission type</span></span>      | <span data-ttu-id="693b4-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="693b4-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="693b4-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="693b4-114">Delegated (work or school account)</span></span> | <span data-ttu-id="693b4-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="693b4-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="693b4-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="693b4-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="693b4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="693b4-117">Not supported.</span></span>    |
|<span data-ttu-id="693b4-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="693b4-118">Application</span></span> | <span data-ttu-id="693b4-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="693b4-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="693b4-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="693b4-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/cell
GET /workbook/worksheets/{id|name}/range(address='<address>')/cell
GET /workbook/tables/{id|name}/columns/{id|name}/range/cell

```
## <a name="request-headers"></a><span data-ttu-id="693b4-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="693b4-121">Request headers</span></span>
| <span data-ttu-id="693b4-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="693b4-122">Name</span></span>       | <span data-ttu-id="693b4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="693b4-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="693b4-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="693b4-124">Authorization</span></span>  | <span data-ttu-id="693b4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="693b4-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="693b4-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="693b4-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="693b4-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="693b4-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="693b4-130">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="693b4-130">Path parameters</span></span>
<span data-ttu-id="693b4-131">En la ruta de acceso, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="693b4-131">In the path, provide the following parameters.</span></span>

| <span data-ttu-id="693b4-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="693b4-132">Parameter</span></span>    | <span data-ttu-id="693b4-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="693b4-133">Type</span></span>   |<span data-ttu-id="693b4-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="693b4-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="693b4-135">row</span><span class="sxs-lookup"><span data-stu-id="693b4-135">row</span></span>|<span data-ttu-id="693b4-136">Int32</span><span class="sxs-lookup"><span data-stu-id="693b4-136">Int32</span></span>|<span data-ttu-id="693b4-p106">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="693b4-p106">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="693b4-139">column</span><span class="sxs-lookup"><span data-stu-id="693b4-139">column</span></span>|<span data-ttu-id="693b4-140">Int32</span><span class="sxs-lookup"><span data-stu-id="693b4-140">Int32</span></span>|<span data-ttu-id="693b4-p107">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="693b4-p107">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="693b4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="693b4-143">Response</span></span>

<span data-ttu-id="693b4-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="693b4-144">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="693b4-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="693b4-145">Example</span></span>
<span data-ttu-id="693b4-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="693b4-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="693b4-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="693b4-147">Request</span></span>
<span data-ttu-id="693b4-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="693b4-148">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/cell(row=5,column=6)
```

##### <a name="response"></a><span data-ttu-id="693b4-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="693b4-149">Response</span></span>
<span data-ttu-id="693b4-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="693b4-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: Cell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->