# <a name="mediacontentratingcanada-resource-type"></a><span data-ttu-id="7d9f3-101">Tipo de recurso mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="7d9f3-101">mediaContentRatingCanada resource type</span></span>

> <span data-ttu-id="7d9f3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7d9f3-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7d9f3-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="7d9f3-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d9f3-104">Properties</span></span>
|<span data-ttu-id="7d9f3-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d9f3-105">Property</span></span>|<span data-ttu-id="7d9f3-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d9f3-106">Type</span></span>|<span data-ttu-id="7d9f3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d9f3-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7d9f3-108">movieRating</span><span class="sxs-lookup"><span data-stu-id="7d9f3-108">movieRating</span></span>|<span data-ttu-id="7d9f3-109">cadena</span><span class="sxs-lookup"><span data-stu-id="7d9f3-109">String</span></span>|<span data-ttu-id="7d9f3-110">Calificación de películas seleccionada para Canadá. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18` y `restricted`.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-110">Movies rating selected for Canada Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, `restricted`.</span></span>|
|<span data-ttu-id="7d9f3-111">tvRating</span><span class="sxs-lookup"><span data-stu-id="7d9f3-111">tvRating</span></span>|<span data-ttu-id="7d9f3-112">cadena</span><span class="sxs-lookup"><span data-stu-id="7d9f3-112">String</span></span>|<span data-ttu-id="7d9f3-113">Calificación de TV seleccionada para Canadá. Los valores posibles son: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-113">TV rating selected for Canada Possible values are: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7d9f3-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7d9f3-114">Relationships</span></span>
<span data-ttu-id="7d9f3-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7d9f3-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7d9f3-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7d9f3-116">JSON Representation</span></span>
<span data-ttu-id="7d9f3-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



