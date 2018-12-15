---
title: tipo de recurso teamsTab
description: 'Una teamsTab es una ficha que ha anclado (adjunto) a un canal dentro de un equipo. '
ms.openlocfilehash: 102d4c0b766d8a0d9bdf22cb2ed76f5e06d87ad5
ms.sourcegitcommit: f3d479edf03935d0edbbc7668a65f7cde2a56c92
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/15/2018
ms.locfileid: "27283622"
---
# <a name="teamstab-resource-type"></a><span data-ttu-id="7221f-103">tipo de recurso teamsTab</span><span class="sxs-lookup"><span data-stu-id="7221f-103">teamsTab resource type</span></span>

> <span data-ttu-id="7221f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7221f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7221f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7221f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7221f-106">Una teamsTab es una [ficha](../resources/teamstab.md) que ha anclado (adjunto) a un [canal](channel.md) dentro de un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="7221f-106">A teamsTab is a [tab](../resources/teamstab.md) that's pinned (attached) to a [channel](channel.md) within a [team](team.md).</span></span> 

## <a name="methods"></a><span data-ttu-id="7221f-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="7221f-107">Methods</span></span>

| <span data-ttu-id="7221f-108">Método</span><span class="sxs-lookup"><span data-stu-id="7221f-108">Method</span></span>       | <span data-ttu-id="7221f-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7221f-109">Return Type</span></span>  |<span data-ttu-id="7221f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7221f-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7221f-111">Fichas de lista</span><span class="sxs-lookup"><span data-stu-id="7221f-111">List tabs</span></span>](../api/teamstab-list.md) | [<span data-ttu-id="7221f-112">teamsTab</span><span class="sxs-lookup"><span data-stu-id="7221f-112">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="7221f-113">Las fichas de listas anclado a un canal.</span><span class="sxs-lookup"><span data-stu-id="7221f-113">Lists tabs pinned to a channel.</span></span>|
|[<span data-ttu-id="7221f-114">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="7221f-114">Get tab</span></span>](../api/teamstab-get.md) | [<span data-ttu-id="7221f-115">teamsTab</span><span class="sxs-lookup"><span data-stu-id="7221f-115">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="7221f-116">Lee una ficha anclada a un canal.</span><span class="sxs-lookup"><span data-stu-id="7221f-116">Reads a tab pinned to a channel.</span></span>|
|[<span data-ttu-id="7221f-117">Agregar ficha</span><span class="sxs-lookup"><span data-stu-id="7221f-117">Add tab</span></span>](../api/teamstab-add.md) | [<span data-ttu-id="7221f-118">teamsTab</span><span class="sxs-lookup"><span data-stu-id="7221f-118">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="7221f-119">(PIN) se agrega una ficha a un canal.</span><span class="sxs-lookup"><span data-stu-id="7221f-119">Adds (pins) a tab to a channel.</span></span>|
|[<span data-ttu-id="7221f-120">Quitar la ficha</span><span class="sxs-lookup"><span data-stu-id="7221f-120">Remove tab</span></span>](../api/teamstab-delete.md) | <span data-ttu-id="7221f-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7221f-121">None</span></span> | <span data-ttu-id="7221f-122">Quita (libera) una ficha de un canal.</span><span class="sxs-lookup"><span data-stu-id="7221f-122">Removes (unpins) a tab from a channel.</span></span>|
|[<span data-ttu-id="7221f-123">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="7221f-123">Update tab</span></span>](../api/teamstab-update.md) | [<span data-ttu-id="7221f-124">teamsTab</span><span class="sxs-lookup"><span data-stu-id="7221f-124">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="7221f-125">Actualiza las propiedades de la ficha.</span><span class="sxs-lookup"><span data-stu-id="7221f-125">Updates the tab properties.</span></span>|


## <a name="properties"></a><span data-ttu-id="7221f-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7221f-126">Properties</span></span>

|<span data-ttu-id="7221f-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7221f-127">Property</span></span>|<span data-ttu-id="7221f-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="7221f-128">Type</span></span>|<span data-ttu-id="7221f-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="7221f-129">Description</span></span>|
|:---------------|:--------|:----------|
|  <span data-ttu-id="7221f-130">id</span><span class="sxs-lookup"><span data-stu-id="7221f-130">id</span></span>              |   <span data-ttu-id="7221f-131">string</span><span class="sxs-lookup"><span data-stu-id="7221f-131">string</span></span>                  |  <span data-ttu-id="7221f-132">Identificador que identifica de forma exclusiva una instancia específica de una ficha de canal lectura sólo.</span><span class="sxs-lookup"><span data-stu-id="7221f-132">Identifier that uniquely identifies a specific instance of a channel tab. Read only.</span></span>     |
|  <span data-ttu-id="7221f-133">displayName</span><span class="sxs-lookup"><span data-stu-id="7221f-133">displayName</span></span>            |   <span data-ttu-id="7221f-134">string</span><span class="sxs-lookup"><span data-stu-id="7221f-134">string</span></span>                  |  <span data-ttu-id="7221f-135">Nombre de la ficha.</span><span class="sxs-lookup"><span data-stu-id="7221f-135">Name of the tab.</span></span>     |
|  <span data-ttu-id="7221f-136">name</span><span class="sxs-lookup"><span data-stu-id="7221f-136">name</span></span>            |   <span data-ttu-id="7221f-137">string</span><span class="sxs-lookup"><span data-stu-id="7221f-137">string</span></span>                  |  <span data-ttu-id="7221f-138">(Obsoleto) Nombre de la ficha.</span><span class="sxs-lookup"><span data-stu-id="7221f-138">(Deprecated) Name of the tab.</span></span>     |
|  <span data-ttu-id="7221f-139">teamsAppId</span><span class="sxs-lookup"><span data-stu-id="7221f-139">teamsAppId</span></span>           |   <span data-ttu-id="7221f-140">string</span><span class="sxs-lookup"><span data-stu-id="7221f-140">string</span></span>             |  <span data-ttu-id="7221f-141">Identificador de la definición de aplicación de la ficha. No se puede cambiar este valor después de la creación de la ficha.</span><span class="sxs-lookup"><span data-stu-id="7221f-141">App definition identifier of the tab. This value cannot be changed after tab creation.</span></span>     |
|  <span data-ttu-id="7221f-142">sortOrderIndex</span><span class="sxs-lookup"><span data-stu-id="7221f-142">sortOrderIndex</span></span>  |   <span data-ttu-id="7221f-143">int</span><span class="sxs-lookup"><span data-stu-id="7221f-143">int</span></span>                     |  <span data-ttu-id="7221f-144">Índice del orden utilizado para la ordenación de las fichas.</span><span class="sxs-lookup"><span data-stu-id="7221f-144">Index of the order used for sorting tabs.</span></span>     |
|  <span data-ttu-id="7221f-145">webUrl</span><span class="sxs-lookup"><span data-stu-id="7221f-145">webUrl</span></span>          |   <span data-ttu-id="7221f-146">string</span><span class="sxs-lookup"><span data-stu-id="7221f-146">string</span></span>                  |  <span data-ttu-id="7221f-147">Dirección url del vínculo profundo de la instancia de ficha.</span><span class="sxs-lookup"><span data-stu-id="7221f-147">Deep link url of the tab instance.</span></span> <span data-ttu-id="7221f-148">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7221f-148">Read only.</span></span>     |
|  <span data-ttu-id="7221f-149">configuration</span><span class="sxs-lookup"><span data-stu-id="7221f-149">configuration</span></span>        |   [<span data-ttu-id="7221f-150">teamsTabConfiguration</span><span class="sxs-lookup"><span data-stu-id="7221f-150">teamsTabConfiguration</span></span>](teamstabconfiguration.md) |  <span data-ttu-id="7221f-151">Contenedor de configuración personalizada que se aplican a una ficha. La ficha se considera configurado sólo una vez que se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7221f-151">Container for custom settings applied to a tab. The tab is considered configured only once this property is set.</span></span>     |

## <a name="relationships"></a><span data-ttu-id="7221f-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7221f-152">Relationships</span></span>

| <span data-ttu-id="7221f-153">Relación</span><span class="sxs-lookup"><span data-stu-id="7221f-153">Relationship</span></span> | <span data-ttu-id="7221f-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="7221f-154">Type</span></span>   | <span data-ttu-id="7221f-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="7221f-155">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="7221f-156">teamsApp</span><span class="sxs-lookup"><span data-stu-id="7221f-156">teamsApp</span></span>|[<span data-ttu-id="7221f-157">teamsApp</span><span class="sxs-lookup"><span data-stu-id="7221f-157">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="7221f-158">La aplicación que está vinculada a la ficha.</span><span class="sxs-lookup"><span data-stu-id="7221f-158">The application that is linked to the tab.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="7221f-159">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7221f-159">JSON representation</span></span>

<span data-ttu-id="7221f-160">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7221f-160">The following is a JSON representation of the resource.</span></span>


<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.teamsTab"
}-->

```json
{  
  "id": "string",
  "displayName": "string",
  "teamsAppId": "string",
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

## <a name="see-also"></a><span data-ttu-id="7221f-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="7221f-161">See also</span></span>

[<span data-ttu-id="7221f-162">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="7221f-162">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)
