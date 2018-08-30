# <a name="historyitem-resource-type"></a><span data-ttu-id="9924c-101">tipo de recurso historyItem</span><span class="sxs-lookup"><span data-stu-id="9924c-101">historyItem resource type</span></span>

<span data-ttu-id="9924c-102">Representa un elemento de historial para una [actividad](projectrome_activity.md) en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9924c-102">Represents a history item for an [activity](projectrome_activity.md) in an app.</span></span> <span data-ttu-id="9924c-103">Las actividades de usuario representan un destino único dentro de la aplicación, por ejemplo, un programa de TV, un documento o una campaña actual de un videojuego.</span><span class="sxs-lookup"><span data-stu-id="9924c-103">User activities represent a single destination within your app - for example, a TV show, a document, or a current campaign in a video game.</span></span> <span data-ttu-id="9924c-104">Cuando un usuario interactúa con dicha actividad, la interacción se captura como un elemento de historial que indica la hora de inicio y final de esa actividad.</span><span class="sxs-lookup"><span data-stu-id="9924c-104">When a user engages with that activity, the engagement is captured as a history item that indicates the start and end time for that activity.</span></span> <span data-ttu-id="9924c-105">Cuando el usuario vuelve a interactuar con esa actividad a lo largo del tiempo, se registran varios elementos de historial para una única actividad de usuario.</span><span class="sxs-lookup"><span data-stu-id="9924c-105">As the user re-engages with that activity over time, multiple history items are recorded for a single user activity.</span></span>

<span data-ttu-id="9924c-106">Cuando una aplicación crea una sesión, se debe agregar un objeto **historyItem** al objeto **activity** para reflejar el período de interactuación de usuario.</span><span class="sxs-lookup"><span data-stu-id="9924c-106">When an app creates a session, a **historyItem** object should be added to the **activity** object to reflect the period of user engagement.</span></span> <span data-ttu-id="9924c-107">Cada vez que un usuario vuelve a intercatuar con una actividad, se agrega un nuevo **historyItem** a la actividad para acumular interactuaciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="9924c-107">Each time a user reengages with an activity, a new history item is added to the activity to accrue user engagement.</span></span>

## <a name="methods"></a><span data-ttu-id="9924c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="9924c-108">Methods</span></span>

|<span data-ttu-id="9924c-109">Método</span><span class="sxs-lookup"><span data-stu-id="9924c-109">Method</span></span> | <span data-ttu-id="9924c-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9924c-110">Return Type</span></span> | <span data-ttu-id="9924c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9924c-111">Description</span></span>|
|:------|:------------|:-----------|
|[<span data-ttu-id="9924c-112">Crear o reemplazar un historyItem</span><span class="sxs-lookup"><span data-stu-id="9924c-112">Create or replace historyItem</span></span>](../api/projectrome_put_historyitem.md) | <span data-ttu-id="9924c-113">[historyItem](projectrome_historyitem.md)</span><span class="sxs-lookup"><span data-stu-id="9924c-113">Added [historyItem](projectrome_historyitem.md)</span></span> | <span data-ttu-id="9924c-114">Crea o reemplaza un **historyItem** existente para esa actividad (upsert).</span><span class="sxs-lookup"><span data-stu-id="9924c-114">Creates or replaces an existing **historyItem** for that activity (upsert).</span></span> <span data-ttu-id="9924c-115">El id. debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="9924c-115">The ID needs to be a GUID.</span></span>|
|[<span data-ttu-id="9924c-116">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="9924c-116">Delete a historyItem</span></span>](../api/projectrome_delete_historyitem.md) | <span data-ttu-id="9924c-117">Sin contenido</span><span class="sxs-lookup"><span data-stu-id="9924c-117">204 No Content</span></span> | <span data-ttu-id="9924c-118">Elimina el **historyItem** especificado para esa actividad.</span><span class="sxs-lookup"><span data-stu-id="9924c-118">Deletes the specified **historyItem** for that activity.</span></span>|

## <a name="properties"></a><span data-ttu-id="9924c-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9924c-119">Properties</span></span>

|<span data-ttu-id="9924c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9924c-120">Name</span></span> | <span data-ttu-id="9924c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="9924c-121">Type</span></span> | <span data-ttu-id="9924c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9924c-122">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="9924c-123">status</span><span class="sxs-lookup"><span data-stu-id="9924c-123">status</span></span> | <span data-ttu-id="9924c-124">status</span><span class="sxs-lookup"><span data-stu-id="9924c-124">status</span></span> | <span data-ttu-id="9924c-125">Establecido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="9924c-125">Set by the server.</span></span> <span data-ttu-id="9924c-126">Un código de estado que se usa para identificar objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="9924c-126">A status code used to identify valid objects.</span></span> <span data-ttu-id="9924c-127">Valores: activo, actualizado, eliminado, ignorado.</span><span class="sxs-lookup"><span data-stu-id="9924c-127">Values: active, updated, deleted, ignored.</span></span>|
|<span data-ttu-id="9924c-128">userTimezone</span><span class="sxs-lookup"><span data-stu-id="9924c-128">userTimezone</span></span> | <span data-ttu-id="9924c-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="9924c-129">String</span></span> | <span data-ttu-id="9924c-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9924c-130">Optional.</span></span> <span data-ttu-id="9924c-131">La zona horaria en la que se encuentra el dispositivo del usuario utilizado para generar la actividad cuando se crea.</span><span class="sxs-lookup"><span data-stu-id="9924c-131">The timezone in which the user's device used to generate the activity was located at activity creation time.</span></span> <span data-ttu-id="9924c-132">Valores proporcionados como identificadores Olson con el fin de admitir la representación multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="9924c-132">Values supplied as Olson IDs in order to support cross-platform representation.</span></span>|
|<span data-ttu-id="9924c-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9924c-133">createdDateTime</span></span> | <span data-ttu-id="9924c-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9924c-134">DateTimeOffset</span></span> | <span data-ttu-id="9924c-135">Establecida por el servidor.</span><span class="sxs-lookup"><span data-stu-id="9924c-135">Set by the server.</span></span> <span data-ttu-id="9924c-136">Fecha y hora en UTC en la que se creó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9924c-136">DateTime in UTC when the object was created on the server.</span></span>|
|<span data-ttu-id="9924c-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9924c-137">lastModifiedDateTime</span></span> | <span data-ttu-id="9924c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9924c-138">DateTimeOffset</span></span> | <span data-ttu-id="9924c-139">Establecida por el servidor.</span><span class="sxs-lookup"><span data-stu-id="9924c-139">Set by the server.</span></span> <span data-ttu-id="9924c-140">Fecha y hora en UTC en la que se modificó el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9924c-140">DateTime in UTC when the object was modified on the server.</span></span>|
|<span data-ttu-id="9924c-141">id</span><span class="sxs-lookup"><span data-stu-id="9924c-141">id</span></span> | <span data-ttu-id="9924c-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="9924c-142">String</span></span> | <span data-ttu-id="9924c-143">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9924c-143">Required.</span></span> <span data-ttu-id="9924c-144">GUID del conjunto de clientes para el objeto **historyItem**.</span><span class="sxs-lookup"><span data-stu-id="9924c-144">Client-set GUID for the **historyItem** object.</span></span>|
|<span data-ttu-id="9924c-145">startedDateTime</span><span class="sxs-lookup"><span data-stu-id="9924c-145">startedDateTime</span></span> | <span data-ttu-id="9924c-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9924c-146">DateTimeOffset</span></span> | <span data-ttu-id="9924c-147">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9924c-147">Required.</span></span> <span data-ttu-id="9924c-148">Fecha y hora en UTC en la que se inició el **historyItem** (sesión de actividad).</span><span class="sxs-lookup"><span data-stu-id="9924c-148">UTC DateTime when the **historyItem** (activity session) was started.</span></span> <span data-ttu-id="9924c-149">Requerida para el historial de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="9924c-149">Required for timeline history.</span></span>|
|<span data-ttu-id="9924c-150">lastActiveDateTime</span><span class="sxs-lookup"><span data-stu-id="9924c-150">lastActiveDateTime</span></span> | <span data-ttu-id="9924c-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9924c-151">DateTimeOffset</span></span> | <span data-ttu-id="9924c-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9924c-152">Optional.</span></span> <span data-ttu-id="9924c-153">Fecha y hora en UTC en la que el **historyItem** (sesión de actividad) se entiende por última vez como activo o terminado; si es nulo, el estado del **historyItem** debería ser Ongoing (en curso).</span><span class="sxs-lookup"><span data-stu-id="9924c-153">UTC DateTime when the **historyItem** (activity session) was last understood as active or finished - if null, **historyItem** status should be Ongoing.</span></span>|
|<span data-ttu-id="9924c-154">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="9924c-154">expirationDateTime</span></span> | <span data-ttu-id="9924c-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9924c-155">DateTimeOffset</span></span> | <span data-ttu-id="9924c-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9924c-156">Optional.</span></span> <span data-ttu-id="9924c-157">Fecha y hora en UTC en la que el **historyItem** experimentará una eliminación permanente.</span><span class="sxs-lookup"><span data-stu-id="9924c-157">UTC DateTime when the **historyItem** will undergo hard-delete.</span></span> <span data-ttu-id="9924c-158">Puede ser establecida por el cliente.</span><span class="sxs-lookup"><span data-stu-id="9924c-158">Can be set by the client.</span></span>|
|<span data-ttu-id="9924c-159">activeDurationSeconds</span><span class="sxs-lookup"><span data-stu-id="9924c-159">activeDurationSeconds</span></span> | <span data-ttu-id="9924c-160">int</span><span class="sxs-lookup"><span data-stu-id="9924c-160">int</span></span> | <span data-ttu-id="9924c-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9924c-161">Optional.</span></span> <span data-ttu-id="9924c-162">La duración de la interactuación del usuario activo.</span><span class="sxs-lookup"><span data-stu-id="9924c-162">The duration of active user engagement.</span></span> <span data-ttu-id="9924c-163">si no se proporciona, esta se calcula a partir de la **startedDateTime** y la **lastActiveDateTime**.</span><span class="sxs-lookup"><span data-stu-id="9924c-163">if not supplied, this is calculated from the **startedDateTime** and **lastActiveDateTime**.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9924c-164">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9924c-164">Relationships</span></span>

|<span data-ttu-id="9924c-165">Relación</span><span class="sxs-lookup"><span data-stu-id="9924c-165">Relationship</span></span> | <span data-ttu-id="9924c-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="9924c-166">Type</span></span> | <span data-ttu-id="9924c-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="9924c-167">Description</span></span>|
|:------------|:-----|:-----------|
|<span data-ttu-id="9924c-168">activity</span><span class="sxs-lookup"><span data-stu-id="9924c-168">activity</span></span>| [<span data-ttu-id="9924c-169">userActivity</span><span class="sxs-lookup"><span data-stu-id="9924c-169">userActivity</span></span>](../resources/projectrome_activity.md) | <span data-ttu-id="9924c-170">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9924c-170">Optional.</span></span> <span data-ttu-id="9924c-171">NavigationProperty/Containment; propiedad de navegación para la actividad asociada.</span><span class="sxs-lookup"><span data-stu-id="9924c-171">NavigationProperty/Containment; navigation property to the associated activity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9924c-172">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9924c-172">JSON representation</span></span>

<span data-ttu-id="9924c-173">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9924c-173">Here is a JSON representation of the resource.</span></span>

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
