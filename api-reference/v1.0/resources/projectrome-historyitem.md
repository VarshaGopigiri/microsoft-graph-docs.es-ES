---
title: tipo de recurso historyItem
description: Representa un elemento de historial para una actividad en una aplicación. Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo. Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad. Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: 029c17e09348977752f3ce5632740b2bdac64e46
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977440"
---
# <a name="historyitem-resource-type"></a><span data-ttu-id="494ff-106">tipo de recurso historyItem</span><span class="sxs-lookup"><span data-stu-id="494ff-106">historyItem resource type</span></span>

<span data-ttu-id="494ff-107">Representa un elemento de historial para una [actividad](projectrome-activity.md) en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="494ff-107">Represents a history item for an [activity](projectrome-activity.md) in an app.</span></span> <span data-ttu-id="494ff-108">Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="494ff-108">User activities represent a single destination within your app - for example, a TV show, a document, or a current campaign in a video game.</span></span> <span data-ttu-id="494ff-109">Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad.</span><span class="sxs-lookup"><span data-stu-id="494ff-109">When a user engages with that activity, the engagement is captured as a history item that indicates the start and end time for that activity.</span></span> <span data-ttu-id="494ff-110">Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.</span><span class="sxs-lookup"><span data-stu-id="494ff-110">As the user re-engages with that activity over time, multiple history items are recorded for a single user activity.</span></span>

<span data-ttu-id="494ff-111">Cuando una aplicación crea una sesión, se debe agregar un objeto **historyItem** para el objeto de **actividad** para reflejar el período de contratación de usuario.</span><span class="sxs-lookup"><span data-stu-id="494ff-111">When an app creates a session, a **historyItem** object should be added to the **activity** object to reflect the period of user engagement.</span></span> <span data-ttu-id="494ff-112">Cada vez que volver a contrata a un usuario con una actividad, se agrega un nuevo **historyItem** a la actividad para acumular compromiso de usuario.</span><span class="sxs-lookup"><span data-stu-id="494ff-112">Each time a user re-engages with an activity, a new **historyItem** is added to the activity to accrue user engagement.</span></span>

## <a name="methods"></a><span data-ttu-id="494ff-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="494ff-113">Methods</span></span>

|<span data-ttu-id="494ff-114">Método</span><span class="sxs-lookup"><span data-stu-id="494ff-114">Method</span></span> | <span data-ttu-id="494ff-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="494ff-115">Return Type</span></span> | <span data-ttu-id="494ff-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="494ff-116">Description</span></span>|
|:------|:------------|:-----------|
|[<span data-ttu-id="494ff-117">Crear o reemplazar historyItem</span><span class="sxs-lookup"><span data-stu-id="494ff-117">Create or replace historyItem</span></span>](../api/projectrome-put-historyitem.md) | [<span data-ttu-id="494ff-118">historyItem</span><span class="sxs-lookup"><span data-stu-id="494ff-118">historyItem</span></span>](projectrome-historyitem.md) | <span data-ttu-id="494ff-119">Crea o reemplaza una existente **historyItem** para esa actividad (upsert).</span><span class="sxs-lookup"><span data-stu-id="494ff-119">Creates or replaces an existing **historyItem** for that activity (upsert).</span></span> <span data-ttu-id="494ff-120">El identificador debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="494ff-120">The ID needs to be a GUID.</span></span>|
|[<span data-ttu-id="494ff-121">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="494ff-121">Delete a historyItem</span></span>](../api/projectrome-delete-historyitem.md) | <span data-ttu-id="494ff-122">Sin contenido</span><span class="sxs-lookup"><span data-stu-id="494ff-122">No Content</span></span> | <span data-ttu-id="494ff-123">Elimina el especificado **historyItem** para esa actividad.</span><span class="sxs-lookup"><span data-stu-id="494ff-123">Deletes the specified **historyItem** for that activity.</span></span>|

## <a name="properties"></a><span data-ttu-id="494ff-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="494ff-124">Properties</span></span>

|<span data-ttu-id="494ff-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="494ff-125">Name</span></span> | <span data-ttu-id="494ff-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="494ff-126">Type</span></span> | <span data-ttu-id="494ff-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="494ff-127">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="494ff-128">status</span><span class="sxs-lookup"><span data-stu-id="494ff-128">status</span></span> | <span data-ttu-id="494ff-129">status</span><span class="sxs-lookup"><span data-stu-id="494ff-129">status</span></span> | <span data-ttu-id="494ff-130">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="494ff-130">Set by the server.</span></span> <span data-ttu-id="494ff-131">Código de estado que se usa para identificar objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="494ff-131">A status code used to identify valid objects.</span></span> <span data-ttu-id="494ff-132">Valores: activo, actualizar, eliminar, pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="494ff-132">Values: active, updated, deleted, ignored.</span></span>|
|<span data-ttu-id="494ff-133">userTimezone</span><span class="sxs-lookup"><span data-stu-id="494ff-133">userTimezone</span></span> | <span data-ttu-id="494ff-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="494ff-134">String</span></span> | <span data-ttu-id="494ff-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494ff-135">Optional.</span></span> <span data-ttu-id="494ff-136">La zona horaria en la que se encuentra el dispositivo del usuario utilizado para generar la actividad en tiempo de creación de la actividad.</span><span class="sxs-lookup"><span data-stu-id="494ff-136">The timezone in which the user's device used to generate the activity was located at activity creation time.</span></span> <span data-ttu-id="494ff-137">Valores proporcionados como Olson identificadores con el fin de admitir la representación de multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="494ff-137">Values supplied as Olson IDs in order to support cross-platform representation.</span></span>|
|<span data-ttu-id="494ff-138">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="494ff-138">createdDateTime</span></span> | <span data-ttu-id="494ff-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="494ff-139">DateTimeOffset</span></span> | <span data-ttu-id="494ff-140">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="494ff-140">Set by the server.</span></span> <span data-ttu-id="494ff-141">Fecha y hora en UTC cuando se creó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="494ff-141">DateTime in UTC when the object was created on the server.</span></span>|
|<span data-ttu-id="494ff-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="494ff-142">lastModifiedDateTime</span></span> | <span data-ttu-id="494ff-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="494ff-143">DateTimeOffset</span></span> | <span data-ttu-id="494ff-144">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="494ff-144">Set by the server.</span></span> <span data-ttu-id="494ff-145">Fecha y hora en UTC cuando se modificó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="494ff-145">DateTime in UTC when the object was modified on the server.</span></span>|
|<span data-ttu-id="494ff-146">id</span><span class="sxs-lookup"><span data-stu-id="494ff-146">id</span></span> | <span data-ttu-id="494ff-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="494ff-147">String</span></span> | <span data-ttu-id="494ff-148">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="494ff-148">Required.</span></span> <span data-ttu-id="494ff-149">GUID del conjunto de clientes para el objeto **historyItem** .</span><span class="sxs-lookup"><span data-stu-id="494ff-149">Client-set GUID for the **historyItem** object.</span></span>|
|<span data-ttu-id="494ff-150">startedDateTime</span><span class="sxs-lookup"><span data-stu-id="494ff-150">startedDateTime</span></span> | <span data-ttu-id="494ff-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="494ff-151">DateTimeOffset</span></span> | <span data-ttu-id="494ff-152">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="494ff-152">Required.</span></span> <span data-ttu-id="494ff-153">DateTime de UTC cuando se inició la **historyItem** (sesión de actividad).</span><span class="sxs-lookup"><span data-stu-id="494ff-153">UTC DateTime when the **historyItem** (activity session) was started.</span></span> <span data-ttu-id="494ff-154">Requerida para el historial de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="494ff-154">Required for timeline history.</span></span>|
|<span data-ttu-id="494ff-155">lastActiveDateTime</span><span class="sxs-lookup"><span data-stu-id="494ff-155">lastActiveDateTime</span></span> | <span data-ttu-id="494ff-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="494ff-156">DateTimeOffset</span></span> | <span data-ttu-id="494ff-157">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494ff-157">Optional.</span></span> <span data-ttu-id="494ff-158">DateTime de UTC cuando la **historyItem** (sesión actividad) se entiende por última vez como estado activo o terminado - si es nulo, **historyItem** debe estar en curso.</span><span class="sxs-lookup"><span data-stu-id="494ff-158">UTC DateTime when the **historyItem** (activity session) was last understood as active or finished - if null, **historyItem** status should be Ongoing.</span></span>|
|<span data-ttu-id="494ff-159">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="494ff-159">expirationDateTime</span></span> | <span data-ttu-id="494ff-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="494ff-160">DateTimeOffset</span></span> | <span data-ttu-id="494ff-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494ff-161">Optional.</span></span> <span data-ttu-id="494ff-162">DateTime de UTC cuando el **historyItem** experimentará eliminar disco duro.</span><span class="sxs-lookup"><span data-stu-id="494ff-162">UTC DateTime when the **historyItem** will undergo hard-delete.</span></span> <span data-ttu-id="494ff-163">Se puede establecer por el cliente.</span><span class="sxs-lookup"><span data-stu-id="494ff-163">Can be set by the client.</span></span>|
|<span data-ttu-id="494ff-164">activeDurationSeconds</span><span class="sxs-lookup"><span data-stu-id="494ff-164">activeDurationSeconds</span></span> | <span data-ttu-id="494ff-165">int</span><span class="sxs-lookup"><span data-stu-id="494ff-165">int</span></span> | <span data-ttu-id="494ff-166">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494ff-166">Optional.</span></span> <span data-ttu-id="494ff-167">La duración de contratación de usuario activo.</span><span class="sxs-lookup"><span data-stu-id="494ff-167">The duration of active user engagement.</span></span> <span data-ttu-id="494ff-168">Si no se proporciona, esto se calcula a partir de la **startedDateTime** y **lastActiveDateTime**.</span><span class="sxs-lookup"><span data-stu-id="494ff-168">if not supplied, this is calculated from the **startedDateTime** and **lastActiveDateTime**.</span></span>|

## <a name="relationships"></a><span data-ttu-id="494ff-169">Relaciones</span><span class="sxs-lookup"><span data-stu-id="494ff-169">Relationships</span></span>

|<span data-ttu-id="494ff-170">Relación</span><span class="sxs-lookup"><span data-stu-id="494ff-170">Relationship</span></span> | <span data-ttu-id="494ff-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="494ff-171">Type</span></span> | <span data-ttu-id="494ff-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="494ff-172">Description</span></span>|
|:------------|:-----|:-----------|
|<span data-ttu-id="494ff-173">actividad</span><span class="sxs-lookup"><span data-stu-id="494ff-173">activity</span></span>| [<span data-ttu-id="494ff-174">userActivity</span><span class="sxs-lookup"><span data-stu-id="494ff-174">userActivity</span></span>](../resources/projectrome-activity.md) | <span data-ttu-id="494ff-175">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494ff-175">Optional.</span></span> <span data-ttu-id="494ff-176">NavigationProperty/contención; propiedad de navegación a la actividad asociada.</span><span class="sxs-lookup"><span data-stu-id="494ff-176">NavigationProperty/Containment; navigation property to the associated activity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="494ff-177">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="494ff-177">JSON representation</span></span>

<span data-ttu-id="494ff-178">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="494ff-178">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "userTimezone",
    "lastActiveDateTime",
    "activeDurationSeconds"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.activityHistoryItem",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
    "status": "active | updated | deleted | ignored",
    "createdDateTime": "DateTimeOffset",
    "lastModifiedDateTime": "DateTimeOffset",
    "id": "String",
    "expirationDateTime": "DateTimeOffset",
    "startedDateTime": "DateTimeOffset",
    "userTimezone": "String",
    "lastActiveDateTime": "DateTimeOffset",
    "activeDurationSeconds":"int"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "historyitem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
