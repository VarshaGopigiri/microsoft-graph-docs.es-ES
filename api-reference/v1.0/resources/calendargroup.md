# <a name="calendargroup-resource-type"></a><span data-ttu-id="033ac-101">Tipo de recurso calendarGroup</span><span class="sxs-lookup"><span data-stu-id="033ac-101">calendarGroup resource type</span></span>

<span data-ttu-id="033ac-102">Un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="033ac-102">A group of calendars.</span></span>

## <a name="methods"></a><span data-ttu-id="033ac-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="033ac-103">Methods</span></span>

| <span data-ttu-id="033ac-104">Método</span><span class="sxs-lookup"><span data-stu-id="033ac-104">Method</span></span>                                                      | <span data-ttu-id="033ac-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="033ac-105">Return Type</span></span>                        | <span data-ttu-id="033ac-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="033ac-106">Description</span></span>                                                   |
| :---------------------------------------------------------- | :--------------------------------- | :------------------------------------------------------------ |
| [<span data-ttu-id="033ac-107">List calendar groups</span><span class="sxs-lookup"><span data-stu-id="033ac-107">List calendar groups</span></span>](../api/user_list_calendargroups.md)  | <span data-ttu-id="033ac-108">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="033ac-108">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="033ac-109">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="033ac-109">Get the user's calendar groups.</span></span>                               |
| [<span data-ttu-id="033ac-110">Create calendar group</span><span class="sxs-lookup"><span data-stu-id="033ac-110">Create calendar group</span></span>](../api/user_post_calendargroups.md) | [<span data-ttu-id="033ac-111">Calendar</span><span class="sxs-lookup"><span data-stu-id="033ac-111">Calendar</span></span>](calendar.md)            | <span data-ttu-id="033ac-112">Crea un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="033ac-112">Create a new calendar group.</span></span>                                  |
| [<span data-ttu-id="033ac-113">Get calendar group</span><span class="sxs-lookup"><span data-stu-id="033ac-113">Get calendar group</span></span>](../api/calendargroup_get.md)           | [<span data-ttu-id="033ac-114">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="033ac-114">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="033ac-115">Lee las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="033ac-115">Read properties and relationships of a calendar group object.</span></span> |
| [<span data-ttu-id="033ac-116">Update</span><span class="sxs-lookup"><span data-stu-id="033ac-116">Update</span></span>](../api/calendargroup_update.md)                    | [<span data-ttu-id="033ac-117">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="033ac-117">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="033ac-118">Actualiza el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="033ac-118">Update calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="033ac-119">Delete</span><span class="sxs-lookup"><span data-stu-id="033ac-119">Delete</span></span>](../api/calendargroup_delete.md)                    | <span data-ttu-id="033ac-120">None</span><span class="sxs-lookup"><span data-stu-id="033ac-120">None</span></span>                               | <span data-ttu-id="033ac-121">Elimina el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="033ac-121">Delete calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="033ac-122">List calendars</span><span class="sxs-lookup"><span data-stu-id="033ac-122">List calendars</span></span>](../api/calendargroup_list_calendars.md)    | <span data-ttu-id="033ac-123">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="033ac-123">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="033ac-124">Muestra la lista de calendarios de un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="033ac-124">List calendars in a calendar group.</span></span>                           |
| [<span data-ttu-id="033ac-125">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="033ac-125">Create Calendar</span></span>](../api/calendargroup_post_calendars.md)   | [<span data-ttu-id="033ac-126">Calendar</span><span class="sxs-lookup"><span data-stu-id="033ac-126">Calendar</span></span>](calendar.md)            | <span data-ttu-id="033ac-127">Crea un calendario en un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="033ac-127">Create a new Calendar in a calendar group.</span></span>                    |

## <a name="properties"></a><span data-ttu-id="033ac-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="033ac-128">Properties</span></span>

| <span data-ttu-id="033ac-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="033ac-129">Property</span></span>  | <span data-ttu-id="033ac-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="033ac-130">Type</span></span>   | <span data-ttu-id="033ac-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="033ac-131">Description</span></span>                                                                                                                                                                                               |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="033ac-132">name</span><span class="sxs-lookup"><span data-stu-id="033ac-132">name</span></span>      | <span data-ttu-id="033ac-133">String</span><span class="sxs-lookup"><span data-stu-id="033ac-133">String</span></span> | <span data-ttu-id="033ac-134">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="033ac-134">The group name.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="033ac-135">changeKey</span><span class="sxs-lookup"><span data-stu-id="033ac-135">changeKey</span></span> | <span data-ttu-id="033ac-136">String</span><span class="sxs-lookup"><span data-stu-id="033ac-136">String</span></span> | <span data-ttu-id="033ac-p101">Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="033ac-p101">Identifies the version of the calendar group. Every time the calendar group is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.</span></span> |
| <span data-ttu-id="033ac-141">classId</span><span class="sxs-lookup"><span data-stu-id="033ac-141">classId</span></span>   | <span data-ttu-id="033ac-142">Guid</span><span class="sxs-lookup"><span data-stu-id="033ac-142">Guid</span></span>   | <span data-ttu-id="033ac-p102">Identificador de la clase. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="033ac-p102">The class identifier. Read-only.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="033ac-145">id</span><span class="sxs-lookup"><span data-stu-id="033ac-145">id</span></span>        | <span data-ttu-id="033ac-146">String</span><span class="sxs-lookup"><span data-stu-id="033ac-146">String</span></span> | <span data-ttu-id="033ac-p103">Identificador único del grupo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="033ac-p103">The group's unique identifier. Read-only.</span></span>                                                                                                                                                                 |

## <a name="relationships"></a><span data-ttu-id="033ac-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="033ac-149">Relationships</span></span>

| <span data-ttu-id="033ac-150">Relación</span><span class="sxs-lookup"><span data-stu-id="033ac-150">Relationship</span></span> | <span data-ttu-id="033ac-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="033ac-151">Type</span></span>                               | <span data-ttu-id="033ac-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="033ac-152">Description</span></span>                                                                    |
| :----------- | :--------------------------------- | :----------------------------------------------------------------------------- |
| <span data-ttu-id="033ac-153">calendars</span><span class="sxs-lookup"><span data-stu-id="033ac-153">calendars</span></span>    | <span data-ttu-id="033ac-154">Colección [calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="033ac-154">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="033ac-p104">Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="033ac-p104">The calendars in the calendar group. Navigation property. Read-only. Nullable.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="033ac-159">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="033ac-159">JSON representation</span></span>

<span data-ttu-id="033ac-160">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="033ac-160">Here is a JSON representation of the resource</span></span>

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
