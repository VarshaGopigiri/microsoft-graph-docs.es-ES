---
title: 'Worksheet: Cell'
description: Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.
ms.openlocfilehash: 5e9134fe9ba685a5770cf0671ce06e740a886891
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031228"
---
# <a name="worksheet-cell"></a><span data-ttu-id="07db6-104">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="07db6-104">Worksheet: Cell</span></span>

<span data-ttu-id="07db6-p102">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="07db6-p102">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="permissions"></a><span data-ttu-id="07db6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="07db6-107">Permissions</span></span>
<span data-ttu-id="07db6-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07db6-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="07db6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07db6-110">Permission type</span></span>      | <span data-ttu-id="07db6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07db6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="07db6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07db6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="07db6-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07db6-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="07db6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07db6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="07db6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07db6-115">Not supported.</span></span>    |
|<span data-ttu-id="07db6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07db6-116">Application</span></span> | <span data-ttu-id="07db6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07db6-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="07db6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07db6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/cell(row={row},column={column})

```

## <a name="function-parameters"></a><span data-ttu-id="07db6-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="07db6-119">Function parameters</span></span>
<span data-ttu-id="07db6-120">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="07db6-120">In the request path, provide the following parameters.</span></span>

| <span data-ttu-id="07db6-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="07db6-121">Parameter</span></span>    | <span data-ttu-id="07db6-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="07db6-122">Type</span></span>   |<span data-ttu-id="07db6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="07db6-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="07db6-124">row</span><span class="sxs-lookup"><span data-stu-id="07db6-124">row</span></span>|<span data-ttu-id="07db6-125">Int32</span><span class="sxs-lookup"><span data-stu-id="07db6-125">Int32</span></span>|<span data-ttu-id="07db6-p104">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="07db6-p104">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="07db6-128">column</span><span class="sxs-lookup"><span data-stu-id="07db6-128">column</span></span>|<span data-ttu-id="07db6-129">Int32</span><span class="sxs-lookup"><span data-stu-id="07db6-129">Int32</span></span>|<span data-ttu-id="07db6-p105">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="07db6-p105">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="07db6-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="07db6-132">Request headers</span></span>
| <span data-ttu-id="07db6-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="07db6-133">Name</span></span>       | <span data-ttu-id="07db6-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="07db6-134">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="07db6-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="07db6-135">Authorization</span></span>  | <span data-ttu-id="07db6-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="07db6-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="07db6-138">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="07db6-138">Workbook-Session-Id</span></span>  | <span data-ttu-id="07db6-p107">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="07db6-p107">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="07db6-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="07db6-141">Request body</span></span>
<span data-ttu-id="07db6-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="07db6-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="07db6-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07db6-143">Response</span></span>

<span data-ttu-id="07db6-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07db6-144">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="07db6-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07db6-145">Example</span></span>
<span data-ttu-id="07db6-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="07db6-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="07db6-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07db6-147">Request</span></span>
<span data-ttu-id="07db6-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07db6-148">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="07db6-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07db6-149">Response</span></span>
<span data-ttu-id="07db6-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="07db6-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
