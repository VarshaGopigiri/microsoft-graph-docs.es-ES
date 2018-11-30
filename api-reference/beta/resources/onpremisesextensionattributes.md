---
title: tipo de recurso onPremisesExtensionAttributes
description: La propiedad **onPremisesExtensionAttributes** de la entidad de usuario contiene quince las propiedades de atributo de extensión personalizada. Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura. Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.
ms.openlocfilehash: 547fc8ac19059611f5983a8b5ee0bd905f130f79
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088637"
---
# <a name="onpremisesextensionattributes-resource-type"></a><span data-ttu-id="998bb-105">tipo de recurso onPremisesExtensionAttributes</span><span class="sxs-lookup"><span data-stu-id="998bb-105">onPremisesExtensionAttributes resource type</span></span>

> <span data-ttu-id="998bb-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="998bb-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="998bb-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="998bb-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="998bb-108">La propiedad **onPremisesExtensionAttributes** de la entidad de [usuario](user.md) contiene quince las propiedades de atributo de extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="998bb-108">The **onPremisesExtensionAttributes** property of the [user](user.md) entity contains fifteen custom extension attribute properties.</span></span> <span data-ttu-id="998bb-109">Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="998bb-109">For an **onPremisesSyncEnabled** user, this set of properties is mastered in on-premises Active Directory and synchronized to Azure AD, and is read-only.</span></span> <span data-ttu-id="998bb-110">Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.</span><span class="sxs-lookup"><span data-stu-id="998bb-110">For a cloud-only user (where **onPremisesSyncEnabled** is false), these properties may be set during creation or update.</span></span>


## <a name="properties"></a><span data-ttu-id="998bb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="998bb-111">Properties</span></span>
| <span data-ttu-id="998bb-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="998bb-112">Property</span></span>     | <span data-ttu-id="998bb-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="998bb-113">Type</span></span>   |<span data-ttu-id="998bb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="998bb-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="998bb-115">extensionAttribute1</span><span class="sxs-lookup"><span data-stu-id="998bb-115">extensionAttribute1</span></span>|<span data-ttu-id="998bb-116">String</span><span class="sxs-lookup"><span data-stu-id="998bb-116">String</span></span>| <span data-ttu-id="998bb-117">Primer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-117">First customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-118">extensionAttribute2</span><span class="sxs-lookup"><span data-stu-id="998bb-118">extensionAttribute2</span></span>|<span data-ttu-id="998bb-119">String</span><span class="sxs-lookup"><span data-stu-id="998bb-119">String</span></span>| <span data-ttu-id="998bb-120">Segundo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-120">Second customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-121">extensionAttribute3</span><span class="sxs-lookup"><span data-stu-id="998bb-121">extensionAttribute3</span></span>|<span data-ttu-id="998bb-122">String</span><span class="sxs-lookup"><span data-stu-id="998bb-122">String</span></span>| <span data-ttu-id="998bb-123">Tercer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-123">Third customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-124">extensionAttribute4</span><span class="sxs-lookup"><span data-stu-id="998bb-124">extensionAttribute4</span></span>|<span data-ttu-id="998bb-125">String</span><span class="sxs-lookup"><span data-stu-id="998bb-125">String</span></span>| <span data-ttu-id="998bb-126">Cuarto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-126">Fourth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-127">extensionAttribute5</span><span class="sxs-lookup"><span data-stu-id="998bb-127">extensionAttribute5</span></span>|<span data-ttu-id="998bb-128">String</span><span class="sxs-lookup"><span data-stu-id="998bb-128">String</span></span>| <span data-ttu-id="998bb-129">Atributo de extensión personalizable quinto.</span><span class="sxs-lookup"><span data-stu-id="998bb-129">Fifth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-130">extensionAttribute6</span><span class="sxs-lookup"><span data-stu-id="998bb-130">extensionAttribute6</span></span>|<span data-ttu-id="998bb-131">String</span><span class="sxs-lookup"><span data-stu-id="998bb-131">String</span></span>| <span data-ttu-id="998bb-132">Atributo de extensión personalizable sexto.</span><span class="sxs-lookup"><span data-stu-id="998bb-132">Sixth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-133">extensionAttribute7</span><span class="sxs-lookup"><span data-stu-id="998bb-133">extensionAttribute7</span></span>|<span data-ttu-id="998bb-134">String</span><span class="sxs-lookup"><span data-stu-id="998bb-134">String</span></span>| <span data-ttu-id="998bb-135">Séptimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-135">Seventh customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-136">extensionAttribute8</span><span class="sxs-lookup"><span data-stu-id="998bb-136">extensionAttribute8</span></span>|<span data-ttu-id="998bb-137">String</span><span class="sxs-lookup"><span data-stu-id="998bb-137">String</span></span>| <span data-ttu-id="998bb-138">Atributo de extensión personalizable octavo.</span><span class="sxs-lookup"><span data-stu-id="998bb-138">Eighth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-139">extensionAttribute9</span><span class="sxs-lookup"><span data-stu-id="998bb-139">extensionAttribute9</span></span>|<span data-ttu-id="998bb-140">String</span><span class="sxs-lookup"><span data-stu-id="998bb-140">String</span></span>| <span data-ttu-id="998bb-141">Noveno atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-141">Ninth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-142">extensionAttribute10</span><span class="sxs-lookup"><span data-stu-id="998bb-142">extensionAttribute10</span></span>|<span data-ttu-id="998bb-143">String</span><span class="sxs-lookup"><span data-stu-id="998bb-143">String</span></span>| <span data-ttu-id="998bb-144">Décimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-144">Tenth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-145">extensionAttribute11</span><span class="sxs-lookup"><span data-stu-id="998bb-145">extensionAttribute11</span></span>|<span data-ttu-id="998bb-146">String</span><span class="sxs-lookup"><span data-stu-id="998bb-146">String</span></span>| <span data-ttu-id="998bb-147">Atributo de extensión undécima personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-147">Eleventh customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-148">extensionAttribute12</span><span class="sxs-lookup"><span data-stu-id="998bb-148">extensionAttribute12</span></span>|<span data-ttu-id="998bb-149">String</span><span class="sxs-lookup"><span data-stu-id="998bb-149">String</span></span>| <span data-ttu-id="998bb-150">Atributo de extensión duodécima personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-150">Twelfth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-151">extensionAttribute13</span><span class="sxs-lookup"><span data-stu-id="998bb-151">extensionAttribute13</span></span>|<span data-ttu-id="998bb-152">String</span><span class="sxs-lookup"><span data-stu-id="998bb-152">String</span></span>| <span data-ttu-id="998bb-153">Atributo de extensión Decimotercera personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-153">Thirteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-154">extensionAttribute14</span><span class="sxs-lookup"><span data-stu-id="998bb-154">extensionAttribute14</span></span>|<span data-ttu-id="998bb-155">String</span><span class="sxs-lookup"><span data-stu-id="998bb-155">String</span></span>| <span data-ttu-id="998bb-156">Atributo de extensión decimocuarta personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-156">Fourteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="998bb-157">extensionAttribute15</span><span class="sxs-lookup"><span data-stu-id="998bb-157">extensionAttribute15</span></span>|<span data-ttu-id="998bb-158">String</span><span class="sxs-lookup"><span data-stu-id="998bb-158">String</span></span>| <span data-ttu-id="998bb-159">Atributo de extensión decimoquinta personalizable.</span><span class="sxs-lookup"><span data-stu-id="998bb-159">Fifteenth customizable extension attribute.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="998bb-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="998bb-160">JSON representation</span></span>

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