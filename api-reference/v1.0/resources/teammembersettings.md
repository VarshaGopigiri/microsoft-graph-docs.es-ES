# <a name="teammembersettings-resource-type"></a><span data-ttu-id="ed9e5-101">tipo de recurso teamMemberSettings</span><span class="sxs-lookup"><span data-stu-id="ed9e5-101">teamMemberSettings resource type</span></span>



<span data-ttu-id="ed9e5-102">Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="ed9e5-102">Settings to configure whether members can perform certain actions, for example, create channels and add bots, in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ed9e5-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed9e5-103">Properties</span></span>
| <span data-ttu-id="ed9e5-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed9e5-104">Property</span></span>     | <span data-ttu-id="ed9e5-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed9e5-105">Type</span></span>   |<span data-ttu-id="ed9e5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed9e5-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ed9e5-107">allowCreateUpdateChannels</span><span class="sxs-lookup"><span data-stu-id="ed9e5-107">allowCreateUpdateChannels</span></span>|<span data-ttu-id="ed9e5-108">Booleano</span><span class="sxs-lookup"><span data-stu-id="ed9e5-108">Boolean</span></span>|<span data-ttu-id="ed9e5-109">Si se establece a miembros es true, puede agregar y actualizar los canales.</span><span class="sxs-lookup"><span data-stu-id="ed9e5-109">If set to true, members can add and update channels.</span></span>|
|<span data-ttu-id="ed9e5-110">allowDeleteChannels</span><span class="sxs-lookup"><span data-stu-id="ed9e5-110">allowDeleteChannels</span></span>|<span data-ttu-id="ed9e5-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="ed9e5-111">Boolean</span></span>|<span data-ttu-id="ed9e5-112">Si se establece en true, miembros puede eliminar canales.</span><span class="sxs-lookup"><span data-stu-id="ed9e5-112">If set to true, members can delete channels.</span></span>|
|<span data-ttu-id="ed9e5-113">allowAddRemoveApps</span><span class="sxs-lookup"><span data-stu-id="ed9e5-113">allowAddRemoveApps</span></span>|<span data-ttu-id="ed9e5-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="ed9e5-114">Boolean</span></span>|<span data-ttu-id="ed9e5-115">Si se establece a miembros es true, puede agregar y quitar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ed9e5-115">If set to true, members can add and remove apps.</span></span>|
|<span data-ttu-id="ed9e5-116">allowCreateUpdateRemoveTabs</span><span class="sxs-lookup"><span data-stu-id="ed9e5-116">allowCreateUpdateRemoveTabs</span></span>|<span data-ttu-id="ed9e5-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="ed9e5-117">Boolean</span></span>|<span data-ttu-id="ed9e5-118">Si se establece en true, miembros puede agregar, actualizar y quitar las fichas.</span><span class="sxs-lookup"><span data-stu-id="ed9e5-118">If set to true, members can add, update, and remove tabs.</span></span> |
|<span data-ttu-id="ed9e5-119">allowCreateUpdateRemoveConnectors</span><span class="sxs-lookup"><span data-stu-id="ed9e5-119">allowCreateUpdateRemoveConnectors</span></span>|<span data-ttu-id="ed9e5-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="ed9e5-120">Boolean</span></span>|<span data-ttu-id="ed9e5-121">Si se establece en true, miembros puede agregar, actualizar y quitar conectores.</span><span class="sxs-lookup"><span data-stu-id="ed9e5-121">If set to true, members can add, update, and remove connectors.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ed9e5-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ed9e5-122">JSON representation</span></span>

<span data-ttu-id="ed9e5-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ed9e5-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMemberSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowDeleteChannels": true,
  "allowAddRemoveApps": true,
  "allowCreateUpdateRemoveTabs": true,
  "allowCreateUpdateRemoveConnectors": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's memberSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
