---
title: tipo de recurso connectorGroup
description: Aquí tiene una representación JSON del recurso.
ms.openlocfilehash: a3131b887216f1f400f70ed8d607477f65793cc7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088209"
---
# <a name="connectorgroup-resource-type"></a><span data-ttu-id="18cd3-103">tipo de recurso connectorGroup</span><span class="sxs-lookup"><span data-stu-id="18cd3-103">connectorGroup resource type</span></span>

> <span data-ttu-id="18cd3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18cd3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18cd3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18cd3-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="methods"></a><span data-ttu-id="18cd3-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="18cd3-106">Methods</span></span>

| <span data-ttu-id="18cd3-107">Método</span><span class="sxs-lookup"><span data-stu-id="18cd3-107">Method</span></span>           | <span data-ttu-id="18cd3-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18cd3-108">Return Type</span></span>    |<span data-ttu-id="18cd3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="18cd3-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="18cd3-110">Obtener connectorGroup</span><span class="sxs-lookup"><span data-stu-id="18cd3-110">Get connectorGroup</span></span>](../api/connectorgroup-get.md) | [<span data-ttu-id="18cd3-111">connectorGroup</span><span class="sxs-lookup"><span data-stu-id="18cd3-111">connectorGroup</span></span>](connectorgroup.md) |<span data-ttu-id="18cd3-112">Leer las propiedades y las relaciones del objeto connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="18cd3-112">Read properties and relationships of connectorGroup object.</span></span>|
|[<span data-ttu-id="18cd3-113">Crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="18cd3-113">Create application</span></span>](../api/connectorgroup-post-applications.md) |[<span data-ttu-id="18cd3-114">application</span><span class="sxs-lookup"><span data-stu-id="18cd3-114">application</span></span>](application.md)| <span data-ttu-id="18cd3-115">Asociación de una aplicación con el grupo de conector por la publicación de la colección de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="18cd3-115">Associate an application with the connector group by posting to the applications collection.</span></span>|
|[<span data-ttu-id="18cd3-116">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="18cd3-116">List applications</span></span>](../api/connectorgroup-list-applications.md) |<span data-ttu-id="18cd3-117">colección de la [aplicación](application.md)</span><span class="sxs-lookup"><span data-stu-id="18cd3-117">[application](application.md) collection</span></span>| <span data-ttu-id="18cd3-118">Obtener la colección de objetos de la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="18cd3-118">Get the associated application object collection.</span></span>|
|[<span data-ttu-id="18cd3-119">Creación de conector</span><span class="sxs-lookup"><span data-stu-id="18cd3-119">Create connector</span></span>](../api/connectorgroup-post-members.md) |[<span data-ttu-id="18cd3-120">conector</span><span class="sxs-lookup"><span data-stu-id="18cd3-120">connector</span></span>](connector.md)| <span data-ttu-id="18cd3-121">Agregar un conector para el conector de grupo de contabilización a la colección members.</span><span class="sxs-lookup"><span data-stu-id="18cd3-121">Add a connector to the connector Group by posting to the members collection.</span></span>|
|[<span data-ttu-id="18cd3-122">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="18cd3-122">List members</span></span>](../api/connectorgroup-list-members.md) |<span data-ttu-id="18cd3-123">colección de [conector](connector.md)</span><span class="sxs-lookup"><span data-stu-id="18cd3-123">[connector](connector.md) collection</span></span>| <span data-ttu-id="18cd3-124">Obtener un conector de colección de objetos.</span><span class="sxs-lookup"><span data-stu-id="18cd3-124">Get a connector object collection.</span></span>|
|[<span data-ttu-id="18cd3-125">Update</span><span class="sxs-lookup"><span data-stu-id="18cd3-125">Update</span></span>](../api/connectorgroup-update.md) | [<span data-ttu-id="18cd3-126">connectorGroup</span><span class="sxs-lookup"><span data-stu-id="18cd3-126">connectorGroup</span></span>](connectorgroup.md)    |<span data-ttu-id="18cd3-127">Actualizar el objeto connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="18cd3-127">Update connectorGroup object.</span></span> |
|[<span data-ttu-id="18cd3-128">Delete</span><span class="sxs-lookup"><span data-stu-id="18cd3-128">Delete</span></span>](../api/connectorgroup-delete.md) | <span data-ttu-id="18cd3-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="18cd3-129">None</span></span> |<span data-ttu-id="18cd3-130">Eliminar el objeto connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="18cd3-130">Delete connectorGroup object.</span></span> <span data-ttu-id="18cd3-131">Todos los conectores deben quitar antes de que se puede eliminar un grupo de conector.</span><span class="sxs-lookup"><span data-stu-id="18cd3-131">All connectors must be remove before a conector group can be deleted.</span></span> |

## <a name="properties"></a><span data-ttu-id="18cd3-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18cd3-132">Properties</span></span>
| <span data-ttu-id="18cd3-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18cd3-133">Property</span></span>     | <span data-ttu-id="18cd3-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="18cd3-134">Type</span></span>   |<span data-ttu-id="18cd3-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="18cd3-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18cd3-136">connectorGroupType</span><span class="sxs-lookup"><span data-stu-id="18cd3-136">connectorGroupType</span></span>|<span data-ttu-id="18cd3-137">string</span><span class="sxs-lookup"><span data-stu-id="18cd3-137">string</span></span>| <span data-ttu-id="18cd3-138">El tipo de conectores que se utilizará junto con el grupo.</span><span class="sxs-lookup"><span data-stu-id="18cd3-138">The type of connectors that will be used with the group.</span></span> <span data-ttu-id="18cd3-139">Los valores posibles son: `applicationProxy`.</span><span class="sxs-lookup"><span data-stu-id="18cd3-139">Possible values are: `applicationProxy`.</span></span>|
|<span data-ttu-id="18cd3-140">id</span><span class="sxs-lookup"><span data-stu-id="18cd3-140">id</span></span>|<span data-ttu-id="18cd3-141">String</span><span class="sxs-lookup"><span data-stu-id="18cd3-141">String</span></span>| <span data-ttu-id="18cd3-142">El identificador del objeto de la connectorGroup</span><span class="sxs-lookup"><span data-stu-id="18cd3-142">The object id of the connectorGroup</span></span>|
|<span data-ttu-id="18cd3-143">isDefault</span><span class="sxs-lookup"><span data-stu-id="18cd3-143">isDefault</span></span>|<span data-ttu-id="18cd3-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="18cd3-144">Boolean</span></span>| <span data-ttu-id="18cd3-145">Indica si la connectorGroup es el grupo predeterminado de conector.</span><span class="sxs-lookup"><span data-stu-id="18cd3-145">Indicates if the connectorGroup is the default connector group.</span></span> <span data-ttu-id="18cd3-146">Sólo un conector grupo puede ser el connectorGroup de forma predeterminada y se establece el sistema.</span><span class="sxs-lookup"><span data-stu-id="18cd3-146">Only a single connector Group can be the default connectorGroup and is set by the system.</span></span>|
|<span data-ttu-id="18cd3-147">name</span><span class="sxs-lookup"><span data-stu-id="18cd3-147">name</span></span>|<span data-ttu-id="18cd3-148">String</span><span class="sxs-lookup"><span data-stu-id="18cd3-148">String</span></span>| <span data-ttu-id="18cd3-149">El nombre asociado con el connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="18cd3-149">The name associated with the connectorGroup.</span></span>|

## <a name="relationships"></a><span data-ttu-id="18cd3-150">Relaciones</span><span class="sxs-lookup"><span data-stu-id="18cd3-150">Relationships</span></span>
| <span data-ttu-id="18cd3-151">Relación</span><span class="sxs-lookup"><span data-stu-id="18cd3-151">Relationship</span></span> | <span data-ttu-id="18cd3-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="18cd3-152">Type</span></span>   |<span data-ttu-id="18cd3-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="18cd3-153">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18cd3-154">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="18cd3-154">applications</span></span>|<span data-ttu-id="18cd3-155">colección de la [aplicación](application.md)</span><span class="sxs-lookup"><span data-stu-id="18cd3-155">[application](application.md) collection</span></span>| <span data-ttu-id="18cd3-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="18cd3-p105">Read-only. Nullable.</span></span>|
|<span data-ttu-id="18cd3-158">members</span><span class="sxs-lookup"><span data-stu-id="18cd3-158">members</span></span>|<span data-ttu-id="18cd3-159">colección de [conector](connector.md)</span><span class="sxs-lookup"><span data-stu-id="18cd3-159">[connector](connector.md) collection</span></span>| <span data-ttu-id="18cd3-p106">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="18cd3-p106">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="18cd3-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="18cd3-162">JSON representation</span></span>

<span data-ttu-id="18cd3-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="18cd3-163">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.connectorGroup"
}-->

```json
{
  "connectorGroupType": "string",
  "id": "String (identifier)",
  "isDefault": true,
  "name": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "connectorGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
