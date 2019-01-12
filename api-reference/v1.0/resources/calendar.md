---
title: tipo de recurso calendar
description: Un calendario que es un contenedor de eventos. Puede ser un calendario de un usuario o el calendario predeterminado de un grupo de Office 365.
localization_priority: Priority
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 6d7f926c26b0fdcf0c70e7f6d02593cff8bb46a6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917625"
---
# <a name="calendar-resource-type"></a><span data-ttu-id="81903-104">tipo de recurso calendar</span><span class="sxs-lookup"><span data-stu-id="81903-104">calendar resource type</span></span>

<span data-ttu-id="81903-105">Un calendario que es un contenedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="81903-105">A calendar which is a container for events.</span></span> <span data-ttu-id="81903-106">Puede ser un calendario de un [usuario](user.md) o el calendario predeterminado de un [grupo](group.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="81903-106">It can be a calendar for a [user](user.md), or the default calendar of an Office 365 [group](group.md).</span></span>

> <span data-ttu-id="81903-107">**Nota:** Existen algunas pequeñas diferencias en la forma en que puede interactuar con los calendarios de usuario y los calendarios de grupo:</span><span class="sxs-lookup"><span data-stu-id="81903-107">**Note:** There are a few minor differences in the way you can interact with user calendars and group calendars:</span></span>

 - <span data-ttu-id="81903-108">Puede organizar sólo los calendarios de usuario en un [calendarGroup](calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="81903-108">You can organize only user calendars in a [calendarGroup](calendargroup.md).</span></span>
 - <span data-ttu-id="81903-109">Outlook acepta automáticamente todas las convocatorias de reunión en nombre de grupos.</span><span class="sxs-lookup"><span data-stu-id="81903-109">Outlook automatically accepts all meeting requests on behalf of groups.</span></span> <span data-ttu-id="81903-110">Para los calendarios de usuario sólo puede [Aceptar](../api/event-accept.md), [Aceptar provisionalmente](../api/event-tentativelyaccept.md)o [Rechazar](../api/event-decline.md) las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="81903-110">You can [accept](../api/event-accept.md), [tentatively accept](../api/event-tentativelyaccept.md), or [decline](../api/event-decline.md)  meeting requests for user calendars only.</span></span>
  - <span data-ttu-id="81903-111">Outlook no admite avisos para eventos de grupo.</span><span class="sxs-lookup"><span data-stu-id="81903-111">Outlook doesn't support reminders for group events.</span></span> <span data-ttu-id="81903-112">Para los calendarios de usuario sólo puede [Posponer](../api/event-snoozereminder.md) o [Descartar](../api/event-dismissreminder.md) un [aviso](reminder.md) .</span><span class="sxs-lookup"><span data-stu-id="81903-112">You can [snooze](../api/event-snoozereminder.md) or [dismiss](../api/event-dismissreminder.md) a [reminder](reminder.md) for user calendars only.</span></span>

## <a name="methods"></a><span data-ttu-id="81903-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="81903-113">Methods</span></span>

| <span data-ttu-id="81903-114">Método</span><span class="sxs-lookup"><span data-stu-id="81903-114">Method</span></span>       | <span data-ttu-id="81903-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81903-115">Return Type</span></span>  |<span data-ttu-id="81903-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="81903-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="81903-117">List calendars</span><span class="sxs-lookup"><span data-stu-id="81903-117">List calendars</span></span>](../api/user-list-calendars.md)|<span data-ttu-id="81903-118">[calendar](calendar.md) collection</span><span class="sxs-lookup"><span data-stu-id="81903-118">[calendar](calendar.md) collection</span></span>|<span data-ttu-id="81903-119">Obtenga todos los calendarios del usuario o los calendarios en el grupo de calendarios predeterminado o en otro grupo de calendarios específico.</span><span class="sxs-lookup"><span data-stu-id="81903-119">Get all the user's calendars, or the calendars in the default or other specific calendar group.</span></span>|
|[<span data-ttu-id="81903-120">Create calendar</span><span class="sxs-lookup"><span data-stu-id="81903-120">Create calendar</span></span>](../api/user-post-calendars.md) |[<span data-ttu-id="81903-121">calendar</span><span class="sxs-lookup"><span data-stu-id="81903-121">calendar</span></span>](calendar.md)| <span data-ttu-id="81903-122">Cree un calendario en el grupo de calendarios predeterminado o en el grupo de calendario especificado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="81903-122">Create a new calendar in the default calendar group or specified calendar group for a user.</span></span>|
|[<span data-ttu-id="81903-123">Get calendar</span><span class="sxs-lookup"><span data-stu-id="81903-123">Get calendar</span></span>](../api/calendar-get.md) | [<span data-ttu-id="81903-124">calendar</span><span class="sxs-lookup"><span data-stu-id="81903-124">calendar</span></span>](calendar.md) |<span data-ttu-id="81903-125">Obtiene las propiedades y relaciones de un objeto de **calendario**.</span><span class="sxs-lookup"><span data-stu-id="81903-125">Get the properties and relationships of a **calendar** object.</span></span> <span data-ttu-id="81903-126">El calendario puede ser de un usuario o el calendario predeterminado de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="81903-126">The calendar can be one for a user, or the default calendar of an Office 365 group.</span></span> |
|[<span data-ttu-id="81903-127">Update</span><span class="sxs-lookup"><span data-stu-id="81903-127">Update</span></span>](../api/calendar-update.md) | [<span data-ttu-id="81903-128">calendar</span><span class="sxs-lookup"><span data-stu-id="81903-128">calendar</span></span>](calendar.md)  |<span data-ttu-id="81903-129">Actualiza las propiedades del objeto de **calendario**.</span><span class="sxs-lookup"><span data-stu-id="81903-129">Update the properties of a **calendar** object.</span></span> <span data-ttu-id="81903-130">El calendario puede ser de un usuario o el calendario predeterminado de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="81903-130">The calendar can be one for a user, or the default calendar of an Office 365 group.</span></span> |
|[<span data-ttu-id="81903-131">Delete</span><span class="sxs-lookup"><span data-stu-id="81903-131">Delete</span></span>](../api/calendar-delete.md) | <span data-ttu-id="81903-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="81903-132">None</span></span> |<span data-ttu-id="81903-133">Elimine el objeto de calendario.</span><span class="sxs-lookup"><span data-stu-id="81903-133">Delete calendar object.</span></span> |
|[<span data-ttu-id="81903-134">List calendarView</span><span class="sxs-lookup"><span data-stu-id="81903-134">List calendarView</span></span>](../api/calendar-list-calendarview.md) |<span data-ttu-id="81903-135">Colección [event](event.md)</span><span class="sxs-lookup"><span data-stu-id="81903-135">[event](event.md) collection</span></span>| <span data-ttu-id="81903-136">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario principal del usuario `(../me/calendarview)` o de un calendario especificado.</span><span class="sxs-lookup"><span data-stu-id="81903-136">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the user's primary calendar `(../me/calendarview)` or from a specified calendar.</span></span>|
|[<span data-ttu-id="81903-137">List events</span><span class="sxs-lookup"><span data-stu-id="81903-137">List events</span></span>](../api/calendar-list-events.md) |<span data-ttu-id="81903-138">Colección [event](event.md)</span><span class="sxs-lookup"><span data-stu-id="81903-138">[event](event.md) collection</span></span>| <span data-ttu-id="81903-p107">Recupera una lista de eventos de un calendario.  La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="81903-p107">Retrieve a list of events in a calendar.  The list contains single instance meetings and series masters.</span></span>|
|[<span data-ttu-id="81903-141">Crear evento</span><span class="sxs-lookup"><span data-stu-id="81903-141">Create event</span></span>](../api/calendar-post-events.md) |[<span data-ttu-id="81903-142">evento</span><span class="sxs-lookup"><span data-stu-id="81903-142">event</span></span>](event.md)| <span data-ttu-id="81903-143">Crear un nuevo evento en el calendario especificado o el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81903-143">Create a new event in the default or specified calendar.</span></span>|
|[<span data-ttu-id="81903-144">findMeetingTimes</span><span class="sxs-lookup"><span data-stu-id="81903-144">findMeetingTimes</span></span>](../api/user-findmeetingtimes.md) |[<span data-ttu-id="81903-145">meetingTimeSuggestionsResult</span><span class="sxs-lookup"><span data-stu-id="81903-145">meetingTimeSuggestionsResult</span></span>](meetingtimesuggestionsresult.md) |<span data-ttu-id="81903-146">Sugerir horas de reunión y las ubicaciones en función de la disponibilidad del organizador y el asistente y las restricciones de hora o la ubicación.</span><span class="sxs-lookup"><span data-stu-id="81903-146">Suggest meeting times and locations based on organizer and attendee availability, and time or location constraints.</span></span> |
|[<span data-ttu-id="81903-147">Create single-value extended property</span><span class="sxs-lookup"><span data-stu-id="81903-147">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[<span data-ttu-id="81903-148">calendar</span><span class="sxs-lookup"><span data-stu-id="81903-148">calendar</span></span>](calendar.md)  |<span data-ttu-id="81903-149">Cree una o varias propiedades extendidas de valor único en un calendario nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="81903-149">Create one or more single-value extended properties in a new or existing calendar.</span></span>   |
|[<span data-ttu-id="81903-150">Get calendar with single-value extended property</span><span class="sxs-lookup"><span data-stu-id="81903-150">Get calendar with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="81903-151">calendar</span><span class="sxs-lookup"><span data-stu-id="81903-151">calendar</span></span>](calendar.md) | <span data-ttu-id="81903-152">Obtenga calendarios que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="81903-152">Get calendars that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="81903-153">Create multi-value extended property</span><span class="sxs-lookup"><span data-stu-id="81903-153">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [<span data-ttu-id="81903-154">calendar</span><span class="sxs-lookup"><span data-stu-id="81903-154">calendar</span></span>](calendar.md) | <span data-ttu-id="81903-155">Cree una o varias propiedades extendidas de varios valores en un calendario nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="81903-155">Create one or more multi-value extended properties in a new or existing calendar.</span></span>  |
|[<span data-ttu-id="81903-156">Get calendar with multi-value extended property</span><span class="sxs-lookup"><span data-stu-id="81903-156">Get calendar with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="81903-157">calendar</span><span class="sxs-lookup"><span data-stu-id="81903-157">calendar</span></span>](calendar.md) | <span data-ttu-id="81903-158">Obtenga un calendario que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="81903-158">Get a calendar that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="81903-159">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81903-159">Properties</span></span>
| <span data-ttu-id="81903-160">Propiedad</span><span class="sxs-lookup"><span data-stu-id="81903-160">Property</span></span>     | <span data-ttu-id="81903-161">Tipo</span><span class="sxs-lookup"><span data-stu-id="81903-161">Type</span></span>   |<span data-ttu-id="81903-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="81903-162">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="81903-163">canEdit</span><span class="sxs-lookup"><span data-stu-id="81903-163">canEdit</span></span> |<span data-ttu-id="81903-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="81903-164">Boolean</span></span> |<span data-ttu-id="81903-p108">Es verdadero si el usuario puede escribir en el calendario; de lo contrario, es falso. Esta propiedad es verdadera para el usuario que creó el calendario. Esta propiedad también es verdadera para un usuario con quien se compartió un calendario y al que se concedió acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="81903-p108">True if the user can write to the calendar, false otherwise. This property is true for the user who created the calendar. This property is also true for a user who has been shared a calendar and granted write access.</span></span> |
|<span data-ttu-id="81903-168">canShare</span><span class="sxs-lookup"><span data-stu-id="81903-168">canShare</span></span> |<span data-ttu-id="81903-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="81903-169">Boolean</span></span> |<span data-ttu-id="81903-p109">Es verdadero si el usuario tiene permiso para compartir el calendario; de lo contrario, es falso. Solo el usuario que creó el calendario puede compartirlo.</span><span class="sxs-lookup"><span data-stu-id="81903-p109">True if the user has the permission to share the calendar, false otherwise. Only the user who created the calendar can share it.</span></span> |
|<span data-ttu-id="81903-172">canViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="81903-172">canViewPrivateItems</span></span> |<span data-ttu-id="81903-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="81903-173">Boolean</span></span> |<span data-ttu-id="81903-174">Es verdadero si el usuario puede leer elementos del calendario que se marcaron como privados; de lo contrario, es falso.</span><span class="sxs-lookup"><span data-stu-id="81903-174">True if the user can read calendar items that have been marked private, false otherwise.</span></span> |
|<span data-ttu-id="81903-175">changeKey</span><span class="sxs-lookup"><span data-stu-id="81903-175">changeKey</span></span>|<span data-ttu-id="81903-176">String</span><span class="sxs-lookup"><span data-stu-id="81903-176">String</span></span>|<span data-ttu-id="81903-p110">Identifica la versión del objeto “calendar”. Cada vez que se cambia el calendario, también se cambia changeKey. Esto permite que Exchange aplique los cambios en la versión correcta del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="81903-p110">Identifies the version of the calendar object. Every time the calendar is changed, changeKey changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.</span></span>|
|<span data-ttu-id="81903-181">color</span><span class="sxs-lookup"><span data-stu-id="81903-181">color</span></span>|<span data-ttu-id="81903-182">calendarColor</span><span class="sxs-lookup"><span data-stu-id="81903-182">calendarColor</span></span>|<span data-ttu-id="81903-p111">Especifica el tema de color para distinguir el calendario de otros calendarios en una interfaz de usuario. Los valores de propiedad son: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span><span class="sxs-lookup"><span data-stu-id="81903-p111">Specifies the color theme to distinguish the calendar from other calendars in a UI. The property values are: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span></span>|
|<span data-ttu-id="81903-185">id</span><span class="sxs-lookup"><span data-stu-id="81903-185">id</span></span>|<span data-ttu-id="81903-186">String</span><span class="sxs-lookup"><span data-stu-id="81903-186">String</span></span>|<span data-ttu-id="81903-p112">El identificador único del grupo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="81903-p112">The group's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="81903-189">name</span><span class="sxs-lookup"><span data-stu-id="81903-189">name</span></span>|<span data-ttu-id="81903-190">String</span><span class="sxs-lookup"><span data-stu-id="81903-190">String</span></span>|<span data-ttu-id="81903-191">El nombre del calendario.</span><span class="sxs-lookup"><span data-stu-id="81903-191">The calendar name.</span></span>|
|<span data-ttu-id="81903-192">owner</span><span class="sxs-lookup"><span data-stu-id="81903-192">owner</span></span> |[<span data-ttu-id="81903-193">emailAddress</span><span class="sxs-lookup"><span data-stu-id="81903-193">emailAddress</span></span>](emailaddress.md) | <span data-ttu-id="81903-p113">Si se establece, representa al usuario que creó o agregó el calendario. Para un calendario que el usuario creó o agregó, la propiedad **owner** se establece en el usuario. Para un calendario compartido con el usuario, la propiedad **owner** se establece en la persona que compartió el calendario con el usuario.</span><span class="sxs-lookup"><span data-stu-id="81903-p113">If set, this represents the user who created or added the calendar. For a calendar that the user created or added, the **owner** property is set to the user. For a calendar shared with the user, the **owner** property is set to the person who shared that calendar with the user.</span></span> |

## <a name="relationships"></a><span data-ttu-id="81903-197">Relaciones</span><span class="sxs-lookup"><span data-stu-id="81903-197">Relationships</span></span>
| <span data-ttu-id="81903-198">Relación</span><span class="sxs-lookup"><span data-stu-id="81903-198">Relationship</span></span> | <span data-ttu-id="81903-199">Tipo</span><span class="sxs-lookup"><span data-stu-id="81903-199">Type</span></span>   |<span data-ttu-id="81903-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="81903-200">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="81903-201">calendarView</span><span class="sxs-lookup"><span data-stu-id="81903-201">calendarView</span></span>|<span data-ttu-id="81903-202">Colección [event](event.md)</span><span class="sxs-lookup"><span data-stu-id="81903-202">[Event](event.md) collection</span></span>|<span data-ttu-id="81903-p114">La vista Calendario del calendario. Propiedad Navigation. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="81903-p114">The calendar view for the calendar. Navigation property. Read-only.</span></span>|
|<span data-ttu-id="81903-206">events</span><span class="sxs-lookup"><span data-stu-id="81903-206">events</span></span>|<span data-ttu-id="81903-207">[Event](event.md) collection</span><span class="sxs-lookup"><span data-stu-id="81903-207">[Event](event.md) collection</span></span>|<span data-ttu-id="81903-p115">Los eventos del calendario. Propiedad Navigation. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="81903-p115">The events in the calendar. Navigation property. Read-only.</span></span>|
|<span data-ttu-id="81903-211">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="81903-211">multiValueExtendedProperties</span></span>|<span data-ttu-id="81903-212">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="81903-212">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="81903-p116">La colección de propiedades extendidas de varios valores definidas para el calendario. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="81903-p116">The collection of multi-value extended properties defined for the calendar. Read-only. Nullable.</span></span>|
|<span data-ttu-id="81903-216">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="81903-216">singleValueExtendedProperties</span></span>|<span data-ttu-id="81903-217">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="81903-217">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="81903-p117">La colección de propiedades extendidas de valor único definidas para el calendario. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="81903-p117">The collection of single-value extended properties defined for the calendar. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="81903-221">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="81903-221">JSON representation</span></span>

<span data-ttu-id="81903-222">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="81903-222">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "calendarView",
    "events",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.calendar",
  "@odata.annotations": [
    {
      "property": "calendarView",
      "capabilities": {
        "changeTracking": true,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "navigability": "single",
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "events",
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
  "canEdit": "boolean",
  "canShare": "boolean",
  "canViewPrivateItems": "boolean",
  "changeKey": "string",
  "color": "String",
  "id": "string (identifier)",
  "name": "string",
  "owner": {"@odata.type": "microsoft.graph.emailAddress"}
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "calendar resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
