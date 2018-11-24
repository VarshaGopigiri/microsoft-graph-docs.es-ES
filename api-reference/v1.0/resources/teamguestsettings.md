# <a name="teamguestsettings-resource-type"></a><span data-ttu-id="66331-101">tipo de recurso teamGuestSettings</span><span class="sxs-lookup"><span data-stu-id="66331-101">teamGuestSettings resource type</span></span>



<span data-ttu-id="66331-102">Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="66331-102">Settings to configure whether guests can create, update, or delete channels in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="66331-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66331-103">Properties</span></span>
| <span data-ttu-id="66331-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66331-104">Property</span></span>     | <span data-ttu-id="66331-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="66331-105">Type</span></span>   |<span data-ttu-id="66331-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="66331-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="66331-107">allowCreateUpdateChannels</span><span class="sxs-lookup"><span data-stu-id="66331-107">allowCreateUpdateChannels</span></span>|<span data-ttu-id="66331-108">Booleano</span><span class="sxs-lookup"><span data-stu-id="66331-108">Boolean</span></span>|<span data-ttu-id="66331-109">Si se establece en true, invitados puede agregar y actualizar los canales.</span><span class="sxs-lookup"><span data-stu-id="66331-109">If set to true, guests can add and update channels.</span></span>|
|<span data-ttu-id="66331-110">allowDeleteChannels</span><span class="sxs-lookup"><span data-stu-id="66331-110">allowDeleteChannels</span></span>|<span data-ttu-id="66331-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="66331-111">Boolean</span></span>|<span data-ttu-id="66331-112">Si se establece en true, invitados puede eliminar canales.</span><span class="sxs-lookup"><span data-stu-id="66331-112">If set to true, guests can delete channels.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="66331-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="66331-113">JSON representation</span></span>

<span data-ttu-id="66331-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="66331-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamGuestSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowDeleteChannels": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's guestSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
