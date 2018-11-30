---
title: 'TableRowCollection: add'
description: 'Agrega filas al final de la tabla. Tenga en cuenta que la API puede aceptar varios datos de las filas con esta API. Adición de una fila a la vez, se podría producir una degradación del rendimiento. El enfoque recomendado sería por lotes las filas juntos en una única llamada en lugar de realizar la inserción de fila única. Para obtener mejores resultados, recopilar las filas que se va a insertar en el lado de la aplicación y llevar a cabo las filas único Agregar operación. Experimente con el número de filas para determinar el número de filas que se use en la llamada a la API único ideal. '
ms.openlocfilehash: fc2b89a25ade4b9d85844716370d95d52689de9d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030119"
---
# <a name="tablerowcollection-add"></a><span data-ttu-id="f3119-108">TableRowCollection: add</span><span class="sxs-lookup"><span data-stu-id="f3119-108">TableRowCollection: add</span></span>

<span data-ttu-id="f3119-109">Agrega filas al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f3119-109">Adds rows to the end of the table.</span></span> <span data-ttu-id="f3119-110">Tenga en cuenta que la API puede aceptar varios datos de las filas con esta API.</span><span class="sxs-lookup"><span data-stu-id="f3119-110">Note that the API can accept multiple rows data using this API.</span></span> <span data-ttu-id="f3119-111">Adición de una fila a la vez, se podría producir una degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f3119-111">Adding one row at a time could lead to performance degradation.</span></span> <span data-ttu-id="f3119-112">El enfoque recomendado sería por lotes las filas juntos en una única llamada en lugar de realizar la inserción de fila única.</span><span class="sxs-lookup"><span data-stu-id="f3119-112">The recommended approach would be to batch the rows together in a single call rather than doing single row insertion.</span></span> <span data-ttu-id="f3119-113">Para obtener mejores resultados, recopilar las filas que se va a insertar en el lado de la aplicación y llevar a cabo las filas único Agregar operación.</span><span class="sxs-lookup"><span data-stu-id="f3119-113">For best results, collect the rows to be inserted on the application side and perform single rows add operation.</span></span> <span data-ttu-id="f3119-114">Experimente con el número de filas para determinar el número de filas que se use en la llamada a la API único ideal.</span><span class="sxs-lookup"><span data-stu-id="f3119-114">Experiment with the number of rows to determine the ideal number of rows to use in single API call.</span></span> 

## <a name="error-handling"></a><span data-ttu-id="f3119-115">Control de errores</span><span class="sxs-lookup"><span data-stu-id="f3119-115">Error Handling</span></span>

<span data-ttu-id="f3119-116">En ocasiones, esta solicitud puede recibir el error HTTP 504.</span><span class="sxs-lookup"><span data-stu-id="f3119-116">This request might occasionally receive a 504 HTTP error.</span></span> <span data-ttu-id="f3119-117">La respuesta adecuada a este error es repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3119-117">The appropriate response to this error is to repeat the request.</span></span>

## <a name="permissions"></a><span data-ttu-id="f3119-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="f3119-118">Permissions</span></span>
<span data-ttu-id="f3119-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3119-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f3119-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3119-121">Permission type</span></span>      | <span data-ttu-id="f3119-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3119-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f3119-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3119-123">Delegated (work or school account)</span></span> | <span data-ttu-id="f3119-124">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f3119-124">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f3119-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3119-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3119-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3119-126">Not supported.</span></span>    |
|<span data-ttu-id="f3119-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3119-127">Application</span></span> | <span data-ttu-id="f3119-128">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3119-128">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f3119-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3119-129">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/add

```
## <a name="request-headers"></a><span data-ttu-id="f3119-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3119-130">Request headers</span></span>
| <span data-ttu-id="f3119-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3119-131">Name</span></span>       | <span data-ttu-id="f3119-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3119-132">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f3119-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="f3119-133">Authorization</span></span>  | <span data-ttu-id="f3119-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3119-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f3119-136">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f3119-136">Workbook-Session-Id</span></span>  | <span data-ttu-id="f3119-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f3119-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f3119-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f3119-139">Request body</span></span>
<span data-ttu-id="f3119-140">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f3119-140">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f3119-141">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f3119-141">Parameter</span></span>    | <span data-ttu-id="f3119-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3119-142">Type</span></span>   |<span data-ttu-id="f3119-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3119-143">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f3119-144">index</span><span class="sxs-lookup"><span data-stu-id="f3119-144">index</span></span>|<span data-ttu-id="f3119-145">Int32</span><span class="sxs-lookup"><span data-stu-id="f3119-145">Int32</span></span>|<span data-ttu-id="f3119-p107">Opcional. Especifica la posición relativa de la nueva fila. Si es null, se produce la adición al final. Las filas situadas debajo de la fila insertada se desplazan hacia abajo. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="f3119-p107">Optional. Specifies the relative position of the new row. If null, the addition happens at the end. Any rows below the inserted row are shifted downwards. Zero-indexed.</span></span>|
|<span data-ttu-id="f3119-151">values</span><span class="sxs-lookup"><span data-stu-id="f3119-151">values</span></span>|<span data-ttu-id="f3119-152">Json</span><span class="sxs-lookup"><span data-stu-id="f3119-152">Json</span></span>|<span data-ttu-id="f3119-p108">Opcional. Matriz bidimensional de valores sin formato de la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f3119-p108">Optional. A 2-dimensional array of unformatted values of the table row.</span></span>|

## <a name="response"></a><span data-ttu-id="f3119-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3119-155">Response</span></span>

<span data-ttu-id="f3119-156">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookTableRow](../resources/tablerow.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3119-156">If successful, this method returns `200 OK` response code and [WorkbookTableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f3119-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3119-157">Example</span></span>
<span data-ttu-id="f3119-158">En este ejemplo se insertan dos filas de datos al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f3119-158">In this example two rows of data are inserted at the end of the table.</span></span> 

##### <a name="request"></a><span data-ttu-id="f3119-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3119-159">Request</span></span>
<span data-ttu-id="f3119-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3119-160">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablerowcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows/add
Content-type: application/json
Content-length: 51

{
  "index": 5,
  "values": [
    [1, 2, 3],
    [4, 5, 6]
  ]
}
```

##### <a name="response"></a><span data-ttu-id="f3119-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3119-161">Response</span></span>
<span data-ttu-id="f3119-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3119-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableRow"
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
  "suppressions": [
    "Warning: /api-reference/v1.0/api/tablerowcollection-add.md/tablerowcollection_add/values:
      Inconsistent types between parameter (Collection) and table (None)",
    "Error: /api-reference/v1.0/api/tablerowcollection-add.md/tablerowcollection_add/values:
      Type mismatch between example and table. Parameter name: values; example type (Collection(Collection)) is a collection, while the table description type (microsoft.graph.Json) is not."
  ],
  "tocPath": ""
}-->
