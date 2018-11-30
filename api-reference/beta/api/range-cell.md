---
title: 'Range: Cell'
description: Obtiene el objeto de intervalo que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del intervalo principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del intervalo.
ms.openlocfilehash: 641de24869d5a57b08f339b7552d67d07be7b75c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090450"
---
# <a name="range-cell"></a><span data-ttu-id="7407f-105">Range: Cell</span><span class="sxs-lookup"><span data-stu-id="7407f-105">Range: Cell</span></span>

> <span data-ttu-id="7407f-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7407f-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7407f-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7407f-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7407f-p103">Obtiene el objeto de intervalo que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del intervalo principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del intervalo.</span><span class="sxs-lookup"><span data-stu-id="7407f-p103">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid. The returned cell is located relative to the top left cell of the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="7407f-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="7407f-111">Permissions</span></span>
<span data-ttu-id="7407f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7407f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7407f-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7407f-114">Permission type</span></span>      | <span data-ttu-id="7407f-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7407f-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7407f-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7407f-116">Delegated (work or school account)</span></span> | <span data-ttu-id="7407f-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7407f-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7407f-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7407f-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7407f-119">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7407f-119">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7407f-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7407f-120">Application</span></span> | <span data-ttu-id="7407f-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7407f-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7407f-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7407f-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Cell
GET /workbook/worksheets/{id|name}/range(address='<address>')/Cell
GET /workbook/tables/{id|name}/columns/{id|name}/range/Cell

```
## <a name="request-headers"></a><span data-ttu-id="7407f-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7407f-123">Request headers</span></span>
| <span data-ttu-id="7407f-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="7407f-124">Name</span></span>       | <span data-ttu-id="7407f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7407f-125">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7407f-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="7407f-126">Authorization</span></span>  | <span data-ttu-id="7407f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7407f-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7407f-129">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="7407f-129">Workbook-Session-Id</span></span>  | <span data-ttu-id="7407f-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7407f-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7407f-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7407f-132">Request body</span></span>
<span data-ttu-id="7407f-133">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7407f-133">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7407f-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7407f-134">Parameter</span></span>    | <span data-ttu-id="7407f-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="7407f-135">Type</span></span>   |<span data-ttu-id="7407f-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="7407f-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7407f-137">row</span><span class="sxs-lookup"><span data-stu-id="7407f-137">row</span></span>|<span data-ttu-id="7407f-138">number</span><span class="sxs-lookup"><span data-stu-id="7407f-138">number</span></span>|<span data-ttu-id="7407f-p107">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="7407f-p107">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="7407f-141">column</span><span class="sxs-lookup"><span data-stu-id="7407f-141">column</span></span>|<span data-ttu-id="7407f-142">number</span><span class="sxs-lookup"><span data-stu-id="7407f-142">number</span></span>|<span data-ttu-id="7407f-p108">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="7407f-p108">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="7407f-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7407f-145">Response</span></span>

<span data-ttu-id="7407f-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7407f-146">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7407f-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7407f-147">Example</span></span>
<span data-ttu-id="7407f-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7407f-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="7407f-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7407f-149">Request</span></span>
<span data-ttu-id="7407f-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7407f-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_cell"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/Cell
Content-type: application/json
Content-length: 37

{
  "row": {
  },
  "column": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="7407f-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7407f-151">Response</span></span>
<span data-ttu-id="7407f-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7407f-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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