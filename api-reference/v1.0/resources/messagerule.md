# <a name="messagerule-resource-type"></a><span data-ttu-id="ccdf8-101">Tipo de recurso messageRule</span><span class="sxs-lookup"><span data-stu-id="ccdf8-101">messageRule resource type</span></span>


<span data-ttu-id="ccdf8-102">Regla que se aplica a los mensajes de la Bandeja de entrada de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-102">A rule that applies to messages in the Inbox of a user.</span></span>

<span data-ttu-id="ccdf8-103">En Outlook, puede establecer reglas de los mensajes entrantes en la Bandeja de entrada para llevar a cabo acciones específicas en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-103">In Outlook, you can set up rules for incoming messages in the Inbox to carry out specific actions upon certain conditions.</span></span> 

<span data-ttu-id="ccdf8-104">Mediante programación, tiene acceso a las reglas a través de la propiedad de navegación **messageRules** de la [carpeta](mailfolder.md) Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-104">Programmatically, you can access rules through the **messageRules** navigation property of the Inbox [folder](mailfolder.md).</span></span> <span data-ttu-id="ccdf8-105">Cada regla se representa mediante este recurso **messageRule**, las acciones de regla disponibles se representan mediante el tipo complejo [messageRuleActions](messageruleactions.md) y las condiciones de regla disponibles se representan mediante el tipo complejo [messageRulePredicates](messagerulepredicates.md).</span><span class="sxs-lookup"><span data-stu-id="ccdf8-105">Each rule is represented by this **messageRule** resource, available rule actions are represented by the [messageRuleActions](messageruleactions.md) complex type, and available rule conditions and exceptions are represented by the [messageRulePredicates](messagerulepredicates.md) complex type.</span></span>


## <a name="properties"></a><span data-ttu-id="ccdf8-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ccdf8-106">Properties</span></span>
| <span data-ttu-id="ccdf8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ccdf8-107">Property</span></span>     | <span data-ttu-id="ccdf8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccdf8-108">Type</span></span>   |<span data-ttu-id="ccdf8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccdf8-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ccdf8-110">actions</span><span class="sxs-lookup"><span data-stu-id="ccdf8-110">Actions</span></span> | [<span data-ttu-id="ccdf8-111">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="ccdf8-111">messageRuleActions</span></span>](messageruleactions.md) | <span data-ttu-id="ccdf8-112">Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-112">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="ccdf8-113">conditions</span><span class="sxs-lookup"><span data-stu-id="ccdf8-113">Conditions</span></span> | [<span data-ttu-id="ccdf8-114">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="ccdf8-114">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="ccdf8-115">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-115">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="ccdf8-116">displayName</span><span class="sxs-lookup"><span data-stu-id="ccdf8-116">displayName</span></span> | <span data-ttu-id="ccdf8-117">String</span><span class="sxs-lookup"><span data-stu-id="ccdf8-117">String</span></span> | <span data-ttu-id="ccdf8-118">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-118">The name of the new formatting rule.</span></span> |
| <span data-ttu-id="ccdf8-119">exceptions</span><span class="sxs-lookup"><span data-stu-id="ccdf8-119">exceptions</span></span> | [<span data-ttu-id="ccdf8-120">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="ccdf8-120">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="ccdf8-121">Condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-121">Exception conditions for the rule.</span></span> |
| <span data-ttu-id="ccdf8-122">hasError</span><span class="sxs-lookup"><span data-stu-id="ccdf8-122">hasError</span></span> | <span data-ttu-id="ccdf8-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="ccdf8-123">Boolean</span></span> | <span data-ttu-id="ccdf8-124">Indica si la regla es una condición de error.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-124">Indicates whether the rule is in an error condition.</span></span> <span data-ttu-id="ccdf8-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-125">Read-only.</span></span> |
| <span data-ttu-id="ccdf8-126">id</span><span class="sxs-lookup"><span data-stu-id="ccdf8-126">id</span></span> |<span data-ttu-id="ccdf8-127">String</span><span class="sxs-lookup"><span data-stu-id="ccdf8-127">String</span></span>|<span data-ttu-id="ccdf8-128">Identificador único de la regla.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-128">The unique identifier of the rule.</span></span> <span data-ttu-id="ccdf8-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-129">Read-only.</span></span>|
| <span data-ttu-id="ccdf8-130">isEnabled</span><span class="sxs-lookup"><span data-stu-id="ccdf8-130">isEnabled</span></span> | <span data-ttu-id="ccdf8-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="ccdf8-131">Boolean</span></span> | <span data-ttu-id="ccdf8-132">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-132">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="ccdf8-133">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="ccdf8-133">isReadOnly</span></span> | <span data-ttu-id="ccdf8-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="ccdf8-134">Boolean</span></span> | <span data-ttu-id="ccdf8-135">Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-135">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="ccdf8-136">sequence</span><span class="sxs-lookup"><span data-stu-id="ccdf8-136">Sequence</span></span> | <span data-ttu-id="ccdf8-137">Int32</span><span class="sxs-lookup"><span data-stu-id="ccdf8-137">Int32</span></span> | <span data-ttu-id="ccdf8-138">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-138">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="ccdf8-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ccdf8-139">JSON representation</span></span>
<span data-ttu-id="ccdf8-140">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
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

## <a name="methods"></a><span data-ttu-id="ccdf8-141">Métodos</span><span class="sxs-lookup"><span data-stu-id="ccdf8-141">Methods</span></span>
| <span data-ttu-id="ccdf8-142">Método</span><span class="sxs-lookup"><span data-stu-id="ccdf8-142">Method</span></span>           | <span data-ttu-id="ccdf8-143">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccdf8-143">Return Type</span></span>    |<span data-ttu-id="ccdf8-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccdf8-144">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ccdf8-145">Enumerar reglas</span><span class="sxs-lookup"><span data-stu-id="ccdf8-145">List rules</span></span>](../api/mailfolder_list_messagerules.md) | <span data-ttu-id="ccdf8-146">Colección [messageRule](messagerule.md)</span><span class="sxs-lookup"><span data-stu-id="ccdf8-146">[messageRule](messagerule.md) collection</span></span> |<span data-ttu-id="ccdf8-147">Obtener todos los objetos **messageRule** definidos para la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-147">Get all the **messageRule** objects defined for the user's Inbox.</span></span>|
|[<span data-ttu-id="ccdf8-148">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="ccdf8-148">Get rule</span></span>](../api/messagerule_get.md) | [<span data-ttu-id="ccdf8-149">messageRule</span><span class="sxs-lookup"><span data-stu-id="ccdf8-149">messageRule</span></span>](messagerule.md) |<span data-ttu-id="ccdf8-150">Leer las propiedades y relaciones de un objeto **messageRule**.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-150">Read the properties and relationships of a **messageRule** object.</span></span>|
|[<span data-ttu-id="ccdf8-151">Crear</span><span class="sxs-lookup"><span data-stu-id="ccdf8-151">Create</span></span>](../api/mailfolder_post_messagerules.md) | [<span data-ttu-id="ccdf8-152">messageRule</span><span class="sxs-lookup"><span data-stu-id="ccdf8-152">messageRule</span></span>](messagerule.md) |<span data-ttu-id="ccdf8-153">Crear un objeto **messageRule** especificando un conjunto de condiciones y acciones.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-153">Create a **messageRule** object by specifying a set of conditions and actions.</span></span>|
|[<span data-ttu-id="ccdf8-154">Actualizar</span><span class="sxs-lookup"><span data-stu-id="ccdf8-154">Update</span></span>](../api/messagerule_update.md) | [<span data-ttu-id="ccdf8-155">messageRule</span><span class="sxs-lookup"><span data-stu-id="ccdf8-155">messageRule</span></span>](messagerule.md) |<span data-ttu-id="ccdf8-156">Cambie las propiedades modificables en un objeto **messageRule** y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-156">Change writable properties on a **messageRule** object and save the changes.</span></span> |
|[<span data-ttu-id="ccdf8-157">Eliminar</span><span class="sxs-lookup"><span data-stu-id="ccdf8-157">Delete</span></span>](../api/messagerule_delete.md) | <span data-ttu-id="ccdf8-158">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ccdf8-158">None</span></span> |<span data-ttu-id="ccdf8-159">Eliminar el objeto **messageRule** especificado.</span><span class="sxs-lookup"><span data-stu-id="ccdf8-159">Delete the specified **messageRule** object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->