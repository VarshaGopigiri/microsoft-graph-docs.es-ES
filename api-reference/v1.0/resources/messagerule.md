# <a name="messagerule-resource-type"></a><span data-ttu-id="6fc2e-101">Tipo de recurso messageRule</span><span class="sxs-lookup"><span data-stu-id="6fc2e-101">messageRule resource type</span></span>


<span data-ttu-id="6fc2e-102">Regla que se aplica a los mensajes de la Bandeja de entrada de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-102">A rule that applies to messages in the Inbox of a user.</span></span>

<span data-ttu-id="6fc2e-103">En Outlook, puede establecer reglas de los mensajes entrantes en la Bandeja de entrada para llevar a cabo acciones específicas en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-103">In Outlook, you can set up rules for incoming messages in the Inbox to carry out specific actions upon certain conditions.</span></span> 

<span data-ttu-id="6fc2e-104">Mediante programación, tiene acceso a las reglas a través de la propiedad de navegación **messageRules** de la [carpeta](mailfolder.md) Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-104">Programmatically, you can access rules through the **messageRules** navigation property of the Inbox [folder](mailfolder.md).</span></span> <span data-ttu-id="6fc2e-105">Cada regla se representa mediante este recurso **messageRule**, las acciones de regla disponibles se representan mediante el tipo complejo [messageRuleActions](messageruleactions.md) y las condiciones de regla disponibles se representan mediante el tipo complejo [messageRulePredicates](messagerulepredicates.md).</span><span class="sxs-lookup"><span data-stu-id="6fc2e-105">Each rule is represented by this **messageRule** resource, available rule actions are represented by the [messageRuleActions](messageruleactions.md) complex type, and available rule conditions and exceptions are represented by the [messageRulePredicates](messagerulepredicates.md) complex type.</span></span>


## <a name="properties"></a><span data-ttu-id="6fc2e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fc2e-106">Properties</span></span>
| <span data-ttu-id="6fc2e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6fc2e-107">Property</span></span>     | <span data-ttu-id="6fc2e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fc2e-108">Type</span></span>   |<span data-ttu-id="6fc2e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fc2e-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6fc2e-110">actions</span><span class="sxs-lookup"><span data-stu-id="6fc2e-110">actions</span></span> | [<span data-ttu-id="6fc2e-111">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="6fc2e-111">messageRuleActions</span></span>](messageruleactions.md) | <span data-ttu-id="6fc2e-112">Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-112">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="6fc2e-113">conditions</span><span class="sxs-lookup"><span data-stu-id="6fc2e-113">conditions</span></span> | [<span data-ttu-id="6fc2e-114">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="6fc2e-114">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="6fc2e-115">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-115">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="6fc2e-116">displayName</span><span class="sxs-lookup"><span data-stu-id="6fc2e-116">displayName</span></span> | <span data-ttu-id="6fc2e-117">String</span><span class="sxs-lookup"><span data-stu-id="6fc2e-117">String</span></span> | <span data-ttu-id="6fc2e-118">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-118">The display name of the rule.</span></span> |
| <span data-ttu-id="6fc2e-119">exceptions</span><span class="sxs-lookup"><span data-stu-id="6fc2e-119">exceptions</span></span> | [<span data-ttu-id="6fc2e-120">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="6fc2e-120">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="6fc2e-121">Condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-121">Exception conditions for the rule.</span></span> |
| <span data-ttu-id="6fc2e-122">hasError</span><span class="sxs-lookup"><span data-stu-id="6fc2e-122">hasError</span></span> | <span data-ttu-id="6fc2e-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="6fc2e-123">Boolean</span></span> | <span data-ttu-id="6fc2e-124">Indica si la regla es una condición de error.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-124">Indicates whether the rule is in an error condition.</span></span> <span data-ttu-id="6fc2e-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-125">Read-only.</span></span> |
| <span data-ttu-id="6fc2e-126">id</span><span class="sxs-lookup"><span data-stu-id="6fc2e-126">id</span></span> |<span data-ttu-id="6fc2e-127">String</span><span class="sxs-lookup"><span data-stu-id="6fc2e-127">String</span></span>|<span data-ttu-id="6fc2e-128">Identificador único de la regla.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-128">The unique identifier of the rule.</span></span> <span data-ttu-id="6fc2e-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-129">Read-only.</span></span>|
| <span data-ttu-id="6fc2e-130">isEnabled</span><span class="sxs-lookup"><span data-stu-id="6fc2e-130">isEnabled</span></span> | <span data-ttu-id="6fc2e-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="6fc2e-131">Boolean</span></span> | <span data-ttu-id="6fc2e-132">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-132">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="6fc2e-133">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="6fc2e-133">isReadOnly</span></span> | <span data-ttu-id="6fc2e-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="6fc2e-134">Boolean</span></span> | <span data-ttu-id="6fc2e-135">Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-135">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="6fc2e-136">sequence</span><span class="sxs-lookup"><span data-stu-id="6fc2e-136">sequence</span></span> | <span data-ttu-id="6fc2e-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6fc2e-137">Int32</span></span> | <span data-ttu-id="6fc2e-138">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-138">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="6fc2e-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6fc2e-139">JSON representation</span></span>
<span data-ttu-id="6fc2e-140">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
   "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.messageRule"
}-->

```json
{
  "actions": {"@odata.type": "microsoft.graph.messageRuleActions"},
  "conditions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "displayName": "String",
  "exceptions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "hasError": "Boolean",
  "id": "String",
  "isEnabled": "Boolean",
  "isReadOnly": "Boolean",
  "sequence": "Int32"
}

```

## <a name="methods"></a><span data-ttu-id="6fc2e-141">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fc2e-141">Methods</span></span>
| <span data-ttu-id="6fc2e-142">Método</span><span class="sxs-lookup"><span data-stu-id="6fc2e-142">Method</span></span>           | <span data-ttu-id="6fc2e-143">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fc2e-143">Return Type</span></span>    |<span data-ttu-id="6fc2e-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fc2e-144">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="6fc2e-145">Enumerar reglas</span><span class="sxs-lookup"><span data-stu-id="6fc2e-145">List rules</span></span>](../api/mailfolder_list_messagerules.md) | <span data-ttu-id="6fc2e-146">Colección [messageRule](messagerule.md)</span><span class="sxs-lookup"><span data-stu-id="6fc2e-146">[messageRule](messagerule.md) collection</span></span> |<span data-ttu-id="6fc2e-147">Obtener todos los objetos **messageRule** definidos para la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-147">Get all the **messageRule** objects defined for the user's Inbox.</span></span>|
|[<span data-ttu-id="6fc2e-148">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="6fc2e-148">Get rule</span></span>](../api/messagerule_get.md) | [<span data-ttu-id="6fc2e-149">messageRule</span><span class="sxs-lookup"><span data-stu-id="6fc2e-149">messageRule</span></span>](messagerule.md) |<span data-ttu-id="6fc2e-150">Leer las propiedades y relaciones de un objeto **messageRule**.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-150">Read the properties and relationships of a **messageRule** object.</span></span>|
|[<span data-ttu-id="6fc2e-151">Crear</span><span class="sxs-lookup"><span data-stu-id="6fc2e-151">Create</span></span>](../api/mailfolder_post_messagerules.md) | [<span data-ttu-id="6fc2e-152">messageRule</span><span class="sxs-lookup"><span data-stu-id="6fc2e-152">messageRule</span></span>](messagerule.md) |<span data-ttu-id="6fc2e-153">Crear un objeto **messageRule** especificando un conjunto de condiciones y acciones.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-153">Create a **messageRule** object by specifying a set of conditions and actions.</span></span>|
|[<span data-ttu-id="6fc2e-154">Actualizar</span><span class="sxs-lookup"><span data-stu-id="6fc2e-154">Update</span></span>](../api/messagerule_update.md) | [<span data-ttu-id="6fc2e-155">messageRule</span><span class="sxs-lookup"><span data-stu-id="6fc2e-155">messageRule</span></span>](messagerule.md) |<span data-ttu-id="6fc2e-156">Cambie las propiedades modificables en un objeto **messageRule** y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-156">Change writable properties on a **messageRule** object and save the changes.</span></span> |
|[<span data-ttu-id="6fc2e-157">Eliminar</span><span class="sxs-lookup"><span data-stu-id="6fc2e-157">Delete</span></span>](../api/messagerule_delete.md) | <span data-ttu-id="6fc2e-158">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6fc2e-158">None</span></span> |<span data-ttu-id="6fc2e-159">Eliminar el objeto **messageRule** especificado.</span><span class="sxs-lookup"><span data-stu-id="6fc2e-159">Delete the specified **messageRule** object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->