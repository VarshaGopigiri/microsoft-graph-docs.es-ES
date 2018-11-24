# <a name="operationerror-resource-type"></a><span data-ttu-id="20466-101">tipo de recurso operationError</span><span class="sxs-lookup"><span data-stu-id="20466-101">operationError resource type</span></span>



<span data-ttu-id="20466-102">Se describen los errores en [teamsAsyncOperation](teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="20466-102">Describes errors in [teamsAsyncOperation](teamsasyncoperation.md).</span></span>

## <a name="operationerror-properties"></a><span data-ttu-id="20466-103">Propiedades de operationError</span><span class="sxs-lookup"><span data-stu-id="20466-103">operationError Properties</span></span>
| <span data-ttu-id="20466-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20466-104">Property</span></span>     | <span data-ttu-id="20466-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="20466-105">Type</span></span>   |<span data-ttu-id="20466-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="20466-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="20466-107">código</span><span class="sxs-lookup"><span data-stu-id="20466-107">code</span></span>|<span data-ttu-id="20466-108">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="20466-108">string (readonly)</span></span>|<span data-ttu-id="20466-109">Código de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="20466-109">Operation error code.</span></span>|
|<span data-ttu-id="20466-110">mensaje</span><span class="sxs-lookup"><span data-stu-id="20466-110">message</span></span>|<span data-ttu-id="20466-111">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="20466-111">string (readonly)</span></span>|<span data-ttu-id="20466-112">Mensaje de error de la operación.</span><span class="sxs-lookup"><span data-stu-id="20466-112">Operation error message.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="20466-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="20466-113">JSON representation</span></span>

<span data-ttu-id="20466-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="20466-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.operationError"
}-->

```json
{
    "code": "TeamUnavailable",
    "message": "The team was not found."
}
```

<!-- uuid: 069fadaa-52db-4ced-85d5-74f7caa2c66f
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation error resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
