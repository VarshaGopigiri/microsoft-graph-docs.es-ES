---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: PersonOrGroupColumn
ms.openlocfilehash: 715c6ca22957cbd951784e6cf32edf2bf47f1098
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="personorgroupcolumn-resource-type"></a><span data-ttu-id="858c5-102">Tipo de recurso PersonOrGroupColumn</span><span class="sxs-lookup"><span data-stu-id="858c5-102">PersonOrGroupColumn resource type</span></span>

<span data-ttu-id="858c5-103">El recurso **personOrGroupColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de columna representan una persona o un grupo seleccionados del directorio.</span><span class="sxs-lookup"><span data-stu-id="858c5-103">The **personOrGroupColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values represent a person or group chosen from the directory.</span></span>

## <a name="json-representation"></a><span data-ttu-id="858c5-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="858c5-104">JSON representation</span></span>

<span data-ttu-id="858c5-105">A continuación se incluye una representación JSON de un recurso **personOrGroupColumn**.</span><span class="sxs-lookup"><span data-stu-id="858c5-105">Here is a JSON representation of a **driveItem** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.personOrGroupColumn", "@property.aka": "chooseFromType=format" } -->

```json
{
  "allowMultipleSelection": true,
  "displayAs": "account | contentType | created | department | ...",
  "chooseFromType": "peopleAndGroups | peopleOnly"
}
```

## <a name="properties"></a><span data-ttu-id="858c5-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="858c5-106">Properties</span></span>

| <span data-ttu-id="858c5-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="858c5-107">Property name</span></span>              | <span data-ttu-id="858c5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="858c5-108">Type</span></span>    | <span data-ttu-id="858c5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="858c5-109">Description</span></span>
|:---------------------------|:--------|:--------------------------------------
| <span data-ttu-id="858c5-110">**allowMultipleSelection**</span><span class="sxs-lookup"><span data-stu-id="858c5-110">**allowMultipleSelection**</span></span> | <span data-ttu-id="858c5-111">boolean</span><span class="sxs-lookup"><span data-stu-id="858c5-111">boolean</span></span> | <span data-ttu-id="858c5-112">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="858c5-112">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="858c5-113">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="858c5-113">**displayAs**</span></span>              | <span data-ttu-id="858c5-114">string</span><span class="sxs-lookup"><span data-stu-id="858c5-114">string</span></span>  | <span data-ttu-id="858c5-115">Cómo mostrar la información sobre la persona o el grupo elegido.</span><span class="sxs-lookup"><span data-stu-id="858c5-115">How to display the information about the person or group chosen.</span></span> <span data-ttu-id="858c5-116">Véalo a continuación.</span><span class="sxs-lookup"><span data-stu-id="858c5-116">See below.</span></span>
| <span data-ttu-id="858c5-117">**chooseFromType**</span><span class="sxs-lookup"><span data-stu-id="858c5-117">**chooseFromType**</span></span>         | <span data-ttu-id="858c5-118">string</span><span class="sxs-lookup"><span data-stu-id="858c5-118">string</span></span>  | <span data-ttu-id="858c5-119">Si quiere permitir la selección solo de personas, o de personas y grupos.</span><span class="sxs-lookup"><span data-stu-id="858c5-119">Whether to allow selection of people only, or people and groups.</span></span> <span data-ttu-id="858c5-120">Debe ser `peopleAndGroups` o `peopleOnly`.</span><span class="sxs-lookup"><span data-stu-id="858c5-120">Must be one of `peopleAndGroups` or `peopleOnly`.</span></span>

## <a name="displayas-values"></a><span data-ttu-id="858c5-121">Valores displayAs</span><span class="sxs-lookup"><span data-stu-id="858c5-121">DisplayAs values</span></span>

| <span data-ttu-id="858c5-122">Valor displayAs</span><span class="sxs-lookup"><span data-stu-id="858c5-122">DisplayAs value</span></span>               | <span data-ttu-id="858c5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="858c5-123">Description</span></span>
|:------------------------------|:-----------------------
| <span data-ttu-id="858c5-124">**account**</span><span class="sxs-lookup"><span data-stu-id="858c5-124">**Account**</span></span>                   | <span data-ttu-id="858c5-125">La cadena de notificación codificada de SharePoint sin formato de la persona o el grupo (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="858c5-125">The raw SharePoint encoded claim string for the person or group (eg.</span></span> <span data-ttu-id="858c5-126">i:0#.f</span><span class="sxs-lookup"><span data-stu-id="858c5-126">i:0#.f</span></span>|<span data-ttu-id="858c5-127">pertenencia</span><span class="sxs-lookup"><span data-stu-id="858c5-127">membership</span></span>|<span data-ttu-id="858c5-128">jane@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="858c5-128">jane@contoso.com).</span></span>
| <span data-ttu-id="858c5-129">**department**</span><span class="sxs-lookup"><span data-stu-id="858c5-129">**department**</span></span>                | <span data-ttu-id="858c5-130">Departamento de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="858c5-130">The person or group's department.</span></span>
| <span data-ttu-id="858c5-131">**firstName**</span><span class="sxs-lookup"><span data-stu-id="858c5-131">**FirstName**</span></span>                 | <span data-ttu-id="858c5-132">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="858c5-132">The person's given name.</span></span>
| <span data-ttu-id="858c5-133">**id**</span><span class="sxs-lookup"><span data-stu-id="858c5-133">**id**</span></span>                        | <span data-ttu-id="858c5-134">Identificador de la persona o el grupo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="858c5-134">The id of the person or group in the directory.</span></span>
| <span data-ttu-id="858c5-135">**lastName**</span><span class="sxs-lookup"><span data-stu-id="858c5-135">**LastName**</span></span>                  | <span data-ttu-id="858c5-136">Apellido de la persona.</span><span class="sxs-lookup"><span data-stu-id="858c5-136">The person's given name.</span></span>
| <span data-ttu-id="858c5-137">**mobilePhone**</span><span class="sxs-lookup"><span data-stu-id="858c5-137">**mobilePhone**</span></span>               | <span data-ttu-id="858c5-138">Número de teléfono móvil de la persona.</span><span class="sxs-lookup"><span data-stu-id="858c5-138">The contact's mobile phone number.</span></span>
| <span data-ttu-id="858c5-139">**name**</span><span class="sxs-lookup"><span data-stu-id="858c5-139">**name**</span></span>                      | <span data-ttu-id="858c5-140">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="858c5-140">The person's given name.</span></span>
| <span data-ttu-id="858c5-141">**nameWithPictureAndDetails**</span><span class="sxs-lookup"><span data-stu-id="858c5-141">**nameWithPictureAndDetails**</span></span> | <span data-ttu-id="858c5-142">Nombre de la persona junto con su imagen y detalles adicionales.</span><span class="sxs-lookup"><span data-stu-id="858c5-142">The person's name along with their picture and additional details.</span></span>
| <span data-ttu-id="858c5-143">**nameWithPresence**</span><span class="sxs-lookup"><span data-stu-id="858c5-143">**nameWithPresence**</span></span>          | <span data-ttu-id="858c5-144">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="858c5-144">Default.</span></span> <span data-ttu-id="858c5-145">Nombre de la persona con un icono de indicador de presencia (disponible/ocupado/etc.).</span><span class="sxs-lookup"><span data-stu-id="858c5-145">The person's name with a presence indicator icon (available/busy/etc.)</span></span>
| <span data-ttu-id="858c5-146">**office**</span><span class="sxs-lookup"><span data-stu-id="858c5-146">**Office**</span></span>                    | <span data-ttu-id="858c5-147">Número de la oficina de la persona.</span><span class="sxs-lookup"><span data-stu-id="858c5-147">The person's office number.</span></span>
| <span data-ttu-id="858c5-148">**pictureOnly36x36**</span><span class="sxs-lookup"><span data-stu-id="858c5-148">**pictureOnly36x36**</span></span>          | <span data-ttu-id="858c5-149">Imagen de la persona, delimitado por un cuadrado de 36x36 píxeles.</span><span class="sxs-lookup"><span data-stu-id="858c5-149">The person's picture, bounded by a 36x36 px square.</span></span>
| <span data-ttu-id="858c5-150">**pictureOnly48x48**</span><span class="sxs-lookup"><span data-stu-id="858c5-150">**pictureOnly48x48**</span></span>          | <span data-ttu-id="858c5-151">Imagen de la persona, delimitado por un cuadrado de 48x48 píxeles.</span><span class="sxs-lookup"><span data-stu-id="858c5-151">The person's picture, bounded by a 48x48 px square.</span></span>
| <span data-ttu-id="858c5-152">**pictureOnly72x72**</span><span class="sxs-lookup"><span data-stu-id="858c5-152">**pictureOnly72x72**</span></span>          | <span data-ttu-id="858c5-153">Imagen de la persona, delimitado por un cuadrado de 72x72 píxeles.</span><span class="sxs-lookup"><span data-stu-id="858c5-153">The person's picture, bounded by a 72x72 px square.</span></span>
| <span data-ttu-id="858c5-154">**sipAddress**</span><span class="sxs-lookup"><span data-stu-id="858c5-154">**sipAddress**</span></span>                | <span data-ttu-id="858c5-155">Dirección SIP de la persona.</span><span class="sxs-lookup"><span data-stu-id="858c5-155">The person's sip address.</span></span>
| <span data-ttu-id="858c5-156">**title**</span><span class="sxs-lookup"><span data-stu-id="858c5-156">**title**</span></span>                     | <span data-ttu-id="858c5-157">Puesto de la persona en la organización.</span><span class="sxs-lookup"><span data-stu-id="858c5-157">The person's title in the organization.</span></span>
| <span data-ttu-id="858c5-158">**userName**</span><span class="sxs-lookup"><span data-stu-id="858c5-158">**Username**</span></span>                  | <span data-ttu-id="858c5-159">Nombre de usuario de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="858c5-159">The person or group's user name.</span></span>
| <span data-ttu-id="858c5-160">**workEmail**</span><span class="sxs-lookup"><span data-stu-id="858c5-160">**workEmail**</span></span>                 | <span data-ttu-id="858c5-161">Dirección de correo electrónico de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="858c5-161">The person or group's email address.</span></span>
| <span data-ttu-id="858c5-162">**workPhone**</span><span class="sxs-lookup"><span data-stu-id="858c5-162">**workPhone**</span></span>                 | <span data-ttu-id="858c5-163">Número de teléfono del trabajo de la persona.</span><span class="sxs-lookup"><span data-stu-id="858c5-163">The person's work phone number.</span></span>

<span data-ttu-id="858c5-164">Nota: Se pueden devolver tipos DisplayAs adicionales.</span><span class="sxs-lookup"><span data-stu-id="858c5-164">Note: Additional DisplayAs types may be returned.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/PersonOrGroupColumn"
} -->
