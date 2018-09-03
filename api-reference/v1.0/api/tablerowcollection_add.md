# <a name="tablerowcollection-add"></a><span data-ttu-id="41a09-101">TableRowCollection: add</span><span class="sxs-lookup"><span data-stu-id="41a09-101">TableRowCollection: add</span></span>

<span data-ttu-id="41a09-102">Agrega filas al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="41a09-102">Adds a row to the end of the table.</span></span> <span data-ttu-id="41a09-103">Tenga en cuenta que la API puede aceptar múltiples filas de datos con esta API.</span><span class="sxs-lookup"><span data-stu-id="41a09-103">Note that the API can accept multiple rows data using this API.</span></span> <span data-ttu-id="41a09-104">La adición de una fila a la vez podría provocar una degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="41a09-104">Adding one row at a time could lead to performance degradation.</span></span> <span data-ttu-id="41a09-105">El método recomendado sería agrupar las filas juntas en una única llamada en lugar de hacer inserciones de una sola fila.</span><span class="sxs-lookup"><span data-stu-id="41a09-105">The recommended approach would be to batch the rows together in a single call rather than doing single row insertion.</span></span> <span data-ttu-id="41a09-106">Para obtener mejores resultados, reúna las filas que se insertarán en el lado de la aplicación y realice una operación de adición de filas únicas.</span><span class="sxs-lookup"><span data-stu-id="41a09-106">For best results, collect the rows to be inserted on the application side and perform single rows add operation.</span></span> <span data-ttu-id="41a09-107">Experimente con el número de filas para determinar el número de filas ideal para usar en una sola llamada API.</span><span class="sxs-lookup"><span data-stu-id="41a09-107">Experiment with the number of rows to determine the ideal number of rows to use in single API call.</span></span> 

## <a name="error-handling"></a><span data-ttu-id="41a09-108">Control de errores</span><span class="sxs-lookup"><span data-stu-id="41a09-108">Error Handling</span></span>

<span data-ttu-id="41a09-109">En ocasiones, esta solicitud puede recibir el error HTTP 504.</span><span class="sxs-lookup"><span data-stu-id="41a09-109">This request might occasionally receive a 504 HTTP error.</span></span> <span data-ttu-id="41a09-110">La respuesta adecuada a este error es repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41a09-110">The appropriate response to this error is to repeat the request.</span></span>

## <a name="permissions"></a><span data-ttu-id="41a09-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="41a09-111">Permissions</span></span>
<span data-ttu-id="41a09-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="41a09-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="41a09-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41a09-114">Permission type</span></span>      | <span data-ttu-id="41a09-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41a09-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="41a09-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41a09-116">Delegated (work or school account)</span></span> | <span data-ttu-id="41a09-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="41a09-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="41a09-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41a09-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="41a09-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41a09-119">Not supported.</span></span>    |
|<span data-ttu-id="41a09-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41a09-120">Application</span></span> | <span data-ttu-id="41a09-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41a09-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="41a09-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41a09-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/add

```
## <a name="request-headers"></a><span data-ttu-id="41a09-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41a09-123">Request headers</span></span>
| <span data-ttu-id="41a09-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="41a09-124">Name</span></span>       | <span data-ttu-id="41a09-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="41a09-125">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="41a09-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="41a09-126">Authorization</span></span>  | <span data-ttu-id="41a09-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="41a09-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="41a09-129">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="41a09-129">Workbook-Session-Id</span></span>  | <span data-ttu-id="41a09-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="41a09-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="41a09-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41a09-132">Request body</span></span>
<span data-ttu-id="41a09-133">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="41a09-133">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="41a09-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="41a09-134">Parameter</span></span>    | <span data-ttu-id="41a09-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="41a09-135">Type</span></span>   |<span data-ttu-id="41a09-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="41a09-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="41a09-137">index</span><span class="sxs-lookup"><span data-stu-id="41a09-137">index</span></span>|<span data-ttu-id="41a09-138">Int32</span><span class="sxs-lookup"><span data-stu-id="41a09-138">Int32</span></span>|<span data-ttu-id="41a09-p106">Opcional. Especifica la posición relativa de la nueva fila. Si es null, se produce la adición al final. Las filas situadas debajo de la fila insertada se desplazan hacia abajo. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="41a09-p106">Optional. Specifies the relative position of the new row. If null, the addition happens at the end. Any rows below the inserted row are shifted downwards. Zero-indexed.</span></span>|
|<span data-ttu-id="41a09-144">values</span><span class="sxs-lookup"><span data-stu-id="41a09-144">values</span></span>|<span data-ttu-id="41a09-145">Json</span><span class="sxs-lookup"><span data-stu-id="41a09-145">Json</span></span>|<span data-ttu-id="41a09-p107">Opcional. Matriz bidimensional de valores sin formato de la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="41a09-p107">Optional. A 2-dimensional array of unformatted values of the table row.</span></span>|

## <a name="response"></a><span data-ttu-id="41a09-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41a09-148">Response</span></span>

<span data-ttu-id="41a09-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookTableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41a09-149">If successful, this method returns `200 OK` response code and [groupSetting](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41a09-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41a09-150">Example</span></span>
<span data-ttu-id="41a09-151">En este ejemplo se insertan dos filas de datos al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="41a09-151">In this example two rows of data are inserted at the end of the table.</span></span> 

##### <a name="request"></a><span data-ttu-id="41a09-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41a09-152">Request</span></span>
<span data-ttu-id="41a09-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41a09-153">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="41a09-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41a09-154">Response</span></span>
<span data-ttu-id="41a09-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41a09-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "Warning: /api-reference/v1.0/api/tablerowcollection_add.md/tablerowcollection_add/values:
      Inconsistent types between parameter (Collection) and table (None)",
    "Error: /api-reference/v1.0/api/tablerowcollection_add.md/tablerowcollection_add/values:
      Type mismatch between example and table. Parameter name: values; example type (Collection(Collection)) is a collection, while the table description type (microsoft.graph.Json) is not."
  ],
  "tocPath": ""
}-->
