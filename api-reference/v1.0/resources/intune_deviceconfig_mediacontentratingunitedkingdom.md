# <a name="mediacontentratingunitedkingdom-resource-type"></a><span data-ttu-id="306c7-101">Tipo de recurso mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="306c7-101">mediaContentRatingUnitedKingdom resource type</span></span>

> <span data-ttu-id="306c7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="306c7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="306c7-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="306c7-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="306c7-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="306c7-104">Properties</span></span>
|<span data-ttu-id="306c7-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="306c7-105">Property</span></span>|<span data-ttu-id="306c7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="306c7-106">Type</span></span>|<span data-ttu-id="306c7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="306c7-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="306c7-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="306c7-108">movieRating</span></span>|<span data-ttu-id="306c7-109">cadena</span><span class="sxs-lookup"><span data-stu-id="306c7-109">String</span></span>|<span data-ttu-id="306c7-110">Calificación de películas seleccionada para Reino Unido. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="306c7-110">Movies rating selected for United Kingdom Possible values are: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15`, `adults`.</span></span>|
|<span data-ttu-id="306c7-111">tvRating</span><span class="sxs-lookup"><span data-stu-id="306c7-111">tvRating</span></span>|<span data-ttu-id="306c7-112">cadena</span><span class="sxs-lookup"><span data-stu-id="306c7-112">String</span></span>|<span data-ttu-id="306c7-113">Calificación de TV seleccionada para Reino Unido. Los valores posibles son: `allAllowed`, `allBlocked` y `caution`.</span><span class="sxs-lookup"><span data-stu-id="306c7-113">TV rating selected for United Kingdom Possible values are: `allAllowed`, `allBlocked`, `caution`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="306c7-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="306c7-114">Relationships</span></span>
<span data-ttu-id="306c7-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="306c7-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="306c7-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="306c7-116">JSON Representation</span></span>
<span data-ttu-id="306c7-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="306c7-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedKingdom",
  "movieRating": "String",
  "tvRating": "String"
}
```



