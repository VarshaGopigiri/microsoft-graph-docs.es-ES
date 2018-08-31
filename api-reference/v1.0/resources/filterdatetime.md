# <a name="filterdatetime-resource-type"></a><span data-ttu-id="ee28a-101">Tipo de recurso FilterDatetime</span><span class="sxs-lookup"><span data-stu-id="ee28a-101">FilterDatetime resource type</span></span>

<span data-ttu-id="ee28a-102">Representa cómo se filtra una fecha cuando se filtran valores.</span><span class="sxs-lookup"><span data-stu-id="ee28a-102">Represents how to filter a date when filtering on values.</span></span>

## <a name="properties"></a><span data-ttu-id="ee28a-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee28a-103">Properties</span></span>
| <span data-ttu-id="ee28a-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee28a-104">Property</span></span>     | <span data-ttu-id="ee28a-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee28a-105">Type</span></span>   |<span data-ttu-id="ee28a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee28a-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee28a-107">date</span><span class="sxs-lookup"><span data-stu-id="ee28a-107">date</span></span>|<span data-ttu-id="ee28a-108">cadena</span><span class="sxs-lookup"><span data-stu-id="ee28a-108">string</span></span>|<span data-ttu-id="ee28a-109">La fecha en formato ISO8601 usada para filtrar los datos.</span><span class="sxs-lookup"><span data-stu-id="ee28a-109">The date in ISO8601 format used to filter data.</span></span>|
|<span data-ttu-id="ee28a-110">specificity</span><span class="sxs-lookup"><span data-stu-id="ee28a-110">specificity</span></span>|<span data-ttu-id="ee28a-111">cadena</span><span class="sxs-lookup"><span data-stu-id="ee28a-111">string</span></span>|<span data-ttu-id="ee28a-112">Cómo de específica tiene que ser la fecha para mantener los datos.</span><span class="sxs-lookup"><span data-stu-id="ee28a-112">How specific the date should be used to keep data.</span></span> <span data-ttu-id="ee28a-113">Por ejemplo, si la fecha es 02/04/2005 y el specifity se establece en "mes", la operación de filtrado mantendrá todas las filas con una fecha en el mes de abril de 2009.</span><span class="sxs-lookup"><span data-stu-id="ee28a-113">How specific the date should be used to keep data. For example, if the date is 2005-04-02 and the specifity is set to "month", the filter operation will keep all rows with a date in the month of april 2009. Possible values are: , , , , , .</span></span> <span data-ttu-id="ee28a-114">Los valores posibles son `Year`, `Monday`, `Day`, `Hour`, `Minute` y `Second`.</span><span class="sxs-lookup"><span data-stu-id="ee28a-114">The possible values are `Year`, `Monday`, `Day`, `Hour`, `Minute`, `Second`, , , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="ee28a-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ee28a-115">Relationships</span></span>
<span data-ttu-id="ee28a-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ee28a-116">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="ee28a-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee28a-117">JSON representation</span></span>

<span data-ttu-id="ee28a-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ee28a-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilterDateTime"
}-->

```json
{
  "date": "string",
  "specificity": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "FilterDatetime resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->