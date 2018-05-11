# <a name="messageruleactions-resource-type"></a><span data-ttu-id="f421e-101">Tipo de recurso messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="f421e-101">messageRuleActions resource type</span></span>


<span data-ttu-id="f421e-102">Representa el conjunto de acciones que están disponibles para una regla.</span><span class="sxs-lookup"><span data-stu-id="f421e-102">Represents the set of actions that are available to a rule.</span></span>

## <a name="properties"></a><span data-ttu-id="f421e-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f421e-103">Properties</span></span>
| <span data-ttu-id="f421e-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f421e-104">Property</span></span>     | <span data-ttu-id="f421e-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="f421e-105">Type</span></span>   |<span data-ttu-id="f421e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f421e-106">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f421e-107">assignCategories</span><span class="sxs-lookup"><span data-stu-id="f421e-107">assignCategories</span></span> | <span data-ttu-id="f421e-108">Colección String</span><span class="sxs-lookup"><span data-stu-id="f421e-108">String collection</span></span> | <span data-ttu-id="f421e-109">Lista de categorías que se asignarán a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f421e-109">A list of categories to be assigned to a message.</span></span> |
| <span data-ttu-id="f421e-110">copyToFolder</span><span class="sxs-lookup"><span data-stu-id="f421e-110">copyToFolder</span></span> | <span data-ttu-id="f421e-111">String</span><span class="sxs-lookup"><span data-stu-id="f421e-111">String</span></span> | <span data-ttu-id="f421e-112">Identificador de la carpeta donde se va a copiar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f421e-112">The ID of a folder that a message is to be copied to.</span></span> |
| <span data-ttu-id="f421e-113">delete</span><span class="sxs-lookup"><span data-stu-id="f421e-113">delete</span></span> | <span data-ttu-id="f421e-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="f421e-114">Boolean</span></span> | <span data-ttu-id="f421e-115">Indica si un mensaje se debe mover a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="f421e-115">Indicates whether a message should be moved to the Deleted Items folder.</span></span> |
| <span data-ttu-id="f421e-116">forwardAsAttachmentTo</span><span class="sxs-lookup"><span data-stu-id="f421e-116">forwardAsAttachmentTo</span></span> | <span data-ttu-id="f421e-117">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="f421e-117">[recipient](recipient.md) collection</span></span> | <span data-ttu-id="f421e-118">Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f421e-118">The email addresses of the recipients to which a message should be forwarded as an attachment.</span></span> |
| <span data-ttu-id="f421e-119">forwardTo</span><span class="sxs-lookup"><span data-stu-id="f421e-119">forwardTo</span></span> | <span data-ttu-id="f421e-120">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="f421e-120">[recipient](recipient.md) collection</span></span> | <span data-ttu-id="f421e-121">Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f421e-121">The email addresses of the recipients to which a message should be forwarded.</span></span> |
| <span data-ttu-id="f421e-122">markAsRead</span><span class="sxs-lookup"><span data-stu-id="f421e-122">markAsRead</span></span> | <span data-ttu-id="f421e-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="f421e-123">Boolean</span></span> | <span data-ttu-id="f421e-124">Indica si un mensaje debe marcarse como leído.</span><span class="sxs-lookup"><span data-stu-id="f421e-124">Indicates whether a message should be marked as read.</span></span> |
| <span data-ttu-id="f421e-125">markImportance</span><span class="sxs-lookup"><span data-stu-id="f421e-125">markImportance</span></span> | <span data-ttu-id="f421e-126">String</span><span class="sxs-lookup"><span data-stu-id="f421e-126">String</span></span> | <span data-ttu-id="f421e-127">Establece la importancia del mensaje, que puede ser: `low`, `normal` o `high`.</span><span class="sxs-lookup"><span data-stu-id="f421e-127">Sets the importance of the message, which can be: `low`, `normal`, `high`.</span></span> |
| <span data-ttu-id="f421e-128">moveToFolder</span><span class="sxs-lookup"><span data-stu-id="f421e-128">moveToFolder</span></span> |  <span data-ttu-id="f421e-129">String</span><span class="sxs-lookup"><span data-stu-id="f421e-129">String</span></span>| <span data-ttu-id="f421e-130">Identificador de la carpeta a la que se moverá un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f421e-130">The ID of the folder that a message will be moved to.</span></span> |
| <span data-ttu-id="f421e-131">permanentDelete</span><span class="sxs-lookup"><span data-stu-id="f421e-131">permanentDelete</span></span> | <span data-ttu-id="f421e-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="f421e-132">Boolean</span></span> | <span data-ttu-id="f421e-133">Indica si un mensaje se debe eliminar permanentemente sin guardarse en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="f421e-133">Indicates whether a message should be permanently deleted and not saved to the Deleted Items folder.</span></span> |
| <span data-ttu-id="f421e-134">redirectTo</span><span class="sxs-lookup"><span data-stu-id="f421e-134">redirectTo</span></span> | [<span data-ttu-id="f421e-135">recipient</span><span class="sxs-lookup"><span data-stu-id="f421e-135">recipient</span></span>](recipient.md) | <span data-ttu-id="f421e-136">Dirección de correo electrónico a la que se debe redirigir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f421e-136">The email address to which a message should be redirected.</span></span> |
| <span data-ttu-id="f421e-137">stopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="f421e-137">stopProcessingRules</span></span> | <span data-ttu-id="f421e-138">Boolean</span><span class="sxs-lookup"><span data-stu-id="f421e-138">Boolean</span></span> | <span data-ttu-id="f421e-139">Indica si se deben evaluar las reglas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f421e-139">Indicates whether subsequent rules should be evaluated.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="f421e-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f421e-140">JSON representation</span></span>
<span data-ttu-id="f421e-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f421e-141">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.messageRuleActions"
}-->

```json
{
  "assignCategories": ["String"],
  "copyToFolder": "String",
  "delete": "Boolean",
  "forwardAsAttachmentTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "forwardTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "markAsRead": "Boolean",
  "markImportance": "String",
  "moveToFolder": "String",
  "permanentDelete": "Boolean",
  "redirectTo": {"@odata.type": "microsoft.graph.recipient"},
  "stopProcessingRules": "Boolean"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRuleActions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->