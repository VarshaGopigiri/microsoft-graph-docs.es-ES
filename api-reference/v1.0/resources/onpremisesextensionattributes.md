# <a name="onpremisesextensionattributes-resource-type"></a><span data-ttu-id="d87f1-101">Tipo de recurso onPremisesExtensionAttributes</span><span class="sxs-lookup"><span data-stu-id="d87f1-101">onPremisesExtensionAttributes resource type</span></span>

<span data-ttu-id="d87f1-102">La propiedad **onPremisesExtensionAttributes** de la entidad de [user](user.md) contiene quince propiedades de atributo de extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="d87f1-102">The **onPremisesExtensionAttributes** property of the [user](user.md) entity contains fifteen custom extension attribute properties.</span></span> <span data-ttu-id="d87f1-103">Para un usuario que tenga habilitado **onPremisesSyncEnabled**, este conjunto de propiedades se controla en Active Directory local, se sincroniza con Azure AD y es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d87f1-103">For an **onPremisesSyncEnabled** user, this set of properties is mastered in on-premises Active Directory and synchronized to Azure AD, and is read-only.</span></span> <span data-ttu-id="d87f1-104">Para un usuario de solo nube (para el que **onPremisesSyncEnabled** es falso), estas propiedades se pueden definir durante la creación o la actualización.</span><span class="sxs-lookup"><span data-stu-id="d87f1-104">For a cloud-only user (where **onPremisesSyncEnabled** is false), these properties may be set during creation or update.</span></span>


## <a name="properties"></a><span data-ttu-id="d87f1-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d87f1-105">Properties</span></span>
| <span data-ttu-id="d87f1-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d87f1-106">Property</span></span>     | <span data-ttu-id="d87f1-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d87f1-107">Type</span></span>   |<span data-ttu-id="d87f1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d87f1-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d87f1-109">extensionAttribute1</span><span class="sxs-lookup"><span data-stu-id="d87f1-109">extensionAttribute1</span></span>|<span data-ttu-id="d87f1-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-110">String</span></span>| <span data-ttu-id="d87f1-111">Primer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-111">First customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-112">extensionAttribute2</span><span class="sxs-lookup"><span data-stu-id="d87f1-112">extensionAttribute2</span></span>|<span data-ttu-id="d87f1-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-113">String</span></span>| <span data-ttu-id="d87f1-114">Segundo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-114">Second customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-115">extensionAttribute3</span><span class="sxs-lookup"><span data-stu-id="d87f1-115">extensionAttribute3</span></span>|<span data-ttu-id="d87f1-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-116">String</span></span>| <span data-ttu-id="d87f1-117">Tercer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-117">Third customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-118">extensionAttribute4</span><span class="sxs-lookup"><span data-stu-id="d87f1-118">extensionAttribute4</span></span>|<span data-ttu-id="d87f1-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-119">String</span></span>| <span data-ttu-id="d87f1-120">Cuarto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-120">Fourth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-121">extensionAttribute5</span><span class="sxs-lookup"><span data-stu-id="d87f1-121">extensionAttribute5</span></span>|<span data-ttu-id="d87f1-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-122">String</span></span>| <span data-ttu-id="d87f1-123">Quinto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-123">Fifth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-124">extensionAttribute6</span><span class="sxs-lookup"><span data-stu-id="d87f1-124">extensionAttribute6</span></span>|<span data-ttu-id="d87f1-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-125">String</span></span>| <span data-ttu-id="d87f1-126">Sexto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-126">Sixth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-127">extensionAttribute7</span><span class="sxs-lookup"><span data-stu-id="d87f1-127">extensionAttribute7</span></span>|<span data-ttu-id="d87f1-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-128">String</span></span>| <span data-ttu-id="d87f1-129">Séptimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-129">Seventh customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-130">extensionAttribute8</span><span class="sxs-lookup"><span data-stu-id="d87f1-130">extensionAttribute8</span></span>|<span data-ttu-id="d87f1-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-131">String</span></span>| <span data-ttu-id="d87f1-132">Octavo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-132">Eighth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-133">extensionAttribute9</span><span class="sxs-lookup"><span data-stu-id="d87f1-133">extensionAttribute9</span></span>|<span data-ttu-id="d87f1-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-134">String</span></span>| <span data-ttu-id="d87f1-135">Noveno atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-135">Ninth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-136">extensionAttribute10</span><span class="sxs-lookup"><span data-stu-id="d87f1-136">extensionAttribute10</span></span>|<span data-ttu-id="d87f1-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-137">String</span></span>| <span data-ttu-id="d87f1-138">Décimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-138">Tenth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-139">extensionAttribute11</span><span class="sxs-lookup"><span data-stu-id="d87f1-139">extensionAttribute11</span></span>|<span data-ttu-id="d87f1-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-140">String</span></span>| <span data-ttu-id="d87f1-141">Undécimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-141">Eleventh customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-142">extensionAttribute12</span><span class="sxs-lookup"><span data-stu-id="d87f1-142">extensionAttribute12</span></span>|<span data-ttu-id="d87f1-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-143">String</span></span>| <span data-ttu-id="d87f1-144">Duodécimo atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-144">Twelfth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-145">extensionAttribute13</span><span class="sxs-lookup"><span data-stu-id="d87f1-145">extensionAttribute13</span></span>|<span data-ttu-id="d87f1-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-146">String</span></span>| <span data-ttu-id="d87f1-147">Decimotercer atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-147">Thirteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-148">extensionAttribute14</span><span class="sxs-lookup"><span data-stu-id="d87f1-148">extensionAttribute14</span></span>|<span data-ttu-id="d87f1-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-149">String</span></span>| <span data-ttu-id="d87f1-150">Decimocuarto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-150">Fourteenth customizable extension attribute.</span></span> |
|<span data-ttu-id="d87f1-151">extensionAttribute15</span><span class="sxs-lookup"><span data-stu-id="d87f1-151">extensionAttribute15</span></span>|<span data-ttu-id="d87f1-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="d87f1-152">String</span></span>| <span data-ttu-id="d87f1-153">Decimoquinto atributo de extensión personalizable.</span><span class="sxs-lookup"><span data-stu-id="d87f1-153">Fifteenth customizable extension attribute.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="d87f1-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d87f1-154">JSON representation</span></span>

<span data-ttu-id="d87f1-155">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d87f1-155">Here is a JSON representation of the resource</span></span>

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