---
title: 'Worksheet: Cell'
description: Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 96069c11d8e520b64854eb7a2a72dc9d5f6de25b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967304"
---
# <a name="worksheet-cell"></a><span data-ttu-id="19ffb-104">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="19ffb-104">Worksheet: Cell</span></span>

<span data-ttu-id="19ffb-p102">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="19ffb-p102">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="permissions"></a><span data-ttu-id="19ffb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="19ffb-107">Permissions</span></span>
<span data-ttu-id="19ffb-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="19ffb-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="19ffb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19ffb-110">Permission type</span></span>      | <span data-ttu-id="19ffb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19ffb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="19ffb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19ffb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="19ffb-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="19ffb-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="19ffb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19ffb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="19ffb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19ffb-115">Not supported.</span></span>    |
|<span data-ttu-id="19ffb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19ffb-116">Application</span></span> | <span data-ttu-id="19ffb-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19ffb-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="19ffb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19ffb-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/cell(row={row},column={column})

```

## <a name="function-parameters"></a><span data-ttu-id="19ffb-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="19ffb-119">Function parameters</span></span>
<span data-ttu-id="19ffb-120">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="19ffb-120">In the request path, provide the following parameters.</span></span>

| <span data-ttu-id="19ffb-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="19ffb-121">Parameter</span></span>    | <span data-ttu-id="19ffb-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="19ffb-122">Type</span></span>   |<span data-ttu-id="19ffb-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="19ffb-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="19ffb-124">row</span><span class="sxs-lookup"><span data-stu-id="19ffb-124">row</span></span>|<span data-ttu-id="19ffb-125">Int32</span><span class="sxs-lookup"><span data-stu-id="19ffb-125">Int32</span></span>|<span data-ttu-id="19ffb-p104">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="19ffb-p104">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="19ffb-128">column</span><span class="sxs-lookup"><span data-stu-id="19ffb-128">column</span></span>|<span data-ttu-id="19ffb-129">Int32</span><span class="sxs-lookup"><span data-stu-id="19ffb-129">Int32</span></span>|<span data-ttu-id="19ffb-p105">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="19ffb-p105">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="19ffb-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19ffb-132">Request headers</span></span>
| <span data-ttu-id="19ffb-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="19ffb-133">Name</span></span>       | <span data-ttu-id="19ffb-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="19ffb-134">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="19ffb-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="19ffb-135">Authorization</span></span>  | <span data-ttu-id="19ffb-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="19ffb-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="19ffb-138">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="19ffb-138">Workbook-Session-Id</span></span>  | <span data-ttu-id="19ffb-p107">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="19ffb-p107">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="19ffb-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19ffb-141">Request body</span></span>
<span data-ttu-id="19ffb-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="19ffb-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="19ffb-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19ffb-143">Response</span></span>

<span data-ttu-id="19ffb-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19ffb-144">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="19ffb-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19ffb-145">Example</span></span>
<span data-ttu-id="19ffb-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="19ffb-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="19ffb-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19ffb-147">Request</span></span>
<span data-ttu-id="19ffb-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="19ffb-148">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="19ffb-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19ffb-149">Response</span></span>
<span data-ttu-id="19ffb-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="19ffb-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
