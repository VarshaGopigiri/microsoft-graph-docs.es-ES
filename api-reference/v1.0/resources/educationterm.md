# <a name="educationterm-resource-type"></a><span data-ttu-id="17baf-101">Tipo de recurso educationTerm</span><span class="sxs-lookup"><span data-stu-id="17baf-101">educationTerm resource type</span></span>

<span data-ttu-id="17baf-102">Período.</span><span class="sxs-lookup"><span data-stu-id="17baf-102">A term.</span></span> <span data-ttu-id="17baf-103">Representa una parte designada del año académico.</span><span class="sxs-lookup"><span data-stu-id="17baf-103">This represents a designated portion of the academic year.</span></span> <span data-ttu-id="17baf-104">Se usa en [educationClass](educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="17baf-104">It is used within [educationClass](educationclass.md).</span></span>

## <a name="properties"></a><span data-ttu-id="17baf-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17baf-105">Properties</span></span>
| <span data-ttu-id="17baf-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17baf-106">Property</span></span>     | <span data-ttu-id="17baf-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="17baf-107">Type</span></span>   |<span data-ttu-id="17baf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="17baf-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="17baf-109">displayName</span><span class="sxs-lookup"><span data-stu-id="17baf-109">displayName</span></span>| <span data-ttu-id="17baf-110">String</span><span class="sxs-lookup"><span data-stu-id="17baf-110">String</span></span>| <span data-ttu-id="17baf-111">Nombre para mostrar del período.</span><span class="sxs-lookup"><span data-stu-id="17baf-111">Display name of the template.</span></span>| 
|<span data-ttu-id="17baf-112">externalId</span><span class="sxs-lookup"><span data-stu-id="17baf-112">externalId</span></span>|<span data-ttu-id="17baf-113">String</span><span class="sxs-lookup"><span data-stu-id="17baf-113">String</span></span>| <span data-ttu-id="17baf-114">Identificador del período en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="17baf-114">ID of term in the syncing system.</span></span>|
|<span data-ttu-id="17baf-115">startDate</span><span class="sxs-lookup"><span data-stu-id="17baf-115">startDate</span></span>|<span data-ttu-id="17baf-116">Date</span><span class="sxs-lookup"><span data-stu-id="17baf-116">Date</span></span>|<span data-ttu-id="17baf-117">Inicio del período.</span><span class="sxs-lookup"><span data-stu-id="17baf-117">Start of the term.</span></span>|
|<span data-ttu-id="17baf-118">endDate</span><span class="sxs-lookup"><span data-stu-id="17baf-118">endDate</span></span>|<span data-ttu-id="17baf-119">Date</span><span class="sxs-lookup"><span data-stu-id="17baf-119">Date</span></span>|<span data-ttu-id="17baf-120">Final del período.</span><span class="sxs-lookup"><span data-stu-id="17baf-120">End of the document.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="17baf-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17baf-121">JSON representation</span></span>

<span data-ttu-id="17baf-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="17baf-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationTerm"
}-->

```json
{
  "displayName": "String",
  "externalId": "String",
  "startDate": "Date",
  "endDate": "Date"
}
```

<!-- uuid: 4e9d671f-3068-4e09-aba2-b39e81a0e452
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationTerm resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->