# <a name="tablecolumncollection-add"></a><span data-ttu-id="6340d-101">TableColumnCollection: add</span><span class="sxs-lookup"><span data-stu-id="6340d-101">TableColumnCollection: add</span></span>

<span data-ttu-id="6340d-102">Agrega una nueva columna a la tabla.</span><span class="sxs-lookup"><span data-stu-id="6340d-102">Adds a new column to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="6340d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6340d-103">Permissions</span></span>
<span data-ttu-id="6340d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6340d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6340d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6340d-106">Permission type</span></span>      | <span data-ttu-id="6340d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6340d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6340d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6340d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6340d-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6340d-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6340d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6340d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6340d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6340d-111">Not supported.</span></span>    |
|<span data-ttu-id="6340d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6340d-112">Application</span></span> | <span data-ttu-id="6340d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6340d-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6340d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6340d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/add

```
## <a name="request-headers"></a><span data-ttu-id="6340d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6340d-115">Request headers</span></span>
| <span data-ttu-id="6340d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6340d-116">Name</span></span>       | <span data-ttu-id="6340d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6340d-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6340d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="6340d-118">Authorization</span></span>  | <span data-ttu-id="6340d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6340d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6340d-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6340d-121">Request body</span></span>
<span data-ttu-id="6340d-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6340d-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6340d-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6340d-123">Parameter</span></span>    | <span data-ttu-id="6340d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="6340d-124">Type</span></span>   |<span data-ttu-id="6340d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6340d-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6340d-126">index</span><span class="sxs-lookup"><span data-stu-id="6340d-126">index</span></span>|<span data-ttu-id="6340d-127">number</span><span class="sxs-lookup"><span data-stu-id="6340d-127">number</span></span>|<span data-ttu-id="6340d-p103">Especifica la posición relativa de la nueva columna. La columna anterior en esta posición se desplaza hacia la derecha. El valor de índice debe ser igual o menor que el valor de índice de la última columna, por lo que no puede usarse para agregar una columna al final de la tabla. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="6340d-p103">Specifies the relative position of the new column. The previous column at this position is shifted to the right. The index value should be equal to or less than the last column's index value, so it cannot be used to append a column at the end of the table. Zero-indexed.</span></span>|
|<span data-ttu-id="6340d-132">values</span><span class="sxs-lookup"><span data-stu-id="6340d-132">values</span></span>|<span data-ttu-id="6340d-133">(boolean, string o number)</span><span class="sxs-lookup"><span data-stu-id="6340d-133">(boolean or string or number)</span></span>|<span data-ttu-id="6340d-p104">Opcional. Matriz bidimensional de valores sin formato de la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6340d-p104">Optional. A 2-dimensional array of unformatted values of the table column.</span></span>|

## <a name="response"></a><span data-ttu-id="6340d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6340d-136">Response</span></span>

<span data-ttu-id="6340d-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6340d-137">If successful, this method returns `200 OK` response code and [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6340d-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6340d-138">Example</span></span>
<span data-ttu-id="6340d-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6340d-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6340d-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6340d-140">Request</span></span>
<span data-ttu-id="6340d-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6340d-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="6340d-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6340d-142">Response</span></span>
<span data-ttu-id="6340d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6340d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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