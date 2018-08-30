# <a name="tablecolumncollection-add"></a><span data-ttu-id="7e028-101">TableColumnCollection: add</span><span class="sxs-lookup"><span data-stu-id="7e028-101">TableColumnCollection: add</span></span>

<span data-ttu-id="7e028-102">Agrega una nueva columna a la tabla.</span><span class="sxs-lookup"><span data-stu-id="7e028-102">Adds a new column to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="7e028-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7e028-103">Permissions</span></span>
<span data-ttu-id="7e028-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7e028-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7e028-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e028-106">Permission type</span></span>      | <span data-ttu-id="7e028-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e028-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7e028-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e028-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7e028-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7e028-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7e028-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e028-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7e028-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e028-111">Not supported.</span></span>    |
|<span data-ttu-id="7e028-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e028-112">Application</span></span> | <span data-ttu-id="7e028-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e028-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7e028-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e028-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/add

```
## <a name="request-headers"></a><span data-ttu-id="7e028-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e028-115">Request headers</span></span>
| <span data-ttu-id="7e028-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="7e028-116">Name</span></span>       | <span data-ttu-id="7e028-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e028-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7e028-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="7e028-118">Authorization</span></span>  | <span data-ttu-id="7e028-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7e028-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7e028-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="7e028-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="7e028-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7e028-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7e028-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e028-124">Request body</span></span>
<span data-ttu-id="7e028-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7e028-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7e028-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7e028-126">Parameter</span></span>    | <span data-ttu-id="7e028-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e028-127">Type</span></span>   |<span data-ttu-id="7e028-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e028-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7e028-129">index</span><span class="sxs-lookup"><span data-stu-id="7e028-129">index</span></span>|<span data-ttu-id="7e028-130">Int32</span><span class="sxs-lookup"><span data-stu-id="7e028-130">Int32</span></span>|<span data-ttu-id="7e028-p104">Especifica la posición relativa de la nueva columna. La columna anterior en esta posición se desplaza hacia la derecha. El valor de índice debe ser igual o menor que el valor de índice de la última columna, por lo que no puede usarse para agregar una columna al final de la tabla. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="7e028-p104">Specifies the relative position of the new column. The previous column at this position is shifted to the right. The index value should be equal to or less than the last column's index value, so it cannot be used to append a column at the end of the table. Zero-indexed.</span></span>|
|<span data-ttu-id="7e028-135">values</span><span class="sxs-lookup"><span data-stu-id="7e028-135">values</span></span>|<span data-ttu-id="7e028-136">Json</span><span class="sxs-lookup"><span data-stu-id="7e028-136">Json</span></span>|<span data-ttu-id="7e028-p105">Opcional. Matriz bidimensional de valores sin formato de la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7e028-p105">Optional. A 2-dimensional array of unformatted values of the table column.</span></span>|
|<span data-ttu-id="7e028-139">name</span><span class="sxs-lookup"><span data-stu-id="7e028-139">name</span></span>|<span data-ttu-id="7e028-140">cadena</span><span class="sxs-lookup"><span data-stu-id="7e028-140">string</span></span>|<span data-ttu-id="7e028-141">nombre</span><span class="sxs-lookup"><span data-stu-id="7e028-141">name</span></span>
## <a name="response"></a><span data-ttu-id="7e028-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e028-142">Response</span></span>

<span data-ttu-id="7e028-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookTableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e028-143">If successful, this method returns `200 OK` response code and [groupSetting](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7e028-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e028-144">Example</span></span>
<span data-ttu-id="7e028-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7e028-145">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="7e028-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e028-146">Request</span></span>
<span data-ttu-id="7e028-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e028-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumncollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/add
Content-type: application/json
Content-length: 51

{
  "index": 3,
  "values": [
    {
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="7e028-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e028-148">Response</span></span>
<span data-ttu-id="7e028-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e028-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableColumn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableColumnCollection: add",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/api/tablecolumncollection_add.md/tablecolumncollection_add/values:
      Inconsistent types between parameter (Object) and table (None)",
    "Error: /api-reference/v1.0/api/tablecolumncollection_add.md/tablecolumncollection_add/values:
      Type mismatch between example and table. Parameter name: values; example type (Collection(Object)) is a collection, while the table description type (microsoft.graph.Json) is not."
  ],
  "tocPath": ""
}-->