---
title: tipo de recurso referencedObject
description: Describe una referencia a otro objeto definido en la misma definición de Active directory.
ms.openlocfilehash: 63645048fd8ba6ad949da43baa261b2842ea4016
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090373"
---
# <a name="referencedobject-resource-type"></a><span data-ttu-id="8996f-103">tipo de recurso referencedObject</span><span class="sxs-lookup"><span data-stu-id="8996f-103">referencedObject resource type</span></span>

> <span data-ttu-id="8996f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8996f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8996f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8996f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8996f-106">Describe una referencia a otro objeto definido en la misma [definición de Active directory](synchronization-directorydefinition.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-106">Describes a reference to another object defined in the same [directory definition](synchronization-directorydefinition.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8996f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8996f-107">Properties</span></span>

| <span data-ttu-id="8996f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8996f-108">Property</span></span>                   | <span data-ttu-id="8996f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8996f-109">Type</span></span>                      | <span data-ttu-id="8996f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8996f-110">Description</span></span>    |
|:---------------------------|:--------------------------|:---------------|
|<span data-ttu-id="8996f-111">referencedObjectName</span><span class="sxs-lookup"><span data-stu-id="8996f-111">referencedObjectName</span></span>        |<span data-ttu-id="8996f-112">String</span><span class="sxs-lookup"><span data-stu-id="8996f-112">String</span></span>                     |<span data-ttu-id="8996f-113">Nombre del objeto que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="8996f-113">Name of the referenced object.</span></span> <span data-ttu-id="8996f-114">Debe coincidir con uno de los objetos en la [definición de Active directory](synchronization-directorydefinition.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-114">Must match one of the objects in the [directory definition](synchronization-directorydefinition.md).</span></span>|
|<span data-ttu-id="8996f-115">referencedProperty</span><span class="sxs-lookup"><span data-stu-id="8996f-115">referencedProperty</span></span>          |<span data-ttu-id="8996f-116">String</span><span class="sxs-lookup"><span data-stu-id="8996f-116">String</span></span>                     |<span data-ttu-id="8996f-117">**Actualmente no se admite**.</span><span class="sxs-lookup"><span data-stu-id="8996f-117">**Currently not supported**.</span></span> <span data-ttu-id="8996f-118">Nombre de la propiedad en el objeto de referencia, el valor para el que se usa como referencia.</span><span class="sxs-lookup"><span data-stu-id="8996f-118">Name of the property in the referenced object, the value for which is used as the reference.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8996f-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8996f-119">JSON representation</span></span>

<span data-ttu-id="8996f-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8996f-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.referencedObject"
}-->

```json
{
  "referencedObjectName": "String",
  "referencedProperty": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "referencedObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
            