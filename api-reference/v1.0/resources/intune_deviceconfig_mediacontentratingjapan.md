# <a name="mediacontentratingjapan-resource-type"></a><span data-ttu-id="b9108-101">Tipo de recurso mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="b9108-101">mediaContentRatingJapan resource type</span></span>

> <span data-ttu-id="b9108-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9108-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9108-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b9108-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="b9108-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9108-104">Properties</span></span>
|<span data-ttu-id="b9108-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9108-105">Property</span></span>|<span data-ttu-id="b9108-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9108-106">Type</span></span>|<span data-ttu-id="b9108-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9108-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b9108-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="b9108-108">movieRating</span></span>|[<span data-ttu-id="b9108-109">ratingJapanMoviesType</span><span class="sxs-lookup"><span data-stu-id="b9108-109">ratingJapanMoviesType</span></span>](../resources/intune_deviceconfig_ratingjapanmoviestype.md)|<span data-ttu-id="b9108-110">Clasificación de películas seleccionada para Japón.</span><span class="sxs-lookup"><span data-stu-id="b9108-110">Movies rating selected for Japan Possible values are: , , , , , .</span></span> <span data-ttu-id="b9108-111">Los valores posibles son `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="b9108-111">The possible values are `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`, , , , , , or .</span></span>|
|<span data-ttu-id="b9108-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="b9108-112">tvRating</span></span>|[<span data-ttu-id="b9108-113">ratingJapanTelevisionType</span><span class="sxs-lookup"><span data-stu-id="b9108-113">ratingJapanTelevisionType</span></span>](../resources/intune_deviceconfig_ratingjapantelevisiontype.md)|<span data-ttu-id="b9108-114">Clasificación de TV seleccionada para Japón.</span><span class="sxs-lookup"><span data-stu-id="b9108-114">TV rating selected for Japan Possible values are: , , .</span></span> <span data-ttu-id="b9108-115">Los valores posibles son: `allAllowed`, `allBlocked` y `explicitAllowed`.</span><span class="sxs-lookup"><span data-stu-id="b9108-115">The possible values are `allAllowed`, `allBlocked`, `explicitAllowed`, , , , , , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="b9108-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b9108-116">Relationships</span></span>
<span data-ttu-id="b9108-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b9108-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b9108-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9108-118">JSON Representation</span></span>
<span data-ttu-id="b9108-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b9108-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingJapan"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingJapan",
  "movieRating": "String",
  "tvRating": "String"
}
```



