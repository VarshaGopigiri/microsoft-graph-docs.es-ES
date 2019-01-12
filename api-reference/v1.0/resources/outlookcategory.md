---
title: Tipo de recurso outlookCategory
description: Representa una categoría en la que un usuario puede agrupar elementos de Outlook tales como mensajes y eventos. El usuario define las categorías en una lista maestra y puede aplicar uno o varios de estos definidos por el usuario
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 490ecaf2e6303cc943646dbed99b3202b8d57525
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953129"
---
# <a name="outlookcategory-resource-type"></a><span data-ttu-id="234f1-104">Tipo de recurso outlookCategory</span><span class="sxs-lookup"><span data-stu-id="234f1-104">outlookCategory resource type</span></span>


<span data-ttu-id="234f1-105">Representa una categoría en la que un usuario puede agrupar elementos de Outlook tales como mensajes y eventos.</span><span class="sxs-lookup"><span data-stu-id="234f1-105">Represents a category by which a user can group Outlook items such as messages and events.</span></span> <span data-ttu-id="234f1-106">El usuario define categorías en una lista principal y puede aplicar una o varias de estas categorías definidas por el usuario a un elemento.</span><span class="sxs-lookup"><span data-stu-id="234f1-106">The user defines categories in a master list, and can apply one or more of these user-defined categories to an item.</span></span> 

<span data-ttu-id="234f1-107">Con la API de REST, puede [crear](../api/outlookuser-post-mastercategories.md) y definir categorías en la lista principal de categorías de un usuario.</span><span class="sxs-lookup"><span data-stu-id="234f1-107">Using the REST API, you can [create](../api/outlookuser-post-mastercategories.md) and define categories in the master list of categories for a user.</span></span> <span data-ttu-id="234f1-108">También puede [obtener esta lista principal de categorías](../api/outlookuser-list-mastercategories.md), [obtener una categoría específica](../api/outlookcategory-get.md), [actualizar](../api/outlookcategory-update.md) el color asociado a una categoría o [eliminar](../api/outlookcategory-delete.md) una categoría.</span><span class="sxs-lookup"><span data-stu-id="234f1-108">You can also [get this master list of categories](../api/outlookuser-list-mastercategories.md), [get a specific category](../api/outlookcategory-get.md), [update](../api/outlookcategory-update.md) the color associated with a category, or [delete](../api/outlookcategory-delete.md) a category.</span></span> <span data-ttu-id="234f1-109">Puede aplicar una categoría a un elemento asignando la propiedad **displayName** de la categoría a la colección **categories** del elemento.</span><span class="sxs-lookup"><span data-stu-id="234f1-109">You can apply a category to an item by assigning the **displayName** property of the category to the **categories** collection of the item.</span></span>
<span data-ttu-id="234f1-110">Los recursos que se pueden asignar a categorías incluyen [contact](contact.md), [event](event.md), [message](message.md) y [post](post.md).</span><span class="sxs-lookup"><span data-stu-id="234f1-110">Resources that can be assigned categories include [contact](contact.md), [event](event.md), [message](message.md), and [post](post.md).</span></span>   

<span data-ttu-id="234f1-111">A cada categoría se le asignan atributos con dos propiedades: **displayName** y **color**.</span><span class="sxs-lookup"><span data-stu-id="234f1-111">Each category is attributed by 2 properties: **displayName** and **color**.</span></span> <span data-ttu-id="234f1-112">El valor de **displayName** debe ser único en la lista principal de un usuario.</span><span class="sxs-lookup"><span data-stu-id="234f1-112">The **displayName** value must be unique in a user's master list.</span></span> <span data-ttu-id="234f1-113">Pero el valor de **color** no tiene que ser único; puede asignarse el mismo color a varias categorías de la lista principal.</span><span class="sxs-lookup"><span data-stu-id="234f1-113">The **color** however does not have to be unique; multiple categories in the master list can be mapped to the same color.</span></span> <span data-ttu-id="234f1-114">Puede asignar hasta 25 colores distintos a las categorías de la lista principal de un usuario.</span><span class="sxs-lookup"><span data-stu-id="234f1-114">You can map up to 25 different colors to categories in a user's master list.</span></span>

## <a name="properties"></a><span data-ttu-id="234f1-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="234f1-115">Properties</span></span>
| <span data-ttu-id="234f1-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="234f1-116">Property</span></span>     | <span data-ttu-id="234f1-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="234f1-117">Type</span></span>   |<span data-ttu-id="234f1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="234f1-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="234f1-119">displayName</span><span class="sxs-lookup"><span data-stu-id="234f1-119">displayName</span></span>|<span data-ttu-id="234f1-120">String</span><span class="sxs-lookup"><span data-stu-id="234f1-120">String</span></span>|<span data-ttu-id="234f1-121">Nombre único que identifica una categoría en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="234f1-121">A unique name that identifies a category in the user's mailbox.</span></span> <span data-ttu-id="234f1-122">Después de crear una categoría, no puede cambiarse el nombre.</span><span class="sxs-lookup"><span data-stu-id="234f1-122">After a category is created, the name cannot be changed.</span></span> <span data-ttu-id="234f1-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="234f1-123">Read-only.</span></span>|
|<span data-ttu-id="234f1-124">color</span><span class="sxs-lookup"><span data-stu-id="234f1-124">color</span></span>|<span data-ttu-id="234f1-125">categoryColor</span><span class="sxs-lookup"><span data-stu-id="234f1-125">categoryColor</span></span>|<span data-ttu-id="234f1-126">Constante de color preestablecida que caracteriza a una categoría y a la que se asigna uno de los 25 colores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="234f1-126">A pre-set color constant that characterizes a category, and that is mapped to one of 25 predefined colors.</span></span> <span data-ttu-id="234f1-127">Vea la nota siguiente.</span><span class="sxs-lookup"><span data-stu-id="234f1-127">See the note below.</span></span> |

> <span data-ttu-id="234f1-128">**Nota** Los posibles valores de **color** son constantes preestablecidas tales como `None`, `preset0` y `preset1`.</span><span class="sxs-lookup"><span data-stu-id="234f1-128">**Note** The possible values for **color** are pre-set constants such as `None`, `preset0` and `preset1`.</span></span> <span data-ttu-id="234f1-129">A cada constante preestablecida se le asigna asimismo un color; el color real depende del cliente de Outlook en que se muestran las categorías.</span><span class="sxs-lookup"><span data-stu-id="234f1-129">Each pre-set constant is further mapped to a color; the actual color is dependent on the Outlook client that the categories are being displayed in.</span></span> <span data-ttu-id="234f1-130">La siguiente tabla muestra los colores asignados a cada constante preestablecida en Outlook (cliente de escritorio).</span><span class="sxs-lookup"><span data-stu-id="234f1-130">The following table shows the colors mapped to each pre-set constant for Outlook (desktop client).</span></span> 

| <span data-ttu-id="234f1-131">Constante preestablecida</span><span class="sxs-lookup"><span data-stu-id="234f1-131">Pre-set constant</span></span>  | <span data-ttu-id="234f1-132">Color al que se asigna en Outlook</span><span class="sxs-lookup"><span data-stu-id="234f1-132">Color mapped to in Outlook</span></span> |
|:---------------|:--------|
| <span data-ttu-id="234f1-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="234f1-133">None</span></span> | <span data-ttu-id="234f1-134">Ningún color asignado</span><span class="sxs-lookup"><span data-stu-id="234f1-134">No color mapped</span></span> |
| <span data-ttu-id="234f1-135">Preset0</span><span class="sxs-lookup"><span data-stu-id="234f1-135">Preset0</span></span> | <span data-ttu-id="234f1-136">Rojo</span><span class="sxs-lookup"><span data-stu-id="234f1-136">Red</span></span> |
| <span data-ttu-id="234f1-137">Preset1</span><span class="sxs-lookup"><span data-stu-id="234f1-137">Preset1</span></span> | <span data-ttu-id="234f1-138">Naranja</span><span class="sxs-lookup"><span data-stu-id="234f1-138">Orange</span></span> |
| <span data-ttu-id="234f1-139">Preset2</span><span class="sxs-lookup"><span data-stu-id="234f1-139">Preset2</span></span> | <span data-ttu-id="234f1-140">Marrón</span><span class="sxs-lookup"><span data-stu-id="234f1-140">Brown</span></span> |
| <span data-ttu-id="234f1-141">Preset3</span><span class="sxs-lookup"><span data-stu-id="234f1-141">Preset3</span></span> | <span data-ttu-id="234f1-142">Amarillo</span><span class="sxs-lookup"><span data-stu-id="234f1-142">Yellow</span></span> |
| <span data-ttu-id="234f1-143">Preset4</span><span class="sxs-lookup"><span data-stu-id="234f1-143">Preset4</span></span> | <span data-ttu-id="234f1-144">Verde</span><span class="sxs-lookup"><span data-stu-id="234f1-144">Green</span></span> |
| <span data-ttu-id="234f1-145">Preset5</span><span class="sxs-lookup"><span data-stu-id="234f1-145">Preset5</span></span> | <span data-ttu-id="234f1-146">Verde azulado</span><span class="sxs-lookup"><span data-stu-id="234f1-146">Teal</span></span> |
| <span data-ttu-id="234f1-147">Preset6</span><span class="sxs-lookup"><span data-stu-id="234f1-147">Preset6</span></span> | <span data-ttu-id="234f1-148">Oliva</span><span class="sxs-lookup"><span data-stu-id="234f1-148">Olive</span></span> |
| <span data-ttu-id="234f1-149">Preset7</span><span class="sxs-lookup"><span data-stu-id="234f1-149">Preset7</span></span> | <span data-ttu-id="234f1-150">Azul</span><span class="sxs-lookup"><span data-stu-id="234f1-150">Blue</span></span> |
| <span data-ttu-id="234f1-151">Preset8</span><span class="sxs-lookup"><span data-stu-id="234f1-151">Preset8</span></span> | <span data-ttu-id="234f1-152">Púrpura</span><span class="sxs-lookup"><span data-stu-id="234f1-152">Purple</span></span> |
| <span data-ttu-id="234f1-153">Preset9</span><span class="sxs-lookup"><span data-stu-id="234f1-153">Preset9</span></span> | <span data-ttu-id="234f1-154">Arándano</span><span class="sxs-lookup"><span data-stu-id="234f1-154">Cranberry</span></span> |
| <span data-ttu-id="234f1-155">Preset10</span><span class="sxs-lookup"><span data-stu-id="234f1-155">Preset10</span></span> | <span data-ttu-id="234f1-156">Acero</span><span class="sxs-lookup"><span data-stu-id="234f1-156">Steel</span></span> |
| <span data-ttu-id="234f1-157">Preset11</span><span class="sxs-lookup"><span data-stu-id="234f1-157">Preset11</span></span> | <span data-ttu-id="234f1-158">Acero oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-158">DarkSteel</span></span> |
| <span data-ttu-id="234f1-159">Preset12</span><span class="sxs-lookup"><span data-stu-id="234f1-159">Preset12</span></span> | <span data-ttu-id="234f1-160">Gris</span><span class="sxs-lookup"><span data-stu-id="234f1-160">Gray</span></span> |
| <span data-ttu-id="234f1-161">Preset13</span><span class="sxs-lookup"><span data-stu-id="234f1-161">Preset13</span></span> | <span data-ttu-id="234f1-162">Gris oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-162">DarkGray</span></span> |
| <span data-ttu-id="234f1-163">Preset14</span><span class="sxs-lookup"><span data-stu-id="234f1-163">Preset14</span></span> | <span data-ttu-id="234f1-164">Negro</span><span class="sxs-lookup"><span data-stu-id="234f1-164">Black</span></span> |
| <span data-ttu-id="234f1-165">Preset15</span><span class="sxs-lookup"><span data-stu-id="234f1-165">Preset15</span></span> | <span data-ttu-id="234f1-166">Rojo oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-166">DarkRed</span></span> |
| <span data-ttu-id="234f1-167">Preset16</span><span class="sxs-lookup"><span data-stu-id="234f1-167">Preset16</span></span> | <span data-ttu-id="234f1-168">Anaranjado oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-168">DarkOrange</span></span> |
| <span data-ttu-id="234f1-169">Preset17</span><span class="sxs-lookup"><span data-stu-id="234f1-169">Preset17</span></span> | <span data-ttu-id="234f1-170">Marrón oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-170">DarkBrown</span></span> |
| <span data-ttu-id="234f1-171">Preset18</span><span class="sxs-lookup"><span data-stu-id="234f1-171">Preset18</span></span> | <span data-ttu-id="234f1-172">Amarillo oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-172">DarkYellow</span></span> |
| <span data-ttu-id="234f1-173">Preset19</span><span class="sxs-lookup"><span data-stu-id="234f1-173">Preset19</span></span> | <span data-ttu-id="234f1-174">Verde oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-174">DarkGreen</span></span> |
| <span data-ttu-id="234f1-175">Preset20</span><span class="sxs-lookup"><span data-stu-id="234f1-175">Preset20</span></span> | <span data-ttu-id="234f1-176">Verde azulado oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-176">DarkTeal</span></span> |
| <span data-ttu-id="234f1-177">Preset21</span><span class="sxs-lookup"><span data-stu-id="234f1-177">Preset21</span></span> | <span data-ttu-id="234f1-178">Oliva oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-178">DarkOlive</span></span> |
| <span data-ttu-id="234f1-179">Preset22</span><span class="sxs-lookup"><span data-stu-id="234f1-179">Preset22</span></span> | <span data-ttu-id="234f1-180">Azul oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-180">DarkBlue</span></span> |
| <span data-ttu-id="234f1-181">Preset23</span><span class="sxs-lookup"><span data-stu-id="234f1-181">Preset23</span></span> | <span data-ttu-id="234f1-182">Púrpura oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-182">DarkPurple</span></span> |
| <span data-ttu-id="234f1-183">Preset24</span><span class="sxs-lookup"><span data-stu-id="234f1-183">Preset24</span></span> | <span data-ttu-id="234f1-184">Arándano oscuro</span><span class="sxs-lookup"><span data-stu-id="234f1-184">DarkCranberry</span></span> |

## <a name="json-representation"></a><span data-ttu-id="234f1-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="234f1-185">JSON representation</span></span>
<span data-ttu-id="234f1-186">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="234f1-186">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.outlookCategory"
}-->

```json
{
  "color": "String",
  "displayName": "String"
}

```

## <a name="methods"></a><span data-ttu-id="234f1-187">Métodos</span><span class="sxs-lookup"><span data-stu-id="234f1-187">Methods</span></span>
| <span data-ttu-id="234f1-188">Método</span><span class="sxs-lookup"><span data-stu-id="234f1-188">Method</span></span>           | <span data-ttu-id="234f1-189">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="234f1-189">Return Type</span></span>    |<span data-ttu-id="234f1-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="234f1-190">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="234f1-191">Enumerar categorías</span><span class="sxs-lookup"><span data-stu-id="234f1-191">List categories</span></span>](../api/outlookuser-list-mastercategories.md) | <span data-ttu-id="234f1-192">Colección [outlookCategory](../resources/outlookcategory.md)</span><span class="sxs-lookup"><span data-stu-id="234f1-192">[outlookCategory](../resources/outlookcategory.md) collection</span></span> |<span data-ttu-id="234f1-193">Obtener todas las categorías que han sido definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="234f1-193">Get all the categories that have been defined for the user.</span></span>|
|[<span data-ttu-id="234f1-194">Obtener categoría</span><span class="sxs-lookup"><span data-stu-id="234f1-194">Get category</span></span>](../api/outlookcategory-get.md) | [<span data-ttu-id="234f1-195">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="234f1-195">outlookCategory</span></span>](../resources/outlookcategory.md) |<span data-ttu-id="234f1-196">Obtener las propiedades y relaciones del objeto **outlookCategory** especificado.</span><span class="sxs-lookup"><span data-stu-id="234f1-196">Get the properties and relationships of the specified **outlookCategory** object.</span></span>|
|[<span data-ttu-id="234f1-197">Crear</span><span class="sxs-lookup"><span data-stu-id="234f1-197">Create</span></span>](../api/outlookuser-post-mastercategories.md) | [<span data-ttu-id="234f1-198">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="234f1-198">outlookCategory</span></span>](../resources/outlookcategory.md) |<span data-ttu-id="234f1-199">Crear un objeto **outlookCategory** en la lista principal de categorías del usuario.</span><span class="sxs-lookup"><span data-stu-id="234f1-199">Create an **outlookCategory** object in the user's master list of categories.</span></span>|
|[<span data-ttu-id="234f1-200">Actualizar</span><span class="sxs-lookup"><span data-stu-id="234f1-200">Update</span></span>](../api/outlookcategory-update.md) | [<span data-ttu-id="234f1-201">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="234f1-201">outlookCategory</span></span>](../resources/outlookcategory.md) |<span data-ttu-id="234f1-202">Actualizar la propiedad modificable **color** del objeto **outlookCategory** especificado.</span><span class="sxs-lookup"><span data-stu-id="234f1-202">Update the writable property, **color**, of the specified **outlookCategory** object.</span></span> |
|[<span data-ttu-id="234f1-203">Eliminar</span><span class="sxs-lookup"><span data-stu-id="234f1-203">Delete</span></span>](../api/outlookcategory-delete.md) | <span data-ttu-id="234f1-204">Ninguno</span><span class="sxs-lookup"><span data-stu-id="234f1-204">None</span></span> |<span data-ttu-id="234f1-205">Eliminar el objeto **outlookCategory** especificado.</span><span class="sxs-lookup"><span data-stu-id="234f1-205">Delete the specified **outlookCategory** object.</span></span> |


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookCategory resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
      "Warning: /api-reference/v1.0/resources/outlookcategory.md:
      Failed to parse any rows out of table with headers: |Pre-set constant|Color mapped to in Outlook|"
  ],
  "tocPath": ""
}-->
 
