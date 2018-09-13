# <a name="mediacontentratinggermany-resource-type"></a><span data-ttu-id="f0e0d-101">Tipo de recurso mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="f0e0d-101">mediaContentRatingGermany resource type</span></span>

> <span data-ttu-id="f0e0d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f0e0d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f0e0d-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f0e0d-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="f0e0d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0e0d-104">Properties</span></span>
|<span data-ttu-id="f0e0d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f0e0d-105">Property</span></span>|<span data-ttu-id="f0e0d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0e0d-106">Type</span></span>|<span data-ttu-id="f0e0d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0e0d-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f0e0d-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="f0e0d-108">movieRating</span></span>|[<span data-ttu-id="f0e0d-109">ratingGermanyMoviesType</span><span class="sxs-lookup"><span data-stu-id="f0e0d-109">ratingGermanyMoviesType</span></span>](../resources/intune_deviceconfig_ratinggermanymoviestype.md)|<span data-ttu-id="f0e0d-p101">Calificación de películas seleccionada para Alemania. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="f0e0d-p101">Movies rating selected for Germany Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="f0e0d-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="f0e0d-112">tvRating</span></span>|[<span data-ttu-id="f0e0d-113">ratingGermanyTelevisionType</span><span class="sxs-lookup"><span data-stu-id="f0e0d-113">ratingGermanyTelevisionType</span></span>](../resources/intune_deviceconfig_ratinggermanytelevisiontype.md)|<span data-ttu-id="f0e0d-p102">Calificación de TV seleccionada para Alemania. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="f0e0d-p102">TV rating selected for Germany Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f0e0d-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f0e0d-116">Relationships</span></span>
<span data-ttu-id="f0e0d-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f0e0d-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f0e0d-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f0e0d-118">JSON Representation</span></span>
<span data-ttu-id="f0e0d-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f0e0d-119">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingGermany"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingGermany",
  "movieRating": "String",
  "tvRating": "String"
}
```








