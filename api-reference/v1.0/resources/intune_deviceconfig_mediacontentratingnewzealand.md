# <a name="mediacontentratingnewzealand-resource-type"></a><span data-ttu-id="4ebd0-101">Tipo de recurso mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="4ebd0-101">mediaContentRatingNewZealand resource type</span></span>

> <span data-ttu-id="4ebd0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4ebd0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4ebd0-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4ebd0-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="4ebd0-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ebd0-104">Properties</span></span>
|<span data-ttu-id="4ebd0-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ebd0-105">Property</span></span>|<span data-ttu-id="4ebd0-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ebd0-106">Type</span></span>|<span data-ttu-id="4ebd0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ebd0-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4ebd0-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="4ebd0-108">movieRating</span></span>|<span data-ttu-id="4ebd0-109">cadena</span><span class="sxs-lookup"><span data-stu-id="4ebd0-109">String</span></span>|<span data-ttu-id="4ebd0-110">Calificación de películas seleccionada para Nueva Zelanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted` y `agesAbove16Restricted`.</span><span class="sxs-lookup"><span data-stu-id="4ebd0-110">Movies rating selected for New Zealand Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span></span>|
|<span data-ttu-id="4ebd0-111">tvRating</span><span class="sxs-lookup"><span data-stu-id="4ebd0-111">tvRating</span></span>|<span data-ttu-id="4ebd0-112">cadena</span><span class="sxs-lookup"><span data-stu-id="4ebd0-112">String</span></span>|<span data-ttu-id="4ebd0-113">Calificación de TV seleccionada para Nueva Zelanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="4ebd0-113">TV rating selected for New Zealand Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4ebd0-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4ebd0-114">Relationships</span></span>
<span data-ttu-id="4ebd0-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4ebd0-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4ebd0-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4ebd0-116">JSON Representation</span></span>
<span data-ttu-id="4ebd0-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4ebd0-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mediaContentRatingNewZealand"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingNewZealand",
  "movieRating": "String",
  "tvRating": "String"
}
```



