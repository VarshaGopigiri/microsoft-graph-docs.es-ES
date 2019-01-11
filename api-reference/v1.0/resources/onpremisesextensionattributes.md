---
title: tipo de recurso onPremisesExtensionAttributes
description: La propiedad **onPremisesExtensionAttributes** de la entidad de usuario contiene quince las propiedades de atributo de extensión personalizada. Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura. Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.
localization_priority: Normal
ms.openlocfilehash: c0cb765efe9e94c8254e45eaa9d55bc16382f6d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824748"
---
# <a name="onpremisesextensionattributes-resource-type"></a><span data-ttu-id="83e72-105">tipo de recurso onPremisesExtensionAttributes</span><span class="sxs-lookup"><span data-stu-id="83e72-105">onPremisesExtensionAttributes resource type</span></span>

<span data-ttu-id="83e72-106">La propiedad **onPremisesExtensionAttributes** de la entidad de [usuario](user.md) contiene quince las propiedades de atributo de extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="83e72-106">The **onPremisesExtensionAttributes** property of the [user](user.md) entity contains fifteen custom extension attribute properties.</span></span> <span data-ttu-id="83e72-107">Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="83e72-107">For an **onPremisesSyncEnabled** user, this set of properties is mastered in on-premises Active Directory and synchronized to Azure AD, and is read-only.</span></span> <span data-ttu-id="83e72-108">Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.</span><span class="sxs-lookup"><span data-stu-id="83e72-108">For a cloud-only user (where **onPremisesSyncEnabled** is false), these properties may be set during creation or update.</span></span>


## <a name="properties"></a><span data-ttu-id="83e72-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83e72-109">Properties</span></span>
| <span data-ttu-id="83e72-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="83e72-110">Property</span></span>     | <span data-ttu-id="83e72-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="83e72-111">Type</span></span>   |<span data-ttu-id="83e72-112">Description</span><span class="sxs-lookup"><span data-stu-id="83e72-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="83e72-113">extensionAttribute1</span><span class="sxs-lookup"><span data-stu-id="83e72-113">extensionAttribute1</span></span>|<span data-ttu-id="83e72-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-114">String</span></span>| <span data-ttu-id="83e72-115">Primer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-115">First customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-116">extensionAttribute2</span><span class="sxs-lookup"><span data-stu-id="83e72-116">extensionAttribute2</span></span>|<span data-ttu-id="83e72-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-117">String</span></span>| <span data-ttu-id="83e72-118">Segundo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-118">Second customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-119">extensionAttribute3</span><span class="sxs-lookup"><span data-stu-id="83e72-119">extensionAttribute3</span></span>|<span data-ttu-id="83e72-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-120">String</span></span>| <span data-ttu-id="83e72-121">Tercer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-121">Third customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-122">extensionAttribute4</span><span class="sxs-lookup"><span data-stu-id="83e72-122">extensionAttribute4</span></span>|<span data-ttu-id="83e72-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-123">String</span></span>| <span data-ttu-id="83e72-124">Cuarto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-124">Fourth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-125">extensionAttribute5</span><span class="sxs-lookup"><span data-stu-id="83e72-125">extensionAttribute5</span></span>|<span data-ttu-id="83e72-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-126">String</span></span>| <span data-ttu-id="83e72-127">Atributo de extensión personalizable quinto.</span><span class="sxs-lookup"><span data-stu-id="83e72-127">Fifth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-128">extensionAttribute6</span><span class="sxs-lookup"><span data-stu-id="83e72-128">extensionAttribute6</span></span>|<span data-ttu-id="83e72-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-129">String</span></span>| <span data-ttu-id="83e72-130">Atributo de extensión personalizable sexto.</span><span class="sxs-lookup"><span data-stu-id="83e72-130">Sixth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-131">extensionAttribute7</span><span class="sxs-lookup"><span data-stu-id="83e72-131">extensionAttribute7</span></span>|<span data-ttu-id="83e72-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-132">String</span></span>| <span data-ttu-id="83e72-133">Séptimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-133">Seventh customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-134">extensionAttribute8</span><span class="sxs-lookup"><span data-stu-id="83e72-134">extensionAttribute8</span></span>|<span data-ttu-id="83e72-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-135">String</span></span>| <span data-ttu-id="83e72-136">Atributo de extensión personalizable octavo.</span><span class="sxs-lookup"><span data-stu-id="83e72-136">Eighth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-137">extensionAttribute9</span><span class="sxs-lookup"><span data-stu-id="83e72-137">extensionAttribute9</span></span>|<span data-ttu-id="83e72-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-138">String</span></span>| <span data-ttu-id="83e72-139">Noveno atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-139">Ninth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-140">extensionAttribute10</span><span class="sxs-lookup"><span data-stu-id="83e72-140">extensionAttribute10</span></span>|<span data-ttu-id="83e72-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-141">String</span></span>| <span data-ttu-id="83e72-142">Décimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-142">Tenth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-143">extensionAttribute11</span><span class="sxs-lookup"><span data-stu-id="83e72-143">extensionAttribute11</span></span>|<span data-ttu-id="83e72-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-144">String</span></span>| <span data-ttu-id="83e72-145">Atributo de extensión undécima personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-145">Eleventh customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-146">extensionAttribute12</span><span class="sxs-lookup"><span data-stu-id="83e72-146">extensionAttribute12</span></span>|<span data-ttu-id="83e72-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-147">String</span></span>| <span data-ttu-id="83e72-148">Atributo de extensión duodécima personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-148">Twelfth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-149">extensionAttribute13</span><span class="sxs-lookup"><span data-stu-id="83e72-149">extensionAttribute13</span></span>|<span data-ttu-id="83e72-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-150">String</span></span>| <span data-ttu-id="83e72-151">Atributo de extensión Decimotercera personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-151">Thirteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-152">extensionAttribute14</span><span class="sxs-lookup"><span data-stu-id="83e72-152">extensionAttribute14</span></span>|<span data-ttu-id="83e72-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-153">String</span></span>| <span data-ttu-id="83e72-154">Atributo de extensión decimocuarta personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-154">Fourteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="83e72-155">extensionAttribute15</span><span class="sxs-lookup"><span data-stu-id="83e72-155">extensionAttribute15</span></span>|<span data-ttu-id="83e72-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="83e72-156">String</span></span>| <span data-ttu-id="83e72-157">Atributo de extensión decimoquinta personalizable.</span><span class="sxs-lookup"><span data-stu-id="83e72-157">Fifteenth customizable extension attribute.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="83e72-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="83e72-158">JSON representation</span></span>

<span data-ttu-id="83e72-159">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="83e72-159">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesExtensionAttributes"
}-->


```json
{
      "extensionAttribute1": "string",
      "extensionAttribute2": "string",
      "extensionAttribute3": "string",
      "extensionAttribute4": "string",
      "extensionAttribute5": "string",
      "extensionAttribute6": "string",
      "extensionAttribute7": "string",
      "extensionAttribute8": "string",
      "extensionAttribute9": "string",
      "extensionAttribute10": "string",
      "extensionAttribute11": "string",
      "extensionAttribute12": "string",
      "extensionAttribute13": "string",
      "extensionAttribute14": "string",
      "extensionAttribute15": "string"
  }

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesExtensionAttributes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
