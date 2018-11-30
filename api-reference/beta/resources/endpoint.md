---
title: Tipo de recurso de extremo
description: 'Los extremos representan las direcciones URL para los recursos asociados a una entidad.  Por ejemplo, cuando se crea un nuevo grupo de Office 365, también se crean los recursos adicionales como parte del grupo de Office 365. Éstas incluyen aspectos como un buzón de grupo para las conversaciones y una carpeta de OneDrive de grupo para los documentos y archivos. Ahora se puede leer para obtener más información acerca de estos recursos de grupo de Office 365, incluidos sus direcciones URL de recursos asociados utilizando la navegación de *extremos* en el tipo de recurso de grupo. Esto permite a las aplicaciones comprender estos recursos e incluso incrustar el recurso de que dirección URL se pueden observar en sus propias experiencias. '
ms.openlocfilehash: 8d95cef8e25095512e94d5aed5ec7540562862bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084778"
---
# <a name="endpoint-resource-type"></a><span data-ttu-id="6c2b3-107">Tipo de recurso de extremo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-107">Endpoint resource type</span></span>

> <span data-ttu-id="6c2b3-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6c2b3-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6c2b3-110">Los extremos representan las direcciones URL para los recursos asociados a una entidad.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-110">Endpoints represent URLs for resources associated with an entity.</span></span>  <span data-ttu-id="6c2b3-111">Por ejemplo, cuando se crea un nuevo grupo de Office 365, también se crean los recursos adicionales como parte del grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-111">For example, when a new Office 365 group is created, additional resources are also created as part of the Office 365 group.</span></span> <span data-ttu-id="6c2b3-112">Éstas incluyen aspectos como un buzón de grupo para las conversaciones y una carpeta de OneDrive de grupo para los documentos y archivos.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-112">These include things like a group mailbox for conversations and a group OneDrive folder for documents and files.</span></span> <span data-ttu-id="6c2b3-113">Ahora se puede leer para obtener más información acerca de estos recursos de grupo de Office 365, incluidos sus direcciones URL de recursos asociados utilizando la navegación de *extremos* en el tipo de recurso de grupo.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-113">Further information about these Office 365 group resources, including their associated resource URLs can now be read using the *endpoints* navigation on the group resource-type.</span></span> <span data-ttu-id="6c2b3-114">Esto permite a las aplicaciones comprender estos recursos e incluso incrustar el recurso de que dirección URL se pueden observar en sus propias experiencias.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-114">This allows applications to understand these resources, and even embed the resource URL experiences in their own experiences.</span></span> 

## <a name="methods"></a><span data-ttu-id="6c2b3-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c2b3-115">Methods</span></span>

| <span data-ttu-id="6c2b3-116">Método</span><span class="sxs-lookup"><span data-stu-id="6c2b3-116">Method</span></span>           | <span data-ttu-id="6c2b3-117">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c2b3-117">Return Type</span></span>    |<span data-ttu-id="6c2b3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c2b3-118">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="6c2b3-119">Extremos de lista</span><span class="sxs-lookup"><span data-stu-id="6c2b3-119">List endpoints</span></span>](../api/group-list-endpoints.md) |<span data-ttu-id="6c2b3-120">Colección de [extremo](endpoint.md)</span><span class="sxs-lookup"><span data-stu-id="6c2b3-120">[Endpoint](endpoint.md) collection</span></span>| <span data-ttu-id="6c2b3-121">Obtener una colección de objetos de extremo.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-121">Get an endpoint object collection.</span></span> |
|[<span data-ttu-id="6c2b3-122">Obtener el extremo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-122">Get endpoint</span></span>](../api/endpoint-get.md) | [<span data-ttu-id="6c2b3-123">Punto de conexión</span><span class="sxs-lookup"><span data-stu-id="6c2b3-123">Endpoint</span></span>](endpoint.md) |<span data-ttu-id="6c2b3-124">Leer las propiedades y relaciones de un objeto de extremo.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-124">Read properties and relationships of an endpoint object.</span></span>|

## <a name="properties"></a><span data-ttu-id="6c2b3-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c2b3-125">Properties</span></span>
| <span data-ttu-id="6c2b3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c2b3-126">Property</span></span>     | <span data-ttu-id="6c2b3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-127">Type</span></span>   |<span data-ttu-id="6c2b3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c2b3-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6c2b3-129">capacidad</span><span class="sxs-lookup"><span data-stu-id="6c2b3-129">capability</span></span>     | <span data-ttu-id="6c2b3-130">String</span><span class="sxs-lookup"><span data-stu-id="6c2b3-130">String</span></span>  | <span data-ttu-id="6c2b3-131">Describe la capacidad que está asociada a este recurso.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-131">Describes the capability that is associated with this resource.</span></span> <span data-ttu-id="6c2b3-132">(por ejemplo, los mensajes, las conversaciones, etcetera.)  No acepta valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-132">(e.g. Messages, Conversations, etc.)  Not nullable.</span></span> <span data-ttu-id="6c2b3-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-133">Read-only.</span></span> |
| <span data-ttu-id="6c2b3-134">id</span><span class="sxs-lookup"><span data-stu-id="6c2b3-134">id</span></span>             | <span data-ttu-id="6c2b3-135">String</span><span class="sxs-lookup"><span data-stu-id="6c2b3-135">String</span></span>  | <span data-ttu-id="6c2b3-136">Identificador único para el extremo; Clave.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-136">Unique identifier for the endpoint; Key.</span></span> <span data-ttu-id="6c2b3-137">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-137">Not nullable.</span></span> <span data-ttu-id="6c2b3-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-138">Read-only.</span></span>|
| <span data-ttu-id="6c2b3-139">providerId</span><span class="sxs-lookup"><span data-stu-id="6c2b3-139">providerId</span></span>     | <span data-ttu-id="6c2b3-140">String</span><span class="sxs-lookup"><span data-stu-id="6c2b3-140">String</span></span>  | <span data-ttu-id="6c2b3-141">Identificador de aplicación de la publicación subyacentes de servicio.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-141">Application id of the publishing underlying service.</span></span> <span data-ttu-id="6c2b3-142">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-142">Not nullable.</span></span> <span data-ttu-id="6c2b3-143">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-143">Read-only.</span></span>|
| <span data-ttu-id="6c2b3-144">providerName</span><span class="sxs-lookup"><span data-stu-id="6c2b3-144">providerName</span></span>   | <span data-ttu-id="6c2b3-145">String</span><span class="sxs-lookup"><span data-stu-id="6c2b3-145">String</span></span>  | <span data-ttu-id="6c2b3-146">Nombre de la publicación subyacentes de servicio.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-146">Name of the publishing underlying service.</span></span> <span data-ttu-id="6c2b3-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-147">Read-only.</span></span>|
| <span data-ttu-id="6c2b3-148">providerResourceId</span><span class="sxs-lookup"><span data-stu-id="6c2b3-148">providerResourceId</span></span>|<span data-ttu-id="6c2b3-149">String</span><span class="sxs-lookup"><span data-stu-id="6c2b3-149">String</span></span>| <span data-ttu-id="6c2b3-150">Para los grupos de Office 365, esto se establece en un nombre para el recurso (por ejemplo, Yammer.FeedURL etcetera.) conocido.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-150">For Office 365 groups, this is set to a well-known name for the resource (e.g. Yammer.FeedURL etc.).</span></span> <span data-ttu-id="6c2b3-151">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-151">Not nullable.</span></span> <span data-ttu-id="6c2b3-152">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-152">Read-only.</span></span>|
| <span data-ttu-id="6c2b3-153">URI</span><span class="sxs-lookup"><span data-stu-id="6c2b3-153">uri</span></span>            | <span data-ttu-id="6c2b3-154">String</span><span class="sxs-lookup"><span data-stu-id="6c2b3-154">String</span></span>  | <span data-ttu-id="6c2b3-155">Dirección URL del recurso publicado.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-155">URL of the published resource.</span></span> <span data-ttu-id="6c2b3-156">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-156">Not nullable.</span></span> <span data-ttu-id="6c2b3-157">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-157">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6c2b3-158">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6c2b3-158">Relationships</span></span>

<span data-ttu-id="6c2b3-159">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-159">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="6c2b3-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6c2b3-160">JSON representation</span></span>
<span data-ttu-id="6c2b3-161">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-161">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.Endpoint"
}-->

```json
{
  "capability": "String",
  "id": "String (identifier)",
  "providerId": "String",
  "providerName": "String",
  "providerResourceId": "String",
  "uri": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Endpoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->