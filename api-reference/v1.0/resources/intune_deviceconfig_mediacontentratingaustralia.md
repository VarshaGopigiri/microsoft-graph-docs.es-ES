# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="5c25d-101">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="5c25d-101">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="5c25d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c25d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c25d-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5c25d-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="5c25d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c25d-104">Properties</span></span>
|<span data-ttu-id="5c25d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c25d-105">Property</span></span>|<span data-ttu-id="5c25d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c25d-106">Type</span></span>|<span data-ttu-id="5c25d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c25d-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c25d-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="5c25d-108">movieRating</span></span>|[<span data-ttu-id="5c25d-109">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="5c25d-109">ratingAustraliaMoviesType</span></span>](../resources/intune_deviceconfig_ratingaustraliamoviestype.md)|<span data-ttu-id="5c25d-110">Clasificación de películas seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="5c25d-110">Movies rating selected for Australia Possible values are: , , , , , , .</span></span> <span data-ttu-id="5c25d-111">Los valores posibles son `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="5c25d-111">The possible values are `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`, , , , , or .</span></span>|
|<span data-ttu-id="5c25d-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="5c25d-112">tvRating</span></span>|[<span data-ttu-id="5c25d-113">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="5c25d-113">ratingAustraliaTelevisionType</span></span>](../resources/intune_deviceconfig_ratingaustraliatelevisiontype.md)|<span data-ttu-id="5c25d-114">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="5c25d-114">TV rating selected for Australia Possible values are: , , , , , , , , .</span></span> <span data-ttu-id="5c25d-115">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="5c25d-115">The possible values are `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`, , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="5c25d-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5c25d-116">Relationships</span></span>
<span data-ttu-id="5c25d-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5c25d-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5c25d-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5c25d-118">JSON Representation</span></span>
<span data-ttu-id="5c25d-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5c25d-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingAustralia"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingAustralia",
  "movieRating": "String",
  "tvRating": "String"
}
```



