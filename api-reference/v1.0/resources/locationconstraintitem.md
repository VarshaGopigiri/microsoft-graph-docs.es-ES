# <a name="locationconstraintitem-resource-type"></a><span data-ttu-id="5965e-101">Tipo de recurso locationConstraintItem</span><span class="sxs-lookup"><span data-stu-id="5965e-101">locationConstraintItem resource type</span></span>

<span data-ttu-id="5965e-102">Las condiciones establecidas por un cliente para la ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="5965e-102">The conditions stated by a client for the location of a meeting.</span></span>

<span data-ttu-id="5965e-103">Derivado de [ubicación](location.md).</span><span class="sxs-lookup"><span data-stu-id="5965e-103">Derived from [location](location.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="5965e-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5965e-104">JSON representation</span></span>

<span data-ttu-id="5965e-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5965e-105">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.location",
  "@odata.type": "microsoft.graph.locationConstraintItem"
}-->

```json
{
  "resolveAvailability": true,
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "displayName": "string",
  "locationEmailAddress": "string"
}

```
## <a name="properties"></a><span data-ttu-id="5965e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5965e-106">Properties</span></span>
| <span data-ttu-id="5965e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5965e-107">Property</span></span>     | <span data-ttu-id="5965e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5965e-108">Type</span></span>   |<span data-ttu-id="5965e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5965e-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5965e-110">address</span><span class="sxs-lookup"><span data-stu-id="5965e-110">address</span></span> | [<span data-ttu-id="5965e-111">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="5965e-111">physicalAddress</span></span>](physicalAddress.md) |<span data-ttu-id="5965e-112">Dirección postal de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="5965e-112">The street address of the location.</span></span> |
| <span data-ttu-id="5965e-113">displayName</span><span class="sxs-lookup"><span data-stu-id="5965e-113">displayName</span></span>  | <span data-ttu-id="5965e-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="5965e-114">String</span></span> | <span data-ttu-id="5965e-115">Nombre asociado a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="5965e-115">The name associated with the location.</span></span>                       |
| <span data-ttu-id="5965e-116">locationEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5965e-116">locationEmailAddress</span></span> | <span data-ttu-id="5965e-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="5965e-117">String</span></span> | <span data-ttu-id="5965e-118">Dirección de correo electrónico opcional en la ubicación</span><span class="sxs-lookup"><span data-stu-id="5965e-118">Optional email address of the location.</span></span> |
| <span data-ttu-id="5965e-119">resolveAvailability</span><span class="sxs-lookup"><span data-stu-id="5965e-119">resolveAvailability</span></span> | <span data-ttu-id="5965e-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="5965e-120">Boolean</span></span> | <span data-ttu-id="5965e-p101">Si se establece en verdadero y el recurso especificado está ocupado [findMeetingTimes](../api/user_findmeetingtimes.md) buscará otro recurso que esté libre. Si se establece en falso y el recurso especificado está ocupado, **findMeetingTimes** devolverá el recurso mejor puntuado en la caché del usuario sin comprobar que esté libre o no. El valor predeterminado es "true".</span><span class="sxs-lookup"><span data-stu-id="5965e-p101">If set to true and the specified resource is busy, [findMeetingTimes](../api/user_findmeetingtimes.md) looks for another resource that is free. If set to false and the specified resource is busy, **findMeetingTimes** returns the resource best ranked in the user's cache without checking if it's free. Default is true.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraintItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->