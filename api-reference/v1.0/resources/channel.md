# <a name="channel-resource-type"></a><span data-ttu-id="cd1c2-101">tipo de recurso de canal</span><span class="sxs-lookup"><span data-stu-id="cd1c2-101">channel resource type</span></span>



<span data-ttu-id="cd1c2-102">Un canal es una colección de los mensajes dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-102">A channel is a collection of messages within a [team](../resources/team.md).</span></span> <span data-ttu-id="cd1c2-103">Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-103">A channel represents a topic, and therefore a logical isolation of discussion, within a team.</span></span> <span data-ttu-id="cd1c2-104">Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".</span><span class="sxs-lookup"><span data-stu-id="cd1c2-104">Examples can be "Friday Team Lunch" channel, and "Architecture Discussion" channel.</span></span>


## <a name="methods"></a><span data-ttu-id="cd1c2-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd1c2-105">Methods</span></span>

| <span data-ttu-id="cd1c2-106">Método</span><span class="sxs-lookup"><span data-stu-id="cd1c2-106">Method</span></span>       | <span data-ttu-id="cd1c2-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd1c2-107">Return Type</span></span>  |<span data-ttu-id="cd1c2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd1c2-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="cd1c2-109">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="cd1c2-109">List channels</span></span>](../api/channel_list.md) | <span data-ttu-id="cd1c2-110">colección de [canal](channel.md)</span><span class="sxs-lookup"><span data-stu-id="cd1c2-110">[channel](channel.md) collection</span></span> | <span data-ttu-id="cd1c2-111">Obtener la lista de canales en este equipo.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-111">Get the list of channels in this team.</span></span>|
|[<span data-ttu-id="cd1c2-112">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="cd1c2-112">Create channel</span></span>](../api/channel_post.md) | [<span data-ttu-id="cd1c2-113">canal</span><span class="sxs-lookup"><span data-stu-id="cd1c2-113">channel</span></span>](channel.md) | <span data-ttu-id="cd1c2-114">Crear un nuevo canal si incluye el nombre para mostrar y la descripción.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-114">Create a new channel by including the display name and description.</span></span>|
|[<span data-ttu-id="cd1c2-115">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="cd1c2-115">Get channel</span></span>](../api/channel_get.md) | [<span data-ttu-id="cd1c2-116">canal</span><span class="sxs-lookup"><span data-stu-id="cd1c2-116">channel</span></span>](channel.md) | <span data-ttu-id="cd1c2-117">Leer las propiedades y relaciones del canal.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-117">Read properties and relationships of the channel.</span></span>|
|[<span data-ttu-id="cd1c2-118">Canal de actualización</span><span class="sxs-lookup"><span data-stu-id="cd1c2-118">Update channel</span></span>](../api/channel_patch.md) | [<span data-ttu-id="cd1c2-119">canal</span><span class="sxs-lookup"><span data-stu-id="cd1c2-119">channel</span></span>](channel.md) | <span data-ttu-id="cd1c2-120">Actualizar las propiedades del canal.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-120">Update properties of the channel.</span></span>|
|[<span data-ttu-id="cd1c2-121">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="cd1c2-121">Delete channel</span></span>](../api/channel_delete.md) | <span data-ttu-id="cd1c2-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd1c2-122">None</span></span> | <span data-ttu-id="cd1c2-123">Eliminar un canal.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-123">Delete a channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="cd1c2-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd1c2-124">Properties</span></span>
| <span data-ttu-id="cd1c2-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd1c2-125">Property</span></span>     | <span data-ttu-id="cd1c2-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd1c2-126">Type</span></span>   |<span data-ttu-id="cd1c2-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd1c2-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cd1c2-128">description</span><span class="sxs-lookup"><span data-stu-id="cd1c2-128">description</span></span>|<span data-ttu-id="cd1c2-129">String</span><span class="sxs-lookup"><span data-stu-id="cd1c2-129">String</span></span>|<span data-ttu-id="cd1c2-130">Descripción textual opcional para el canal.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-130">Optional textual description for the channel.</span></span>|
|<span data-ttu-id="cd1c2-131">displayName</span><span class="sxs-lookup"><span data-stu-id="cd1c2-131">displayName</span></span>|<span data-ttu-id="cd1c2-132">String</span><span class="sxs-lookup"><span data-stu-id="cd1c2-132">String</span></span>|<span data-ttu-id="cd1c2-133">Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-133">Channel name as it will appear to the user in Microsoft Teams.</span></span>|
|<span data-ttu-id="cd1c2-134">id</span><span class="sxs-lookup"><span data-stu-id="cd1c2-134">id</span></span>|<span data-ttu-id="cd1c2-135">String</span><span class="sxs-lookup"><span data-stu-id="cd1c2-135">String</span></span>|<span data-ttu-id="cd1c2-136">Identificador único de la de los canales.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-136">The channels's unique identifier.</span></span> <span data-ttu-id="cd1c2-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-137">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cd1c2-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cd1c2-138">Relationships</span></span>
| <span data-ttu-id="cd1c2-139">Relación</span><span class="sxs-lookup"><span data-stu-id="cd1c2-139">Relationship</span></span> | <span data-ttu-id="cd1c2-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd1c2-140">Type</span></span>   |<span data-ttu-id="cd1c2-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd1c2-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cd1c2-142">fichas</span><span class="sxs-lookup"><span data-stu-id="cd1c2-142">tabs</span></span>|<span data-ttu-id="cd1c2-143">colección de [teamsTab](../resources/teamstab.md)</span><span class="sxs-lookup"><span data-stu-id="cd1c2-143">[teamsTab](../resources/teamstab.md) collection</span></span>|<span data-ttu-id="cd1c2-144">Una colección de todas las fichas en el canal.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-144">A collection of all the tabs in the channel.</span></span> <span data-ttu-id="cd1c2-145">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-145">A navigation property.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="cd1c2-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd1c2-146">JSON representation</span></span>

<span data-ttu-id="cd1c2-147">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cd1c2-147">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "chatthreads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.channel"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "channel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
