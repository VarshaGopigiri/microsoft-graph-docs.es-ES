# <a name="mediacontentratingunitedkingdom-resource-type"></a><span data-ttu-id="817c4-101">Tipo de recurso mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="817c4-101">mediaContentRatingUnitedKingdom resource type</span></span>

> <span data-ttu-id="817c4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="817c4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="817c4-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="817c4-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="817c4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="817c4-104">Properties</span></span>
|<span data-ttu-id="817c4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="817c4-105">Property</span></span>|<span data-ttu-id="817c4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="817c4-106">Type</span></span>|<span data-ttu-id="817c4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="817c4-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="817c4-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="817c4-108">movieRating</span></span>|[<span data-ttu-id="817c4-109">ratingUnitedKingdomMoviesType</span><span class="sxs-lookup"><span data-stu-id="817c4-109">ratingUnitedKingdomMoviesType</span></span>](../resources/intune_deviceconfig_ratingunitedkingdommoviestype.md)|<span data-ttu-id="817c4-110">Películas de clasificación seleccionado para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="817c4-110">Movies rating selected for United Kingdom.</span></span> <span data-ttu-id="817c4-111">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="817c4-111">Possible values are: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15`, `adults`.</span></span>|
|<span data-ttu-id="817c4-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="817c4-112">tvRating</span></span>|[<span data-ttu-id="817c4-113">ratingUnitedKingdomTelevisionType</span><span class="sxs-lookup"><span data-stu-id="817c4-113">ratingUnitedKingdomTelevisionType</span></span>](../resources/intune_deviceconfig_ratingunitedkingdomtelevisiontype.md)|<span data-ttu-id="817c4-114">Clasificación de TV seleccionada para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="817c4-114">TV rating selected for United Kingdom.</span></span> <span data-ttu-id="817c4-115">Los valores posibles son: `allAllowed`, `allBlocked` y `caution`.</span><span class="sxs-lookup"><span data-stu-id="817c4-115">Possible values are: `allAllowed`, `allBlocked`, `caution`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="817c4-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="817c4-116">Relationships</span></span>
<span data-ttu-id="817c4-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="817c4-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="817c4-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="817c4-118">JSON Representation</span></span>
<span data-ttu-id="817c4-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="817c4-119">Here is a JSON representation of the resource.</span></span>
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



