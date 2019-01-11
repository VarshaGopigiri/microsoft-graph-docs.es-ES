---
title: tipo de recurso historyItem
description: Representa un elemento de historial para una actividad en una aplicación. Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo. Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad. Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.
localization_priority: Normal
ms.openlocfilehash: 7eb6d72b55530d1938c9c092dd5b80f54929a3e8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825777"
---
# <a name="historyitem-resource-type"></a><span data-ttu-id="3b948-106">tipo de recurso historyItem</span><span class="sxs-lookup"><span data-stu-id="3b948-106">historyItem resource type</span></span>

> <span data-ttu-id="3b948-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b948-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b948-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b948-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b948-109">Representa un elemento de historial para una [actividad](projectrome-activity.md) en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b948-109">Represents a history item for an [activity](projectrome-activity.md) in an app.</span></span> <span data-ttu-id="3b948-110">Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b948-110">User activities represent a single destination within your app - for example, a TV show, a document, or a current campaign in a video game.</span></span> <span data-ttu-id="3b948-111">Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad.</span><span class="sxs-lookup"><span data-stu-id="3b948-111">When a user engages with that activity, the engagement is captured as a history item that indicates the start and end time for that activity.</span></span> <span data-ttu-id="3b948-112">Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.</span><span class="sxs-lookup"><span data-stu-id="3b948-112">As the user re-engages with that activity over time, multiple history items are recorded for a single user activity.</span></span>

<span data-ttu-id="3b948-113">Cuando una aplicación crea una sesión, se debe agregar un objeto **historyItem** para el objeto de **actividad** para reflejar el período de contratación de usuario.</span><span class="sxs-lookup"><span data-stu-id="3b948-113">When an app creates a session, a **historyItem** object should be added to the **activity** object to reflect the period of user engagement.</span></span> <span data-ttu-id="3b948-114">Cada vez que volver a contrata a un usuario con una actividad, se agrega un nuevo **historyItem** a la actividad para acumular compromiso de usuario.</span><span class="sxs-lookup"><span data-stu-id="3b948-114">Each time a user re-engages with an activity, a new **historyItem** is added to the activity to accrue user engagement.</span></span>

## <a name="methods"></a><span data-ttu-id="3b948-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b948-115">Methods</span></span>

|<span data-ttu-id="3b948-116">Método</span><span class="sxs-lookup"><span data-stu-id="3b948-116">Method</span></span> | <span data-ttu-id="3b948-117">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b948-117">Return Type</span></span> | <span data-ttu-id="3b948-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b948-118">Description</span></span>|
|:------|:------------|:-----------|
|[<span data-ttu-id="3b948-119">Crear o reemplazar historyItem</span><span class="sxs-lookup"><span data-stu-id="3b948-119">Create or replace historyItem</span></span>](../api/projectrome-put-historyitem.md) | [<span data-ttu-id="3b948-120">historyItem</span><span class="sxs-lookup"><span data-stu-id="3b948-120">historyItem</span></span>](projectrome-historyitem.md) | <span data-ttu-id="3b948-121">Crea o reemplaza una existente **historyItem** para esa actividad (upsert).</span><span class="sxs-lookup"><span data-stu-id="3b948-121">Creates or replaces an existing **historyItem** for that activity (upsert).</span></span> <span data-ttu-id="3b948-122">El identificador debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="3b948-122">The ID needs to be a GUID.</span></span>|
|[<span data-ttu-id="3b948-123">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="3b948-123">Delete a historyItem</span></span>](../api/projectrome-delete-historyitem.md) | <span data-ttu-id="3b948-124">Sin contenido</span><span class="sxs-lookup"><span data-stu-id="3b948-124">No Content</span></span> | <span data-ttu-id="3b948-125">Elimina el especificado **historyItem** para esa actividad.</span><span class="sxs-lookup"><span data-stu-id="3b948-125">Deletes the specified **historyItem** for that activity.</span></span>|

## <a name="properties"></a><span data-ttu-id="3b948-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b948-126">Properties</span></span>

|<span data-ttu-id="3b948-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="3b948-127">Name</span></span> | <span data-ttu-id="3b948-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b948-128">Type</span></span> | <span data-ttu-id="3b948-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b948-129">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="3b948-130">status</span><span class="sxs-lookup"><span data-stu-id="3b948-130">status</span></span> | <span data-ttu-id="3b948-131">EnumType</span><span class="sxs-lookup"><span data-stu-id="3b948-131">EnumType</span></span> | <span data-ttu-id="3b948-132">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="3b948-132">Set by the server.</span></span> <span data-ttu-id="3b948-133">Código de estado que se usa para identificar objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="3b948-133">A status code used to identify valid objects.</span></span> <span data-ttu-id="3b948-134">Valores: activo, actualizar, eliminar, pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="3b948-134">Values: active, updated, deleted, ignored.</span></span>|
|<span data-ttu-id="3b948-135">userTimezone</span><span class="sxs-lookup"><span data-stu-id="3b948-135">userTimezone</span></span> | <span data-ttu-id="3b948-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="3b948-136">String</span></span> | <span data-ttu-id="3b948-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b948-137">Optional.</span></span> <span data-ttu-id="3b948-138">La zona horaria en la que se encuentra el dispositivo del usuario utilizado para generar la actividad en tiempo de creación de la actividad.</span><span class="sxs-lookup"><span data-stu-id="3b948-138">The timezone in which the user's device used to generate the activity was located at activity creation time.</span></span> <span data-ttu-id="3b948-139">Valores proporcionados como Olson identificadores con el fin de admitir la representación de multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="3b948-139">Values supplied as Olson IDs in order to support cross-platform representation.</span></span>|
|<span data-ttu-id="3b948-140">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3b948-140">createdDateTime</span></span> | <span data-ttu-id="3b948-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3b948-141">DateTimeOffset</span></span> | <span data-ttu-id="3b948-142">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="3b948-142">Set by the server.</span></span> <span data-ttu-id="3b948-143">Fecha y hora en UTC cuando se creó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3b948-143">DateTime in UTC when the object was created on the server.</span></span>|
|<span data-ttu-id="3b948-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3b948-144">lastModifiedDateTime</span></span> | <span data-ttu-id="3b948-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3b948-145">DateTimeOffset</span></span> | <span data-ttu-id="3b948-146">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="3b948-146">Set by the server.</span></span> <span data-ttu-id="3b948-147">Fecha y hora en UTC cuando se modificó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3b948-147">DateTime in UTC when the object was modified on the server.</span></span>|
|<span data-ttu-id="3b948-148">id</span><span class="sxs-lookup"><span data-stu-id="3b948-148">id</span></span> | <span data-ttu-id="3b948-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="3b948-149">String</span></span> | <span data-ttu-id="3b948-150">Necesario.</span><span class="sxs-lookup"><span data-stu-id="3b948-150">Required.</span></span> <span data-ttu-id="3b948-151">GUID del conjunto de clientes para el objeto **historyItem** .</span><span class="sxs-lookup"><span data-stu-id="3b948-151">Client-set GUID for the **historyItem** object.</span></span>|
|<span data-ttu-id="3b948-152">startedDateTime</span><span class="sxs-lookup"><span data-stu-id="3b948-152">startedDateTime</span></span> | <span data-ttu-id="3b948-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3b948-153">DateTimeOffset</span></span> | <span data-ttu-id="3b948-154">Necesario.</span><span class="sxs-lookup"><span data-stu-id="3b948-154">Required.</span></span> <span data-ttu-id="3b948-155">DateTime de UTC cuando se inició la **historyItem** (sesión de actividad).</span><span class="sxs-lookup"><span data-stu-id="3b948-155">UTC DateTime when the **historyItem** (activity session) was started.</span></span> <span data-ttu-id="3b948-156">Requerida para el historial de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3b948-156">Required for timeline history.</span></span>|
|<span data-ttu-id="3b948-157">lastActiveDateTime</span><span class="sxs-lookup"><span data-stu-id="3b948-157">lastActiveDateTime</span></span> | <span data-ttu-id="3b948-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3b948-158">DateTimeOffset</span></span> | <span data-ttu-id="3b948-159">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b948-159">Optional.</span></span> <span data-ttu-id="3b948-160">DateTime de UTC cuando la **historyItem** (sesión actividad) se entiende por última vez como estado activo o terminado - si es nulo, **historyItem** debe estar en curso.</span><span class="sxs-lookup"><span data-stu-id="3b948-160">UTC DateTime when the **historyItem** (activity session) was last understood as active or finished - if null, **historyItem** status should be Ongoing.</span></span>|
|<span data-ttu-id="3b948-161">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="3b948-161">expirationDateTime</span></span> | <span data-ttu-id="3b948-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3b948-162">DateTimeOffset</span></span> | <span data-ttu-id="3b948-163">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b948-163">Optional.</span></span> <span data-ttu-id="3b948-164">DateTime de UTC cuando el **historyItem** experimentará eliminar disco duro.</span><span class="sxs-lookup"><span data-stu-id="3b948-164">UTC DateTime when the **historyItem** will undergo hard-delete.</span></span> <span data-ttu-id="3b948-165">Se puede establecer por el cliente.</span><span class="sxs-lookup"><span data-stu-id="3b948-165">Can be set by the client.</span></span>|
|<span data-ttu-id="3b948-166">activeDurationSeconds</span><span class="sxs-lookup"><span data-stu-id="3b948-166">activeDurationSeconds</span></span> | <span data-ttu-id="3b948-167">int</span><span class="sxs-lookup"><span data-stu-id="3b948-167">int</span></span> | <span data-ttu-id="3b948-168">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b948-168">Optional.</span></span> <span data-ttu-id="3b948-169">La duración de contratación de usuario activo.</span><span class="sxs-lookup"><span data-stu-id="3b948-169">The duration of active user engagement.</span></span> <span data-ttu-id="3b948-170">Si no se proporciona, esto se calcula a partir de la **startedDateTime** y **lastActiveDateTime**.</span><span class="sxs-lookup"><span data-stu-id="3b948-170">if not supplied, this is calculated from the **startedDateTime** and **lastActiveDateTime**.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3b948-171">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3b948-171">Relationships</span></span>

|<span data-ttu-id="3b948-172">Relación</span><span class="sxs-lookup"><span data-stu-id="3b948-172">Relationship</span></span> | <span data-ttu-id="3b948-173">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b948-173">Type</span></span> | <span data-ttu-id="3b948-174">Description</span><span class="sxs-lookup"><span data-stu-id="3b948-174">Description</span></span>|
|:------------|:-----|:-----------|
|<span data-ttu-id="3b948-175">actividad</span><span class="sxs-lookup"><span data-stu-id="3b948-175">activity</span></span>| [<span data-ttu-id="3b948-176">activity</span><span class="sxs-lookup"><span data-stu-id="3b948-176">activity</span></span>](../resources/projectrome-activity.md) | <span data-ttu-id="3b948-177">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3b948-177">Optional.</span></span> <span data-ttu-id="3b948-178">NavigationProperty/contención; propiedad de navegación a la actividad asociada.</span><span class="sxs-lookup"><span data-stu-id="3b948-178">NavigationProperty/Containment; navigation property to the associated activity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3b948-179">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3b948-179">JSON representation</span></span>

<span data-ttu-id="3b948-180">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3b948-180">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "userTimezone",
    "lastActiveDateTime",
    "activeDurationSeconds"
  ],
  "@odata.type": "microsoft.graph.historyItem"
}-->

```json
{
    "status": "String (EnumType)",
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
