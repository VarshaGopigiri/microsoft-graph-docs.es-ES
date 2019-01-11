---
title: Tipo de recurso calendarGroup
description: Un grupo de calendarios de usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 1acc95f95c550c2bd48f8c6d3a117666b666b20f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818581"
---
# <a name="calendargroup-resource-type"></a><span data-ttu-id="5fc0d-103">Tipo de recurso calendarGroup</span><span class="sxs-lookup"><span data-stu-id="5fc0d-103">calendarGroup resource type</span></span>

<span data-ttu-id="5fc0d-104">Un grupo de calendarios de usuario.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-104">A group of user calendars.</span></span>

## <a name="methods"></a><span data-ttu-id="5fc0d-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="5fc0d-105">Methods</span></span>

| <span data-ttu-id="5fc0d-106">Método</span><span class="sxs-lookup"><span data-stu-id="5fc0d-106">Method</span></span>                                                      | <span data-ttu-id="5fc0d-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fc0d-107">Return Type</span></span>                        | <span data-ttu-id="5fc0d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fc0d-108">Description</span></span>                                                   |
| :---------------------------------------------------------- | :--------------------------------- | :------------------------------------------------------------ |
| [<span data-ttu-id="5fc0d-109">List calendar groups</span><span class="sxs-lookup"><span data-stu-id="5fc0d-109">List calendar groups</span></span>](../api/user-list-calendargroups.md)  | <span data-ttu-id="5fc0d-110">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="5fc0d-110">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="5fc0d-111">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-111">Get the user's calendar groups.</span></span>                               |
| [<span data-ttu-id="5fc0d-112">Create calendar group</span><span class="sxs-lookup"><span data-stu-id="5fc0d-112">Create calendar group</span></span>](../api/user-post-calendargroups.md) | [<span data-ttu-id="5fc0d-113">Calendar</span><span class="sxs-lookup"><span data-stu-id="5fc0d-113">Calendar</span></span>](calendar.md)            | <span data-ttu-id="5fc0d-114">Crea un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-114">Create a new calendar group.</span></span>                                  |
| [<span data-ttu-id="5fc0d-115">Get calendar group</span><span class="sxs-lookup"><span data-stu-id="5fc0d-115">Get calendar group</span></span>](../api/calendargroup-get.md)           | [<span data-ttu-id="5fc0d-116">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="5fc0d-116">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="5fc0d-117">Lee las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-117">Read properties and relationships of a calendar group object.</span></span> |
| [<span data-ttu-id="5fc0d-118">Update</span><span class="sxs-lookup"><span data-stu-id="5fc0d-118">Update</span></span>](../api/calendargroup-update.md)                    | [<span data-ttu-id="5fc0d-119">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="5fc0d-119">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="5fc0d-120">Actualiza el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-120">Update calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="5fc0d-121">Delete</span><span class="sxs-lookup"><span data-stu-id="5fc0d-121">Delete</span></span>](../api/calendargroup-delete.md)                    | <span data-ttu-id="5fc0d-122">None</span><span class="sxs-lookup"><span data-stu-id="5fc0d-122">None</span></span>                               | <span data-ttu-id="5fc0d-123">Elimina el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-123">Delete calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="5fc0d-124">List calendars</span><span class="sxs-lookup"><span data-stu-id="5fc0d-124">List calendars</span></span>](../api/calendargroup-list-calendars.md)    | <span data-ttu-id="5fc0d-125">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="5fc0d-125">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="5fc0d-126">Muestra la lista de calendarios de un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-126">List calendars in a calendar group.</span></span>                           |
| [<span data-ttu-id="5fc0d-127">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="5fc0d-127">Create Calendar</span></span>](../api/calendargroup-post-calendars.md)   | [<span data-ttu-id="5fc0d-128">Calendar</span><span class="sxs-lookup"><span data-stu-id="5fc0d-128">Calendar</span></span>](calendar.md)            | <span data-ttu-id="5fc0d-129">Crea un calendario en un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-129">Create a new Calendar in a calendar group.</span></span>                    |

## <a name="properties"></a><span data-ttu-id="5fc0d-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5fc0d-130">Properties</span></span>

| <span data-ttu-id="5fc0d-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5fc0d-131">Property</span></span>  | <span data-ttu-id="5fc0d-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fc0d-132">Type</span></span>   | <span data-ttu-id="5fc0d-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fc0d-133">Description</span></span>                                                                                                                                                                                               |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="5fc0d-134">name</span><span class="sxs-lookup"><span data-stu-id="5fc0d-134">name</span></span>      | <span data-ttu-id="5fc0d-135">String</span><span class="sxs-lookup"><span data-stu-id="5fc0d-135">String</span></span> | <span data-ttu-id="5fc0d-136">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-136">The group name.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="5fc0d-137">changeKey</span><span class="sxs-lookup"><span data-stu-id="5fc0d-137">changeKey</span></span> | <span data-ttu-id="5fc0d-138">String</span><span class="sxs-lookup"><span data-stu-id="5fc0d-138">String</span></span> | <span data-ttu-id="5fc0d-p101">Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-p101">Identifies the version of the calendar group. Every time the calendar group is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.</span></span> |
| <span data-ttu-id="5fc0d-143">classId</span><span class="sxs-lookup"><span data-stu-id="5fc0d-143">classId</span></span>   | <span data-ttu-id="5fc0d-144">Guid</span><span class="sxs-lookup"><span data-stu-id="5fc0d-144">Guid</span></span>   | <span data-ttu-id="5fc0d-p102">Identificador de la clase. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-p102">The class identifier. Read-only.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="5fc0d-147">id</span><span class="sxs-lookup"><span data-stu-id="5fc0d-147">id</span></span>        | <span data-ttu-id="5fc0d-148">String</span><span class="sxs-lookup"><span data-stu-id="5fc0d-148">String</span></span> | <span data-ttu-id="5fc0d-p103">Identificador único del grupo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-p103">The group's unique identifier. Read-only.</span></span>                                                                                                                                                                 |

## <a name="relationships"></a><span data-ttu-id="5fc0d-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5fc0d-151">Relationships</span></span>

| <span data-ttu-id="5fc0d-152">Relación</span><span class="sxs-lookup"><span data-stu-id="5fc0d-152">Relationship</span></span> | <span data-ttu-id="5fc0d-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fc0d-153">Type</span></span>                               | <span data-ttu-id="5fc0d-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fc0d-154">Description</span></span>                                                                    |
| :----------- | :--------------------------------- | :----------------------------------------------------------------------------- |
| <span data-ttu-id="5fc0d-155">calendars</span><span class="sxs-lookup"><span data-stu-id="5fc0d-155">calendars</span></span>    | <span data-ttu-id="5fc0d-156">Colección [calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="5fc0d-156">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="5fc0d-p104">Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5fc0d-p104">The calendars in the calendar group. Navigation property. Read-only. Nullable.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="5fc0d-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5fc0d-161">JSON representation</span></span>

<span data-ttu-id="5fc0d-162">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5fc0d-162">Here is a JSON representation of the resource</span></span>

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
