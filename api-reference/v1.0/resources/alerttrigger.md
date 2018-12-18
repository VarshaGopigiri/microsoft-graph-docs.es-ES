---
title: tipo de recurso alertTrigger
description: Contiene información acerca de las propiedades que desencadena una detección (existen propiedades de la entidad de alerta).
author: Preetikr
ms.openlocfilehash: f0888e6caf78d806909f818a8b72fb21320e7796
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341272"
---
# <a name="alerttrigger-resource-type"></a><span data-ttu-id="d1059-103">tipo de recurso alertTrigger</span><span class="sxs-lookup"><span data-stu-id="d1059-103">alertTrigger resource type</span></span>

<span data-ttu-id="d1059-104">Contiene información acerca de las propiedades que desencadena una detección (existen propiedades de la entidad de alerta).</span><span class="sxs-lookup"><span data-stu-id="d1059-104">Contains information about the properties that triggered a detection (properties exist in the alert entity).</span></span>

## <a name="properties"></a><span data-ttu-id="d1059-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1059-105">Properties</span></span>

| <span data-ttu-id="d1059-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1059-106">Property</span></span>   | <span data-ttu-id="d1059-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1059-107">Type</span></span>|<span data-ttu-id="d1059-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1059-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d1059-109">name</span><span class="sxs-lookup"><span data-stu-id="d1059-109">name</span></span>|<span data-ttu-id="d1059-110">String</span><span class="sxs-lookup"><span data-stu-id="d1059-110">String</span></span>|<span data-ttu-id="d1059-111">Nombre de la propiedad que actúa como un desencadenador de detección.</span><span class="sxs-lookup"><span data-stu-id="d1059-111">Name of the property serving as a detection trigger.</span></span>|
|<span data-ttu-id="d1059-112">type</span><span class="sxs-lookup"><span data-stu-id="d1059-112">type</span></span>|<span data-ttu-id="d1059-113">String</span><span class="sxs-lookup"><span data-stu-id="d1059-113">String</span></span>|<span data-ttu-id="d1059-114">Tipo de la propiedad en el par de clave: valor de interpretación.</span><span class="sxs-lookup"><span data-stu-id="d1059-114">Type of the property in the key:value pair for interpretation.</span></span> <span data-ttu-id="d1059-115">Por ejemplo, String, Boolean, etcetera.</span><span class="sxs-lookup"><span data-stu-id="d1059-115">For example, String, Boolean, etc.</span></span>|
|<span data-ttu-id="d1059-116">valor</span><span class="sxs-lookup"><span data-stu-id="d1059-116">value</span></span>|<span data-ttu-id="d1059-117">String</span><span class="sxs-lookup"><span data-stu-id="d1059-117">String</span></span>|<span data-ttu-id="d1059-118">Valor de la propiedad que actúa como un desencadenador de detección.</span><span class="sxs-lookup"><span data-stu-id="d1059-118">Value of the property serving as a detection trigger.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d1059-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1059-119">JSON representation</span></span>

<span data-ttu-id="d1059-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d1059-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.alertTrigger"
}-->

```json
{
  "name": "String",
  "type": "String",
  "value": "String"
}

```

## <a name="example"></a><span data-ttu-id="d1059-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1059-121">Example</span></span>

```json
{
  "name": "hostState.privateIpAddress",
  "type": "String",
  "value": "10.154.9.40"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alertTrigger resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->