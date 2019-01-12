---
title: 'TableRowCollection: add'
description: 'Agrega filas al final de la tabla. Tenga en cuenta que la API puede aceptar varios datos de las filas con esta API. Adición de una fila a la vez, se podría producir una degradación del rendimiento. El enfoque recomendado sería por lotes las filas juntos en una única llamada en lugar de realizar la inserción de fila única. Para obtener mejores resultados, recopilar las filas que se va a insertar en el lado de la aplicación y llevar a cabo las filas único Agregar operación. Experimente con el número de filas para determinar el número de filas que se use en la llamada a la API único ideal. '
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 45126e74b8b4a242481b7cba3ca8d2664c48cc7c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969691"
---
# <a name="tablerowcollection-add"></a><span data-ttu-id="96581-108">TableRowCollection: add</span><span class="sxs-lookup"><span data-stu-id="96581-108">TableRowCollection: add</span></span>

> <span data-ttu-id="96581-109">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96581-109">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96581-110">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96581-110">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="96581-111">Agrega filas al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="96581-111">Adds rows to the end of the table.</span></span> <span data-ttu-id="96581-112">Tenga en cuenta que la API puede aceptar varios datos de las filas con esta API.</span><span class="sxs-lookup"><span data-stu-id="96581-112">Note that the API can accept multiple rows data using this API.</span></span> <span data-ttu-id="96581-113">Adición de una fila a la vez, se podría producir una degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="96581-113">Adding one row at a time could lead to performance degradation.</span></span> <span data-ttu-id="96581-114">El enfoque recomendado sería por lotes las filas juntos en una única llamada en lugar de realizar la inserción de fila única.</span><span class="sxs-lookup"><span data-stu-id="96581-114">The recommended approach would be to batch the rows together in a single call rather than doing single row insertion.</span></span> <span data-ttu-id="96581-115">Para obtener mejores resultados, recopilar las filas que se va a insertar en el lado de la aplicación y llevar a cabo las filas único Agregar operación.</span><span class="sxs-lookup"><span data-stu-id="96581-115">For best results, collect the rows to be inserted on the application side and perform single rows add operation.</span></span> <span data-ttu-id="96581-116">Experimente con el número de filas para determinar el número de filas que se use en la llamada a la API único ideal.</span><span class="sxs-lookup"><span data-stu-id="96581-116">Experiment with the number of rows to determine the ideal number of rows to use in single API call.</span></span> 

## <a name="error-handling"></a><span data-ttu-id="96581-117">Control de errores</span><span class="sxs-lookup"><span data-stu-id="96581-117">Error Handling</span></span>

<span data-ttu-id="96581-118">En ocasiones, esta solicitud puede recibir el error HTTP 504.</span><span class="sxs-lookup"><span data-stu-id="96581-118">This request might occasionally receive a 504 HTTP error.</span></span> <span data-ttu-id="96581-119">La respuesta adecuada a este error es repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="96581-119">The appropriate response to this error is to repeat the request.</span></span>

## <a name="permissions"></a><span data-ttu-id="96581-120">Permisos</span><span class="sxs-lookup"><span data-stu-id="96581-120">Permissions</span></span>
<span data-ttu-id="96581-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="96581-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="96581-123">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="96581-123">Permission type</span></span>      | <span data-ttu-id="96581-124">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="96581-124">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="96581-125">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="96581-125">Delegated (work or school account)</span></span> | <span data-ttu-id="96581-126">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="96581-126">Files.ReadWrite</span></span>    |
|<span data-ttu-id="96581-127">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="96581-127">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="96581-128">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="96581-128">Files.ReadWrite</span></span>    |
|<span data-ttu-id="96581-129">Aplicación</span><span class="sxs-lookup"><span data-stu-id="96581-129">Application</span></span> | <span data-ttu-id="96581-130">No admitida.</span><span class="sxs-lookup"><span data-stu-id="96581-130">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="96581-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="96581-131">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/add

```
## <a name="request-headers"></a><span data-ttu-id="96581-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="96581-132">Request headers</span></span>
| <span data-ttu-id="96581-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="96581-133">Name</span></span>       | <span data-ttu-id="96581-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="96581-134">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="96581-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="96581-135">Authorization</span></span>  | <span data-ttu-id="96581-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="96581-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="96581-138">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="96581-138">Workbook-Session-Id</span></span>  | <span data-ttu-id="96581-p107">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="96581-p107">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="96581-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="96581-141">Request body</span></span>
<span data-ttu-id="96581-142">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="96581-142">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="96581-143">Parámetro</span><span class="sxs-lookup"><span data-stu-id="96581-143">Parameter</span></span>    | <span data-ttu-id="96581-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="96581-144">Type</span></span>   |<span data-ttu-id="96581-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="96581-145">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="96581-146">index</span><span class="sxs-lookup"><span data-stu-id="96581-146">index</span></span>|<span data-ttu-id="96581-147">number</span><span class="sxs-lookup"><span data-stu-id="96581-147">number</span></span>|<span data-ttu-id="96581-p108">Opcional. Especifica la posición relativa de la nueva fila. Si es null, se produce la adición al final. Las filas situadas debajo de la fila insertada se desplazan hacia abajo. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="96581-p108">Optional. Specifies the relative position of the new row. If null, the addition happens at the end. Any rows below the inserted row are shifted downwards. Zero-indexed.</span></span>|
|<span data-ttu-id="96581-153">values</span><span class="sxs-lookup"><span data-stu-id="96581-153">values</span></span>|<span data-ttu-id="96581-154">(boolean, string o number)</span><span class="sxs-lookup"><span data-stu-id="96581-154">(boolean or string or number)</span></span>|<span data-ttu-id="96581-155">Opcional.</span><span class="sxs-lookup"><span data-stu-id="96581-155">Optional.</span></span> <span data-ttu-id="96581-156">Una matriz 2 dimensional de valores sin formato de las filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="96581-156">A 2-dimensional array of unformatted values of the table rows.</span></span>|

## <a name="response"></a><span data-ttu-id="96581-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96581-157">Response</span></span>

<span data-ttu-id="96581-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="96581-158">If successful, this method returns `200 OK` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="96581-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="96581-159">Example</span></span>
<span data-ttu-id="96581-160">En este ejemplo se insertan dos filas de datos al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="96581-160">In this example two rows of data are inserted at the end of the table.</span></span> 

##### <a name="request"></a><span data-ttu-id="96581-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="96581-161">Request</span></span>
<span data-ttu-id="96581-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="96581-162">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablerowcollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/rows/add
Content-type: application/json
Content-length: 51

{
  "index": null,
  "values": [
    [1, 2, 3],
    [4, 5, 6]
  ]
}
```

##### <a name="response"></a><span data-ttu-id="96581-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96581-163">Response</span></span>
<span data-ttu-id="96581-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="96581-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRowCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
