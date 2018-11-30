---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: PersonOrGroupColumn
ms.openlocfilehash: b0c6eab7d2111870192a4ed6c30c1cbd72e4163e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031362"
---
# <a name="personorgroupcolumn-resource-type"></a><span data-ttu-id="1dac1-102">Tipo de recurso PersonOrGroupColumn</span><span class="sxs-lookup"><span data-stu-id="1dac1-102">PersonOrGroupColumn resource type</span></span>

<span data-ttu-id="1dac1-103">El recurso **personOrGroupColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de columna representan una persona o un grupo seleccionados del directorio.</span><span class="sxs-lookup"><span data-stu-id="1dac1-103">The **personOrGroupColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values represent a person or group chosen from the directory.</span></span>

## <a name="json-representation"></a><span data-ttu-id="1dac1-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1dac1-104">JSON representation</span></span>

<span data-ttu-id="1dac1-105">A continuación se incluye una representación JSON de un recurso **personOrGroupColumn**.</span><span class="sxs-lookup"><span data-stu-id="1dac1-105">Here is a JSON representation of a **personOrGroupColumn** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.personOrGroupColumn", "@property.aka": "chooseFromType=format" } -->

```json
{
  "allowMultipleSelection": true,
  "displayAs": "account | contentType | created | department | ...",
  "chooseFromType": "peopleAndGroups | peopleOnly"
}
```

## <a name="properties"></a><span data-ttu-id="1dac1-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1dac1-106">Properties</span></span>

| <span data-ttu-id="1dac1-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="1dac1-107">Property name</span></span>              | <span data-ttu-id="1dac1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1dac1-108">Type</span></span>    | <span data-ttu-id="1dac1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dac1-109">Description</span></span>
|:---------------------------|:--------|:--------------------------------------
| <span data-ttu-id="1dac1-110">**allowMultipleSelection**</span><span class="sxs-lookup"><span data-stu-id="1dac1-110">**allowMultipleSelection**</span></span> | <span data-ttu-id="1dac1-111">boolean</span><span class="sxs-lookup"><span data-stu-id="1dac1-111">boolean</span></span> | <span data-ttu-id="1dac1-112">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="1dac1-112">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="1dac1-113">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="1dac1-113">**displayAs**</span></span>              | <span data-ttu-id="1dac1-114">string</span><span class="sxs-lookup"><span data-stu-id="1dac1-114">string</span></span>  | <span data-ttu-id="1dac1-115">Cómo mostrar la información sobre la persona o el grupo elegido.</span><span class="sxs-lookup"><span data-stu-id="1dac1-115">How to display the information about the person or group chosen.</span></span> <span data-ttu-id="1dac1-116">Véalo a continuación.</span><span class="sxs-lookup"><span data-stu-id="1dac1-116">See below.</span></span>
| <span data-ttu-id="1dac1-117">**chooseFromType**</span><span class="sxs-lookup"><span data-stu-id="1dac1-117">**chooseFromType**</span></span>         | <span data-ttu-id="1dac1-118">string</span><span class="sxs-lookup"><span data-stu-id="1dac1-118">string</span></span>  | <span data-ttu-id="1dac1-119">Si quiere permitir la selección solo de personas, o de personas y grupos.</span><span class="sxs-lookup"><span data-stu-id="1dac1-119">Whether to allow selection of people only, or people and groups.</span></span> <span data-ttu-id="1dac1-120">Debe ser `peopleAndGroups` o `peopleOnly`.</span><span class="sxs-lookup"><span data-stu-id="1dac1-120">Must be one of `peopleAndGroups` or `peopleOnly`.</span></span>

## <a name="displayas-options"></a><span data-ttu-id="1dac1-121">Opciones de displayAs</span><span class="sxs-lookup"><span data-stu-id="1dac1-121">DisplayAs options</span></span>

| <span data-ttu-id="1dac1-122">Valor displayAs</span><span class="sxs-lookup"><span data-stu-id="1dac1-122">DisplayAs value</span></span>               | <span data-ttu-id="1dac1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dac1-123">Description</span></span>
|:------------------------------|:-----------------------
| <span data-ttu-id="1dac1-124">**account**</span><span class="sxs-lookup"><span data-stu-id="1dac1-124">**account**</span></span>                   | <span data-ttu-id="1dac1-125">La cadena de notificación codificada de SharePoint sin formato de la persona o el grupo (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="1dac1-125">The raw SharePoint encoded claim string for the person or group (eg.</span></span> <span data-ttu-id="1dac1-126">i:0#.f</span><span class="sxs-lookup"><span data-stu-id="1dac1-126">i:0#.f</span></span>|<span data-ttu-id="1dac1-127">membership</span><span class="sxs-lookup"><span data-stu-id="1dac1-127">membership</span></span>|<span data-ttu-id="1dac1-128">jane@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="1dac1-128">jane@contoso.com).</span></span>
| <span data-ttu-id="1dac1-129">**department**</span><span class="sxs-lookup"><span data-stu-id="1dac1-129">**department**</span></span>                | <span data-ttu-id="1dac1-130">Departamento de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="1dac1-130">The person or group's department.</span></span>
| <span data-ttu-id="1dac1-131">**firstName**</span><span class="sxs-lookup"><span data-stu-id="1dac1-131">**firstName**</span></span>                 | <span data-ttu-id="1dac1-132">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="1dac1-132">The person's first name.</span></span>
| <span data-ttu-id="1dac1-133">**id**</span><span class="sxs-lookup"><span data-stu-id="1dac1-133">**id**</span></span>                        | <span data-ttu-id="1dac1-134">Identificador de la persona o el grupo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="1dac1-134">The id of the person or group in the directory.</span></span>
| <span data-ttu-id="1dac1-135">**lastName**</span><span class="sxs-lookup"><span data-stu-id="1dac1-135">**lastName**</span></span>                  | <span data-ttu-id="1dac1-136">Apellido de la persona.</span><span class="sxs-lookup"><span data-stu-id="1dac1-136">The person's last name.</span></span>
| <span data-ttu-id="1dac1-137">**mobilePhone**</span><span class="sxs-lookup"><span data-stu-id="1dac1-137">**mobilePhone**</span></span>               | <span data-ttu-id="1dac1-138">Número de teléfono móvil de la persona.</span><span class="sxs-lookup"><span data-stu-id="1dac1-138">The person's mobile phone number.</span></span>
| <span data-ttu-id="1dac1-139">**name**</span><span class="sxs-lookup"><span data-stu-id="1dac1-139">**name**</span></span>                      | <span data-ttu-id="1dac1-140">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="1dac1-140">The person's name.</span></span>
| <span data-ttu-id="1dac1-141">**nameWithPictureAndDetails**</span><span class="sxs-lookup"><span data-stu-id="1dac1-141">**nameWithPictureAndDetails**</span></span> | <span data-ttu-id="1dac1-142">Nombre de la persona junto con su imagen y detalles adicionales.</span><span class="sxs-lookup"><span data-stu-id="1dac1-142">The person's name along with their picture and additional details.</span></span>
| <span data-ttu-id="1dac1-143">**nameWithPresence**</span><span class="sxs-lookup"><span data-stu-id="1dac1-143">**nameWithPresence**</span></span>          | <span data-ttu-id="1dac1-144">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1dac1-144">Default.</span></span> <span data-ttu-id="1dac1-145">Nombre de la persona con un icono de indicador de presencia (disponible/ocupado/etc.).</span><span class="sxs-lookup"><span data-stu-id="1dac1-145">The person's name with a presence indicator icon (available/busy/etc.)</span></span>
| <span data-ttu-id="1dac1-146">**office**</span><span class="sxs-lookup"><span data-stu-id="1dac1-146">**office**</span></span>                    | <span data-ttu-id="1dac1-147">Número de la oficina de la persona.</span><span class="sxs-lookup"><span data-stu-id="1dac1-147">The person's office number.</span></span>
| <span data-ttu-id="1dac1-148">**pictureOnly36x36**</span><span class="sxs-lookup"><span data-stu-id="1dac1-148">**pictureOnly36x36**</span></span>          | <span data-ttu-id="1dac1-149">Imagen de la persona, delimitado por un cuadrado de 36x36 píxeles.</span><span class="sxs-lookup"><span data-stu-id="1dac1-149">The person's picture, bounded by a 36x36 px square.</span></span>
| <span data-ttu-id="1dac1-150">**pictureOnly48x48**</span><span class="sxs-lookup"><span data-stu-id="1dac1-150">**pictureOnly48x48**</span></span>          | <span data-ttu-id="1dac1-151">Imagen de la persona, delimitado por un cuadrado de 48x48 píxeles.</span><span class="sxs-lookup"><span data-stu-id="1dac1-151">The person's picture, bounded by a 48x48 px square.</span></span>
| <span data-ttu-id="1dac1-152">**pictureOnly72x72**</span><span class="sxs-lookup"><span data-stu-id="1dac1-152">**pictureOnly72x72**</span></span>          | <span data-ttu-id="1dac1-153">Imagen de la persona, delimitado por un cuadrado de 72x72 píxeles.</span><span class="sxs-lookup"><span data-stu-id="1dac1-153">The person's picture, bounded by a 72x72 px square.</span></span>
| <span data-ttu-id="1dac1-154">**sipAddress**</span><span class="sxs-lookup"><span data-stu-id="1dac1-154">**sipAddress**</span></span>                | <span data-ttu-id="1dac1-155">Dirección SIP de la persona.</span><span class="sxs-lookup"><span data-stu-id="1dac1-155">The person's sip address.</span></span>
| <span data-ttu-id="1dac1-156">**title**</span><span class="sxs-lookup"><span data-stu-id="1dac1-156">**title**</span></span>                     | <span data-ttu-id="1dac1-157">Puesto de la persona en la organización.</span><span class="sxs-lookup"><span data-stu-id="1dac1-157">The person's title in the organization.</span></span>
| <span data-ttu-id="1dac1-158">**userName**</span><span class="sxs-lookup"><span data-stu-id="1dac1-158">**userName**</span></span>                  | <span data-ttu-id="1dac1-159">Nombre de usuario de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="1dac1-159">The person or group's user name.</span></span>
| <span data-ttu-id="1dac1-160">**workEmail**</span><span class="sxs-lookup"><span data-stu-id="1dac1-160">**workEmail**</span></span>                 | <span data-ttu-id="1dac1-161">Dirección de correo electrónico de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="1dac1-161">The person or group's email address.</span></span>
| <span data-ttu-id="1dac1-162">**workPhone**</span><span class="sxs-lookup"><span data-stu-id="1dac1-162">**workPhone**</span></span>                 | <span data-ttu-id="1dac1-163">Número de teléfono del trabajo de la persona.</span><span class="sxs-lookup"><span data-stu-id="1dac1-163">The person's work phone number.</span></span>

<span data-ttu-id="1dac1-164">Nota: Se pueden devolver tipos DisplayAs adicionales.</span><span class="sxs-lookup"><span data-stu-id="1dac1-164">Note: Additional DisplayAs types may be returned.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/personorgroupcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(peopleAndGroups,peopleOnly) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/personorgroupcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(account,contentType,created,department,...) are in resource, but () are in table"
  ],
  "tocPath": "Resources/PersonOrGroupColumn"
} -->
