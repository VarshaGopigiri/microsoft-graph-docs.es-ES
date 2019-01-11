---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: PersonOrGroupColumn
localization_priority: Normal
ms.openlocfilehash: 2b874a7b33c759eb8f81a3a5654115eaaf63c8f9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805694"
---
# <a name="personorgroupcolumn-resource-type"></a><span data-ttu-id="df0dd-102">Tipo de recurso PersonOrGroupColumn</span><span class="sxs-lookup"><span data-stu-id="df0dd-102">PersonOrGroupColumn resource type</span></span>

<span data-ttu-id="df0dd-103">El recurso **personOrGroupColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de columna representan una persona o un grupo seleccionados del directorio.</span><span class="sxs-lookup"><span data-stu-id="df0dd-103">The **personOrGroupColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values represent a person or group chosen from the directory.</span></span>

## <a name="json-representation"></a><span data-ttu-id="df0dd-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="df0dd-104">JSON representation</span></span>

<span data-ttu-id="df0dd-105">A continuación se incluye una representación JSON de un recurso **personOrGroupColumn**.</span><span class="sxs-lookup"><span data-stu-id="df0dd-105">Here is a JSON representation of a **personOrGroupColumn** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.personOrGroupColumn", "@property.aka": "chooseFromType=format" } -->

```json
{
  "allowMultipleSelection": true,
  "displayAs": "account | contentType | created | department | ...",
  "chooseFromType": "peopleAndGroups | peopleOnly"
}
```

## <a name="properties"></a><span data-ttu-id="df0dd-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df0dd-106">Properties</span></span>

| <span data-ttu-id="df0dd-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="df0dd-107">Property name</span></span>              | <span data-ttu-id="df0dd-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="df0dd-108">Type</span></span>    | <span data-ttu-id="df0dd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="df0dd-109">Description</span></span>
|:---------------------------|:--------|:--------------------------------------
| <span data-ttu-id="df0dd-110">**allowMultipleSelection**</span><span class="sxs-lookup"><span data-stu-id="df0dd-110">**allowMultipleSelection**</span></span> | <span data-ttu-id="df0dd-111">boolean</span><span class="sxs-lookup"><span data-stu-id="df0dd-111">boolean</span></span> | <span data-ttu-id="df0dd-112">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="df0dd-112">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="df0dd-113">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="df0dd-113">**displayAs**</span></span>              | <span data-ttu-id="df0dd-114">string</span><span class="sxs-lookup"><span data-stu-id="df0dd-114">string</span></span>  | <span data-ttu-id="df0dd-115">Cómo mostrar la información sobre la persona o el grupo elegido.</span><span class="sxs-lookup"><span data-stu-id="df0dd-115">How to display the information about the person or group chosen.</span></span> <span data-ttu-id="df0dd-116">Véalo a continuación.</span><span class="sxs-lookup"><span data-stu-id="df0dd-116">See below.</span></span>
| <span data-ttu-id="df0dd-117">**chooseFromType**</span><span class="sxs-lookup"><span data-stu-id="df0dd-117">**chooseFromType**</span></span>         | <span data-ttu-id="df0dd-118">string</span><span class="sxs-lookup"><span data-stu-id="df0dd-118">string</span></span>  | <span data-ttu-id="df0dd-119">Si quiere permitir la selección solo de personas, o de personas y grupos.</span><span class="sxs-lookup"><span data-stu-id="df0dd-119">Whether to allow selection of people only, or people and groups.</span></span> <span data-ttu-id="df0dd-120">Debe ser `peopleAndGroups` o `peopleOnly`.</span><span class="sxs-lookup"><span data-stu-id="df0dd-120">Must be one of `peopleAndGroups` or `peopleOnly`.</span></span>

## <a name="displayas-options"></a><span data-ttu-id="df0dd-121">Opciones de displayAs</span><span class="sxs-lookup"><span data-stu-id="df0dd-121">DisplayAs options</span></span>

| <span data-ttu-id="df0dd-122">Valor displayAs</span><span class="sxs-lookup"><span data-stu-id="df0dd-122">DisplayAs value</span></span>               | <span data-ttu-id="df0dd-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="df0dd-123">Description</span></span>
|:------------------------------|:-----------------------
| <span data-ttu-id="df0dd-124">**account**</span><span class="sxs-lookup"><span data-stu-id="df0dd-124">**account**</span></span>                   | <span data-ttu-id="df0dd-125">La cadena de notificación codificada de SharePoint sin formato de la persona o el grupo (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="df0dd-125">The raw SharePoint encoded claim string for the person or group (eg.</span></span> <span data-ttu-id="df0dd-126">i:0#.f</span><span class="sxs-lookup"><span data-stu-id="df0dd-126">i:0#.f</span></span>|<span data-ttu-id="df0dd-127">membership</span><span class="sxs-lookup"><span data-stu-id="df0dd-127">membership</span></span>|<span data-ttu-id="df0dd-128">jane@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="df0dd-128">jane@contoso.com).</span></span>
| <span data-ttu-id="df0dd-129">**department**</span><span class="sxs-lookup"><span data-stu-id="df0dd-129">**department**</span></span>                | <span data-ttu-id="df0dd-130">Departamento de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="df0dd-130">The person or group's department.</span></span>
| <span data-ttu-id="df0dd-131">**firstName**</span><span class="sxs-lookup"><span data-stu-id="df0dd-131">**firstName**</span></span>                 | <span data-ttu-id="df0dd-132">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="df0dd-132">The person's first name.</span></span>
| <span data-ttu-id="df0dd-133">**id**</span><span class="sxs-lookup"><span data-stu-id="df0dd-133">**id**</span></span>                        | <span data-ttu-id="df0dd-134">Identificador de la persona o el grupo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="df0dd-134">The id of the person or group in the directory.</span></span>
| <span data-ttu-id="df0dd-135">**lastName**</span><span class="sxs-lookup"><span data-stu-id="df0dd-135">**lastName**</span></span>                  | <span data-ttu-id="df0dd-136">Apellido de la persona.</span><span class="sxs-lookup"><span data-stu-id="df0dd-136">The person's last name.</span></span>
| <span data-ttu-id="df0dd-137">**mobilePhone**</span><span class="sxs-lookup"><span data-stu-id="df0dd-137">**mobilePhone**</span></span>               | <span data-ttu-id="df0dd-138">Número de teléfono móvil de la persona.</span><span class="sxs-lookup"><span data-stu-id="df0dd-138">The person's mobile phone number.</span></span>
| <span data-ttu-id="df0dd-139">**name**</span><span class="sxs-lookup"><span data-stu-id="df0dd-139">**name**</span></span>                      | <span data-ttu-id="df0dd-140">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="df0dd-140">The person's name.</span></span>
| <span data-ttu-id="df0dd-141">**nameWithPictureAndDetails**</span><span class="sxs-lookup"><span data-stu-id="df0dd-141">**nameWithPictureAndDetails**</span></span> | <span data-ttu-id="df0dd-142">Nombre de la persona junto con su imagen y detalles adicionales.</span><span class="sxs-lookup"><span data-stu-id="df0dd-142">The person's name along with their picture and additional details.</span></span>
| <span data-ttu-id="df0dd-143">**nameWithPresence**</span><span class="sxs-lookup"><span data-stu-id="df0dd-143">**nameWithPresence**</span></span>          | <span data-ttu-id="df0dd-144">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="df0dd-144">Default.</span></span> <span data-ttu-id="df0dd-145">Nombre de la persona con un icono de indicador de presencia (disponible/ocupado/etc.).</span><span class="sxs-lookup"><span data-stu-id="df0dd-145">The person's name with a presence indicator icon (available/busy/etc.)</span></span>
| <span data-ttu-id="df0dd-146">**office**</span><span class="sxs-lookup"><span data-stu-id="df0dd-146">**office**</span></span>                    | <span data-ttu-id="df0dd-147">Número de la oficina de la persona.</span><span class="sxs-lookup"><span data-stu-id="df0dd-147">The person's office number.</span></span>
| <span data-ttu-id="df0dd-148">**pictureOnly36x36**</span><span class="sxs-lookup"><span data-stu-id="df0dd-148">**pictureOnly36x36**</span></span>          | <span data-ttu-id="df0dd-149">Imagen de la persona, delimitado por un cuadrado de 36x36 píxeles.</span><span class="sxs-lookup"><span data-stu-id="df0dd-149">The person's picture, bounded by a 36x36 px square.</span></span>
| <span data-ttu-id="df0dd-150">**pictureOnly48x48**</span><span class="sxs-lookup"><span data-stu-id="df0dd-150">**pictureOnly48x48**</span></span>          | <span data-ttu-id="df0dd-151">Imagen de la persona, delimitado por un cuadrado de 48x48 píxeles.</span><span class="sxs-lookup"><span data-stu-id="df0dd-151">The person's picture, bounded by a 48x48 px square.</span></span>
| <span data-ttu-id="df0dd-152">**pictureOnly72x72**</span><span class="sxs-lookup"><span data-stu-id="df0dd-152">**pictureOnly72x72**</span></span>          | <span data-ttu-id="df0dd-153">Imagen de la persona, delimitado por un cuadrado de 72x72 píxeles.</span><span class="sxs-lookup"><span data-stu-id="df0dd-153">The person's picture, bounded by a 72x72 px square.</span></span>
| <span data-ttu-id="df0dd-154">**sipAddress**</span><span class="sxs-lookup"><span data-stu-id="df0dd-154">**sipAddress**</span></span>                | <span data-ttu-id="df0dd-155">Dirección SIP de la persona.</span><span class="sxs-lookup"><span data-stu-id="df0dd-155">The person's sip address.</span></span>
| <span data-ttu-id="df0dd-156">**title**</span><span class="sxs-lookup"><span data-stu-id="df0dd-156">**title**</span></span>                     | <span data-ttu-id="df0dd-157">Puesto de la persona en la organización.</span><span class="sxs-lookup"><span data-stu-id="df0dd-157">The person's title in the organization.</span></span>
| <span data-ttu-id="df0dd-158">**userName**</span><span class="sxs-lookup"><span data-stu-id="df0dd-158">**userName**</span></span>                  | <span data-ttu-id="df0dd-159">Nombre de usuario de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="df0dd-159">The person or group's user name.</span></span>
| <span data-ttu-id="df0dd-160">**workEmail**</span><span class="sxs-lookup"><span data-stu-id="df0dd-160">**workEmail**</span></span>                 | <span data-ttu-id="df0dd-161">Dirección de correo electrónico de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="df0dd-161">The person or group's email address.</span></span>
| <span data-ttu-id="df0dd-162">**workPhone**</span><span class="sxs-lookup"><span data-stu-id="df0dd-162">**workPhone**</span></span>                 | <span data-ttu-id="df0dd-163">Número de teléfono del trabajo de la persona.</span><span class="sxs-lookup"><span data-stu-id="df0dd-163">The person's work phone number.</span></span>

<span data-ttu-id="df0dd-164">Nota: Se pueden devolver tipos DisplayAs adicionales.</span><span class="sxs-lookup"><span data-stu-id="df0dd-164">Note: Additional DisplayAs types may be returned.</span></span>

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
