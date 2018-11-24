# <a name="teammessagingsettings-resource-type"></a><span data-ttu-id="3a022-101">tipo de recurso teamMessagingSettings</span><span class="sxs-lookup"><span data-stu-id="3a022-101">teamMessagingSettings resource type</span></span>



<span data-ttu-id="3a022-102">La configuración de mensajería y menciones en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="3a022-102">Settings to configure messaging and mentions in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3a022-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a022-103">Properties</span></span>
| <span data-ttu-id="3a022-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a022-104">Property</span></span>     | <span data-ttu-id="3a022-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a022-105">Type</span></span>   |<span data-ttu-id="3a022-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a022-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3a022-107">allowUserEditMessages</span><span class="sxs-lookup"><span data-stu-id="3a022-107">allowUserEditMessages</span></span>|<span data-ttu-id="3a022-108">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a022-108">Boolean</span></span>|<span data-ttu-id="3a022-109">Si se establece en true, los usuarios puede editar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="3a022-109">If set to true, users can edit their messages.</span></span>|
|<span data-ttu-id="3a022-110">allowUserDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="3a022-110">allowUserDeleteMessages</span></span>|<span data-ttu-id="3a022-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a022-111">Boolean</span></span>|<span data-ttu-id="3a022-112">Si se establece en true, los usuarios puede eliminar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="3a022-112">If set to true, users can delete their messages.</span></span>|
|<span data-ttu-id="3a022-113">allowOwnerDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="3a022-113">allowOwnerDeleteMessages</span></span>|<span data-ttu-id="3a022-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a022-114">Boolean</span></span>|<span data-ttu-id="3a022-115">Si se establece en true, propietarios puede eliminar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="3a022-115">If set to true, owners can delete any message.</span></span>|
|<span data-ttu-id="3a022-116">allowTeamMentions</span><span class="sxs-lookup"><span data-stu-id="3a022-116">allowTeamMentions</span></span>|<span data-ttu-id="3a022-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a022-117">Boolean</span></span>|<span data-ttu-id="3a022-118">Si establece en true, se permiten menciones de @team.</span><span class="sxs-lookup"><span data-stu-id="3a022-118">If set to true, @team mentions are allowed.</span></span>|
|<span data-ttu-id="3a022-119">allowChannelMentions</span><span class="sxs-lookup"><span data-stu-id="3a022-119">allowChannelMentions</span></span>|<span data-ttu-id="3a022-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a022-120">Boolean</span></span>|<span data-ttu-id="3a022-121">Si establece en true, se permiten menciones de @channel.</span><span class="sxs-lookup"><span data-stu-id="3a022-121">If set to true, @channel mentions are allowed.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3a022-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a022-122">JSON representation</span></span>

<span data-ttu-id="3a022-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3a022-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMessagingSettings"
}-->

```json
{
  "allowUserEditMessages": true,
  "allowUserDeleteMessages": true,
  "allowOwnerDeleteMessages": true,
  "allowTeamMentions": true,
  "allowChannelMentions": true    
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's messagingSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
