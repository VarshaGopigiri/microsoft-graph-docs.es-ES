# <a name="location-resource-type"></a><span data-ttu-id="05093-101">Tipo de recurso Location</span><span class="sxs-lookup"><span data-stu-id="05093-101">Location resource type</span></span>

<span data-ttu-id="05093-102">Representa información de ubicación de un evento.</span><span class="sxs-lookup"><span data-stu-id="05093-102">Represents location information of an event.</span></span>


## <a name="properties"></a><span data-ttu-id="05093-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="05093-103">Properties</span></span>
| <span data-ttu-id="05093-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05093-104">Property</span></span>  | <span data-ttu-id="05093-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="05093-105">Type</span></span>   | <span data-ttu-id="05093-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="05093-106">Description</span></span>                                                     |
|:----------|:-------|:----------------------------------------------------------------|
| <span data-ttu-id="05093-107">address</span><span class="sxs-lookup"><span data-stu-id="05093-107">address</span></span> | [<span data-ttu-id="05093-108">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="05093-108">physicalAddress</span></span>](physicaladdress.md) |<span data-ttu-id="05093-109">Dirección postal de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="05093-109">The street address of the location.</span></span> |
| <span data-ttu-id="05093-110">displayName</span><span class="sxs-lookup"><span data-stu-id="05093-110">displayName</span></span>  | <span data-ttu-id="05093-111">String</span><span class="sxs-lookup"><span data-stu-id="05093-111">String</span></span> | <span data-ttu-id="05093-112">Nombre asociado a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="05093-112">The name associated with the location.</span></span>                       |
| <span data-ttu-id="05093-113">locationEmailAddress</span><span class="sxs-lookup"><span data-stu-id="05093-113">locationEmailAddress</span></span> | <span data-ttu-id="05093-114">String</span><span class="sxs-lookup"><span data-stu-id="05093-114">String</span></span> | <span data-ttu-id="05093-115">Dirección de correo electrónico opcional en la ubicación</span><span class="sxs-lookup"><span data-stu-id="05093-115">Optional email address of the location.</span></span>              |

## <a name="json-representation"></a><span data-ttu-id="05093-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="05093-116">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.location"
}-->
```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "displayName": "string",
  "locationEmailAddress": "string"
}

```

## <a name="remarks"></a><span data-ttu-id="05093-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05093-117">Remarks</span></span>

<span data-ttu-id="05093-118">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="05093-118">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "location resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
