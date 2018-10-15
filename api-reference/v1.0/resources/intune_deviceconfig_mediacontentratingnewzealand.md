# <a name="mediacontentratingnewzealand-resource-type"></a><span data-ttu-id="2506f-101">Tipo de recurso mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="2506f-101">mediaContentRatingNewZealand resource type</span></span>

> <span data-ttu-id="2506f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2506f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2506f-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2506f-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="2506f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2506f-104">Properties</span></span>
|<span data-ttu-id="2506f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2506f-105">Property</span></span>|<span data-ttu-id="2506f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2506f-106">Type</span></span>|<span data-ttu-id="2506f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2506f-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2506f-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="2506f-108">movieRating</span></span>|[<span data-ttu-id="2506f-109">ratingNewZealandMoviesType</span><span class="sxs-lookup"><span data-stu-id="2506f-109">ratingNewZealandMoviesType</span></span>](../resources/intune_deviceconfig_ratingnewzealandmoviestype.md)|<span data-ttu-id="2506f-p101">Clasificación de películas seleccionada para Nueva Zelanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span><span class="sxs-lookup"><span data-stu-id="2506f-p101">Movies rating selected for New Zealand Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span></span>|
|<span data-ttu-id="2506f-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="2506f-112">tvRating</span></span>|[<span data-ttu-id="2506f-113">ratingNewZealandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="2506f-113">ratingNewZealandTelevisionType</span></span>](../resources/intune_deviceconfig_ratingnewzealandtelevisiontype.md)|<span data-ttu-id="2506f-p102">Clasificación de TV seleccionada para Nueva Zelanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span><span class="sxs-lookup"><span data-stu-id="2506f-p102">TV rating selected for New Zealand Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2506f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2506f-116">Relationships</span></span>
<span data-ttu-id="2506f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2506f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2506f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2506f-118">JSON Representation</span></span>
<span data-ttu-id="2506f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2506f-119">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingNewZealand"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingNewZealand",
  "movieRating": "String",
  "tvRating": "String"
}
```








