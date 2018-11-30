---
title: tipo de recurso alertTrigger
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 353f7dd09b11a2bfc509b53665c7f13ec390c80a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083145"
---
# <a name="alerttrigger-resource-type"></a><span data-ttu-id="25b79-104">tipo de recurso alertTrigger</span><span class="sxs-lookup"><span data-stu-id="25b79-104">alertTrigger resource type</span></span>

 > <span data-ttu-id="25b79-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="25b79-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="25b79-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="25b79-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="25b79-107">Contiene información acerca de las propiedades que desencadena una detección (existen propiedades de la entidad de alerta).</span><span class="sxs-lookup"><span data-stu-id="25b79-107">Contains information about the properties that triggered a detection (properties exist in the alert entity).</span></span>

## <a name="properties"></a><span data-ttu-id="25b79-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25b79-108">Properties</span></span>

| <span data-ttu-id="25b79-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25b79-109">Property</span></span>   | <span data-ttu-id="25b79-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="25b79-110">Type</span></span>|<span data-ttu-id="25b79-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="25b79-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25b79-112">name</span><span class="sxs-lookup"><span data-stu-id="25b79-112">name</span></span>|<span data-ttu-id="25b79-113">String</span><span class="sxs-lookup"><span data-stu-id="25b79-113">String</span></span>|<span data-ttu-id="25b79-114">Nombre de la propiedad que actúa como un desencadenador de detección.</span><span class="sxs-lookup"><span data-stu-id="25b79-114">Name of the property serving as a detection trigger.</span></span>|
|<span data-ttu-id="25b79-115">type</span><span class="sxs-lookup"><span data-stu-id="25b79-115">type</span></span>|<span data-ttu-id="25b79-116">String</span><span class="sxs-lookup"><span data-stu-id="25b79-116">String</span></span>|<span data-ttu-id="25b79-117">Tipo de la propiedad en el par de clave: valor de interpretación.</span><span class="sxs-lookup"><span data-stu-id="25b79-117">Type of the property in the key:value pair for interpretation.</span></span> <span data-ttu-id="25b79-118">Por ejemplo, String, Boolean, etcetera.</span><span class="sxs-lookup"><span data-stu-id="25b79-118">For example, String, Boolean, etc.</span></span>|
|<span data-ttu-id="25b79-119">valor</span><span class="sxs-lookup"><span data-stu-id="25b79-119">value</span></span>|<span data-ttu-id="25b79-120">String</span><span class="sxs-lookup"><span data-stu-id="25b79-120">String</span></span>|<span data-ttu-id="25b79-121">Valor de la propiedad que actúa como un desencadenador de detección.</span><span class="sxs-lookup"><span data-stu-id="25b79-121">Value of the property serving as a detection trigger.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="25b79-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25b79-122">JSON representation</span></span>

<span data-ttu-id="25b79-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="25b79-123">The following is a JSON representation of the resource.</span></span>

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

## <a name="example"></a><span data-ttu-id="25b79-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25b79-124">Example</span></span>

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
