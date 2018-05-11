# <a name="timezonebase-resource-type"></a><span data-ttu-id="735c1-101">Tipo de recurso timeZoneBase</span><span class="sxs-lookup"><span data-stu-id="735c1-101">timeZoneBase resource type</span></span>

<span data-ttu-id="735c1-102">Representación básica de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="735c1-102">The basic representation of a time zone.</span></span>


## <a name="properties"></a><span data-ttu-id="735c1-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="735c1-103">Properties</span></span>
| <span data-ttu-id="735c1-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="735c1-104">Property</span></span>     | <span data-ttu-id="735c1-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="735c1-105">Type</span></span>   |<span data-ttu-id="735c1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="735c1-106">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="735c1-107">name</span><span class="sxs-lookup"><span data-stu-id="735c1-107">name</span></span> | <span data-ttu-id="735c1-108">string</span><span class="sxs-lookup"><span data-stu-id="735c1-108">string</span></span> | <span data-ttu-id="735c1-109">Nombre de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="735c1-109">The name of a time zone.</span></span> <span data-ttu-id="735c1-110">Puede ser un nombre de zona de hora estándar como "hora estándar de Hawái-Aleutianas" o "zona horaria personalizada" para una zona horaria personalizada.</span><span class="sxs-lookup"><span data-stu-id="735c1-110">It can be a standard time zone name such as "Hawaii-Aleutian Standard Time", or "Customized Time Zone" for a custom time zone.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="735c1-111">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="735c1-111">JSON representation</span></span>

<span data-ttu-id="735c1-112">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="735c1-112">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneBase"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->