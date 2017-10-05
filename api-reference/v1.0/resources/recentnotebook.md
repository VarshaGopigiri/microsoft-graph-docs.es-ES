# <a name="recentnotebook-resource-type"></a><span data-ttu-id="af0be-101">Tipo de recurso recentNotebook</span><span class="sxs-lookup"><span data-stu-id="af0be-101">recentNotebook resource type</span></span>

<span data-ttu-id="af0be-102">Bloc de notas de OneNote al que se ha accedido recientemente.</span><span class="sxs-lookup"><span data-stu-id="af0be-102">A recently accessed OneNote notebook.</span></span> <span data-ttu-id="af0be-103">Un **recentNotebook** es similar a un [notebook](notebook.md) pero tiene menos propiedades.</span><span class="sxs-lookup"><span data-stu-id="af0be-103">A **recentNotebook** is similar to a [notebook](notebook.md) but has fewer properties.</span></span>

## <a name="properties"></a><span data-ttu-id="af0be-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af0be-104">Properties</span></span>
| <span data-ttu-id="af0be-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af0be-105">Property</span></span>     | <span data-ttu-id="af0be-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="af0be-106">Type</span></span>   |<span data-ttu-id="af0be-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="af0be-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="af0be-108">name</span><span class="sxs-lookup"><span data-stu-id="af0be-108">name</span></span>|<span data-ttu-id="af0be-109">String</span><span class="sxs-lookup"><span data-stu-id="af0be-109">String</span></span>|<span data-ttu-id="af0be-110">Nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="af0be-110">The name of the notebook.</span></span>|
|<span data-ttu-id="af0be-111">lastAccessedTime</span><span class="sxs-lookup"><span data-stu-id="af0be-111">lastAccessedTime</span></span>|<span data-ttu-id="af0be-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="af0be-112">DateTimeOffset</span></span>|<span data-ttu-id="af0be-113">La fecha y la hora en que se modificó por última vez el bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="af0be-113">The date and time when the notebook was last modified.</span></span> <span data-ttu-id="af0be-114">La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC.</span><span class="sxs-lookup"><span data-stu-id="af0be-114">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="af0be-115">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="af0be-115">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span> <span data-ttu-id="af0be-116">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af0be-116">Read-only.</span></span>|
|<span data-ttu-id="af0be-117">links</span><span class="sxs-lookup"><span data-stu-id="af0be-117">links</span></span>|[<span data-ttu-id="af0be-118">recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="af0be-118">recentNotebookLinks</span></span>](recentnotebooklinks.md)|<span data-ttu-id="af0be-119">Vínculos para abrir el bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="af0be-119">Links for opening the notebook.</span></span> <span data-ttu-id="af0be-120">El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="af0be-120">The `oneNoteClientURL` link opens the notebook in the OneNote native client if it's installed.</span></span> <span data-ttu-id="af0be-121">El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="af0be-121">The `oneNoteWebURL` link opens the notebook in OneNote Online.</span></span>|
|<span data-ttu-id="af0be-122">sourceService</span><span class="sxs-lookup"><span data-stu-id="af0be-122">sourceService</span></span>|<span data-ttu-id="af0be-123">String</span><span class="sxs-lookup"><span data-stu-id="af0be-123">String</span></span>|<span data-ttu-id="af0be-124">Almacén de back-end donde reside el Bloc de notas, `OneDriveForBusiness` o `OneDrive`.</span><span class="sxs-lookup"><span data-stu-id="af0be-124">The backend store where the Notebook resides, either `OneDriveForBusiness` or `OneDrive`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="af0be-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af0be-125">JSON representation</span></span>

<span data-ttu-id="af0be-126">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="af0be-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recentNotebook"
}-->

```json
{
  "displayName": "String",
  "lastAccessedTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.recentNotebookLinks"},
  "sourceService": "String"
}

```

## <a name="methods"></a><span data-ttu-id="af0be-127">Métodos</span><span class="sxs-lookup"><span data-stu-id="af0be-127">Methods</span></span>

| <span data-ttu-id="af0be-128">Método</span><span class="sxs-lookup"><span data-stu-id="af0be-128">Method</span></span>           | <span data-ttu-id="af0be-129">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af0be-129">Return Type</span></span>    |<span data-ttu-id="af0be-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="af0be-130">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="af0be-131">getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="af0be-131">getRecentNotebooks</span></span>](../api/notebook_getrecentnotebooks.md) | <span data-ttu-id="af0be-132">Colección [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="af0be-132">[Notebook](notebook.md) collection</span></span> | <span data-ttu-id="af0be-133">Obtener una colección de los blocs de notas a los que el usuario ha accedido más recientemente.</span><span class="sxs-lookup"><span data-stu-id="af0be-133">Get a collection of the most recently accessed notebooks for the user.</span></span> |
