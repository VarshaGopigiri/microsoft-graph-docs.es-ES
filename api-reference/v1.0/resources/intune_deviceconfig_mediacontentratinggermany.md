# <a name="mediacontentratinggermany-resource-type"></a><span data-ttu-id="f6a73-101">Tipo de recurso mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="f6a73-101">mediaContentRatingGermany resource type</span></span>

> <span data-ttu-id="f6a73-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6a73-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6a73-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f6a73-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="f6a73-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6a73-104">Properties</span></span>
|<span data-ttu-id="f6a73-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6a73-105">Property</span></span>|<span data-ttu-id="f6a73-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6a73-106">Type</span></span>|<span data-ttu-id="f6a73-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6a73-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6a73-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="f6a73-108">movieRating</span></span>|<span data-ttu-id="f6a73-109">cadena</span><span class="sxs-lookup"><span data-stu-id="f6a73-109">String</span></span>|<span data-ttu-id="f6a73-110">Calificación de películas seleccionada para Alemania. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="f6a73-110">Movies rating selected for Germany Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="f6a73-111">tvRating</span><span class="sxs-lookup"><span data-stu-id="f6a73-111">tvRating</span></span>|<span data-ttu-id="f6a73-112">cadena</span><span class="sxs-lookup"><span data-stu-id="f6a73-112">String</span></span>|<span data-ttu-id="f6a73-113">Calificación de TV seleccionada para Alemania. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="f6a73-113">TV rating selected for Germany Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f6a73-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f6a73-114">Relationships</span></span>
<span data-ttu-id="f6a73-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f6a73-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f6a73-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6a73-116">JSON Representation</span></span>
<span data-ttu-id="f6a73-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f6a73-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mediaContentRatingGermany"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingGermany",
  "movieRating": "String",
  "tvRating": "String"
}
```



