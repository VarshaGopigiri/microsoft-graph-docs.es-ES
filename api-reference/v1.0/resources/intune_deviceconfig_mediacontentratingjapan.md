# <a name="mediacontentratingjapan-resource-type"></a><span data-ttu-id="4647a-101">Tipo de recurso mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="4647a-101">mediaContentRatingJapan resource type</span></span>

> <span data-ttu-id="4647a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4647a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4647a-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4647a-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="4647a-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4647a-104">Properties</span></span>
|<span data-ttu-id="4647a-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4647a-105">Property</span></span>|<span data-ttu-id="4647a-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4647a-106">Type</span></span>|<span data-ttu-id="4647a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4647a-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4647a-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="4647a-108">movieRating</span></span>|[<span data-ttu-id="4647a-109">ratingJapanMoviesType</span><span class="sxs-lookup"><span data-stu-id="4647a-109">ratingJapanMoviesType</span></span>](../resources/intune_deviceconfig_ratingjapanmoviestype.md)|<span data-ttu-id="4647a-p101">Calificación de películas seleccionada para Japón. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="4647a-p101">Movies rating selected for Japan Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="4647a-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="4647a-112">tvRating</span></span>|[<span data-ttu-id="4647a-113">ratingJapanTelevisionType</span><span class="sxs-lookup"><span data-stu-id="4647a-113">ratingJapanTelevisionType</span></span>](../resources/intune_deviceconfig_ratingjapantelevisiontype.md)|<span data-ttu-id="4647a-p102">Calificación de TV seleccionada para Japón. Los valores posibles son: `allAllowed`, `allBlocked` y `explicitAllowed`.</span><span class="sxs-lookup"><span data-stu-id="4647a-p102">TV rating selected for Japan Possible values are: `allAllowed`, `allBlocked`, `explicitAllowed`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4647a-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4647a-116">Relationships</span></span>
<span data-ttu-id="4647a-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4647a-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4647a-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4647a-118">JSON Representation</span></span>
<span data-ttu-id="4647a-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4647a-119">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingJapan"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingJapan",
  "movieRating": "String",
  "tvRating": "String"
}
```








