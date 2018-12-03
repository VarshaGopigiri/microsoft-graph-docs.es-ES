---
title: tipo de recurso attributeMapping
description: Define cómo deben flujo de valores para el atributo de destino determinada durante la sincronización.
ms.openlocfilehash: e4fd8ba0aece448f358d51373dfca0157759a23e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086514"
---
# <a name="attributemapping-resource-type"></a><span data-ttu-id="c377b-103">tipo de recurso attributeMapping</span><span class="sxs-lookup"><span data-stu-id="c377b-103">attributeMapping resource type</span></span>

> <span data-ttu-id="c377b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c377b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c377b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c377b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c377b-106">Define cómo deben flujo de valores para el atributo de destino determinada durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="c377b-106">Defines how values for the given target attribute should flow during synchronization.</span></span>

## <a name="properties"></a><span data-ttu-id="c377b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c377b-107">Properties</span></span>

| <span data-ttu-id="c377b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c377b-108">Property</span></span>                  | <span data-ttu-id="c377b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c377b-109">Type</span></span>                      | <span data-ttu-id="c377b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c377b-110">Description</span></span>    |
|:--------------------------|:--------------------------|:---------------|
|<span data-ttu-id="c377b-111">defaultValue</span><span class="sxs-lookup"><span data-stu-id="c377b-111">defaultValue</span></span>               | <span data-ttu-id="c377b-112">String</span><span class="sxs-lookup"><span data-stu-id="c377b-112">String</span></span>                    |<span data-ttu-id="c377b-113">Valor que se usará en caso de que la propiedad de **origen** se evalúa a predeterminado `null`.</span><span class="sxs-lookup"><span data-stu-id="c377b-113">Default value to be used in case the **source** property was evaluated to `null`.</span></span> <span data-ttu-id="c377b-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c377b-114">Optional.</span></span>|
|<span data-ttu-id="c377b-115">exportMissingReferences</span><span class="sxs-lookup"><span data-stu-id="c377b-115">exportMissingReferences</span></span>    |<span data-ttu-id="c377b-116">String</span><span class="sxs-lookup"><span data-stu-id="c377b-116">String</span></span>                     |<span data-ttu-id="c377b-117">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="c377b-117">For internal use only.</span></span>|
|<span data-ttu-id="c377b-118">flowBehavior</span><span class="sxs-lookup"><span data-stu-id="c377b-118">flowBehavior</span></span>               |<span data-ttu-id="c377b-119">attributeFlowBehavior</span><span class="sxs-lookup"><span data-stu-id="c377b-119">attributeFlowBehavior</span></span>      |<span data-ttu-id="c377b-120">Define cuándo se debe exportar este atributo en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="c377b-120">Defines when this attribute should be exported to the target directory.</span></span> <span data-ttu-id="c377b-121">Los valores posibles son: `FlowWhenChanged` y `FlowAlways`.</span><span class="sxs-lookup"><span data-stu-id="c377b-121">Possible values are: `FlowWhenChanged` and `FlowAlways`.</span></span> <span data-ttu-id="c377b-122">El valor predeterminado es `FlowWhenChanged`.</span><span class="sxs-lookup"><span data-stu-id="c377b-122">Default is `FlowWhenChanged`.</span></span> |
|<span data-ttu-id="c377b-123">Tasa</span><span class="sxs-lookup"><span data-stu-id="c377b-123">flowType</span></span>                   |<span data-ttu-id="c377b-124">attributeFlowType</span><span class="sxs-lookup"><span data-stu-id="c377b-124">attributeFlowType</span></span>          |<span data-ttu-id="c377b-125">Define cuándo debe actualizarse este atributo en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="c377b-125">Defines when this attribute should be updated in the target directory.</span></span> <span data-ttu-id="c377b-126">Los valores posibles son: `Always` (valor predeterminado), `ObjectAddOnly` (sólo cuando se crea un objeto nuevo), `MultiValueAddOnly` (sólo cuando el cambio va a agregar nuevos valores a un atributo de varios valores).</span><span class="sxs-lookup"><span data-stu-id="c377b-126">Possible values are: `Always` (default), `ObjectAddOnly` (only when new object is created), `MultiValueAddOnly` (only when the change is adding new values to a multi-valued attribute).</span></span> |
|<span data-ttu-id="c377b-127">matchingPriority</span><span class="sxs-lookup"><span data-stu-id="c377b-127">matchingPriority</span></span>           |<span data-ttu-id="c377b-128">Int32</span><span class="sxs-lookup"><span data-stu-id="c377b-128">Int32</span></span>                      |<span data-ttu-id="c377b-129">Si es mayor que 0, se usará este atributo para llevar a cabo a una coincidencia inicial de los objetos entre los directorios de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="c377b-129">If higher than 0, this attribute will be used to perform an initial match of the objects between source and target directories.</span></span> <span data-ttu-id="c377b-130">El motor de sincronización intentará buscar el objeto que coincida con el atributo con el valor más bajo de coincidencia prioridad en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="c377b-130">The synchronization engine will try to find the matching object using attribute with lowest value of matching priority first.</span></span> <span data-ttu-id="c377b-131">Si no se ha encontrado el atributo con la siguiente prioridad coincidente se va a usar y así sucesivamente un hasta que se encuentra coincidencia o se dejan no más atributos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="c377b-131">If not found, the attribute with the next matching priority will be used, and so on a until match is found or no more matching attributes are left.</span></span> <span data-ttu-id="c377b-132">Sólo los atributos que se espera que tienen valores únicos, como correo electrónico, deben usarse como atributos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="c377b-132">Only attributes that are expected to have unique values, such as email, should be used as matching attributes.</span></span>|
|<span data-ttu-id="c377b-133">source</span><span class="sxs-lookup"><span data-stu-id="c377b-133">source</span></span>                     |[<span data-ttu-id="c377b-134">attributeMappingSource</span><span class="sxs-lookup"><span data-stu-id="c377b-134">attributeMappingSource</span></span>](synchronization-attributemappingsource.md)     | <span data-ttu-id="c377b-135">Define cómo debe ser un valor extrajo (o transforma) desde el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="c377b-135">Defines how a value should be extracted (or transformed) from the source object.</span></span> |
|<span data-ttu-id="c377b-136">/TargetAttributeName</span><span class="sxs-lookup"><span data-stu-id="c377b-136">targetAttributeName</span></span>        |<span data-ttu-id="c377b-137">String</span><span class="sxs-lookup"><span data-stu-id="c377b-137">String</span></span>                     |<span data-ttu-id="c377b-138">Nombre del atributo en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c377b-138">Name of the attribute on the target object.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="c377b-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c377b-139">JSON representation</span></span>

<span data-ttu-id="c377b-140">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="c377b-140">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMapping"
}-->

```json
{
  "defaultValue": "String",
  "exportMissingReferences": true,
  "flowBehavior": "String",
  "flowType": "String",
  "matchingPriority": 1024,
  "source": {"@odata.type": "microsoft.graph.attributeMappingSource"},
  "targetAttributeName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMapping resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->