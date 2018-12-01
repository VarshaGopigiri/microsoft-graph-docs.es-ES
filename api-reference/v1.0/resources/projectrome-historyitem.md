---
title: tipo de recurso historyItem
description: Representa un elemento de historial para una actividad en una aplicación. Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo. Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad. Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.
ms.openlocfilehash: f413da4280f7b39f0be2a9dafd872ebee041ccc8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031258"
---
# <a name="historyitem-resource-type"></a><span data-ttu-id="bccbb-106">tipo de recurso historyItem</span><span class="sxs-lookup"><span data-stu-id="bccbb-106">historyItem resource type</span></span>

<span data-ttu-id="bccbb-107">Representa un elemento de historial para una [actividad](projectrome-activity.md) en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="bccbb-107">Represents a history item for an [activity](projectrome-activity.md) in an app.</span></span> <span data-ttu-id="bccbb-108">Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bccbb-108">User activities represent a single destination within your app - for example, a TV show, a document, or a current campaign in a video game.</span></span> <span data-ttu-id="bccbb-109">Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad.</span><span class="sxs-lookup"><span data-stu-id="bccbb-109">When a user engages with that activity, the engagement is captured as a history item that indicates the start and end time for that activity.</span></span> <span data-ttu-id="bccbb-110">Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.</span><span class="sxs-lookup"><span data-stu-id="bccbb-110">As the user re-engages with that activity over time, multiple history items are recorded for a single user activity.</span></span>

<span data-ttu-id="bccbb-111">Cuando una aplicación crea una sesión, se debe agregar un objeto **historyItem** para el objeto de **actividad** para reflejar el período de contratación de usuario.</span><span class="sxs-lookup"><span data-stu-id="bccbb-111">When an app creates a session, a **historyItem** object should be added to the **activity** object to reflect the period of user engagement.</span></span> <span data-ttu-id="bccbb-112">Cada vez que volver a contrata a un usuario con una actividad, se agrega un nuevo **historyItem** a la actividad para acumular compromiso de usuario.</span><span class="sxs-lookup"><span data-stu-id="bccbb-112">Each time a user re-engages with an activity, a new **historyItem** is added to the activity to accrue user engagement.</span></span>

## <a name="methods"></a><span data-ttu-id="bccbb-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="bccbb-113">Methods</span></span>

|<span data-ttu-id="bccbb-114">Método</span><span class="sxs-lookup"><span data-stu-id="bccbb-114">Method</span></span> | <span data-ttu-id="bccbb-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bccbb-115">Return Type</span></span> | <span data-ttu-id="bccbb-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bccbb-116">Description</span></span>|
|:------|:------------|:-----------|
|[<span data-ttu-id="bccbb-117">Crear o reemplazar historyItem</span><span class="sxs-lookup"><span data-stu-id="bccbb-117">Create or replace historyItem</span></span>](../api/projectrome-put-historyitem.md) | [<span data-ttu-id="bccbb-118">historyItem</span><span class="sxs-lookup"><span data-stu-id="bccbb-118">historyItem</span></span>](projectrome-historyitem.md) | <span data-ttu-id="bccbb-119">Crea o reemplaza una existente **historyItem** para esa actividad (upsert).</span><span class="sxs-lookup"><span data-stu-id="bccbb-119">Creates or replaces an existing **historyItem** for that activity (upsert).</span></span> <span data-ttu-id="bccbb-120">El identificador debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="bccbb-120">The ID needs to be a GUID.</span></span>|
|[<span data-ttu-id="bccbb-121">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="bccbb-121">Delete a historyItem</span></span>](../api/projectrome-delete-historyitem.md) | <span data-ttu-id="bccbb-122">Sin contenido</span><span class="sxs-lookup"><span data-stu-id="bccbb-122">No Content</span></span> | <span data-ttu-id="bccbb-123">Elimina el especificado **historyItem** para esa actividad.</span><span class="sxs-lookup"><span data-stu-id="bccbb-123">Deletes the specified **historyItem** for that activity.</span></span>|

## <a name="properties"></a><span data-ttu-id="bccbb-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bccbb-124">Properties</span></span>

|<span data-ttu-id="bccbb-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="bccbb-125">Name</span></span> | <span data-ttu-id="bccbb-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="bccbb-126">Type</span></span> | <span data-ttu-id="bccbb-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="bccbb-127">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="bccbb-128">status</span><span class="sxs-lookup"><span data-stu-id="bccbb-128">status</span></span> | <span data-ttu-id="bccbb-129">status</span><span class="sxs-lookup"><span data-stu-id="bccbb-129">status</span></span> | <span data-ttu-id="bccbb-130">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="bccbb-130">Set by the server.</span></span> <span data-ttu-id="bccbb-131">Código de estado que se usa para identificar objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="bccbb-131">A status code used to identify valid objects.</span></span> <span data-ttu-id="bccbb-132">Valores: activo, actualizar, eliminar, pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="bccbb-132">Values: active, updated, deleted, ignored.</span></span>|
|<span data-ttu-id="bccbb-133">userTimezone</span><span class="sxs-lookup"><span data-stu-id="bccbb-133">userTimezone</span></span> | <span data-ttu-id="bccbb-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="bccbb-134">String</span></span> | <span data-ttu-id="bccbb-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bccbb-135">Optional.</span></span> <span data-ttu-id="bccbb-136">La zona horaria en la que se encuentra el dispositivo del usuario utilizado para generar la actividad en tiempo de creación de la actividad.</span><span class="sxs-lookup"><span data-stu-id="bccbb-136">The timezone in which the user's device used to generate the activity was located at activity creation time.</span></span> <span data-ttu-id="bccbb-137">Valores proporcionados como Olson identificadores con el fin de admitir la representación de multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="bccbb-137">Values supplied as Olson IDs in order to support cross-platform representation.</span></span>|
|<span data-ttu-id="bccbb-138">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bccbb-138">createdDateTime</span></span> | <span data-ttu-id="bccbb-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bccbb-139">DateTimeOffset</span></span> | <span data-ttu-id="bccbb-140">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="bccbb-140">Set by the server.</span></span> <span data-ttu-id="bccbb-141">Fecha y hora en UTC cuando se creó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="bccbb-141">DateTime in UTC when the object was created on the server.</span></span>|
|<span data-ttu-id="bccbb-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bccbb-142">lastModifiedDateTime</span></span> | <span data-ttu-id="bccbb-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bccbb-143">DateTimeOffset</span></span> | <span data-ttu-id="bccbb-144">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="bccbb-144">Set by the server.</span></span> <span data-ttu-id="bccbb-145">Fecha y hora en UTC cuando se modificó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="bccbb-145">DateTime in UTC when the object was modified on the server.</span></span>|
|<span data-ttu-id="bccbb-146">id</span><span class="sxs-lookup"><span data-stu-id="bccbb-146">id</span></span> | <span data-ttu-id="bccbb-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="bccbb-147">String</span></span> | <span data-ttu-id="bccbb-148">Necesario.</span><span class="sxs-lookup"><span data-stu-id="bccbb-148">Required.</span></span> <span data-ttu-id="bccbb-149">GUID del conjunto de clientes para el objeto **historyItem** .</span><span class="sxs-lookup"><span data-stu-id="bccbb-149">Client-set GUID for the **historyItem** object.</span></span>|
|<span data-ttu-id="bccbb-150">startedDateTime</span><span class="sxs-lookup"><span data-stu-id="bccbb-150">startedDateTime</span></span> | <span data-ttu-id="bccbb-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bccbb-151">DateTimeOffset</span></span> | <span data-ttu-id="bccbb-152">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bccbb-152">Required.</span></span> <span data-ttu-id="bccbb-153">DateTime de UTC cuando se inició la **historyItem** (sesión de actividad).</span><span class="sxs-lookup"><span data-stu-id="bccbb-153">UTC DateTime when the **historyItem** (activity session) was started.</span></span> <span data-ttu-id="bccbb-154">Requerida para el historial de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="bccbb-154">Required for timeline history.</span></span>|
|<span data-ttu-id="bccbb-155">lastActiveDateTime</span><span class="sxs-lookup"><span data-stu-id="bccbb-155">lastActiveDateTime</span></span> | <span data-ttu-id="bccbb-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bccbb-156">DateTimeOffset</span></span> | <span data-ttu-id="bccbb-157">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bccbb-157">Optional.</span></span> <span data-ttu-id="bccbb-158">DateTime de UTC cuando la **historyItem** (sesión actividad) se entiende por última vez como estado activo o terminado - si es nulo, **historyItem** debe estar en curso.</span><span class="sxs-lookup"><span data-stu-id="bccbb-158">UTC DateTime when the **historyItem** (activity session) was last understood as active or finished - if null, **historyItem** status should be Ongoing.</span></span>|
|<span data-ttu-id="bccbb-159">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="bccbb-159">expirationDateTime</span></span> | <span data-ttu-id="bccbb-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bccbb-160">DateTimeOffset</span></span> | <span data-ttu-id="bccbb-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bccbb-161">Optional.</span></span> <span data-ttu-id="bccbb-162">DateTime de UTC cuando el **historyItem** experimentará eliminar disco duro.</span><span class="sxs-lookup"><span data-stu-id="bccbb-162">UTC DateTime when the **historyItem** will undergo hard-delete.</span></span> <span data-ttu-id="bccbb-163">Se puede establecer por el cliente.</span><span class="sxs-lookup"><span data-stu-id="bccbb-163">Can be set by the client.</span></span>|
|<span data-ttu-id="bccbb-164">activeDurationSeconds</span><span class="sxs-lookup"><span data-stu-id="bccbb-164">activeDurationSeconds</span></span> | <span data-ttu-id="bccbb-165">int</span><span class="sxs-lookup"><span data-stu-id="bccbb-165">int</span></span> | <span data-ttu-id="bccbb-166">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bccbb-166">Optional.</span></span> <span data-ttu-id="bccbb-167">La duración de contratación de usuario activo.</span><span class="sxs-lookup"><span data-stu-id="bccbb-167">The duration of active user engagement.</span></span> <span data-ttu-id="bccbb-168">Si no se proporciona, esto se calcula a partir de la **startedDateTime** y **lastActiveDateTime**.</span><span class="sxs-lookup"><span data-stu-id="bccbb-168">if not supplied, this is calculated from the **startedDateTime** and **lastActiveDateTime**.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bccbb-169">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bccbb-169">Relationships</span></span>

|<span data-ttu-id="bccbb-170">Relación</span><span class="sxs-lookup"><span data-stu-id="bccbb-170">Relationship</span></span> | <span data-ttu-id="bccbb-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="bccbb-171">Type</span></span> | <span data-ttu-id="bccbb-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="bccbb-172">Description</span></span>|
|:------------|:-----|:-----------|
|<span data-ttu-id="bccbb-173">actividad</span><span class="sxs-lookup"><span data-stu-id="bccbb-173">activity</span></span>| [<span data-ttu-id="bccbb-174">userActivity</span><span class="sxs-lookup"><span data-stu-id="bccbb-174">userActivity</span></span>](../resources/projectrome-activity.md) | <span data-ttu-id="bccbb-175">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bccbb-175">Optional.</span></span> <span data-ttu-id="bccbb-176">NavigationProperty/contención; propiedad de navegación a la actividad asociada.</span><span class="sxs-lookup"><span data-stu-id="bccbb-176">NavigationProperty/Containment; navigation property to the associated activity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bccbb-177">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bccbb-177">JSON representation</span></span>

<span data-ttu-id="bccbb-178">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bccbb-178">Here is a JSON representation of the resource.</span></span>

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
