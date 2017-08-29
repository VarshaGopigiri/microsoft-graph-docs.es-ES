# <a name="calendargroup-resource-type"></a><span data-ttu-id="5c0e4-101">Tipo de recurso calendarGroup</span><span class="sxs-lookup"><span data-stu-id="5c0e4-101">calendarGroup resource type</span></span>

<span data-ttu-id="5c0e4-102">Grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-102">A group of calendars.</span></span>

<span data-ttu-id="5c0e4-p101">**Nota** Outlook.com solo admite el grupo de calendarios predeterminado que es accesible mediante el acceso directo ../me/calendars. No se puede eliminar ese grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-p101">**Note** Outlook.com supports only the default calendar group which is accessible by the ../me/calendars shortcut. You cannot delete that calendar group.</span></span>

## <a name="methods"></a><span data-ttu-id="5c0e4-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c0e4-105">Methods</span></span>

| <span data-ttu-id="5c0e4-106">Método</span><span class="sxs-lookup"><span data-stu-id="5c0e4-106">Method</span></span>       | <span data-ttu-id="5c0e4-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c0e4-107">Return Type</span></span>  |<span data-ttu-id="5c0e4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c0e4-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5c0e4-109">List calendar groups</span><span class="sxs-lookup"><span data-stu-id="5c0e4-109">List calendar groups</span></span>](../api/user_list_calendargroups.md) |<span data-ttu-id="5c0e4-110">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="5c0e4-110">[Calendar](calendar.md) collection</span></span>| <span data-ttu-id="5c0e4-111">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-111">Get the user's calendar groups.</span></span>|
|[<span data-ttu-id="5c0e4-112">Create calendar group</span><span class="sxs-lookup"><span data-stu-id="5c0e4-112">Create calendar group</span></span>](../api/user_post_calendargroups.md) |[<span data-ttu-id="5c0e4-113">Calendar</span><span class="sxs-lookup"><span data-stu-id="5c0e4-113">Calendar</span></span>](calendar.md)| <span data-ttu-id="5c0e4-114">Crea un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-114">Create a new calendar group.</span></span>|
|[<span data-ttu-id="5c0e4-115">Get calendar group</span><span class="sxs-lookup"><span data-stu-id="5c0e4-115">Get calendar group</span></span>](../api/calendargroup_get.md) | [<span data-ttu-id="5c0e4-116">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="5c0e4-116">calendarGroup</span></span>](calendargroup.md) |<span data-ttu-id="5c0e4-117">Lee las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-117">Read properties and relationships of a calendar group object.</span></span>|
|[<span data-ttu-id="5c0e4-118">Update</span><span class="sxs-lookup"><span data-stu-id="5c0e4-118">Update</span></span>](../api/calendargroup_update.md) | [<span data-ttu-id="5c0e4-119">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="5c0e4-119">calendarGroup</span></span>](calendargroup.md) |<span data-ttu-id="5c0e4-120">Actualiza el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-120">Update calendarGroup object.</span></span> |
|[<span data-ttu-id="5c0e4-121">Delete</span><span class="sxs-lookup"><span data-stu-id="5c0e4-121">Delete</span></span>](../api/calendargroup_delete.md) | <span data-ttu-id="5c0e4-122">None</span><span class="sxs-lookup"><span data-stu-id="5c0e4-122">None</span></span> |<span data-ttu-id="5c0e4-123">Elimina el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-123">Delete calendarGroup object.</span></span> |
|[<span data-ttu-id="5c0e4-124">List calendars</span><span class="sxs-lookup"><span data-stu-id="5c0e4-124">List calendars</span></span>](../api/calendargroup_list_calendars.md) |<span data-ttu-id="5c0e4-125">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="5c0e4-125">[Calendar](calendar.md) collection</span></span>| <span data-ttu-id="5c0e4-126">Muestra la lista de calendarios de un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-126">List calendars in a calendar group.</span></span>|
|[<span data-ttu-id="5c0e4-127">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="5c0e4-127">Create Calendar</span></span>](../api/calendargroup_post_calendars.md) |[<span data-ttu-id="5c0e4-128">Calendar</span><span class="sxs-lookup"><span data-stu-id="5c0e4-128">Calendar</span></span>](calendar.md)| <span data-ttu-id="5c0e4-129">Crea un calendario en un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-129">Create a new Calendar in a calendar group.</span></span>|

## <a name="properties"></a><span data-ttu-id="5c0e4-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c0e4-130">Properties</span></span>
| <span data-ttu-id="5c0e4-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c0e4-131">Property</span></span>     | <span data-ttu-id="5c0e4-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c0e4-132">Type</span></span>   |<span data-ttu-id="5c0e4-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c0e4-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5c0e4-134">name</span><span class="sxs-lookup"><span data-stu-id="5c0e4-134">name</span></span>|<span data-ttu-id="5c0e4-135">String</span><span class="sxs-lookup"><span data-stu-id="5c0e4-135">String</span></span>|<span data-ttu-id="5c0e4-136">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-136">The group name.</span></span>|
|<span data-ttu-id="5c0e4-137">changeKey</span><span class="sxs-lookup"><span data-stu-id="5c0e4-137">changeKey</span></span>|<span data-ttu-id="5c0e4-138">String</span><span class="sxs-lookup"><span data-stu-id="5c0e4-138">String</span></span>|<span data-ttu-id="5c0e4-p102">Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-p102">Identifies the version of the calendar group. Every time the calendar group is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.</span></span>|
|<span data-ttu-id="5c0e4-143">classId</span><span class="sxs-lookup"><span data-stu-id="5c0e4-143">classId</span></span>|<span data-ttu-id="5c0e4-144">Guid</span><span class="sxs-lookup"><span data-stu-id="5c0e4-144">Guid</span></span>|<span data-ttu-id="5c0e4-p103">Identificador de la clase. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-p103">The class identifier. Read-only.</span></span>|
|<span data-ttu-id="5c0e4-147">id</span><span class="sxs-lookup"><span data-stu-id="5c0e4-147">id</span></span>|<span data-ttu-id="5c0e4-148">String</span><span class="sxs-lookup"><span data-stu-id="5c0e4-148">String</span></span>|<span data-ttu-id="5c0e4-p104">Identificador único del grupo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-p104">The group's unique identifier. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5c0e4-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5c0e4-151">Relationships</span></span>
| <span data-ttu-id="5c0e4-152">Relación</span><span class="sxs-lookup"><span data-stu-id="5c0e4-152">Relationship</span></span> | <span data-ttu-id="5c0e4-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c0e4-153">Type</span></span>   |<span data-ttu-id="5c0e4-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c0e4-154">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5c0e4-155">calendars</span><span class="sxs-lookup"><span data-stu-id="5c0e4-155">calendars</span></span>|<span data-ttu-id="5c0e4-156">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="5c0e4-156">[Calendar](calendar.md) collection</span></span>|<span data-ttu-id="5c0e4-p105">Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5c0e4-p105">The calendars in the calendar group. Navigation property. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5c0e4-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5c0e4-161">JSON representation</span></span>

<span data-ttu-id="5c0e4-162">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5c0e4-162">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "calendars"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.calendarGroup"
}-->

```json
{
  "changeKey": "string",
  "classId": "guid",
  "id": "string (identifier)",
  "name": "string"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "calendarGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
