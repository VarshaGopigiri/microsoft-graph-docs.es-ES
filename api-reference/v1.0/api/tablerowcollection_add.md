# <a name="tablerowcollection-add"></a><span data-ttu-id="0a436-101">TableRowCollection: add</span><span class="sxs-lookup"><span data-stu-id="0a436-101">TableRowCollection: add</span></span>

<span data-ttu-id="0a436-102">Agrega una nueva fila a la tabla.</span><span class="sxs-lookup"><span data-stu-id="0a436-102">Adds a new row to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="0a436-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="0a436-103">Permissions</span></span>
<span data-ttu-id="0a436-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0a436-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0a436-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a436-106">Permission type</span></span>      | <span data-ttu-id="0a436-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a436-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0a436-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a436-108">Delegated (work or school account)</span></span> | <span data-ttu-id="0a436-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0a436-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0a436-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a436-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0a436-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a436-111">Not supported.</span></span>    |
|<span data-ttu-id="0a436-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a436-112">Application</span></span> | <span data-ttu-id="0a436-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a436-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0a436-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a436-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/add

```
## <a name="request-headers"></a><span data-ttu-id="0a436-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a436-115">Request headers</span></span>
| <span data-ttu-id="0a436-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a436-116">Name</span></span>       | <span data-ttu-id="0a436-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a436-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0a436-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a436-118">Authorization</span></span>  | <span data-ttu-id="0a436-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a436-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0a436-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0a436-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="0a436-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a436-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a436-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a436-124">Request body</span></span>
<span data-ttu-id="0a436-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0a436-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0a436-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0a436-126">Parameter</span></span>    | <span data-ttu-id="0a436-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a436-127">Type</span></span>   |<span data-ttu-id="0a436-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a436-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0a436-129">index</span><span class="sxs-lookup"><span data-stu-id="0a436-129">index</span></span>|<span data-ttu-id="0a436-130">number</span><span class="sxs-lookup"><span data-stu-id="0a436-130">number</span></span>|<span data-ttu-id="0a436-p104">Opcional. Especifica la posición relativa de la nueva fila. Si es null, se produce la adición al final. Las filas situadas debajo de la fila insertada se desplazan hacia abajo. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="0a436-p104">Optional. Specifies the relative position of the new row. If null, the addition happens at the end. Any rows below the inserted row are shifted downwards. Zero-indexed.</span></span>|
|<span data-ttu-id="0a436-136">values</span><span class="sxs-lookup"><span data-stu-id="0a436-136">values</span></span>|<span data-ttu-id="0a436-137">(boolean, string o number)</span><span class="sxs-lookup"><span data-stu-id="0a436-137">(boolean or string or number)</span></span>|<span data-ttu-id="0a436-p105">Opcional. Matriz bidimensional de valores sin formato de la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0a436-p105">Optional. A 2-dimensional array of unformatted values of the table row.</span></span>|

## <a name="response"></a><span data-ttu-id="0a436-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a436-140">Response</span></span>

<span data-ttu-id="0a436-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a436-141">If successful, this method returns `200 OK` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a436-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a436-142">Example</span></span>
<span data-ttu-id="0a436-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0a436-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0a436-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a436-144">Request</span></span>
<span data-ttu-id="0a436-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a436-145">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="0a436-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a436-146">Response</span></span>
<span data-ttu-id="0a436-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a436-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
