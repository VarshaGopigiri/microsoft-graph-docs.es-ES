---
title: tipo de recurso connectorGroup
description: Aquí tiene una representación JSON del recurso.
localization_priority: Normal
ms.openlocfilehash: 211efe5d8caae57457a6a5cc4fa95d145cd176f3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823194"
---
# <a name="connectorgroup-resource-type"></a><span data-ttu-id="9580f-103">tipo de recurso connectorGroup</span><span class="sxs-lookup"><span data-stu-id="9580f-103">connectorGroup resource type</span></span>

> <span data-ttu-id="9580f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9580f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9580f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9580f-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="methods"></a><span data-ttu-id="9580f-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="9580f-106">Methods</span></span>

| <span data-ttu-id="9580f-107">Método</span><span class="sxs-lookup"><span data-stu-id="9580f-107">Method</span></span>           | <span data-ttu-id="9580f-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9580f-108">Return Type</span></span>    |<span data-ttu-id="9580f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9580f-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9580f-110">Obtener connectorGroup</span><span class="sxs-lookup"><span data-stu-id="9580f-110">Get connectorGroup</span></span>](../api/connectorgroup-get.md) | [<span data-ttu-id="9580f-111">connectorGroup</span><span class="sxs-lookup"><span data-stu-id="9580f-111">connectorGroup</span></span>](connectorgroup.md) |<span data-ttu-id="9580f-112">Leer las propiedades y las relaciones del objeto connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="9580f-112">Read properties and relationships of connectorGroup object.</span></span>|
|[<span data-ttu-id="9580f-113">Crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="9580f-113">Create application</span></span>](../api/connectorgroup-post-applications.md) |[<span data-ttu-id="9580f-114">application</span><span class="sxs-lookup"><span data-stu-id="9580f-114">application</span></span>](application.md)| <span data-ttu-id="9580f-115">Asociación de una aplicación con el grupo de conector por la publicación de la colección de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9580f-115">Associate an application with the connector group by posting to the applications collection.</span></span>|
|[<span data-ttu-id="9580f-116">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="9580f-116">List applications</span></span>](../api/connectorgroup-list-applications.md) |<span data-ttu-id="9580f-117">colección de la [aplicación](application.md)</span><span class="sxs-lookup"><span data-stu-id="9580f-117">[application](application.md) collection</span></span>| <span data-ttu-id="9580f-118">Obtener la colección de objetos de la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9580f-118">Get the associated application object collection.</span></span>|
|[<span data-ttu-id="9580f-119">Creación de conector</span><span class="sxs-lookup"><span data-stu-id="9580f-119">Create connector</span></span>](../api/connectorgroup-post-members.md) |[<span data-ttu-id="9580f-120">conector</span><span class="sxs-lookup"><span data-stu-id="9580f-120">connector</span></span>](connector.md)| <span data-ttu-id="9580f-121">Agregar un conector para el conector de grupo de contabilización a la colección members.</span><span class="sxs-lookup"><span data-stu-id="9580f-121">Add a connector to the connector Group by posting to the members collection.</span></span>|
|[<span data-ttu-id="9580f-122">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="9580f-122">List members</span></span>](../api/connectorgroup-list-members.md) |<span data-ttu-id="9580f-123">colección de [conector](connector.md)</span><span class="sxs-lookup"><span data-stu-id="9580f-123">[connector](connector.md) collection</span></span>| <span data-ttu-id="9580f-124">Obtener un conector de colección de objetos.</span><span class="sxs-lookup"><span data-stu-id="9580f-124">Get a connector object collection.</span></span>|
|[<span data-ttu-id="9580f-125">Update</span><span class="sxs-lookup"><span data-stu-id="9580f-125">Update</span></span>](../api/connectorgroup-update.md) | [<span data-ttu-id="9580f-126">connectorGroup</span><span class="sxs-lookup"><span data-stu-id="9580f-126">connectorGroup</span></span>](connectorgroup.md)    |<span data-ttu-id="9580f-127">Actualizar el objeto connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="9580f-127">Update connectorGroup object.</span></span> |
|[<span data-ttu-id="9580f-128">Delete</span><span class="sxs-lookup"><span data-stu-id="9580f-128">Delete</span></span>](../api/connectorgroup-delete.md) | <span data-ttu-id="9580f-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9580f-129">None</span></span> |<span data-ttu-id="9580f-130">Eliminar el objeto connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="9580f-130">Delete connectorGroup object.</span></span> <span data-ttu-id="9580f-131">Todos los conectores deben quitar antes de que se puede eliminar un grupo de conector.</span><span class="sxs-lookup"><span data-stu-id="9580f-131">All connectors must be remove before a conector group can be deleted.</span></span> |

## <a name="properties"></a><span data-ttu-id="9580f-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9580f-132">Properties</span></span>
| <span data-ttu-id="9580f-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9580f-133">Property</span></span>     | <span data-ttu-id="9580f-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="9580f-134">Type</span></span>   |<span data-ttu-id="9580f-135">Description</span><span class="sxs-lookup"><span data-stu-id="9580f-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9580f-136">connectorGroupType</span><span class="sxs-lookup"><span data-stu-id="9580f-136">connectorGroupType</span></span>|<span data-ttu-id="9580f-137">string</span><span class="sxs-lookup"><span data-stu-id="9580f-137">string</span></span>| <span data-ttu-id="9580f-138">El tipo de conectores que se utilizará junto con el grupo.</span><span class="sxs-lookup"><span data-stu-id="9580f-138">The type of connectors that will be used with the group.</span></span> <span data-ttu-id="9580f-139">Los valores posibles son: `applicationProxy`.</span><span class="sxs-lookup"><span data-stu-id="9580f-139">Possible values are: `applicationProxy`.</span></span>|
|<span data-ttu-id="9580f-140">id</span><span class="sxs-lookup"><span data-stu-id="9580f-140">id</span></span>|<span data-ttu-id="9580f-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="9580f-141">String</span></span>| <span data-ttu-id="9580f-142">El identificador del objeto de la connectorGroup</span><span class="sxs-lookup"><span data-stu-id="9580f-142">The object id of the connectorGroup</span></span>|
|<span data-ttu-id="9580f-143">isDefault</span><span class="sxs-lookup"><span data-stu-id="9580f-143">isDefault</span></span>|<span data-ttu-id="9580f-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="9580f-144">Boolean</span></span>| <span data-ttu-id="9580f-145">Indica si la connectorGroup es el grupo predeterminado de conector.</span><span class="sxs-lookup"><span data-stu-id="9580f-145">Indicates if the connectorGroup is the default connector group.</span></span> <span data-ttu-id="9580f-146">Sólo un conector grupo puede ser el connectorGroup de forma predeterminada y se establece el sistema.</span><span class="sxs-lookup"><span data-stu-id="9580f-146">Only a single connector Group can be the default connectorGroup and is set by the system.</span></span>|
|<span data-ttu-id="9580f-147">name</span><span class="sxs-lookup"><span data-stu-id="9580f-147">name</span></span>|<span data-ttu-id="9580f-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="9580f-148">String</span></span>| <span data-ttu-id="9580f-149">El nombre asociado con el connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="9580f-149">The name associated with the connectorGroup.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9580f-150">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9580f-150">Relationships</span></span>
| <span data-ttu-id="9580f-151">Relación</span><span class="sxs-lookup"><span data-stu-id="9580f-151">Relationship</span></span> | <span data-ttu-id="9580f-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="9580f-152">Type</span></span>   |<span data-ttu-id="9580f-153">Description</span><span class="sxs-lookup"><span data-stu-id="9580f-153">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9580f-154">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9580f-154">applications</span></span>|<span data-ttu-id="9580f-155">colección de la [aplicación](application.md)</span><span class="sxs-lookup"><span data-stu-id="9580f-155">[application](application.md) collection</span></span>| <span data-ttu-id="9580f-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9580f-p105">Read-only. Nullable.</span></span>|
|<span data-ttu-id="9580f-158">members</span><span class="sxs-lookup"><span data-stu-id="9580f-158">members</span></span>|<span data-ttu-id="9580f-159">colección de [conector](connector.md)</span><span class="sxs-lookup"><span data-stu-id="9580f-159">[connector](connector.md) collection</span></span>| <span data-ttu-id="9580f-p106">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9580f-p106">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9580f-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9580f-162">JSON representation</span></span>

<span data-ttu-id="9580f-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9580f-163">Here is a JSON representation of the resource.</span></span>

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
