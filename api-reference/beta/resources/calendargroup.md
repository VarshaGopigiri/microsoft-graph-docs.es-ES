---
title: Tipo de recurso calendarGroup
description: Un grupo de calendarios de usuario.
author: angelgolfer-ms
ms.openlocfilehash: fda8a3006631f45d49e83363d61f7b0363675ed1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334373"
---
# <a name="calendargroup-resource-type"></a><span data-ttu-id="a30a6-103">Tipo de recurso calendarGroup</span><span class="sxs-lookup"><span data-stu-id="a30a6-103">calendarGroup resource type</span></span>

> <span data-ttu-id="a30a6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a30a6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a30a6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a30a6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a30a6-106">Un grupo de calendarios de usuario.</span><span class="sxs-lookup"><span data-stu-id="a30a6-106">A group of user calendars.</span></span>

## <a name="methods"></a><span data-ttu-id="a30a6-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a30a6-107">Methods</span></span>

| <span data-ttu-id="a30a6-108">Método</span><span class="sxs-lookup"><span data-stu-id="a30a6-108">Method</span></span>                                                      | <span data-ttu-id="a30a6-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a30a6-109">Return Type</span></span>                        | <span data-ttu-id="a30a6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a30a6-110">Description</span></span>                                                   |
| :---------------------------------------------------------- | :--------------------------------- | :------------------------------------------------------------ |
| [<span data-ttu-id="a30a6-111">List calendar groups</span><span class="sxs-lookup"><span data-stu-id="a30a6-111">List calendar groups</span></span>](../api/user-list-calendargroups.md)  | <span data-ttu-id="a30a6-112">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="a30a6-112">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="a30a6-113">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="a30a6-113">Get the user's calendar groups.</span></span>                               |
| [<span data-ttu-id="a30a6-114">Create calendar group</span><span class="sxs-lookup"><span data-stu-id="a30a6-114">Create calendar group</span></span>](../api/user-post-calendargroups.md) | [<span data-ttu-id="a30a6-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="a30a6-115">Calendar</span></span>](calendar.md)            | <span data-ttu-id="a30a6-116">Crea un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a30a6-116">Create a new calendar group.</span></span>                                  |
| [<span data-ttu-id="a30a6-117">Get calendar group</span><span class="sxs-lookup"><span data-stu-id="a30a6-117">Get calendar group</span></span>](../api/calendargroup-get.md)           | [<span data-ttu-id="a30a6-118">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="a30a6-118">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="a30a6-119">Lee las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a30a6-119">Read properties and relationships of a calendar group object.</span></span> |
| [<span data-ttu-id="a30a6-120">Update</span><span class="sxs-lookup"><span data-stu-id="a30a6-120">Update</span></span>](../api/calendargroup-update.md)                    | [<span data-ttu-id="a30a6-121">calendarGroup</span><span class="sxs-lookup"><span data-stu-id="a30a6-121">calendarGroup</span></span>](calendargroup.md)  | <span data-ttu-id="a30a6-122">Actualiza el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="a30a6-122">Update calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="a30a6-123">Delete</span><span class="sxs-lookup"><span data-stu-id="a30a6-123">Delete</span></span>](../api/calendargroup-delete.md)                    | <span data-ttu-id="a30a6-124">None</span><span class="sxs-lookup"><span data-stu-id="a30a6-124">None</span></span>                               | <span data-ttu-id="a30a6-125">Elimina el objeto calendarGroup.</span><span class="sxs-lookup"><span data-stu-id="a30a6-125">Delete calendarGroup object.</span></span>                                  |
| [<span data-ttu-id="a30a6-126">List calendars</span><span class="sxs-lookup"><span data-stu-id="a30a6-126">List calendars</span></span>](../api/calendargroup-list-calendars.md)    | <span data-ttu-id="a30a6-127">Colección [Calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="a30a6-127">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="a30a6-128">Muestra la lista de calendarios de un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a30a6-128">List calendars in a calendar group.</span></span>                           |
| [<span data-ttu-id="a30a6-129">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="a30a6-129">Create Calendar</span></span>](../api/calendargroup-post-calendars.md)   | [<span data-ttu-id="a30a6-130">Calendar</span><span class="sxs-lookup"><span data-stu-id="a30a6-130">Calendar</span></span>](calendar.md)            | <span data-ttu-id="a30a6-131">Crea un calendario en un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a30a6-131">Create a new Calendar in a calendar group.</span></span>                    |

## <a name="properties"></a><span data-ttu-id="a30a6-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a30a6-132">Properties</span></span>

| <span data-ttu-id="a30a6-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a30a6-133">Property</span></span>  | <span data-ttu-id="a30a6-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="a30a6-134">Type</span></span>   | <span data-ttu-id="a30a6-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="a30a6-135">Description</span></span>                                                                                                                                                                                               |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="a30a6-136">name</span><span class="sxs-lookup"><span data-stu-id="a30a6-136">name</span></span>      | <span data-ttu-id="a30a6-137">String</span><span class="sxs-lookup"><span data-stu-id="a30a6-137">String</span></span> | <span data-ttu-id="a30a6-138">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="a30a6-138">The group name.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="a30a6-139">changeKey</span><span class="sxs-lookup"><span data-stu-id="a30a6-139">changeKey</span></span> | <span data-ttu-id="a30a6-140">String</span><span class="sxs-lookup"><span data-stu-id="a30a6-140">String</span></span> | <span data-ttu-id="a30a6-p102">Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a30a6-p102">Identifies the version of the calendar group. Every time the calendar group is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.</span></span> |
| <span data-ttu-id="a30a6-145">classId</span><span class="sxs-lookup"><span data-stu-id="a30a6-145">classId</span></span>   | <span data-ttu-id="a30a6-146">Guid</span><span class="sxs-lookup"><span data-stu-id="a30a6-146">Guid</span></span>   | <span data-ttu-id="a30a6-p103">Identificador de la clase. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a30a6-p103">The class identifier. Read-only.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a30a6-149">id</span><span class="sxs-lookup"><span data-stu-id="a30a6-149">id</span></span>        | <span data-ttu-id="a30a6-150">String</span><span class="sxs-lookup"><span data-stu-id="a30a6-150">String</span></span> | <span data-ttu-id="a30a6-p104">Identificador único del grupo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a30a6-p104">The group's unique identifier. Read-only.</span></span>                                                                                                                                                                 |

## <a name="relationships"></a><span data-ttu-id="a30a6-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a30a6-153">Relationships</span></span>

| <span data-ttu-id="a30a6-154">Relación</span><span class="sxs-lookup"><span data-stu-id="a30a6-154">Relationship</span></span> | <span data-ttu-id="a30a6-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="a30a6-155">Type</span></span>                               | <span data-ttu-id="a30a6-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="a30a6-156">Description</span></span>                                                                    |
| :----------- | :--------------------------------- | :----------------------------------------------------------------------------- |
| <span data-ttu-id="a30a6-157">calendars</span><span class="sxs-lookup"><span data-stu-id="a30a6-157">calendars</span></span>    | <span data-ttu-id="a30a6-158">Colección [calendar](calendar.md)</span><span class="sxs-lookup"><span data-stu-id="a30a6-158">[Calendar](calendar.md) collection</span></span> | <span data-ttu-id="a30a6-p105">Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="a30a6-p105">The calendars in the calendar group. Navigation property. Read-only. Nullable.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a30a6-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a30a6-163">JSON representation</span></span>

<span data-ttu-id="a30a6-164">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a30a6-164">Here is a JSON representation of the resource</span></span>

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
