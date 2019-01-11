---
title: tipo de recurso attributeDefinition
description: Describe un atributo de un objeto.
localization_priority: Normal
ms.openlocfilehash: 63b7f67808ab6695b30f5464d72aed2814e46c5a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829683"
---
# <a name="attributedefinition-resource-type"></a><span data-ttu-id="3e7e4-103">tipo de recurso attributeDefinition</span><span class="sxs-lookup"><span data-stu-id="3e7e4-103">attributeDefinition resource type</span></span>

> <span data-ttu-id="3e7e4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3e7e4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3e7e4-106">Describe un atributo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-106">Describes an attribute of an object.</span></span>

## <a name="properties"></a><span data-ttu-id="3e7e4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e7e4-107">Properties</span></span>

| <span data-ttu-id="3e7e4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3e7e4-108">Property</span></span>      | <span data-ttu-id="3e7e4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e7e4-109">Type</span></span>      | <span data-ttu-id="3e7e4-110">Description</span><span class="sxs-lookup"><span data-stu-id="3e7e4-110">Description</span></span>    |
|:--------------|:----------|:---------------|
|<span data-ttu-id="3e7e4-111">delimitador</span><span class="sxs-lookup"><span data-stu-id="3e7e4-111">anchor</span></span>         |<span data-ttu-id="3e7e4-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="3e7e4-112">Boolean</span></span>    | <span data-ttu-id="3e7e4-113">`true`Si el atributo debe utilizarse como el delimitador para el objeto.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-113">`true` if the attribute should be used as the anchor for the object.</span></span> <span data-ttu-id="3e7e4-114">Atributos de anclaje deben tener un valor único que identifica un objeto y deben ser inmutables.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-114">Anchor attributes must have a unique value identifying an object, and must be immutable.</span></span> <span data-ttu-id="3e7e4-115">El valor predeterminado es `false`.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-115">Default is `false`.</span></span> <span data-ttu-id="3e7e4-116">Uno y sólo uno, de los atributos del objeto deben designarse como el delimitador para admitir la sincronización.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-116">One, and only one, of the object's attributes must be designated as the anchor to support synchronization.</span></span> |
|<span data-ttu-id="3e7e4-117">caseExact</span><span class="sxs-lookup"><span data-stu-id="3e7e4-117">caseExact</span></span>      |<span data-ttu-id="3e7e4-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="3e7e4-118">Boolean</span></span>    |<span data-ttu-id="3e7e4-119">`true`Si el valor de este atributo debe tratarse como entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-119">`true` if value of this attribute should be treated as case-sensitive.</span></span> <span data-ttu-id="3e7e4-120">Esta configuración afecta a cómo el motor de sincronización detecta cambios para el atributo.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-120">This setting affects how the synchronization engine detects changes for the attribute.</span></span>|
|<span data-ttu-id="3e7e4-121">metadatos</span><span class="sxs-lookup"><span data-stu-id="3e7e4-121">metadata</span></span>       |[<span data-ttu-id="3e7e4-122">metadataEntry</span><span class="sxs-lookup"><span data-stu-id="3e7e4-122">metadataEntry</span></span>](../resources/synchronization-metadataentry.md)    |<span data-ttu-id="3e7e4-123">Propiedades de extensión adicionales.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-123">Additional extension properties.</span></span> <span data-ttu-id="3e7e4-124">A menos que se mencionan explícitamente, no se deben cambiar los valores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-124">Unless mentioned explicitly, metadata values should not be changed.</span></span>|
|<span data-ttu-id="3e7e4-125">multivalor</span><span class="sxs-lookup"><span data-stu-id="3e7e4-125">multivalued</span></span>    |<span data-ttu-id="3e7e4-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="3e7e4-126">Boolean</span></span>    |<span data-ttu-id="3e7e4-127">`true`Si un atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-127">`true` if an attribute can have multiple values.</span></span> <span data-ttu-id="3e7e4-128">El valor predeterminado es `false`.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-128">Default is `false`.</span></span>|
|<span data-ttu-id="3e7e4-129">mutabilidad</span><span class="sxs-lookup"><span data-stu-id="3e7e4-129">mutability</span></span>     |<span data-ttu-id="3e7e4-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="3e7e4-130">String</span></span>     |<span data-ttu-id="3e7e4-131">Mutabilidad de un atributo.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-131">An attribute's mutability.</span></span> <span data-ttu-id="3e7e4-132">Los valores posibles son: `ReadWrite`, `ReadOnly`, `Immutable`, `WriteOnly`.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-132">Possible values are:  `ReadWrite`, `ReadOnly`, `Immutable`, `WriteOnly`.</span></span> <span data-ttu-id="3e7e4-133">El valor predeterminado es `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-133">Default is `ReadWrite`.</span></span>|
|<span data-ttu-id="3e7e4-134">name</span><span class="sxs-lookup"><span data-stu-id="3e7e4-134">name</span></span>           |<span data-ttu-id="3e7e4-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="3e7e4-135">String</span></span>     |<span data-ttu-id="3e7e4-136">Nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-136">Name of the attribute.</span></span> <span data-ttu-id="3e7e4-137">Debe ser único dentro de la definición del objeto.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-137">Must be unique within the object definition.</span></span> <span data-ttu-id="3e7e4-138">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-138">Not nullable.</span></span>|
|<span data-ttu-id="3e7e4-139">necesario</span><span class="sxs-lookup"><span data-stu-id="3e7e4-139">required</span></span>       |<span data-ttu-id="3e7e4-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="3e7e4-140">Boolean</span></span>    |<span data-ttu-id="3e7e4-141">`true`Si se requiere el atributo.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-141">`true` if attribute is required.</span></span> <span data-ttu-id="3e7e4-142">No se puede crear el objeto si falta alguno de los atributos necesarios.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-142">Object can not be created if any of the required attributes are missing.</span></span> <span data-ttu-id="3e7e4-143">Si durante la sincronización, el atributo required no tiene ningún valor, se usará el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-143">If during synchronization, the required attribute has no value, the default value will be used.</span></span> <span data-ttu-id="3e7e4-144">Si no se ha establecido el valor predeterminado, sincronización registrará un error.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-144">If default the value was not set, synchronization will record an error.</span></span>|
|<span data-ttu-id="3e7e4-145">referencedObjects</span><span class="sxs-lookup"><span data-stu-id="3e7e4-145">referencedObjects</span></span>|[<span data-ttu-id="3e7e4-146">referencedObject</span><span class="sxs-lookup"><span data-stu-id="3e7e4-146">referencedObject</span></span>](../resources/synchronization-referencedobject.md) |<span data-ttu-id="3e7e4-147">Para los atributos con `reference` escriba, objetos de listas que se hace referencia (por ejemplo, el `manager` mostrarían una lista de atributo `User` como el objeto que se hace referencia).</span><span class="sxs-lookup"><span data-stu-id="3e7e4-147">For attributes with `reference` type, lists referenced objects (for example, the `manager` attribute would list `User` as the referenced object).</span></span>|
|<span data-ttu-id="3e7e4-148">type</span><span class="sxs-lookup"><span data-stu-id="3e7e4-148">type</span></span>           |<span data-ttu-id="3e7e4-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="3e7e4-149">String</span></span>     |<span data-ttu-id="3e7e4-150">Tipo de valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-150">Attribute value type.</span></span> <span data-ttu-id="3e7e4-151">Valores posibles: `String`, `Integer`, `Reference`, `Binary`, `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-151">Possible values are: `String`, `Integer`, `Reference`, `Binary`, `Boolean`.</span></span> <span data-ttu-id="3e7e4-152">El valor predeterminado es `String`.</span><span class="sxs-lookup"><span data-stu-id="3e7e4-152">Default is `String`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3e7e4-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3e7e4-153">JSON representation</span></span>

<span data-ttu-id="3e7e4-154">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3e7e4-154">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeDefinition"
}-->

```json
{
  "anchor": true,
  "caseExact": true,
  "defaultValue": "String",
  "metadata": [{"@odata.type": "microsoft.graph.metadataEntry"}],
  "multivalued": true,
  "mutability": "String",
  "name": "String",
  "referencedObjects": [{"@odata.type": "microsoft.graph.referencedObject"}],
  "required": true,
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeDefinition resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
