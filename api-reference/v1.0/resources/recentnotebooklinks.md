# <a name="recentnotebooklinks-resource-type"></a><span data-ttu-id="e549f-101">Tipo de recurso recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="e549f-101">recentNotebookLinks resource type</span></span>

<span data-ttu-id="e549f-102">Vínculos para abrir un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e549f-102">Links for opening a OneNote notebook.</span></span> <span data-ttu-id="e549f-103">Este tipo de recurso existe como propiedad en un recurso [recentNotebook](recentnotebook.md).</span><span class="sxs-lookup"><span data-stu-id="e549f-103">This resource type exists as a property on a [recentNotebook](recentnotebook.md) resource.</span></span>

## <a name="properties"></a><span data-ttu-id="e549f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e549f-104">Properties</span></span>
| <span data-ttu-id="e549f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e549f-105">Property</span></span>     | <span data-ttu-id="e549f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e549f-106">Type</span></span>   |<span data-ttu-id="e549f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e549f-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e549f-108">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="e549f-108">oneNoteClientUrl</span></span>|[<span data-ttu-id="e549f-109">externalLink</span><span class="sxs-lookup"><span data-stu-id="e549f-109">externalLink</span></span>](externallink.md)|<span data-ttu-id="e549f-110">Abre el bloc de notas en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="e549f-110">Opens the notebook in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="e549f-111">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="e549f-111">oneNoteWebUrl</span></span>|[<span data-ttu-id="e549f-112">externalLink</span><span class="sxs-lookup"><span data-stu-id="e549f-112">externalLink</span></span>](externallink.md)|<span data-ttu-id="e549f-113">Abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="e549f-113">Opens the notebook in OneNote Online.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e549f-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e549f-114">JSON representation</span></span>

<span data-ttu-id="e549f-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e549f-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recentNotebookLinks"
}-->

```json
{
  "oneNoteClientUrl": {"@odata.type": "microsoft.graph.externalLink"},
  "oneNoteWebUrl": {"@odata.type": "microsoft.graph.externalLink"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recentNotebookLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
