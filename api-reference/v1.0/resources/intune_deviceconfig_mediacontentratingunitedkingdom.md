# <a name="mediacontentratingunitedkingdom-resource-type"></a><span data-ttu-id="7f494-101">Tipo de recurso mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="7f494-101">mediaContentRatingUnitedKingdom resource type</span></span>

> <span data-ttu-id="7f494-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7f494-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7f494-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7f494-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="7f494-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7f494-104">Properties</span></span>
|<span data-ttu-id="7f494-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7f494-105">Property</span></span>|<span data-ttu-id="7f494-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f494-106">Type</span></span>|<span data-ttu-id="7f494-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f494-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7f494-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="7f494-108">movieRating</span></span>|[<span data-ttu-id="7f494-109">ratingUnitedKingdomMoviesType</span><span class="sxs-lookup"><span data-stu-id="7f494-109">ratingUnitedKingdomMoviesType</span></span>](../resources/intune_deviceconfig_ratingunitedkingdommoviestype.md)|<span data-ttu-id="7f494-110">Clasificación de películas seleccionada para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="7f494-110">Movies rating selected for United Kingdom Possible values are: , , , , , , , , .</span></span> <span data-ttu-id="7f494-111">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="7f494-111">The possible values are `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15`, `adults`, , , or .</span></span>|
|<span data-ttu-id="7f494-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="7f494-112">tvRating</span></span>|[<span data-ttu-id="7f494-113">ratingUnitedKingdomTelevisionType</span><span class="sxs-lookup"><span data-stu-id="7f494-113">ratingUnitedKingdomTelevisionType</span></span>](../resources/intune_deviceconfig_ratingunitedkingdomtelevisiontype.md)|<span data-ttu-id="7f494-114">Clasificación de TV seleccionada para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="7f494-114">TV rating selected for United Kingdom Possible values are: , , .</span></span> <span data-ttu-id="7f494-115">Los valores posibles son: `allAllowed`, `allBlocked` y `caution`.</span><span class="sxs-lookup"><span data-stu-id="7f494-115">The possible values are `allAllowed`, `allBlocked`, `caution`, , , , , , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="7f494-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7f494-116">Relationships</span></span>
<span data-ttu-id="7f494-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7f494-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7f494-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7f494-118">JSON Representation</span></span>
<span data-ttu-id="7f494-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7f494-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedKingdom",
  "movieRating": "String",
  "tvRating": "String"
}
```



