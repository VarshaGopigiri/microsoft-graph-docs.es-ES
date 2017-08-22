# <a name="tablerowcollection-add"></a><span data-ttu-id="4f79d-101">TableRowCollection: add</span><span class="sxs-lookup"><span data-stu-id="4f79d-101">TableRowCollection: add</span></span>

<span data-ttu-id="4f79d-102">Agrega una nueva fila a la tabla.</span><span class="sxs-lookup"><span data-stu-id="4f79d-102">Adds a new row to the table.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4f79d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4f79d-103">Prerequisites</span></span>
<span data-ttu-id="4f79d-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="4f79d-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="4f79d-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4f79d-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="4f79d-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f79d-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/add

```
## <a name="request-headers"></a><span data-ttu-id="4f79d-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f79d-107">Request headers</span></span>
| <span data-ttu-id="4f79d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f79d-108">Name</span></span>       | <span data-ttu-id="4f79d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f79d-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4f79d-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="4f79d-110">Authorization</span></span>  | <span data-ttu-id="4f79d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f79d-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="4f79d-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f79d-113">Request body</span></span>
<span data-ttu-id="4f79d-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4f79d-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4f79d-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4f79d-115">Parameter</span></span>    | <span data-ttu-id="4f79d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f79d-116">Type</span></span>   |<span data-ttu-id="4f79d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f79d-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4f79d-118">index</span><span class="sxs-lookup"><span data-stu-id="4f79d-118">index</span></span>|<span data-ttu-id="4f79d-119">number</span><span class="sxs-lookup"><span data-stu-id="4f79d-119">number</span></span>|<span data-ttu-id="4f79d-p102">Opcional. Especifica la posición relativa de la nueva fila. Si es null, se produce la adición al final. Las filas situadas debajo de la fila insertada se desplazan hacia abajo. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="4f79d-p102">Optional. Specifies the relative position of the new row. If null, the addition happens at the end. Any rows below the inserted row are shifted downwards. Zero-indexed.</span></span>|
|<span data-ttu-id="4f79d-125">values</span><span class="sxs-lookup"><span data-stu-id="4f79d-125">values</span></span>|<span data-ttu-id="4f79d-126">(boolean, string o number)</span><span class="sxs-lookup"><span data-stu-id="4f79d-126">(boolean or string or number)</span></span>|<span data-ttu-id="4f79d-p103">Opcional. Matriz bidimensional de valores sin formato de la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4f79d-p103">Optional. A 2-dimensional array of unformatted values of the table row.</span></span>|

## <a name="response"></a><span data-ttu-id="4f79d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f79d-129">Response</span></span>

<span data-ttu-id="4f79d-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f79d-130">If successful, this method returns `200, OK` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f79d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f79d-131">Example</span></span>
<span data-ttu-id="4f79d-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4f79d-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4f79d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f79d-133">Request</span></span>
<span data-ttu-id="4f79d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f79d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablerowcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows/add
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

##### <a name="response"></a><span data-ttu-id="4f79d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f79d-135">Response</span></span>
<span data-ttu-id="4f79d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f79d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
