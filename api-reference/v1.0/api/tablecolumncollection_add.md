# <a name="tablecolumncollection-add"></a><span data-ttu-id="b0550-101">TableColumnCollection: add</span><span class="sxs-lookup"><span data-stu-id="b0550-101">TableColumnCollection: add</span></span>

<span data-ttu-id="b0550-102">Agrega una nueva columna a la tabla.</span><span class="sxs-lookup"><span data-stu-id="b0550-102">Adds a new column to the table.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b0550-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b0550-103">Prerequisites</span></span>
<span data-ttu-id="b0550-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="b0550-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="b0550-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b0550-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="b0550-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b0550-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/add

```
## <a name="request-headers"></a><span data-ttu-id="b0550-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b0550-107">Request headers</span></span>
| <span data-ttu-id="b0550-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b0550-108">Name</span></span>       | <span data-ttu-id="b0550-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0550-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b0550-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b0550-110">Authorization</span></span>  | <span data-ttu-id="b0550-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0550-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="b0550-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b0550-113">Request body</span></span>
<span data-ttu-id="b0550-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b0550-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b0550-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b0550-115">Parameter</span></span>    | <span data-ttu-id="b0550-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0550-116">Type</span></span>   |<span data-ttu-id="b0550-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0550-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b0550-118">index</span><span class="sxs-lookup"><span data-stu-id="b0550-118">index</span></span>|<span data-ttu-id="b0550-119">number</span><span class="sxs-lookup"><span data-stu-id="b0550-119">number</span></span>|<span data-ttu-id="b0550-p102">Especifica la posición relativa de la nueva columna. La columna anterior en esta posición se desplaza hacia la derecha. El valor de índice debe ser igual o menor que el valor de índice de la última columna, por lo que no puede usarse para agregar una columna al final de la tabla. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="b0550-p102">Specifies the relative position of the new column. The previous column at this position is shifted to the right. The index value should be equal to or less than the last column's index value, so it cannot be used to append a column at the end of the table. Zero-indexed.</span></span>|
|<span data-ttu-id="b0550-124">values</span><span class="sxs-lookup"><span data-stu-id="b0550-124">values</span></span>|<span data-ttu-id="b0550-125">(boolean, string o number)</span><span class="sxs-lookup"><span data-stu-id="b0550-125">(boolean or string or number)</span></span>|<span data-ttu-id="b0550-p103">Opcional. Matriz bidimensional de valores sin formato de la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b0550-p103">Optional. A 2-dimensional array of unformatted values of the table column.</span></span>|

## <a name="response"></a><span data-ttu-id="b0550-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0550-128">Response</span></span>

<span data-ttu-id="b0550-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto [TableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0550-129">If successful, this method returns `200, OK` response code and [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b0550-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b0550-130">Example</span></span>
<span data-ttu-id="b0550-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b0550-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b0550-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b0550-132">Request</span></span>
<span data-ttu-id="b0550-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b0550-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumncollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/add
Content-type: application/json
Content-length: 51

{
  "index": {
  },
  "values": [
    {
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="b0550-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0550-134">Response</span></span>
<span data-ttu-id="b0550-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b0550-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn"
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
  "tocPath": ""
}-->