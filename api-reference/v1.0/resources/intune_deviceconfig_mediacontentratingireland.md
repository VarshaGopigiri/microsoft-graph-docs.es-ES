# <a name="mediacontentratingireland-resource-type"></a><span data-ttu-id="714ef-101">Tipo de recurso mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="714ef-101">mediaContentRatingIreland resource type</span></span>

> <span data-ttu-id="714ef-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="714ef-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="714ef-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="714ef-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="714ef-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="714ef-104">Properties</span></span>
|<span data-ttu-id="714ef-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="714ef-105">Property</span></span>|<span data-ttu-id="714ef-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="714ef-106">Type</span></span>|<span data-ttu-id="714ef-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="714ef-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="714ef-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="714ef-108">movieRating</span></span>|[<span data-ttu-id="714ef-109">ratingIrelandMoviesType</span><span class="sxs-lookup"><span data-stu-id="714ef-109">ratingIrelandMoviesType</span></span>](../resources/intune_deviceconfig_ratingirelandmoviestype.md)|<span data-ttu-id="714ef-110">Clasificación de películas seleccionada para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="714ef-110">Movies rating selected for Ireland Possible values are: , , , , , , , .</span></span> <span data-ttu-id="714ef-111">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="714ef-111">The possible values are `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16`, `adults`, , , , or .</span></span>|
|<span data-ttu-id="714ef-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="714ef-112">tvRating</span></span>|[<span data-ttu-id="714ef-113">ratingIrelandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="714ef-113">ratingIrelandTelevisionType</span></span>](../resources/intune_deviceconfig_ratingirelandtelevisiontype.md)|<span data-ttu-id="714ef-114">Clasificación de TV seleccionada para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="714ef-114">TV rating selected for Ireland Possible values are: , , , , , , .</span></span> <span data-ttu-id="714ef-115">Los valores posibles son `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision` y `mature`.</span><span class="sxs-lookup"><span data-stu-id="714ef-115">The possible values are `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision`, `mature`, , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="714ef-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="714ef-116">Relationships</span></span>
<span data-ttu-id="714ef-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="714ef-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="714ef-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="714ef-118">JSON Representation</span></span>
<span data-ttu-id="714ef-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="714ef-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingIreland"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingIreland",
  "movieRating": "String",
  "tvRating": "String"
}
```



