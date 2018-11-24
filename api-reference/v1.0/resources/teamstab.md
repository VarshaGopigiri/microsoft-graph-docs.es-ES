# <a name="teamstab-resource-type"></a><span data-ttu-id="82c9c-101">tipo de recurso teamsTab</span><span class="sxs-lookup"><span data-stu-id="82c9c-101">teamsTab resource type</span></span>



<span data-ttu-id="82c9c-102">Una teamsTab es una [ficha](../resources/teamstab.md) que ha anclado (adjunto) a un [canal](channel.md) dentro de un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="82c9c-102">A teamsTab is a [tab](../resources/teamstab.md) that's pinned (attached) to a [channel](channel.md) within a [team](team.md).</span></span> 

## <a name="methods"></a><span data-ttu-id="82c9c-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="82c9c-103">Methods</span></span>

| <span data-ttu-id="82c9c-104">Método</span><span class="sxs-lookup"><span data-stu-id="82c9c-104">Method</span></span>       | <span data-ttu-id="82c9c-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82c9c-105">Return Type</span></span>  |<span data-ttu-id="82c9c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="82c9c-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="82c9c-107">Fichas de lista</span><span class="sxs-lookup"><span data-stu-id="82c9c-107">List tabs</span></span>](../api/teamstab_list.md) | [<span data-ttu-id="82c9c-108">teamsTab</span><span class="sxs-lookup"><span data-stu-id="82c9c-108">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="82c9c-109">Las fichas de listas anclado a un canal.</span><span class="sxs-lookup"><span data-stu-id="82c9c-109">Lists tabs pinned to a channel.</span></span>|
|[<span data-ttu-id="82c9c-110">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="82c9c-110">Get tab</span></span>](../api/teamstab_get.md) | [<span data-ttu-id="82c9c-111">teamsTab</span><span class="sxs-lookup"><span data-stu-id="82c9c-111">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="82c9c-112">Lee una ficha anclada a un canal.</span><span class="sxs-lookup"><span data-stu-id="82c9c-112">Reads a tab pinned to a channel.</span></span>|
|[<span data-ttu-id="82c9c-113">Agregar ficha</span><span class="sxs-lookup"><span data-stu-id="82c9c-113">Add tab</span></span>](../api/teamstab_add.md) | [<span data-ttu-id="82c9c-114">teamsTab</span><span class="sxs-lookup"><span data-stu-id="82c9c-114">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="82c9c-115">(PIN) se agrega una ficha a un canal.</span><span class="sxs-lookup"><span data-stu-id="82c9c-115">Adds (pins) a tab to a channel.</span></span>|
|[<span data-ttu-id="82c9c-116">Quitar la ficha</span><span class="sxs-lookup"><span data-stu-id="82c9c-116">Remove tab</span></span>](../api/teamstab_delete.md) | <span data-ttu-id="82c9c-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="82c9c-117">None</span></span> | <span data-ttu-id="82c9c-118">Quita (libera) una ficha de un canal.</span><span class="sxs-lookup"><span data-stu-id="82c9c-118">Removes (unpins) a tab from a channel.</span></span>|
|[<span data-ttu-id="82c9c-119">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="82c9c-119">Update tab</span></span>](../api/teamstab_update.md) | [<span data-ttu-id="82c9c-120">teamsTab</span><span class="sxs-lookup"><span data-stu-id="82c9c-120">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="82c9c-121">Actualiza las propiedades de la ficha.</span><span class="sxs-lookup"><span data-stu-id="82c9c-121">Updates the tab properties.</span></span>|


## <a name="properties"></a><span data-ttu-id="82c9c-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82c9c-122">Properties</span></span>

|<span data-ttu-id="82c9c-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82c9c-123">Property</span></span>|<span data-ttu-id="82c9c-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="82c9c-124">Type</span></span>|<span data-ttu-id="82c9c-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="82c9c-125">Description</span></span>|
|:---------------|:--------|:----------|
|  <span data-ttu-id="82c9c-126">id</span><span class="sxs-lookup"><span data-stu-id="82c9c-126">id</span></span>              |   <span data-ttu-id="82c9c-127">string</span><span class="sxs-lookup"><span data-stu-id="82c9c-127">string</span></span>                  |  <span data-ttu-id="82c9c-128">Identificador que identifica de forma exclusiva una instancia específica de una ficha de canal lectura sólo.</span><span class="sxs-lookup"><span data-stu-id="82c9c-128">Identifier that uniquely identifies a specific instance of a channel tab. Read only.</span></span>     |
|  <span data-ttu-id="82c9c-129">displayName</span><span class="sxs-lookup"><span data-stu-id="82c9c-129">displayName</span></span>            |   <span data-ttu-id="82c9c-130">string</span><span class="sxs-lookup"><span data-stu-id="82c9c-130">string</span></span>                  |  <span data-ttu-id="82c9c-131">Nombre de la ficha.</span><span class="sxs-lookup"><span data-stu-id="82c9c-131">Name of the tab.</span></span>     |
|  <span data-ttu-id="82c9c-132">sortOrderIndex</span><span class="sxs-lookup"><span data-stu-id="82c9c-132">sortOrderIndex</span></span>  |   <span data-ttu-id="82c9c-133">int</span><span class="sxs-lookup"><span data-stu-id="82c9c-133">int</span></span>                     |  <span data-ttu-id="82c9c-134">Índice del orden utilizado para la ordenación de las fichas</span><span class="sxs-lookup"><span data-stu-id="82c9c-134">Index of the order used for sorting tabs</span></span>     |
|  <span data-ttu-id="82c9c-135">webUrl</span><span class="sxs-lookup"><span data-stu-id="82c9c-135">webUrl</span></span>          |   <span data-ttu-id="82c9c-136">string</span><span class="sxs-lookup"><span data-stu-id="82c9c-136">string</span></span>                  |  <span data-ttu-id="82c9c-137">Dirección url del vínculo profundo de la instancia de ficha.</span><span class="sxs-lookup"><span data-stu-id="82c9c-137">Deep link url of the tab instance.</span></span> <span data-ttu-id="82c9c-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="82c9c-138">Read only.</span></span>     |
|  <span data-ttu-id="82c9c-139">configuration</span><span class="sxs-lookup"><span data-stu-id="82c9c-139">configuration</span></span>        |   [<span data-ttu-id="82c9c-140">teamsTabConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c9c-140">teamsTabConfiguration</span></span>](teamstabconfiguration.md) |  <span data-ttu-id="82c9c-141">Contenedor de configuración personalizada que se aplican a una ficha. La ficha se considera configurado sólo una vez que se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="82c9c-141">Container for custom settings applied to a tab. The tab is considered configured only once this property is set.</span></span>     |

## <a name="relationships"></a><span data-ttu-id="82c9c-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="82c9c-142">Relationships</span></span>

| <span data-ttu-id="82c9c-143">Relación</span><span class="sxs-lookup"><span data-stu-id="82c9c-143">Relationship</span></span> | <span data-ttu-id="82c9c-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="82c9c-144">Type</span></span>   | <span data-ttu-id="82c9c-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="82c9c-145">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="82c9c-146">teamsApp</span><span class="sxs-lookup"><span data-stu-id="82c9c-146">teamsApp</span></span>|[<span data-ttu-id="82c9c-147">teamsApp</span><span class="sxs-lookup"><span data-stu-id="82c9c-147">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="82c9c-148">La aplicación que está vinculada a la ficha. Esto no se puede cambiar después de la creación de la ficha.</span><span class="sxs-lookup"><span data-stu-id="82c9c-148">The application that is linked to the tab. This cannot be changed after tab creation.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="82c9c-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="82c9c-149">JSON representation</span></span>

<span data-ttu-id="82c9c-150">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="82c9c-150">The following is a JSON representation of the resource.</span></span>


<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.teamsTab"
}-->

```json
{  
  "id": "string",
  "displayName": "string",
  "sortOrderIndex": "string",
  "webUrl": "string",
  "configuration" : "teamsTabConfiguration"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsTab resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

## <a name="see-also"></a><span data-ttu-id="82c9c-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="82c9c-151">See also</span></span>

[<span data-ttu-id="82c9c-152">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="82c9c-152">Configuring the built-in tab types</span></span>](../../../concepts/teams-configuring-builtin-tabs.md)
