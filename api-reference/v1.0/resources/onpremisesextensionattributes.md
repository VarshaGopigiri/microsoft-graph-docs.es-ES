---
title: tipo de recurso onPremisesExtensionAttributes
description: La propiedad **onPremisesExtensionAttributes** de la entidad de usuario contiene quince las propiedades de atributo de extensión personalizada. Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura. Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.
ms.openlocfilehash: e5a56b5a846cf48cfc819b6d884689be10d6992e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030834"
---
# <a name="onpremisesextensionattributes-resource-type"></a><span data-ttu-id="7006b-105">tipo de recurso onPremisesExtensionAttributes</span><span class="sxs-lookup"><span data-stu-id="7006b-105">onPremisesExtensionAttributes resource type</span></span>

<span data-ttu-id="7006b-106">La propiedad **onPremisesExtensionAttributes** de la entidad de [usuario](user.md) contiene quince las propiedades de atributo de extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="7006b-106">The **onPremisesExtensionAttributes** property of the [user](user.md) entity contains fifteen custom extension attribute properties.</span></span> <span data-ttu-id="7006b-107">Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="7006b-107">For an **onPremisesSyncEnabled** user, this set of properties is mastered in on-premises Active Directory and synchronized to Azure AD, and is read-only.</span></span> <span data-ttu-id="7006b-108">Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.</span><span class="sxs-lookup"><span data-stu-id="7006b-108">For a cloud-only user (where **onPremisesSyncEnabled** is false), these properties may be set during creation or update.</span></span>


## <a name="properties"></a><span data-ttu-id="7006b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7006b-109">Properties</span></span>
| <span data-ttu-id="7006b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7006b-110">Property</span></span>     | <span data-ttu-id="7006b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7006b-111">Type</span></span>   |<span data-ttu-id="7006b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7006b-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7006b-113">extensionAttribute1</span><span class="sxs-lookup"><span data-stu-id="7006b-113">extensionAttribute1</span></span>|<span data-ttu-id="7006b-114">String</span><span class="sxs-lookup"><span data-stu-id="7006b-114">String</span></span>| <span data-ttu-id="7006b-115">Primer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-115">First customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-116">extensionAttribute2</span><span class="sxs-lookup"><span data-stu-id="7006b-116">extensionAttribute2</span></span>|<span data-ttu-id="7006b-117">String</span><span class="sxs-lookup"><span data-stu-id="7006b-117">String</span></span>| <span data-ttu-id="7006b-118">Segundo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-118">Second customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-119">extensionAttribute3</span><span class="sxs-lookup"><span data-stu-id="7006b-119">extensionAttribute3</span></span>|<span data-ttu-id="7006b-120">String</span><span class="sxs-lookup"><span data-stu-id="7006b-120">String</span></span>| <span data-ttu-id="7006b-121">Tercer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-121">Third customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-122">extensionAttribute4</span><span class="sxs-lookup"><span data-stu-id="7006b-122">extensionAttribute4</span></span>|<span data-ttu-id="7006b-123">String</span><span class="sxs-lookup"><span data-stu-id="7006b-123">String</span></span>| <span data-ttu-id="7006b-124">Cuarto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-124">Fourth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-125">extensionAttribute5</span><span class="sxs-lookup"><span data-stu-id="7006b-125">extensionAttribute5</span></span>|<span data-ttu-id="7006b-126">String</span><span class="sxs-lookup"><span data-stu-id="7006b-126">String</span></span>| <span data-ttu-id="7006b-127">Atributo de extensión personalizable quinto.</span><span class="sxs-lookup"><span data-stu-id="7006b-127">Fifth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-128">extensionAttribute6</span><span class="sxs-lookup"><span data-stu-id="7006b-128">extensionAttribute6</span></span>|<span data-ttu-id="7006b-129">String</span><span class="sxs-lookup"><span data-stu-id="7006b-129">String</span></span>| <span data-ttu-id="7006b-130">Atributo de extensión personalizable sexto.</span><span class="sxs-lookup"><span data-stu-id="7006b-130">Sixth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-131">extensionAttribute7</span><span class="sxs-lookup"><span data-stu-id="7006b-131">extensionAttribute7</span></span>|<span data-ttu-id="7006b-132">String</span><span class="sxs-lookup"><span data-stu-id="7006b-132">String</span></span>| <span data-ttu-id="7006b-133">Séptimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-133">Seventh customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-134">extensionAttribute8</span><span class="sxs-lookup"><span data-stu-id="7006b-134">extensionAttribute8</span></span>|<span data-ttu-id="7006b-135">String</span><span class="sxs-lookup"><span data-stu-id="7006b-135">String</span></span>| <span data-ttu-id="7006b-136">Atributo de extensión personalizable octavo.</span><span class="sxs-lookup"><span data-stu-id="7006b-136">Eighth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-137">extensionAttribute9</span><span class="sxs-lookup"><span data-stu-id="7006b-137">extensionAttribute9</span></span>|<span data-ttu-id="7006b-138">String</span><span class="sxs-lookup"><span data-stu-id="7006b-138">String</span></span>| <span data-ttu-id="7006b-139">Noveno atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-139">Ninth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-140">extensionAttribute10</span><span class="sxs-lookup"><span data-stu-id="7006b-140">extensionAttribute10</span></span>|<span data-ttu-id="7006b-141">String</span><span class="sxs-lookup"><span data-stu-id="7006b-141">String</span></span>| <span data-ttu-id="7006b-142">Décimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-142">Tenth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-143">extensionAttribute11</span><span class="sxs-lookup"><span data-stu-id="7006b-143">extensionAttribute11</span></span>|<span data-ttu-id="7006b-144">String</span><span class="sxs-lookup"><span data-stu-id="7006b-144">String</span></span>| <span data-ttu-id="7006b-145">Atributo de extensión undécima personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-145">Eleventh customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-146">extensionAttribute12</span><span class="sxs-lookup"><span data-stu-id="7006b-146">extensionAttribute12</span></span>|<span data-ttu-id="7006b-147">String</span><span class="sxs-lookup"><span data-stu-id="7006b-147">String</span></span>| <span data-ttu-id="7006b-148">Atributo de extensión duodécima personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-148">Twelfth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-149">extensionAttribute13</span><span class="sxs-lookup"><span data-stu-id="7006b-149">extensionAttribute13</span></span>|<span data-ttu-id="7006b-150">String</span><span class="sxs-lookup"><span data-stu-id="7006b-150">String</span></span>| <span data-ttu-id="7006b-151">Atributo de extensión Decimotercera personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-151">Thirteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-152">extensionAttribute14</span><span class="sxs-lookup"><span data-stu-id="7006b-152">extensionAttribute14</span></span>|<span data-ttu-id="7006b-153">String</span><span class="sxs-lookup"><span data-stu-id="7006b-153">String</span></span>| <span data-ttu-id="7006b-154">Atributo de extensión decimocuarta personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-154">Fourteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="7006b-155">extensionAttribute15</span><span class="sxs-lookup"><span data-stu-id="7006b-155">extensionAttribute15</span></span>|<span data-ttu-id="7006b-156">String</span><span class="sxs-lookup"><span data-stu-id="7006b-156">String</span></span>| <span data-ttu-id="7006b-157">Atributo de extensión decimoquinta personalizable.</span><span class="sxs-lookup"><span data-stu-id="7006b-157">Fifteenth customizable extension attribute.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="7006b-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7006b-158">JSON representation</span></span>

<span data-ttu-id="7006b-159">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7006b-159">Here is a JSON representation of the resource</span></span>

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