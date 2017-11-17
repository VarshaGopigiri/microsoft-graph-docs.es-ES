<span data-ttu-id="81915-p102">Tipo de operación asincrónica. Los valores pueden ser *ForceDelete* o *Verification*</span><span class="sxs-lookup"><span data-stu-id="81915-p102">Type of asynchronous operation. The values can be *ForceDelete* or *Verification*</span></span> | Tipo de operación asincrónica. Los valores pueden ser *ForceDelete* o *Verification* |
| <span data-ttu-id="81915-115">status</span><span class="sxs-lookup"><span data-stu-id="81915-115">status</span></span> | <span data-ttu-id="81915-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="81915-116">String</span></span> | <span data-ttu-id="81915-117">Estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="81915-117">Current status of the operation.</span></span> <br> <span data-ttu-id="81915-118">*Programada*: La operación se ha programado, pero no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="81915-118">*Scheduled* - Operation has been scheduled but has not started.</span></span> <br> <span data-ttu-id="81915-119">*En curso*: La tarea se ha iniciado y está en curso.</span><span class="sxs-lookup"><span data-stu-id="81915-119">*InProgress* - Task has started and is in progress.</span></span> <br> <span data-ttu-id="81915-120">*Error*: Se ha producido un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="81915-120">*Failed* - Operation has failed.</span></span> |

## <span data-ttu-id="81915-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="81915-121">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="81915-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="81915-122">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainState"
}-->

```json
{
  "lastActionDateTime": "String (timestamp)",
  "operation": "String",
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->