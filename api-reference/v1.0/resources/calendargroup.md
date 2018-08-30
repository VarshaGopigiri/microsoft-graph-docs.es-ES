# <a name="calendargroup-resource-type"></a><span data-ttu-id="7a67e-101">Tipo de recurso calendarGroup</span><span class="sxs-lookup"><span data-stu-id="7a67e-101">calendarGroup resource type</span></span>

<span data-ttu-id="7a67e-102">Un grupo de calendarios de usuario.</span><span class="sxs-lookup"><span data-stu-id="7a67e-102">A group of calendars.</span></span>

## <a name="methods"></a><span data-ttu-id="7a67e-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="7a67e-103">Methods</span></span>

| <span data-ttu-id="7a67e-104">Método</span><span class="sxs-lookup"><span data-stu-id="7a67e-104">Method</span></span>                                                      | <span data-ttu-id="7a67e-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a67e-105">Return Type</span></span>                        | <span data-ttu-id="7a67e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a67e-106">Description</span></span>                                                   |
| :---------------------------------------------------------- | :--------------------------------- | :------------------------------------------------------------ |
| [<span data-ttu-id="7a67e-107">List calendar groups</span><span class="sxs-lookup"><span data-stu-id="7a67e-107">List calendar groups</span></span>](../api/user_list_calendargroups.md)  | <span data-ttu-id="7a67e-108">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="7a67e-108">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="7a67e-109">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="7a67e-109">Get the user's calendar groups.</span></span>                               |
| [<span data-ttu-id="7a67e-110">Create calendar group</span><span class="sxs-lookup"><span data-stu-id="7a67e-110">Create calendar group</span></span>](../api/user_post_calendargroups.md) | [<span data-ttu-id="7a67e-111">Calendario</span><span class="sxs-lookup"><span data-stu-id="7a67e-111">Calendar</span></span>](calendar.md)            | <span data-ttu-id="7a67e-112">Crea un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="7a67e-112">Create a new calendar group.</span></span>                                  |
| [<span data-ttu-id="7a67e-113">Get calendar group</span><span class="sxs-lookup"><span data-stu-id="7a67e-113">Get calendar group</span></span>](../api/calendargroup_get.md)           | [<span data-ttu-id="7a67e-114">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="7a67e-114">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="7a67e-115">Lee las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="7a67e-115">Read properties and relationships of a calendar group object.</span></span> |
| [<span data-ttu-id="7a67e-116">Update</span><span class="sxs-lookup"><span data-stu-id="7a67e-116">Update</span></span>](../api/calendargroup_update.md)                    | [<span data-ttu-id="7a67e-117">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="7a67e-117">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="7a67e-118">Actualiza el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="7a67e-118">Update calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="7a67e-119">Delete</span><span class="sxs-lookup"><span data-stu-id="7a67e-119">Delete</span></span>](../api/calendargroup_delete.md)                    | <span data-ttu-id="7a67e-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7a67e-120">None</span></span>                               | <span data-ttu-id="7a67e-121">Elimina el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="7a67e-121">Delete calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="7a67e-122">List calendars</span><span class="sxs-lookup"><span data-stu-id="7a67e-122">List calendars</span></span>](../api/calendargroup_list_calendars.md)    | <span data-ttu-id="7a67e-123">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="7a67e-123">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="7a67e-124">Muestra la lista de calendarios de un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="7a67e-124">List calendars in a calendar group.</span></span>                           |
| [<span data-ttu-id="7a67e-125">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="7a67e-125">Create Calendar</span></span>](../api/calendargroup_post_calendars.md)   | [<span data-ttu-id="7a67e-126">Calendario</span><span class="sxs-lookup"><span data-stu-id="7a67e-126">Calendar</span></span>](calendar.md)            | <span data-ttu-id="7a67e-127">Crea un calendario en un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="7a67e-127">Create a new Calendar in a calendar group.</span></span>                    |

## <a name="properties"></a><span data-ttu-id="7a67e-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a67e-128">Properties</span></span>

| <span data-ttu-id="7a67e-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a67e-129">Property</span></span>  | <span data-ttu-id="7a67e-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a67e-130">Type</span></span>   | <span data-ttu-id="7a67e-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a67e-131">Description</span></span>                                                                                                                                                                                               |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="7a67e-132">name</span><span class="sxs-lookup"><span data-stu-id="7a67e-132">name</span></span>      | <span data-ttu-id="7a67e-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a67e-133">String</span></span> | <span data-ttu-id="7a67e-134">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="7a67e-134">The group name.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="7a67e-135">changeKey</span><span class="sxs-lookup"><span data-stu-id="7a67e-135">changeKey</span></span> | <span data-ttu-id="7a67e-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a67e-136">String</span></span> | <span data-ttu-id="7a67e-p101">Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7a67e-p101">Identifies the version of the calendar group. Every time the calendar group is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.</span></span> |
| <span data-ttu-id="7a67e-141">classId</span><span class="sxs-lookup"><span data-stu-id="7a67e-141">classId</span></span>   | <span data-ttu-id="7a67e-142">Guid</span><span class="sxs-lookup"><span data-stu-id="7a67e-142">Guid</span></span>   | <span data-ttu-id="7a67e-p102">Identificador de la clase. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7a67e-p102">The class identifier. Read-only.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="7a67e-145">id</span><span class="sxs-lookup"><span data-stu-id="7a67e-145">id</span></span>        | <span data-ttu-id="7a67e-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a67e-146">String</span></span> | <span data-ttu-id="7a67e-p103">Identificador único del grupo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7a67e-p103">The group's unique identifier. Read-only.</span></span>                                                                                                                                                                 |

## <a name="relationships"></a><span data-ttu-id="7a67e-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7a67e-149">Relationships</span></span>

| <span data-ttu-id="7a67e-150">Relación</span><span class="sxs-lookup"><span data-stu-id="7a67e-150">Relationship</span></span> | <span data-ttu-id="7a67e-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a67e-151">Type</span></span>                               | <span data-ttu-id="7a67e-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a67e-152">Description</span></span>                                                                    |
| :----------- | :--------------------------------- | :----------------------------------------------------------------------------- |
| <span data-ttu-id="7a67e-153">calendars</span><span class="sxs-lookup"><span data-stu-id="7a67e-153">calendars</span></span>    | <span data-ttu-id="7a67e-154">Colección [calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="7a67e-154">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="7a67e-p104">Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="7a67e-p104">The calendars in the calendar group. Navigation property. Read-only. Nullable.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="7a67e-159">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a67e-159">JSON representation</span></span>

<span data-ttu-id="7a67e-160">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7a67e-160">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "calendars"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.calendarGroup",
  "@odata.annotations": [
    {
      "property": "calendars",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "navigability": "single",
        "searchable": false
      }
    }
  ]
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
