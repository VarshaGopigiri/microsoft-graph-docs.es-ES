# <a name="mediacontentratingcanada-resource-type"></a><span data-ttu-id="d6070-101">Tipo de recurso mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="d6070-101">mediaContentRatingCanada resource type</span></span>

> <span data-ttu-id="d6070-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d6070-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d6070-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d6070-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="d6070-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6070-104">Properties</span></span>
|<span data-ttu-id="d6070-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6070-105">Property</span></span>|<span data-ttu-id="d6070-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6070-106">Type</span></span>|<span data-ttu-id="d6070-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6070-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d6070-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="d6070-108">movieRating</span></span>|[<span data-ttu-id="d6070-109">ratingCanadaMoviesType</span><span class="sxs-lookup"><span data-stu-id="d6070-109">ratingCanadaMoviesType</span></span>](../resources/intune_deviceconfig_ratingcanadamoviestype.md)|<span data-ttu-id="d6070-110">Clasificación de películas seleccionada para Canadá.</span><span class="sxs-lookup"><span data-stu-id="d6070-110">Movies rating selected for Canada Possible values are: , , , , , , .</span></span> <span data-ttu-id="d6070-111">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18` y `restricted`.</span><span class="sxs-lookup"><span data-stu-id="d6070-111">The possible values are `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, `restricted`, , , , , or .</span></span>|
|<span data-ttu-id="d6070-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="d6070-112">tvRating</span></span>|[<span data-ttu-id="d6070-113">ratingCanadaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="d6070-113">ratingCanadaTelevisionType</span></span>](../resources/intune_deviceconfig_ratingcanadatelevisiontype.md)|<span data-ttu-id="d6070-114">Clasificación de TV seleccionada para Canadá.</span><span class="sxs-lookup"><span data-stu-id="d6070-114">TV rating selected for Canada Possible values are: , , , , , , , .</span></span> <span data-ttu-id="d6070-115">Los valores posibles son: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="d6070-115">The possible values are `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="d6070-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d6070-116">Relationships</span></span>
<span data-ttu-id="d6070-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d6070-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d6070-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d6070-118">JSON Representation</span></span>
<span data-ttu-id="d6070-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d6070-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingCanada"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingCanada",
  "movieRating": "String",
  "tvRating": "String"
}
```



