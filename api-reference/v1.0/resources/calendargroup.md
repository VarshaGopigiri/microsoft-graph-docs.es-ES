---
title: Tipo de recurso calendarGroup
description: Un grupo de calendarios de usuario.
ms.openlocfilehash: 6cc3ec5ed206109b341d0fc69845c9bd19df9373
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028640"
---
# <a name="calendargroup-resource-type"></a><span data-ttu-id="32367-103">Tipo de recurso calendarGroup</span><span class="sxs-lookup"><span data-stu-id="32367-103">calendarGroup resource type</span></span>

<span data-ttu-id="32367-104">Un grupo de calendarios de usuario.</span><span class="sxs-lookup"><span data-stu-id="32367-104">A group of user calendars.</span></span>

## <a name="methods"></a><span data-ttu-id="32367-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="32367-105">Methods</span></span>

| <span data-ttu-id="32367-106">Método</span><span class="sxs-lookup"><span data-stu-id="32367-106">Method</span></span>                                                      | <span data-ttu-id="32367-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32367-107">Return Type</span></span>                        | <span data-ttu-id="32367-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="32367-108">Description</span></span>                                                   |
| :---------------------------------------------------------- | :--------------------------------- | :------------------------------------------------------------ |
| [<span data-ttu-id="32367-109">List calendar groups</span><span class="sxs-lookup"><span data-stu-id="32367-109">List calendar groups</span></span>](../api/user-list-calendargroups.md)  | <span data-ttu-id="32367-110">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="32367-110">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="32367-111">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="32367-111">Get the user's calendar groups.</span></span>                               |
| [<span data-ttu-id="32367-112">Create calendar group</span><span class="sxs-lookup"><span data-stu-id="32367-112">Create calendar group</span></span>](../api/user-post-calendargroups.md) | [<span data-ttu-id="32367-113">Calendar</span><span class="sxs-lookup"><span data-stu-id="32367-113">Calendar</span></span>](calendar.md)            | <span data-ttu-id="32367-114">Crea un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="32367-114">Create a new calendar group.</span></span>                                  |
| [<span data-ttu-id="32367-115">Get calendar group</span><span class="sxs-lookup"><span data-stu-id="32367-115">Get calendar group</span></span>](../api/calendargroup-get.md)           | [<span data-ttu-id="32367-116">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="32367-116">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="32367-117">Lee las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="32367-117">Read properties and relationships of a calendar group object.</span></span> |
| [<span data-ttu-id="32367-118">Update</span><span class="sxs-lookup"><span data-stu-id="32367-118">Update</span></span>](../api/calendargroup-update.md)                    | [<span data-ttu-id="32367-119">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="32367-119">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="32367-120">Actualiza el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="32367-120">Update calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="32367-121">Delete</span><span class="sxs-lookup"><span data-stu-id="32367-121">Delete</span></span>](../api/calendargroup-delete.md)                    | <span data-ttu-id="32367-122">None</span><span class="sxs-lookup"><span data-stu-id="32367-122">None</span></span>                               | <span data-ttu-id="32367-123">Elimina el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="32367-123">Delete calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="32367-124">List calendars</span><span class="sxs-lookup"><span data-stu-id="32367-124">List calendars</span></span>](../api/calendargroup-list-calendars.md)    | <span data-ttu-id="32367-125">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="32367-125">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="32367-126">Muestra la lista de calendarios de un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="32367-126">List calendars in a calendar group.</span></span>                           |
| [<span data-ttu-id="32367-127">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="32367-127">Create Calendar</span></span>](../api/calendargroup-post-calendars.md)   | [<span data-ttu-id="32367-128">Calendar</span><span class="sxs-lookup"><span data-stu-id="32367-128">Calendar</span></span>](calendar.md)            | <span data-ttu-id="32367-129">Crea un calendario en un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="32367-129">Create a new Calendar in a calendar group.</span></span>                    |

## <a name="properties"></a><span data-ttu-id="32367-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32367-130">Properties</span></span>

| <span data-ttu-id="32367-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32367-131">Property</span></span>  | <span data-ttu-id="32367-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="32367-132">Type</span></span>   | <span data-ttu-id="32367-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="32367-133">Description</span></span>                                                                                                                                                                                               |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="32367-134">name</span><span class="sxs-lookup"><span data-stu-id="32367-134">name</span></span>      | <span data-ttu-id="32367-135">String</span><span class="sxs-lookup"><span data-stu-id="32367-135">String</span></span> | <span data-ttu-id="32367-136">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="32367-136">The group name.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="32367-137">changeKey</span><span class="sxs-lookup"><span data-stu-id="32367-137">changeKey</span></span> | <span data-ttu-id="32367-138">String</span><span class="sxs-lookup"><span data-stu-id="32367-138">String</span></span> | <span data-ttu-id="32367-p101">Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32367-p101">Identifies the version of the calendar group. Every time the calendar group is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.</span></span> |
| <span data-ttu-id="32367-143">classId</span><span class="sxs-lookup"><span data-stu-id="32367-143">classId</span></span>   | <span data-ttu-id="32367-144">Guid</span><span class="sxs-lookup"><span data-stu-id="32367-144">Guid</span></span>   | <span data-ttu-id="32367-p102">Identificador de la clase. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32367-p102">The class identifier. Read-only.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="32367-147">id</span><span class="sxs-lookup"><span data-stu-id="32367-147">id</span></span>        | <span data-ttu-id="32367-148">String</span><span class="sxs-lookup"><span data-stu-id="32367-148">String</span></span> | <span data-ttu-id="32367-p103">Identificador único del grupo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32367-p103">The group's unique identifier. Read-only.</span></span>                                                                                                                                                                 |

## <a name="relationships"></a><span data-ttu-id="32367-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="32367-151">Relationships</span></span>

| <span data-ttu-id="32367-152">Relación</span><span class="sxs-lookup"><span data-stu-id="32367-152">Relationship</span></span> | <span data-ttu-id="32367-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="32367-153">Type</span></span>                               | <span data-ttu-id="32367-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="32367-154">Description</span></span>                                                                    |
| :----------- | :--------------------------------- | :----------------------------------------------------------------------------- |
| <span data-ttu-id="32367-155">calendars</span><span class="sxs-lookup"><span data-stu-id="32367-155">calendars</span></span>    | <span data-ttu-id="32367-156">Colección [calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="32367-156">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="32367-p104">Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="32367-p104">The calendars in the calendar group. Navigation property. Read-only. Nullable.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="32367-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32367-161">JSON representation</span></span>

<span data-ttu-id="32367-162">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="32367-162">Here is a JSON representation of the resource</span></span>

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
