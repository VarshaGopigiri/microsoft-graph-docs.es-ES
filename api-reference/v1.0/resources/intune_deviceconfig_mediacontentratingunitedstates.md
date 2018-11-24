# <a name="mediacontentratingunitedstates-resource-type"></a><span data-ttu-id="184c7-101">Tipo de recurso mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="184c7-101">mediaContentRatingUnitedStates resource type</span></span>

> <span data-ttu-id="184c7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="184c7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="184c7-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="184c7-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="184c7-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="184c7-104">Properties</span></span>
|<span data-ttu-id="184c7-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="184c7-105">Property</span></span>|<span data-ttu-id="184c7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="184c7-106">Type</span></span>|<span data-ttu-id="184c7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="184c7-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="184c7-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="184c7-108">movieRating</span></span>|[<span data-ttu-id="184c7-109">ratingUnitedStatesMoviesType</span><span class="sxs-lookup"><span data-stu-id="184c7-109">ratingUnitedStatesMoviesType</span></span>](../resources/intune_deviceconfig_ratingunitedstatesmoviestype.md)|<span data-ttu-id="184c7-110">Películas de clasificación seleccionado para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="184c7-110">Movies rating selected for United States.</span></span> <span data-ttu-id="184c7-111">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="184c7-111">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted`, `adults`.</span></span>|
|<span data-ttu-id="184c7-112">tvRating</span><span class="sxs-lookup"><span data-stu-id="184c7-112">tvRating</span></span>|[<span data-ttu-id="184c7-113">ratingUnitedStatesTelevisionType</span><span class="sxs-lookup"><span data-stu-id="184c7-113">ratingUnitedStatesTelevisionType</span></span>](../resources/intune_deviceconfig_ratingunitedstatestelevisiontype.md)|<span data-ttu-id="184c7-114">Clasificación de TV seleccionada para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="184c7-114">TV rating selected for United States.</span></span> <span data-ttu-id="184c7-115">Los valores posibles son: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="184c7-115">Possible values are: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="184c7-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="184c7-116">Relationships</span></span>
<span data-ttu-id="184c7-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="184c7-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="184c7-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="184c7-118">JSON Representation</span></span>
<span data-ttu-id="184c7-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="184c7-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedStates",
  "movieRating": "String",
  "tvRating": "String"
}
```



