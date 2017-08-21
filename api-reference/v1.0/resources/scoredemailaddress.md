# <a name="scoredemailaddress-resource-type"></a><span data-ttu-id="ccdba-101">Tipo de recurso scoredEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ccdba-101">scoredEmailAddress resource type</span></span>

<span data-ttu-id="ccdba-102">Representa una dirección de correo electrónico con puntuación.</span><span class="sxs-lookup"><span data-stu-id="ccdba-102">Represents a scored email address.</span></span>


## <a name="properties"></a><span data-ttu-id="ccdba-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ccdba-103">Properties</span></span>
| <span data-ttu-id="ccdba-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ccdba-104">Property</span></span>     | <span data-ttu-id="ccdba-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccdba-105">Type</span></span>   |<span data-ttu-id="ccdba-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccdba-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ccdba-107">address</span><span class="sxs-lookup"><span data-stu-id="ccdba-107">address</span></span>|<span data-ttu-id="ccdba-108">string</span><span class="sxs-lookup"><span data-stu-id="ccdba-108">string</span></span>|<span data-ttu-id="ccdba-109">La dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ccdba-109">The user's email address.</span></span>|
|<span data-ttu-id="ccdba-110">relevanceScore</span><span class="sxs-lookup"><span data-stu-id="ccdba-110">relevanceScore</span></span>|<span data-ttu-id="ccdba-111">double</span><span class="sxs-lookup"><span data-stu-id="ccdba-111">double</span></span>|<span data-ttu-id="ccdba-p101">La puntuación de relevancia de la dirección de correo electrónico. Una puntuación de relevancia se usa como criterio de ordenación con respecto a los demás resultados devueltos. Un valor de puntuación de relevancia más alto corresponde a un resultado más relevante. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="ccdba-p101">The relevance score of the email address. A relevance score is used as a sort key, in relation to the other returned results. A higher relevance score value corresponds to a more relevant result. Relevance is determined by the user’s communication and collaboration patterns and business relationships.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ccdba-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ccdba-116">JSON representation</span></span>

<span data-ttu-id="ccdba-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ccdba-117">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scoredEmailAddress"
}-->

```json
{
  "address": "string",
  "relevanceScore": 1024
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scoredEmailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
