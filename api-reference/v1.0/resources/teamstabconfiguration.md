# <a name="teamstabconfiguration-resource-type-open-type"></a><span data-ttu-id="dfa45-101">tipo de recurso teamsTabConfiguration (Open Type)</span><span class="sxs-lookup"><span data-stu-id="dfa45-101">teamsTabConfiguration resource type (Open Type)</span></span>



<span data-ttu-id="dfa45-102">La configuración que determinan el contenido de una [ficha](teamstab.md). Cuando una ficha de forma interactiva se configura, esta información se establece mediante la aplicación de proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="dfa45-102">The settings that determine the content of a [tab](teamstab.md). When a tab is interactively configured, this information is set by the tab provider application.</span></span>
<span data-ttu-id="dfa45-103">Además de las propiedades que aparece a continuación, algunas aplicaciones de proveedor de la ficha especifican propiedades personalizadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="dfa45-103">In addition to the properties below, some tab provider applications specify additional custom properties.</span></span>

## <a name="properties"></a><span data-ttu-id="dfa45-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfa45-104">Properties</span></span>

|<span data-ttu-id="dfa45-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dfa45-105">Property</span></span>|<span data-ttu-id="dfa45-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfa45-106">Type</span></span>|<span data-ttu-id="dfa45-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfa45-107">Description</span></span>|
|-|-|-|
|  <span data-ttu-id="dfa45-108">entityId</span><span class="sxs-lookup"><span data-stu-id="dfa45-108">entityId</span></span>   |   <span data-ttu-id="dfa45-109">string</span><span class="sxs-lookup"><span data-stu-id="dfa45-109">string</span></span> |  <span data-ttu-id="dfa45-110">Identificador de la entidad hospedada por el proveedor de la ficha.</span><span class="sxs-lookup"><span data-stu-id="dfa45-110">Identifier for the entity hosted by the tab provider.</span></span>     |
|  <span data-ttu-id="dfa45-111">contentUrl</span><span class="sxs-lookup"><span data-stu-id="dfa45-111">contentUrl</span></span> |   <span data-ttu-id="dfa45-112">string</span><span class="sxs-lookup"><span data-stu-id="dfa45-112">string</span></span> |  <span data-ttu-id="dfa45-113">Dirección URL utilizada para representar el contenido de la ficha en los equipos.</span><span class="sxs-lookup"><span data-stu-id="dfa45-113">Url used for rendering tab contents in Teams.</span></span> <span data-ttu-id="dfa45-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dfa45-114">Required.</span></span>    |
|  <span data-ttu-id="dfa45-115">removeUrl</span><span class="sxs-lookup"><span data-stu-id="dfa45-115">removeUrl</span></span>  |   <span data-ttu-id="dfa45-116">string</span><span class="sxs-lookup"><span data-stu-id="dfa45-116">string</span></span> |  <span data-ttu-id="dfa45-117">Dirección URL de los equipos cliente llamado cuando se quita una ficha mediante el cliente de los equipos.</span><span class="sxs-lookup"><span data-stu-id="dfa45-117">Url called by Teams client when a Tab is removed using the Teams Client.</span></span>     |
|  <span data-ttu-id="dfa45-118">websiteUrl</span><span class="sxs-lookup"><span data-stu-id="dfa45-118">websiteUrl</span></span> |   <span data-ttu-id="dfa45-119">string</span><span class="sxs-lookup"><span data-stu-id="dfa45-119">string</span></span> |  <span data-ttu-id="dfa45-120">Dirección URL para mostrar el contenido de la ficha fuera de los equipos.</span><span class="sxs-lookup"><span data-stu-id="dfa45-120">Url for showing tab contents outside of Teams.</span></span>     |

## <a name="json-representation"></a><span data-ttu-id="dfa45-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dfa45-121">JSON representation</span></span>

<span data-ttu-id="dfa45-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dfa45-122">The following is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsTabConfiguration"
}-->

```json
{
   "entityId": "string",
   "contentUrl": "string (HTTPS Url)",
   "websiteUrl": "string (HTTPS Url)",
   "removeUrl": "string (HTTPS Url)"  
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsTabConfiguration complex type (Open Type)",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
