---
title: tipo de recurso synchronizationRule
description: Define cómo se debe realizar la sincronización para el motor de sincronización, incluidos los objetos que desea sincronizar y en qué dirección, cómo los objetos desde el directorio de origen deben coincidir con los objetos en el directorio de destino y cómo los atributos debe transformarse cuando se está sincronizando desde el origen al directorio de destino.
ms.openlocfilehash: c860228637a6cc3ad9137851408379bd7f779c75
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085080"
---
# <a name="synchronizationrule-resource-type"></a><span data-ttu-id="1b377-103">tipo de recurso synchronizationRule</span><span class="sxs-lookup"><span data-stu-id="1b377-103">synchronizationRule resource type</span></span>

> <span data-ttu-id="1b377-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1b377-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1b377-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1b377-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1b377-106">Define cómo se debe realizar la sincronización para el motor de sincronización, incluidos los objetos que desea sincronizar y en qué dirección, cómo los objetos desde el directorio de origen deben coincidir con los objetos en el directorio de destino y cómo los atributos debe transformarse cuando se está sincronizando desde el origen al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="1b377-106">Defines how the synchronization should be performed for the synchronization engine, including which objects to synchronize and in which direction, how objects from the source directory should be matched with objects in the target directory, and how attributes should be transformed when they're synchronized from the source to the target directory.</span></span>

><span data-ttu-id="1b377-107">**Nota:** Reglas de sincronización definición sincronización en una dirección - desde el directorio de origen al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="1b377-107">**Note:** Synchronization rules define synchronization in one direction - from the source directory to the target directory.</span></span> <span data-ttu-id="1b377-108">Los directorios de origen y de destino se definen como parte de las propiedades de la regla.</span><span class="sxs-lookup"><span data-stu-id="1b377-108">The source and target directories are defined as part of the rule properties.</span></span>

<span data-ttu-id="1b377-109">Reglas de sincronización se actualizan como parte del [esquema de sincronización](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="1b377-109">Synchronization rules are updated as part of the [synchronization schema](synchronization-synchronizationschema.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1b377-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b377-110">Properties</span></span>

| <span data-ttu-id="1b377-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1b377-111">Property</span></span>      | <span data-ttu-id="1b377-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b377-112">Type</span></span>      | <span data-ttu-id="1b377-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b377-113">Description</span></span>    |
|:--------------|:----------|:---------------|
|<span data-ttu-id="1b377-114">editable</span><span class="sxs-lookup"><span data-stu-id="1b377-114">editable</span></span>       |<span data-ttu-id="1b377-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="1b377-115">Boolean</span></span>    |<span data-ttu-id="1b377-116">`true`Si la regla de sincronización se puede personalizar; `false` si esta regla es de sólo lectura y no se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="1b377-116">`true` if the synchronization rule can be customized; `false` if this rule is read-only and should not be changed.</span></span>|
|<span data-ttu-id="1b377-117">id</span><span class="sxs-lookup"><span data-stu-id="1b377-117">id</span></span>             |<span data-ttu-id="1b377-118">String</span><span class="sxs-lookup"><span data-stu-id="1b377-118">String</span></span>     |<span data-ttu-id="1b377-119">Identificador de regla de sincronización.</span><span class="sxs-lookup"><span data-stu-id="1b377-119">Synchronization rule identifier.</span></span> <span data-ttu-id="1b377-120">Debe ser uno de los identificadores reconocidos por el motor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="1b377-120">Must be one of the identifiers recognized by the synchronization engine.</span></span> <span data-ttu-id="1b377-121">Admite la regla de identificadores pueden encontrarse en la plantilla de sincronización devuelta por la API.</span><span class="sxs-lookup"><span data-stu-id="1b377-121">Supported rule identifiers can be found in the synchronization template returned by the API.</span></span>|
|<span data-ttu-id="1b377-122">metadatos</span><span class="sxs-lookup"><span data-stu-id="1b377-122">metadata</span></span>       |<span data-ttu-id="1b377-123">colección de [stringKeyStringValuePair](synchronization-stringkeystringvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="1b377-123">[stringKeyStringValuePair](synchronization-stringkeystringvaluepair.md) collection</span></span> |<span data-ttu-id="1b377-124">Propiedades de extensión adicionales.</span><span class="sxs-lookup"><span data-stu-id="1b377-124">Additional extension properties.</span></span> <span data-ttu-id="1b377-125">A menos que así lo indique explícitamente el equipo de soporte técnico, no se deben cambiar los valores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="1b377-125">Unless instructed explicitly by the support team, metadata values should not be changed.</span></span>|
|<span data-ttu-id="1b377-126">name</span><span class="sxs-lookup"><span data-stu-id="1b377-126">name</span></span>           |<span data-ttu-id="1b377-127">String</span><span class="sxs-lookup"><span data-stu-id="1b377-127">String</span></span>     |<span data-ttu-id="1b377-128">Nombre legible de la regla de sincronización.</span><span class="sxs-lookup"><span data-stu-id="1b377-128">Human-readable name of the synchronization rule.</span></span> <span data-ttu-id="1b377-129">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="1b377-129">Not nullable.</span></span>|
|<span data-ttu-id="1b377-130">objectMappings</span><span class="sxs-lookup"><span data-stu-id="1b377-130">objectMappings</span></span> |<span data-ttu-id="1b377-131">colección de [objectMapping](synchronization-objectmapping.md)</span><span class="sxs-lookup"><span data-stu-id="1b377-131">[objectMapping](synchronization-objectmapping.md) collection</span></span>    |<span data-ttu-id="1b377-132">Colección de asignaciones de objeto admitidos por la regla.</span><span class="sxs-lookup"><span data-stu-id="1b377-132">Collection of object mappings supported by the rule.</span></span> <span data-ttu-id="1b377-133">Indica al motor de sincronización los objetos que se deben sincronizar.</span><span class="sxs-lookup"><span data-stu-id="1b377-133">Tells the synchronization engine which objects should be synchronized.</span></span>|
|<span data-ttu-id="1b377-134">prioridad</span><span class="sxs-lookup"><span data-stu-id="1b377-134">priority</span></span>       |<span data-ttu-id="1b377-135">Entero</span><span class="sxs-lookup"><span data-stu-id="1b377-135">Integer</span></span>    |<span data-ttu-id="1b377-136">Prioridad con respecto a las demás reglas en la [synchronizationSchema](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="1b377-136">Priority relative to other rules in the [synchronizationSchema](synchronization-synchronizationschema.md).</span></span> <span data-ttu-id="1b377-137">En primer lugar se procesarán las reglas con el número de prioridad más baja.</span><span class="sxs-lookup"><span data-stu-id="1b377-137">Rules with the lowest priority number will be processed first.</span></span>|
|<span data-ttu-id="1b377-138">sourceDirectoryName</span><span class="sxs-lookup"><span data-stu-id="1b377-138">sourceDirectoryName</span></span>       |<span data-ttu-id="1b377-139">String</span><span class="sxs-lookup"><span data-stu-id="1b377-139">String</span></span>    |<span data-ttu-id="1b377-140">Nombre del directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="1b377-140">Name of the source directory.</span></span> <span data-ttu-id="1b377-141">Debe coincidir con una de las definiciones de Active directory en [synchronizationSchema](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="1b377-141">Must match one of the directory definitions in [synchronizationSchema](synchronization-synchronizationschema.md).</span></span>|
|<span data-ttu-id="1b377-142">targetDirectoryName</span><span class="sxs-lookup"><span data-stu-id="1b377-142">targetDirectoryName</span></span>       |<span data-ttu-id="1b377-143">String</span><span class="sxs-lookup"><span data-stu-id="1b377-143">String</span></span>    |<span data-ttu-id="1b377-144">Nombre del directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="1b377-144">Name of the target directory.</span></span> <span data-ttu-id="1b377-145">Debe coincidir con una de las definiciones de Active directory en [synchronizationSchema](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="1b377-145">Must match one of the directory definitions in [synchronizationSchema](synchronization-synchronizationschema.md).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1b377-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1b377-146">JSON representation</span></span>

<span data-ttu-id="1b377-147">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1b377-147">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationRule"
}-->

```json
{
  "editable": true,
  "id": "String",
  "metadata": [{"@odata.type": "microsoft.graph.stringKeyStringValuePair"}],
  "name": "String",
  "objectMappings": [{"@odata.type": "microsoft.graph.objectMapping"}],
  "priority": 1024,
  "sourceDirectoryName": "String",
  "targetDirectoryName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->