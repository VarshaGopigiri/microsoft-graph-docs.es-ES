# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="25a73-101">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="25a73-101">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="25a73-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25a73-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25a73-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="25a73-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="25a73-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25a73-104">Properties</span></span>
|<span data-ttu-id="25a73-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25a73-105">Property</span></span>|<span data-ttu-id="25a73-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="25a73-106">Type</span></span>|<span data-ttu-id="25a73-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="25a73-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25a73-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="25a73-108">movieRating</span></span>|[<span data-ttu-id="25a73-109">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="25a73-109">ratingAustraliaMoviesType</span></span>](../resources/intune_deviceconfig_ratingaustraliamoviestype.md)|<span data-ttu-id="25a73-110">Películas de clasificación seleccionado para Australia.</span><span class="sxs-lookup"><span data-stu-id="25a73-110">Movies rating selected for Australia.</span></span> <span data-ttu-id="25a73-111">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="25a73-111">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="25a73-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="25a73-112">tvRating</span></span>|[<span data-ttu-id="25a73-113">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="25a73-113">ratingAustraliaTelevisionType</span></span>](../resources/intune_deviceconfig_ratingaustraliatelevisiontype.md)|<span data-ttu-id="25a73-114">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="25a73-114">TV rating selected for Australia.</span></span> <span data-ttu-id="25a73-115">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="25a73-115">Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="25a73-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="25a73-116">Relationships</span></span>
<span data-ttu-id="25a73-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="25a73-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="25a73-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25a73-118">JSON Representation</span></span>
<span data-ttu-id="25a73-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="25a73-119">Here is a JSON representation of the resource.</span></span>
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



