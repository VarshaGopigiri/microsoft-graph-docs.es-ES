# <a name="mediacontentratingfrance-resource-type"></a><span data-ttu-id="467a0-101">Tipo de recurso mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="467a0-101">mediaContentRatingFrance resource type</span></span>

> <span data-ttu-id="467a0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="467a0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="467a0-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="467a0-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="467a0-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="467a0-104">Properties</span></span>
|<span data-ttu-id="467a0-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="467a0-105">Property</span></span>|<span data-ttu-id="467a0-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="467a0-106">Type</span></span>|<span data-ttu-id="467a0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="467a0-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="467a0-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="467a0-108">movieRating</span></span>|[<span data-ttu-id="467a0-109">ratingFranceMoviesType</span><span class="sxs-lookup"><span data-stu-id="467a0-109">ratingFranceMoviesType</span></span>](../resources/intune_deviceconfig_ratingfrancemoviestype.md)|<span data-ttu-id="467a0-110">Películas de clasificación seleccionado para Francia.</span><span class="sxs-lookup"><span data-stu-id="467a0-110">Movies rating selected for France.</span></span> <span data-ttu-id="467a0-111">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="467a0-111">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|
|<span data-ttu-id="467a0-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="467a0-112">tvRating</span></span>|[<span data-ttu-id="467a0-113">ratingFranceTelevisionType</span><span class="sxs-lookup"><span data-stu-id="467a0-113">ratingFranceTelevisionType</span></span>](../resources/intune_deviceconfig_ratingfrancetelevisiontype.md)|<span data-ttu-id="467a0-114">Clasificación de TV seleccionada para Francia.</span><span class="sxs-lookup"><span data-stu-id="467a0-114">TV rating selected for France.</span></span> <span data-ttu-id="467a0-115">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="467a0-115">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="467a0-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="467a0-116">Relationships</span></span>
<span data-ttu-id="467a0-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="467a0-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="467a0-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="467a0-118">JSON Representation</span></span>
<span data-ttu-id="467a0-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="467a0-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingFrance"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingFrance",
  "movieRating": "String",
  "tvRating": "String"
}
```



