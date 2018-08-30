# <a name="recentnotebook-resource-type"></a><span data-ttu-id="5c957-101">Tipo de recurso recentNotebook</span><span class="sxs-lookup"><span data-stu-id="5c957-101">recentNotebook resource type</span></span>

<span data-ttu-id="5c957-102">Bloc de notas de OneNote al que se ha accedido recientemente.</span><span class="sxs-lookup"><span data-stu-id="5c957-102">A recently accessed OneNote notebook.</span></span> <span data-ttu-id="5c957-103">Un **recentNotebook** es similar a un [notebook](notebook.md) pero tiene menos propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c957-103">A **recentNotebook** is similar to a [notebook](notebook.md) but has fewer properties.</span></span>

## <a name="properties"></a><span data-ttu-id="5c957-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c957-104">Properties</span></span>
| <span data-ttu-id="5c957-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c957-105">Property</span></span>     | <span data-ttu-id="5c957-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c957-106">Type</span></span>   |<span data-ttu-id="5c957-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c957-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5c957-108">displayName</span><span class="sxs-lookup"><span data-stu-id="5c957-108">displayName</span></span>|<span data-ttu-id="5c957-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c957-109">String</span></span>|<span data-ttu-id="5c957-110">Nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="5c957-110">The name of the notebook.</span></span>|
|<span data-ttu-id="5c957-111">lastAccessedTime</span><span class="sxs-lookup"><span data-stu-id="5c957-111">lastAccessedTime</span></span>|<span data-ttu-id="5c957-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c957-112">DateTimeOffset</span></span>|<span data-ttu-id="5c957-p102">La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c957-p102">The date and time when the notebook was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="5c957-117">links</span><span class="sxs-lookup"><span data-stu-id="5c957-117">links</span></span>|[<span data-ttu-id="5c957-118">recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="5c957-118">recentNotebookLinks</span></span>](recentnotebooklinks.md)|<span data-ttu-id="5c957-119">Vínculos para abrir el bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="5c957-119">Links for opening the notebook.</span></span> <span data-ttu-id="5c957-120">El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="5c957-120">The `oneNoteClientURL` link opens the notebook in the OneNote client, if it's installed.</span></span> <span data-ttu-id="5c957-121">El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="5c957-121">The `oneNoteWebURL` link opens the notebook in OneNote Online.</span></span>|
|<span data-ttu-id="5c957-122">sourceService</span><span class="sxs-lookup"><span data-stu-id="5c957-122">sourceService</span></span>|<span data-ttu-id="5c957-123">onenoteSourceService</span><span class="sxs-lookup"><span data-stu-id="5c957-123">onenoteSourceService values</span></span>|<span data-ttu-id="5c957-124">Almacén de back-end donde reside el Bloc de notas, `OneDriveForBusiness` o `OneDrive`.</span><span class="sxs-lookup"><span data-stu-id="5c957-124">The backend store where the Notebook resides, either `OneDriveForBusiness` or `OneDrive`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5c957-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5c957-125">JSON representation</span></span>

<span data-ttu-id="5c957-126">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5c957-126">The following is a JSON representation of the resource.</span></span>

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

## <a name="methods"></a><span data-ttu-id="5c957-127">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c957-127">Methods</span></span>

| <span data-ttu-id="5c957-128">Método</span><span class="sxs-lookup"><span data-stu-id="5c957-128">Method</span></span>           | <span data-ttu-id="5c957-129">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c957-129">Return Type</span></span>    |<span data-ttu-id="5c957-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c957-130">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5c957-131">getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="5c957-131">getRecentNotebooks</span></span>](../api/notebook_getrecentnotebooks.md) | <span data-ttu-id="5c957-132">Colección [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="5c957-132">[notebook](notebook.md) collection</span></span> | <span data-ttu-id="5c957-133">Obtener una colección de los blocs de notas a los que el usuario ha accedido más recientemente.</span><span class="sxs-lookup"><span data-stu-id="5c957-133">Get a collection of the most recently accessed notebooks for the user.</span></span> |
