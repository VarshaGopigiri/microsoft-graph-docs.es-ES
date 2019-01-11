---
title: Tipo de recurso outlookCategory
description: Representa una categoría en la que un usuario puede agrupar elementos de Outlook tales como mensajes y eventos. En Outlook, el usuario define las categorías en una lista maestra y puede aplicar uno o varios de estos definidos por el usuario
localization_priority: Normal
ms.openlocfilehash: b9c1a3a1813195a36dd1f1cf587cf69d2ddb5f1b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816761"
---
# <a name="outlookcategory-resource-type"></a><span data-ttu-id="ca689-104">Tipo de recurso outlookCategory</span><span class="sxs-lookup"><span data-stu-id="ca689-104">outlookCategory resource type</span></span>

> <span data-ttu-id="ca689-105">**Importante:** Las API de la versión de /beta en Microsoft Graph están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="ca689-105">**Important:** APIs under the /beta version in Microsoft Graph are subject to change.</span></span> <span data-ttu-id="ca689-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ca689-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ca689-107">Representa una categoría en la que un usuario puede agrupar elementos de Outlook tales como mensajes y eventos.</span><span class="sxs-lookup"><span data-stu-id="ca689-107">Represents a category by which a user can group Outlook items such as messages and events.</span></span> <span data-ttu-id="ca689-108">En Outlook, el usuario define las categorías en una lista maestra y puede aplicar una o varias de estas categorías definidas por el usuario a un elemento.</span><span class="sxs-lookup"><span data-stu-id="ca689-108">In Outlook, the user defines categories in a master list, and can apply one or more of these user-defined categories to an item.</span></span> 

<span data-ttu-id="ca689-109">Con la API de REST, puede [crear](../api/outlookuser-post-mastercategories.md) y definir categorías en la lista principal de categorías de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ca689-109">Using the REST API, you can [create](../api/outlookuser-post-mastercategories.md) and define categories in the master list of categories for a user.</span></span> <span data-ttu-id="ca689-110">También puede [obtener esta lista principal de categorías](../api/outlookuser-list-mastercategories.md), [obtener una categoría específica](../api/outlookcategory-get.md), [actualizar](../api/outlookcategory-update.md) el color asociado a una categoría o [eliminar](../api/outlookcategory-delete.md) una categoría.</span><span class="sxs-lookup"><span data-stu-id="ca689-110">You can also [get this master list of categories](../api/outlookuser-list-mastercategories.md), [get a specific category](../api/outlookcategory-get.md), [update](../api/outlookcategory-update.md) the color associated with a category, or [delete](../api/outlookcategory-delete.md) a category.</span></span> <span data-ttu-id="ca689-111">Puede aplicar una categoría a un elemento asignando la propiedad **displayName** de la categoría a la colección **categories** del elemento.</span><span class="sxs-lookup"><span data-stu-id="ca689-111">You can apply a category to an item by assigning the **displayName** property of the category to the **categories** collection of the item.</span></span>
<span data-ttu-id="ca689-112">Recursos que se pueden asignar categorías incluyen [póngase en contacto con](contact.md), [evento](event.md), [mensaje](message.md), [outlookTask](outlooktask.md)y [registrar](post.md).</span><span class="sxs-lookup"><span data-stu-id="ca689-112">Resources that can be assigned categories include [contact](contact.md), [event](event.md), [message](message.md), [outlookTask](outlooktask.md), and [post](post.md).</span></span>   

<span data-ttu-id="ca689-113">A cada categoría se le asignan atributos con dos propiedades: **displayName** y **color**.</span><span class="sxs-lookup"><span data-stu-id="ca689-113">Each category is attributed by 2 properties: **displayName** and **color**.</span></span> <span data-ttu-id="ca689-114">El valor de **displayName** debe ser único en la lista principal de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ca689-114">The **displayName** value must be unique in a user's master list.</span></span> <span data-ttu-id="ca689-115">Pero el valor de **color** no tiene que ser único; puede asignarse el mismo color a varias categorías de la lista principal.</span><span class="sxs-lookup"><span data-stu-id="ca689-115">The **color** however does not have to be unique; multiple categories in the master list can be mapped to the same color.</span></span> <span data-ttu-id="ca689-116">Puede asignar hasta 25 colores distintos a las categorías de la lista principal de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ca689-116">You can map up to 25 different colors to categories in a user's master list.</span></span>

## <a name="properties"></a><span data-ttu-id="ca689-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca689-117">Properties</span></span>
| <span data-ttu-id="ca689-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca689-118">Property</span></span>     | <span data-ttu-id="ca689-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca689-119">Type</span></span>   |<span data-ttu-id="ca689-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca689-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ca689-121">displayName</span><span class="sxs-lookup"><span data-stu-id="ca689-121">displayName</span></span>|<span data-ttu-id="ca689-122">String</span><span class="sxs-lookup"><span data-stu-id="ca689-122">String</span></span>|<span data-ttu-id="ca689-123">Nombre único que identifica una categoría en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ca689-123">A unique name that identifies a category in the user's mailbox.</span></span> <span data-ttu-id="ca689-124">Después de crear una categoría, no puede cambiarse el nombre.</span><span class="sxs-lookup"><span data-stu-id="ca689-124">After a category is created, the name cannot be changed.</span></span> <span data-ttu-id="ca689-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ca689-125">Read-only.</span></span>|
|<span data-ttu-id="ca689-126">color</span><span class="sxs-lookup"><span data-stu-id="ca689-126">color</span></span>|<span data-ttu-id="ca689-127">String</span><span class="sxs-lookup"><span data-stu-id="ca689-127">String</span></span>|<span data-ttu-id="ca689-128">Constante de color preestablecida que caracteriza a una categoría y a la que se asigna uno de los 25 colores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ca689-128">A pre-set color constant that characterizes a category, and that is mapped to one of 25 predefined colors.</span></span> <span data-ttu-id="ca689-129">Vea la nota siguiente.</span><span class="sxs-lookup"><span data-stu-id="ca689-129">See the note below.</span></span> |

> <span data-ttu-id="ca689-130">**Nota** Los posibles valores de **color** son constantes preestablecidas tales como `None`, `preset0` y `preset1`.</span><span class="sxs-lookup"><span data-stu-id="ca689-130">**Note** The possible values for **color** are pre-set constants such as `None`, `preset0` and `preset1`.</span></span> <span data-ttu-id="ca689-131">A cada constante preestablecida se le asigna asimismo un color; el color real depende del cliente de Outlook en que se muestran las categorías.</span><span class="sxs-lookup"><span data-stu-id="ca689-131">Each pre-set constant is further mapped to a color; the actual color is dependent on the Outlook client that the categories are being displayed in.</span></span> <span data-ttu-id="ca689-132">La siguiente tabla muestra los colores asignados a cada constante preestablecida en Outlook (cliente de escritorio).</span><span class="sxs-lookup"><span data-stu-id="ca689-132">The following table shows the colors mapped to each pre-set constant for Outlook (desktop client).</span></span> 


| <span data-ttu-id="ca689-133">Constante preestablecida</span><span class="sxs-lookup"><span data-stu-id="ca689-133">Pre-set constant</span></span>  | <span data-ttu-id="ca689-134">Color al que se asigna en Outlook</span><span class="sxs-lookup"><span data-stu-id="ca689-134">Color mapped to in Outlook</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ca689-135">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ca689-135">None</span></span> | <span data-ttu-id="ca689-136">Ningún color asignado</span><span class="sxs-lookup"><span data-stu-id="ca689-136">No color mapped</span></span> |
| <span data-ttu-id="ca689-137">Preset0</span><span class="sxs-lookup"><span data-stu-id="ca689-137">Preset0</span></span> | <span data-ttu-id="ca689-138">Rojo</span><span class="sxs-lookup"><span data-stu-id="ca689-138">Red</span></span> |
| <span data-ttu-id="ca689-139">Preset1</span><span class="sxs-lookup"><span data-stu-id="ca689-139">Preset1</span></span> | <span data-ttu-id="ca689-140">Naranja</span><span class="sxs-lookup"><span data-stu-id="ca689-140">Orange</span></span> |
| <span data-ttu-id="ca689-141">Preset2</span><span class="sxs-lookup"><span data-stu-id="ca689-141">Preset2</span></span> | <span data-ttu-id="ca689-142">Marrón</span><span class="sxs-lookup"><span data-stu-id="ca689-142">Brown</span></span> |
| <span data-ttu-id="ca689-143">Preset3</span><span class="sxs-lookup"><span data-stu-id="ca689-143">Preset3</span></span> | <span data-ttu-id="ca689-144">Amarillo</span><span class="sxs-lookup"><span data-stu-id="ca689-144">Yellow</span></span> |
| <span data-ttu-id="ca689-145">Preset4</span><span class="sxs-lookup"><span data-stu-id="ca689-145">Preset4</span></span> | <span data-ttu-id="ca689-146">Verde</span><span class="sxs-lookup"><span data-stu-id="ca689-146">Green</span></span> |
| <span data-ttu-id="ca689-147">Preset5</span><span class="sxs-lookup"><span data-stu-id="ca689-147">Preset5</span></span> | <span data-ttu-id="ca689-148">Verde azulado</span><span class="sxs-lookup"><span data-stu-id="ca689-148">Teal</span></span> |
| <span data-ttu-id="ca689-149">Preset6</span><span class="sxs-lookup"><span data-stu-id="ca689-149">Preset6</span></span> | <span data-ttu-id="ca689-150">Oliva</span><span class="sxs-lookup"><span data-stu-id="ca689-150">Olive</span></span> |
| <span data-ttu-id="ca689-151">Preset7</span><span class="sxs-lookup"><span data-stu-id="ca689-151">Preset7</span></span> | <span data-ttu-id="ca689-152">Azul</span><span class="sxs-lookup"><span data-stu-id="ca689-152">Blue</span></span> |
| <span data-ttu-id="ca689-153">Preset8</span><span class="sxs-lookup"><span data-stu-id="ca689-153">Preset8</span></span> | <span data-ttu-id="ca689-154">Púrpura</span><span class="sxs-lookup"><span data-stu-id="ca689-154">Purple</span></span> |
| <span data-ttu-id="ca689-155">Preset9</span><span class="sxs-lookup"><span data-stu-id="ca689-155">Preset9</span></span> | <span data-ttu-id="ca689-156">Arándano</span><span class="sxs-lookup"><span data-stu-id="ca689-156">Cranberry</span></span> |
| <span data-ttu-id="ca689-157">Preset10</span><span class="sxs-lookup"><span data-stu-id="ca689-157">Preset10</span></span> | <span data-ttu-id="ca689-158">Acero</span><span class="sxs-lookup"><span data-stu-id="ca689-158">Steel</span></span> |
| <span data-ttu-id="ca689-159">Preset11</span><span class="sxs-lookup"><span data-stu-id="ca689-159">Preset11</span></span> | <span data-ttu-id="ca689-160">Acero oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-160">DarkSteel</span></span> |
| <span data-ttu-id="ca689-161">Preset12</span><span class="sxs-lookup"><span data-stu-id="ca689-161">Preset12</span></span> | <span data-ttu-id="ca689-162">Gris</span><span class="sxs-lookup"><span data-stu-id="ca689-162">Gray</span></span> |
| <span data-ttu-id="ca689-163">Preset13</span><span class="sxs-lookup"><span data-stu-id="ca689-163">Preset13</span></span> | <span data-ttu-id="ca689-164">Gris oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-164">DarkGray</span></span> |
| <span data-ttu-id="ca689-165">Preset14</span><span class="sxs-lookup"><span data-stu-id="ca689-165">Preset14</span></span> | <span data-ttu-id="ca689-166">Negro</span><span class="sxs-lookup"><span data-stu-id="ca689-166">Black</span></span> |
| <span data-ttu-id="ca689-167">Preset15</span><span class="sxs-lookup"><span data-stu-id="ca689-167">Preset15</span></span> | <span data-ttu-id="ca689-168">Rojo oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-168">DarkRed</span></span> |
| <span data-ttu-id="ca689-169">Preset16</span><span class="sxs-lookup"><span data-stu-id="ca689-169">Preset16</span></span> | <span data-ttu-id="ca689-170">Anaranjado oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-170">DarkOrange</span></span> |
| <span data-ttu-id="ca689-171">Preset17</span><span class="sxs-lookup"><span data-stu-id="ca689-171">Preset17</span></span> | <span data-ttu-id="ca689-172">Marrón oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-172">DarkBrown</span></span> |
| <span data-ttu-id="ca689-173">Preset18</span><span class="sxs-lookup"><span data-stu-id="ca689-173">Preset18</span></span> | <span data-ttu-id="ca689-174">Amarillo oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-174">DarkYellow</span></span> |
| <span data-ttu-id="ca689-175">Preset19</span><span class="sxs-lookup"><span data-stu-id="ca689-175">Preset19</span></span> | <span data-ttu-id="ca689-176">Verde oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-176">DarkGreen</span></span> |
| <span data-ttu-id="ca689-177">Preset20</span><span class="sxs-lookup"><span data-stu-id="ca689-177">Preset20</span></span> | <span data-ttu-id="ca689-178">Verde azulado oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-178">DarkTeal</span></span> |
| <span data-ttu-id="ca689-179">Preset21</span><span class="sxs-lookup"><span data-stu-id="ca689-179">Preset21</span></span> | <span data-ttu-id="ca689-180">Oliva oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-180">DarkOlive</span></span> |
| <span data-ttu-id="ca689-181">Preset22</span><span class="sxs-lookup"><span data-stu-id="ca689-181">Preset22</span></span> | <span data-ttu-id="ca689-182">Azul oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-182">DarkBlue</span></span> |
| <span data-ttu-id="ca689-183">Preset23</span><span class="sxs-lookup"><span data-stu-id="ca689-183">Preset23</span></span> | <span data-ttu-id="ca689-184">Púrpura oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-184">DarkPurple</span></span> |
| <span data-ttu-id="ca689-185">Preset24</span><span class="sxs-lookup"><span data-stu-id="ca689-185">Preset24</span></span> | <span data-ttu-id="ca689-186">Arándano oscuro</span><span class="sxs-lookup"><span data-stu-id="ca689-186">DarkCranberry</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ca689-187">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ca689-187">JSON representation</span></span>
<span data-ttu-id="ca689-188">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca689-188">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookCategory"
}-->

```json
{
  "color": "String",
  "displayName": "String"
}

```

## <a name="methods"></a><span data-ttu-id="ca689-189">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca689-189">Methods</span></span>
| <span data-ttu-id="ca689-190">Método</span><span class="sxs-lookup"><span data-stu-id="ca689-190">Method</span></span>           | <span data-ttu-id="ca689-191">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca689-191">Return Type</span></span>    |<span data-ttu-id="ca689-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca689-192">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ca689-193">Enumerar categorías</span><span class="sxs-lookup"><span data-stu-id="ca689-193">List categories</span></span>](../api/outlookuser-list-mastercategories.md) | <span data-ttu-id="ca689-194">Colección [outlookCategory](../resources/outlookcategory.md)</span><span class="sxs-lookup"><span data-stu-id="ca689-194">[outlookCategory](../resources/outlookcategory.md) collection</span></span> |<span data-ttu-id="ca689-195">Obtener todas las categorías que han sido definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ca689-195">Get all the categories that have been defined for the user.</span></span>|
|[<span data-ttu-id="ca689-196">Obtener categoría</span><span class="sxs-lookup"><span data-stu-id="ca689-196">Get category</span></span>](../api/outlookcategory-get.md) | [<span data-ttu-id="ca689-197">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="ca689-197">outlookCategory</span></span>](../resources/outlookcategory.md) |<span data-ttu-id="ca689-198">Obtener las propiedades y relaciones del objeto **outlookCategory** especificado.</span><span class="sxs-lookup"><span data-stu-id="ca689-198">Get the properties and relationships of the specified **outlookCategory** object.</span></span>|
|[<span data-ttu-id="ca689-199">Crear</span><span class="sxs-lookup"><span data-stu-id="ca689-199">Create</span></span>](../api/outlookuser-post-mastercategories.md) | [<span data-ttu-id="ca689-200">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="ca689-200">outlookCategory</span></span>](../resources/outlookcategory.md) |<span data-ttu-id="ca689-201">Crear un objeto **outlookCategory** en la lista principal de categorías del usuario.</span><span class="sxs-lookup"><span data-stu-id="ca689-201">Create an **outlookCategory** object in the user's master list of categories.</span></span>|
|[<span data-ttu-id="ca689-202">Actualizar</span><span class="sxs-lookup"><span data-stu-id="ca689-202">Update</span></span>](../api/outlookcategory-update.md) | [<span data-ttu-id="ca689-203">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="ca689-203">outlookCategory</span></span>](../resources/outlookcategory.md) |<span data-ttu-id="ca689-204">Actualizar la propiedad modificable **color** del objeto **outlookCategory** especificado.</span><span class="sxs-lookup"><span data-stu-id="ca689-204">Update the writable property, **color**, of the specified **outlookCategory** object.</span></span> |
|[<span data-ttu-id="ca689-205">Eliminar</span><span class="sxs-lookup"><span data-stu-id="ca689-205">Delete</span></span>](../api/outlookcategory-delete.md) | <span data-ttu-id="ca689-206">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ca689-206">None</span></span> |<span data-ttu-id="ca689-207">Eliminar el objeto **outlookCategory** especificado.</span><span class="sxs-lookup"><span data-stu-id="ca689-207">Delete the specified **outlookCategory** object.</span></span> |


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookCategory resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
      "Warning: /api-reference/beta/resources/outlookcategory.md:
      Failed to parse any rows out of table with headers: |Pre-set constant|Color mapped to in Outlook|"
  ],
  "tocPath": ""
}-->
 
