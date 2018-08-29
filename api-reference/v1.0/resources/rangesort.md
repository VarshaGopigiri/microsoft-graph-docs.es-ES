# <a name="rangesort-resource-type"></a><span data-ttu-id="ba8c1-101">Tipo de recurso RangeSort</span><span class="sxs-lookup"><span data-stu-id="ba8c1-101">RangeSort resource type</span></span>

<span data-ttu-id="ba8c1-102">Administra operaciones de ordenación en objetos Range.</span><span class="sxs-lookup"><span data-stu-id="ba8c1-102">Manages sorting operations on Range objects.</span></span>


## <a name="methods"></a><span data-ttu-id="ba8c1-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="ba8c1-103">Methods</span></span>

| <span data-ttu-id="ba8c1-104">Método</span><span class="sxs-lookup"><span data-stu-id="ba8c1-104">Method</span></span>           | <span data-ttu-id="ba8c1-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba8c1-105">Return Type</span></span>    |<span data-ttu-id="ba8c1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba8c1-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ba8c1-107">Apply</span><span class="sxs-lookup"><span data-stu-id="ba8c1-107">Apply</span></span>](../api/rangesort_apply.md)|<span data-ttu-id="ba8c1-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ba8c1-108">None</span></span>|<span data-ttu-id="ba8c1-109">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="ba8c1-109">Perform a sort operation.</span></span>|

## <a name="properties"></a><span data-ttu-id="ba8c1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ba8c1-110">Properties</span></span>
<span data-ttu-id="ba8c1-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ba8c1-111">None</span></span>

## <a name="relationships"></a><span data-ttu-id="ba8c1-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ba8c1-112">Relationships</span></span>
<span data-ttu-id="ba8c1-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ba8c1-113">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="ba8c1-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ba8c1-114">JSON representation</span></span>

<span data-ttu-id="ba8c1-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ba8c1-115">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookRangeSort"
}-->

```json
{
}
```

##### <a name="request"></a><span data-ttu-id="ba8c1-116">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba8c1-116">Request</span></span>
<span data-ttu-id="ba8c1-117">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba8c1-117">Here is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "name": "range_sort"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/sort
```

##### <a name="response"></a><span data-ttu-id="ba8c1-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba8c1-118">Response</span></span>
<span data-ttu-id="ba8c1-119">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba8c1-119">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeSort"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeSort resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->