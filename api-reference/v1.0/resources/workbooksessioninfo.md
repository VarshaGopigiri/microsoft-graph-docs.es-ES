# <a name="workbooksessioninfo-resource-type"></a><span data-ttu-id="e9eea-101">Tipo de recurso workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="e9eea-101">workbookSessionInfo resource type</span></span>

<span data-ttu-id="e9eea-102">Proporciona información sobre la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="e9eea-102">Provides information about workbook session.</span></span>


## <a name="json-representation"></a><span data-ttu-id="e9eea-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e9eea-103">JSON representation</span></span>

<span data-ttu-id="e9eea-104">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e9eea-104">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.workbookSessionInfo"
}-->

```json
{
  "id": "string",
  "persistChanges": true
}
```

## <a name="properties"></a><span data-ttu-id="e9eea-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9eea-105">Properties</span></span>

| <span data-ttu-id="e9eea-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9eea-106">Property</span></span> | <span data-ttu-id="e9eea-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9eea-107">Type</span></span>  | <span data-ttu-id="e9eea-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9eea-108">Description</span></span>                               |
|:---------|:------|:------------------------------------------|
| <span data-ttu-id="e9eea-109">id</span><span class="sxs-lookup"><span data-stu-id="e9eea-109">id</span></span>  | <span data-ttu-id="e9eea-110">string</span><span class="sxs-lookup"><span data-stu-id="e9eea-110">string</span></span> | <span data-ttu-id="e9eea-111">Identificador de la sesión del libro.</span><span class="sxs-lookup"><span data-stu-id="e9eea-111">Id of the workbook session.</span></span> |
| <span data-ttu-id="e9eea-112">persistChanges</span><span class="sxs-lookup"><span data-stu-id="e9eea-112">persistChanges</span></span> | <span data-ttu-id="e9eea-113">string</span><span class="sxs-lookup"><span data-stu-id="e9eea-113">string</span></span> |  <span data-ttu-id="e9eea-114">`true` para la sesión persistente.</span><span class="sxs-lookup"><span data-stu-id="e9eea-114">`true` for persistent session.</span></span> <span data-ttu-id="e9eea-115">`false` para la sesión no persistente (modo de visualización)</span><span class="sxs-lookup"><span data-stu-id="e9eea-115">`false` for non-persistent session (view mode)</span></span> |

