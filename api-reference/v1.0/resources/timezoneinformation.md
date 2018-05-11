# <a name="timezoneinformation-resource-type"></a><span data-ttu-id="355b4-101">Tipo de recurso timeZoneInformation</span><span class="sxs-lookup"><span data-stu-id="355b4-101">timeZoneInformation resource type</span></span>


<span data-ttu-id="355b4-102">Representa una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="355b4-102">Represents information about a time zone.</span></span> <span data-ttu-id="355b4-103">El formato admitido es Windows y, cuando se corrija el problema conocido actual, también se admitirá el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](http://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="355b4-103">The supported format is Windows, and [Internet Assigned Numbers Authority (IANA) time zone](http://www.iana.org/time-zones) (also known as Olson time zone) format as well when the current known problem is fixed.</span></span>

## <a name="properties"></a><span data-ttu-id="355b4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="355b4-104">Properties</span></span>
| <span data-ttu-id="355b4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="355b4-105">Property</span></span>     | <span data-ttu-id="355b4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="355b4-106">Type</span></span>   |<span data-ttu-id="355b4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="355b4-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="355b4-108">alias</span><span class="sxs-lookup"><span data-stu-id="355b4-108">alias</span></span>|<span data-ttu-id="355b4-109">string</span><span class="sxs-lookup"><span data-stu-id="355b4-109">string</span></span>|<span data-ttu-id="355b4-110">Identificador de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="355b4-110">An identifier for the time zone.</span></span>|
|<span data-ttu-id="355b4-111">displayName</span><span class="sxs-lookup"><span data-stu-id="355b4-111">displayName</span></span>|<span data-ttu-id="355b4-112">string</span><span class="sxs-lookup"><span data-stu-id="355b4-112">string</span></span>|<span data-ttu-id="355b4-113">Cadena de visualización que representa la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="355b4-113">A display string that represents the time zone.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="355b4-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="355b4-114">JSON representation</span></span>

<span data-ttu-id="355b4-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="355b4-115">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneInformation"
}-->

```json
{
  "alias": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->