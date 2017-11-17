# <a name="tablecolumncollection-itemat"></a><span data-ttu-id="b31d3-101">TableColumnCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="b31d3-101">TableColumnCollection: ItemAt</span></span>

<span data-ttu-id="b31d3-102">Obtiene una columna en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="b31d3-102">Gets a column based on its position in the collection.</span></span>
## <a name="permissions"></a><span data-ttu-id="b31d3-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b31d3-103">Permissions</span></span>
<span data-ttu-id="b31d3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b31d3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b31d3-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b31d3-106">Permission type</span></span>      | <span data-ttu-id="b31d3-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b31d3-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b31d3-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b31d3-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b31d3-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b31d3-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b31d3-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b31d3-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b31d3-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b31d3-111">Not supported.</span></span>    |
|<span data-ttu-id="b31d3-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b31d3-112">Application</span></span> | <span data-ttu-id="b31d3-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b31d3-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b31d3-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b31d3-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/ItemAt
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="b31d3-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b31d3-115">Request headers</span></span>
| <span data-ttu-id="b31d3-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="b31d3-116">Name</span></span>       | <span data-ttu-id="b31d3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b31d3-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b31d3-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="b31d3-118">Authorization</span></span>  | <span data-ttu-id="b31d3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b31d3-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b31d3-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b31d3-121">Request body</span></span>
<span data-ttu-id="b31d3-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b31d3-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b31d3-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b31d3-123">Parameter</span></span>    | <span data-ttu-id="b31d3-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="b31d3-124">Type</span></span>   |<span data-ttu-id="b31d3-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="b31d3-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b31d3-126">index</span><span class="sxs-lookup"><span data-stu-id="b31d3-126">index</span></span>|<span data-ttu-id="b31d3-127">number</span><span class="sxs-lookup"><span data-stu-id="b31d3-127">number</span></span>|<span data-ttu-id="b31d3-p103">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="b31d3-p103">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="b31d3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b31d3-130">Response</span></span>

<span data-ttu-id="b31d3-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b31d3-131">If successful, this method returns `200 OK` response code and [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b31d3-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b31d3-132">Example</span></span>
<span data-ttu-id="b31d3-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b31d3-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b31d3-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b31d3-134">Request</span></span>
<span data-ttu-id="b31d3-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b31d3-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumncollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="b31d3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b31d3-136">Response</span></span>
<span data-ttu-id="b31d3-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b31d3-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableColumnCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->