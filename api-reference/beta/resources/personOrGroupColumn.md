---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: PersonOrGroupColumn
ms.openlocfilehash: 116e3a61938926ab75534bb2dc88363cc7d15196
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084085"
---
# <a name="personorgroupcolumn-resource-type"></a><span data-ttu-id="7240c-102">Tipo de recurso PersonOrGroupColumn</span><span class="sxs-lookup"><span data-stu-id="7240c-102">PersonOrGroupColumn resource type</span></span>

> <span data-ttu-id="7240c-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7240c-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7240c-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7240c-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7240c-105">El recurso **personOrGroupColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de columna representan una persona o un grupo seleccionados del directorio.</span><span class="sxs-lookup"><span data-stu-id="7240c-105">The **personOrGroupColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values represent a person or group chosen from the directory.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7240c-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7240c-106">JSON representation</span></span>

<span data-ttu-id="7240c-107">A continuación se incluye una representación JSON de un recurso **personOrGroupColumn**.</span><span class="sxs-lookup"><span data-stu-id="7240c-107">Here is a JSON representation of a **personOrGroupColumn** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.personOrGroupColumn", "@property.aka": "chooseFromType=format" } -->

```json
{
  "allowMultipleSelection": true,
  "displayAs": "account | contentType | created | department | ...",
  "chooseFromType": "peopleAndGroups | peopleOnly"
}
```

## <a name="properties"></a><span data-ttu-id="7240c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7240c-108">Properties</span></span>

| <span data-ttu-id="7240c-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="7240c-109">Property name</span></span>              | <span data-ttu-id="7240c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7240c-110">Type</span></span>    | <span data-ttu-id="7240c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7240c-111">Description</span></span>
|:---------------------------|:--------|:--------------------------------------
| <span data-ttu-id="7240c-112">**allowMultipleSelection**</span><span class="sxs-lookup"><span data-stu-id="7240c-112">**allowMultipleSelection**</span></span> | <span data-ttu-id="7240c-113">boolean</span><span class="sxs-lookup"><span data-stu-id="7240c-113">boolean</span></span> | <span data-ttu-id="7240c-114">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="7240c-114">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="7240c-115">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="7240c-115">**displayAs**</span></span>              | <span data-ttu-id="7240c-116">string</span><span class="sxs-lookup"><span data-stu-id="7240c-116">string</span></span>  | <span data-ttu-id="7240c-117">Cómo mostrar la información sobre la persona o el grupo elegido.</span><span class="sxs-lookup"><span data-stu-id="7240c-117">How to display the information about the person or group chosen.</span></span> <span data-ttu-id="7240c-118">Véalo a continuación.</span><span class="sxs-lookup"><span data-stu-id="7240c-118">See below.</span></span>
| <span data-ttu-id="7240c-119">**chooseFromType**</span><span class="sxs-lookup"><span data-stu-id="7240c-119">**chooseFromType**</span></span>         | <span data-ttu-id="7240c-120">string</span><span class="sxs-lookup"><span data-stu-id="7240c-120">string</span></span>  | <span data-ttu-id="7240c-121">Si quiere permitir la selección solo de personas, o de personas y grupos.</span><span class="sxs-lookup"><span data-stu-id="7240c-121">Whether to allow selection of people only, or people and groups.</span></span> <span data-ttu-id="7240c-122">Debe ser `peopleAndGroups` o `peopleOnly`.</span><span class="sxs-lookup"><span data-stu-id="7240c-122">Must be one of `peopleAndGroups` or `peopleOnly`.</span></span>

## <a name="displayas-values"></a><span data-ttu-id="7240c-123">Valores displayAs</span><span class="sxs-lookup"><span data-stu-id="7240c-123">DisplayAs values</span></span>

| <span data-ttu-id="7240c-124">Valor displayAs</span><span class="sxs-lookup"><span data-stu-id="7240c-124">DisplayAs value</span></span>               | <span data-ttu-id="7240c-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7240c-125">Description</span></span>
|:------------------------------|:-----------------------
| <span data-ttu-id="7240c-126">**account**</span><span class="sxs-lookup"><span data-stu-id="7240c-126">**account**</span></span>                   | <span data-ttu-id="7240c-127">La cadena de notificación codificada de SharePoint sin formato de la persona o el grupo (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="7240c-127">The raw SharePoint encoded claim string for the person or group (eg.</span></span> <span data-ttu-id="7240c-128">i:0#.f</span><span class="sxs-lookup"><span data-stu-id="7240c-128">i:0#.f</span></span>|<span data-ttu-id="7240c-129">membership</span><span class="sxs-lookup"><span data-stu-id="7240c-129">membership</span></span>|<span data-ttu-id="7240c-130">jane@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7240c-130">jane@contoso.com).</span></span>
| <span data-ttu-id="7240c-131">**department**</span><span class="sxs-lookup"><span data-stu-id="7240c-131">**department**</span></span>                | <span data-ttu-id="7240c-132">Departamento de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="7240c-132">The person or group's department.</span></span>
| <span data-ttu-id="7240c-133">**firstName**</span><span class="sxs-lookup"><span data-stu-id="7240c-133">**firstName**</span></span>                 | <span data-ttu-id="7240c-134">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="7240c-134">The person's first name.</span></span>
| <span data-ttu-id="7240c-135">**id**</span><span class="sxs-lookup"><span data-stu-id="7240c-135">**id**</span></span>                        | <span data-ttu-id="7240c-136">Identificador de la persona o el grupo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="7240c-136">The id of the person or group in the directory.</span></span>
| <span data-ttu-id="7240c-137">**lastName**</span><span class="sxs-lookup"><span data-stu-id="7240c-137">**lastName**</span></span>                  | <span data-ttu-id="7240c-138">Apellido de la persona.</span><span class="sxs-lookup"><span data-stu-id="7240c-138">The person's last name.</span></span>
| <span data-ttu-id="7240c-139">**mobilePhone**</span><span class="sxs-lookup"><span data-stu-id="7240c-139">**mobilePhone**</span></span>               | <span data-ttu-id="7240c-140">Número de teléfono móvil de la persona.</span><span class="sxs-lookup"><span data-stu-id="7240c-140">The person's mobile phone number.</span></span>
| <span data-ttu-id="7240c-141">**name**</span><span class="sxs-lookup"><span data-stu-id="7240c-141">**name**</span></span>                      | <span data-ttu-id="7240c-142">Nombre de la persona.</span><span class="sxs-lookup"><span data-stu-id="7240c-142">The person's name.</span></span>
| <span data-ttu-id="7240c-143">**nameWithPictureAndDetails**</span><span class="sxs-lookup"><span data-stu-id="7240c-143">**nameWithPictureAndDetails**</span></span> | <span data-ttu-id="7240c-144">Nombre de la persona junto con su imagen y detalles adicionales.</span><span class="sxs-lookup"><span data-stu-id="7240c-144">The person's name along with their picture and additional details.</span></span>
| <span data-ttu-id="7240c-145">**nameWithPresence**</span><span class="sxs-lookup"><span data-stu-id="7240c-145">**nameWithPresence**</span></span>          | <span data-ttu-id="7240c-146">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7240c-146">Default.</span></span> <span data-ttu-id="7240c-147">Nombre de la persona con un icono de indicador de presencia (disponible/ocupado/etc.).</span><span class="sxs-lookup"><span data-stu-id="7240c-147">The person's name with a presence indicator icon (available/busy/etc.)</span></span>
| <span data-ttu-id="7240c-148">**office**</span><span class="sxs-lookup"><span data-stu-id="7240c-148">**office**</span></span>                    | <span data-ttu-id="7240c-149">Número de la oficina de la persona.</span><span class="sxs-lookup"><span data-stu-id="7240c-149">The person's office number.</span></span>
| <span data-ttu-id="7240c-150">**pictureOnly36x36**</span><span class="sxs-lookup"><span data-stu-id="7240c-150">**pictureOnly36x36**</span></span>          | <span data-ttu-id="7240c-151">Imagen de la persona, delimitado por un cuadrado de 36x36 píxeles.</span><span class="sxs-lookup"><span data-stu-id="7240c-151">The person's picture, bounded by a 36x36 px square.</span></span>
| <span data-ttu-id="7240c-152">**pictureOnly48x48**</span><span class="sxs-lookup"><span data-stu-id="7240c-152">**pictureOnly48x48**</span></span>          | <span data-ttu-id="7240c-153">Imagen de la persona, delimitado por un cuadrado de 48x48 píxeles.</span><span class="sxs-lookup"><span data-stu-id="7240c-153">The person's picture, bounded by a 48x48 px square.</span></span>
| <span data-ttu-id="7240c-154">**pictureOnly72x72**</span><span class="sxs-lookup"><span data-stu-id="7240c-154">**pictureOnly72x72**</span></span>          | <span data-ttu-id="7240c-155">Imagen de la persona, delimitado por un cuadrado de 72x72 píxeles.</span><span class="sxs-lookup"><span data-stu-id="7240c-155">The person's picture, bounded by a 72x72 px square.</span></span>
| <span data-ttu-id="7240c-156">**sipAddress**</span><span class="sxs-lookup"><span data-stu-id="7240c-156">**sipAddress**</span></span>                | <span data-ttu-id="7240c-157">Dirección SIP de la persona.</span><span class="sxs-lookup"><span data-stu-id="7240c-157">The person's sip address.</span></span>
| <span data-ttu-id="7240c-158">**title**</span><span class="sxs-lookup"><span data-stu-id="7240c-158">**title**</span></span>                     | <span data-ttu-id="7240c-159">Puesto de la persona en la organización.</span><span class="sxs-lookup"><span data-stu-id="7240c-159">The person's title in the organization.</span></span>
| <span data-ttu-id="7240c-160">**userName**</span><span class="sxs-lookup"><span data-stu-id="7240c-160">**userName**</span></span>                  | <span data-ttu-id="7240c-161">Nombre de usuario de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="7240c-161">The person or group's user name.</span></span>
| <span data-ttu-id="7240c-162">**workEmail**</span><span class="sxs-lookup"><span data-stu-id="7240c-162">**workEmail**</span></span>                 | <span data-ttu-id="7240c-163">Dirección de correo electrónico de la persona o el grupo.</span><span class="sxs-lookup"><span data-stu-id="7240c-163">The person or group's email address.</span></span>
| <span data-ttu-id="7240c-164">**workPhone**</span><span class="sxs-lookup"><span data-stu-id="7240c-164">**workPhone**</span></span>                 | <span data-ttu-id="7240c-165">Número de teléfono del trabajo de la persona.</span><span class="sxs-lookup"><span data-stu-id="7240c-165">The person's work phone number.</span></span>

<span data-ttu-id="7240c-166">Nota: Se pueden devolver tipos DisplayAs adicionales.</span><span class="sxs-lookup"><span data-stu-id="7240c-166">Note: Additional DisplayAs types may be returned.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/PersonOrGroupColumn"
} -->
