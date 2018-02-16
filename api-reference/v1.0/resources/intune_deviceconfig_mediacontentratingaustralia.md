# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="ee483-101">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="ee483-101">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="ee483-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ee483-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ee483-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ee483-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="ee483-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee483-104">Properties</span></span>
|<span data-ttu-id="ee483-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee483-105">Property</span></span>|<span data-ttu-id="ee483-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee483-106">Type</span></span>|<span data-ttu-id="ee483-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee483-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ee483-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="ee483-108">movieRating</span></span>|<span data-ttu-id="ee483-109">cadena</span><span class="sxs-lookup"><span data-stu-id="ee483-109">String</span></span>|<span data-ttu-id="ee483-110">Calificación de películas seleccionada para Australia. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="ee483-110">Movies rating selected for Australia Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="ee483-111">tvRating</span><span class="sxs-lookup"><span data-stu-id="ee483-111">tvRating</span></span>|<span data-ttu-id="ee483-112">cadena</span><span class="sxs-lookup"><span data-stu-id="ee483-112">String</span></span>|<span data-ttu-id="ee483-113">Calificación de TV seleccionada para Australia. Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="ee483-113">TV rating selected for Australia Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ee483-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ee483-114">Relationships</span></span>
<span data-ttu-id="ee483-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ee483-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ee483-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee483-116">JSON Representation</span></span>
<span data-ttu-id="ee483-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ee483-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mediaContentRatingAustralia"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingAustralia",
  "movieRating": "String",
  "tvRating": "String"
}
```



