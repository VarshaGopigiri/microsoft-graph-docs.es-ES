# <a name="locationconstraint-resource-type"></a><span data-ttu-id="351a4-101">Tipo de recurso locationConstraint</span><span class="sxs-lookup"><span data-stu-id="351a4-101">locationConstraint resource type</span></span>

<span data-ttu-id="351a4-102">Las condiciones establecidas por un cliente para la ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="351a4-102">The conditions stated by a client for the location of a meeting.</span></span>

## <a name="json-representation"></a><span data-ttu-id="351a4-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="351a4-103">JSON representation</span></span>

<span data-ttu-id="351a4-104">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="351a4-104">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.locationConstraint"
}-->

```json
{
  "isRequired": true,
  "locations": [{"@odata.type": "microsoft.graph.locationConstraintItem"}],
  "suggestLocation": true
}

```
## <a name="properties"></a><span data-ttu-id="351a4-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="351a4-105">Properties</span></span>
| <span data-ttu-id="351a4-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="351a4-106">Property</span></span>     | <span data-ttu-id="351a4-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="351a4-107">Type</span></span>   |<span data-ttu-id="351a4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="351a4-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="351a4-109">isRequired</span><span class="sxs-lookup"><span data-stu-id="351a4-109">isRequired</span></span>|<span data-ttu-id="351a4-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="351a4-110">Boolean</span></span>|<span data-ttu-id="351a4-p101">El cliente solicita que el servicio incluya en la respuesta una ubicación para la reunión. Si esto es verdadero y todos los recursos están ocupados, [findMeetingTimes](../api/user_findmeetingtimes.md) no devolverá ninguna sugerencia de fecha de reunión. Si esto es falso y todos los recursos están ocupados, **findMeetingTimes** buscará igual fechas de reunión sin ubicación.</span><span class="sxs-lookup"><span data-stu-id="351a4-p101">The client requests the service to include in the response a meeting location for the meeting. If this is true and all the resources are busy, [findMeetingTimes](../api/user_findmeetingtimes.md) will not return any meeting time suggestions. If this is false and all the resources are busy, **findMeetingTimes** would still look for meeting times without locations.</span></span> |
|<span data-ttu-id="351a4-114">locations</span><span class="sxs-lookup"><span data-stu-id="351a4-114">locations</span></span>|<span data-ttu-id="351a4-115">Colección [locationConstraintItem](locationconstraintitem.md)</span><span class="sxs-lookup"><span data-stu-id="351a4-115">[locationConstraintItem](locationconstraintitem.md) collection</span></span>|<span data-ttu-id="351a4-116">Información de restricciones para una o más ubicaciones que el cliente solicita para la reunión.</span><span class="sxs-lookup"><span data-stu-id="351a4-116">Constraint information for one or more locations that the client requests for the meeting.</span></span>|
|<span data-ttu-id="351a4-117">suggestLocation</span><span class="sxs-lookup"><span data-stu-id="351a4-117">suggestLocation</span></span>|<span data-ttu-id="351a4-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="351a4-118">Boolean</span></span>|<span data-ttu-id="351a4-119">El cliente solicita al servicio que sugiera una o más ubicaciones de reunión.</span><span class="sxs-lookup"><span data-stu-id="351a4-119">The client requests the service to suggest one or more meeting locations.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->