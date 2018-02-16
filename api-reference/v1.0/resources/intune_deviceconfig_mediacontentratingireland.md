# <a name="mediacontentratingireland-resource-type"></a><span data-ttu-id="94aae-101">Tipo de recurso mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="94aae-101">mediaContentRatingIreland resource type</span></span>

> <span data-ttu-id="94aae-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="94aae-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="94aae-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="94aae-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="94aae-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94aae-104">Properties</span></span>
|<span data-ttu-id="94aae-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="94aae-105">Property</span></span>|<span data-ttu-id="94aae-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="94aae-106">Type</span></span>|<span data-ttu-id="94aae-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="94aae-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="94aae-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="94aae-108">movieRating</span></span>|<span data-ttu-id="94aae-109">cadena</span><span class="sxs-lookup"><span data-stu-id="94aae-109">String</span></span>|<span data-ttu-id="94aae-110">Calificación de películas seleccionada para Irlanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="94aae-110">Movies rating selected for Ireland Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="94aae-111">tvRating</span><span class="sxs-lookup"><span data-stu-id="94aae-111">tvRating</span></span>|<span data-ttu-id="94aae-112">cadena</span><span class="sxs-lookup"><span data-stu-id="94aae-112">String</span></span>|<span data-ttu-id="94aae-113">Calificación de TV seleccionada para Irlanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision` y `mature`.</span><span class="sxs-lookup"><span data-stu-id="94aae-113">TV rating selected for Ireland Possible values are: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision`, `mature`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="94aae-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="94aae-114">Relationships</span></span>
<span data-ttu-id="94aae-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="94aae-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="94aae-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="94aae-116">JSON Representation</span></span>
<span data-ttu-id="94aae-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="94aae-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



