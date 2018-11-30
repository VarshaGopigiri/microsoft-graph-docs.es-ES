---
title: Tipo de recurso educationSchool
description: 'Centro educativo. El recurso **educationSchool** actualmente corresponde a un recurso administrativeUnit y comparte el mismo identificador.  '
ms.openlocfilehash: 6a478428874c7c600f60a6924dc06be5f4e3ba11
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088562"
---
# <a name="educationschool-resource-type"></a><span data-ttu-id="a2791-104">Tipo de recurso educationSchool</span><span class="sxs-lookup"><span data-stu-id="a2791-104">educationSchool resource type</span></span>

> <span data-ttu-id="a2791-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2791-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2791-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2791-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a2791-107">Centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-107">A school.</span></span> <span data-ttu-id="a2791-108">El recurso **educationSchool** actualmente corresponde a un recurso [administrativeUnit](administrativeunit.md) y comparte el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="a2791-108">The **educationSchool** resource currently corresponds to an [administrativeUnit](administrativeunit.md) resource and shares the same ID.</span></span>  

<span data-ttu-id="a2791-109">Este recurso es un subtipo de [educationOrganization](educationorganization.md).</span><span class="sxs-lookup"><span data-stu-id="a2791-109">This resource is a subtype of [educationOrganization](educationorganization.md).</span></span>




## <a name="methods"></a><span data-ttu-id="a2791-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2791-110">Methods</span></span>

| <span data-ttu-id="a2791-111">Método</span><span class="sxs-lookup"><span data-stu-id="a2791-111">Method</span></span>           | <span data-ttu-id="a2791-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2791-112">Return Type</span></span>    |<span data-ttu-id="a2791-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2791-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a2791-114">Get</span><span class="sxs-lookup"><span data-stu-id="a2791-114">Get</span></span>](../api/educationschool-get.md) | [<span data-ttu-id="a2791-115">educationSchool</span><span class="sxs-lookup"><span data-stu-id="a2791-115">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="a2791-116">Lea las propiedades y relaciones de un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="a2791-116">Read properties and relationships of an **educationSchool** object.</span></span>|
|[<span data-ttu-id="a2791-117">Agregar clase</span><span class="sxs-lookup"><span data-stu-id="a2791-117">Add class</span></span>](../api/educationschool-post-classes.md) |[<span data-ttu-id="a2791-118">educationClass</span><span class="sxs-lookup"><span data-stu-id="a2791-118">educationClass</span></span>](educationclass.md)| <span data-ttu-id="a2791-119">Agregue un nuevo **educationClass** en el centro educativo publicando en la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="a2791-119">Add a new **educationClass** for the school by posting to the classes navigation property.</span></span>|
|[<span data-ttu-id="a2791-120">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="a2791-120">List classes</span></span>](../api/educationschool-list-classes.md) |<span data-ttu-id="a2791-121">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="a2791-121">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="a2791-122">Obtenga la colección de objetos **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="a2791-122">Get the **educationClass** object collection.</span></span>|
|[<span data-ttu-id="a2791-123">Quitar clase</span><span class="sxs-lookup"><span data-stu-id="a2791-123">Remove class</span></span>](../api/educationschool-delete-classes.md) |[<span data-ttu-id="a2791-124">educationClass</span><span class="sxs-lookup"><span data-stu-id="a2791-124">educationClass</span></span>](educationclass.md)| <span data-ttu-id="a2791-125">Quite un **educationClass** del centro educativo mediante la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="a2791-125">Remove an **educationClass** from the school through the classes navigation property.</span></span>|
|[<span data-ttu-id="a2791-126">Agregar usuario</span><span class="sxs-lookup"><span data-stu-id="a2791-126">Add user</span></span>](../api/educationschool-post-users.md) |[<span data-ttu-id="a2791-127">educationUser</span><span class="sxs-lookup"><span data-stu-id="a2791-127">educationUser</span></span>](educationuser.md)| <span data-ttu-id="a2791-128">Agregue un nuevo **educationUser** en el centro educativo publicando en la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="a2791-128">Add a new **educationUser** for the school by posting to the **users** navigation property.</span></span>|
|[<span data-ttu-id="a2791-129">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="a2791-129">List users</span></span>](../api/educationschool-list-users.md) |<span data-ttu-id="a2791-130">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="a2791-130">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="a2791-131">Obtenga la colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="a2791-131">Get the **educationUser** object collection.</span></span>|
|[<span data-ttu-id="a2791-132">Quitar usuario</span><span class="sxs-lookup"><span data-stu-id="a2791-132">Remove user</span></span>](../api/educationschool-delete-users.md) |[<span data-ttu-id="a2791-133">educationUser</span><span class="sxs-lookup"><span data-stu-id="a2791-133">educationUser</span></span>](educationuser.md)| <span data-ttu-id="a2791-134">Quite un **educationUser** del centro educativo mediante la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="a2791-134">Remove an **educationUser** from the school through the **users** navigation property.</span></span>|
|[<span data-ttu-id="a2791-135">Obtener administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="a2791-135">Get administrativeUnit</span></span>](../api/educationschool-get-administrativeunit.md) |[<span data-ttu-id="a2791-136">administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="a2791-136">administrativeUnit</span></span>](administrativeunit.md)| <span data-ttu-id="a2791-137">Obtenga el directorio simple **administrativeUnit** correspondiente a este objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="a2791-137">Get the **administrativeUnit** that corresponds to this **educationSchool**.</span></span>|
|[<span data-ttu-id="a2791-138">Actualizar</span><span class="sxs-lookup"><span data-stu-id="a2791-138">Update</span></span>](../api/educationschool-update.md) | [<span data-ttu-id="a2791-139">educationSchool</span><span class="sxs-lookup"><span data-stu-id="a2791-139">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="a2791-140">Actualice un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="a2791-140">Update an **educationSchool** object.</span></span> |
|[<span data-ttu-id="a2791-141">Eliminar</span><span class="sxs-lookup"><span data-stu-id="a2791-141">Delete</span></span>](../api/educationschool-delete.md) | <span data-ttu-id="a2791-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a2791-142">None</span></span> |<span data-ttu-id="a2791-143">Elimine un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="a2791-143">Delete an **educationSchool** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="a2791-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2791-144">Properties</span></span>
| <span data-ttu-id="a2791-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2791-145">Property</span></span>     | <span data-ttu-id="a2791-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2791-146">Type</span></span>   |<span data-ttu-id="a2791-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2791-147">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2791-148">id</span><span class="sxs-lookup"><span data-stu-id="a2791-148">id</span></span>|<span data-ttu-id="a2791-149">String</span><span class="sxs-lookup"><span data-stu-id="a2791-149">String</span></span>|<span data-ttu-id="a2791-150">GUID de este centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-150">GUID of this school.</span></span>|
|<span data-ttu-id="a2791-151">displayName</span><span class="sxs-lookup"><span data-stu-id="a2791-151">displayName</span></span>| <span data-ttu-id="a2791-152">String</span><span class="sxs-lookup"><span data-stu-id="a2791-152">String</span></span>| <span data-ttu-id="a2791-153">Nombre para mostrar del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-153">Display name of the school.</span></span>| 
|<span data-ttu-id="a2791-154">description</span><span class="sxs-lookup"><span data-stu-id="a2791-154">description</span></span>| <span data-ttu-id="a2791-155">String</span><span class="sxs-lookup"><span data-stu-id="a2791-155">String</span></span> | <span data-ttu-id="a2791-156">Descripción del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-156">Description of the school.</span></span>| 
|<span data-ttu-id="a2791-157">status</span><span class="sxs-lookup"><span data-stu-id="a2791-157">status</span></span>| <span data-ttu-id="a2791-158">string</span><span class="sxs-lookup"><span data-stu-id="a2791-158">string</span></span>| <span data-ttu-id="a2791-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2791-159">Read-Only.</span></span> <span data-ttu-id="a2791-160">Los valores posibles son: `inactive`, `active`, `expired` y `deleteable`.</span><span class="sxs-lookup"><span data-stu-id="a2791-160">Possible values are: `inactive`, `active`, `expired`, `deleteable`.</span></span>|
|<span data-ttu-id="a2791-161">externalSource</span><span class="sxs-lookup"><span data-stu-id="a2791-161">externalSource</span></span>| <span data-ttu-id="a2791-162">string</span><span class="sxs-lookup"><span data-stu-id="a2791-162">string</span></span>| <span data-ttu-id="a2791-163">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2791-163">Read-Only.</span></span>  <span data-ttu-id="a2791-164">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="a2791-164">Possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="a2791-165">principalEmail</span><span class="sxs-lookup"><span data-stu-id="a2791-165">principalEmail</span></span>| <span data-ttu-id="a2791-166">String</span><span class="sxs-lookup"><span data-stu-id="a2791-166">String</span></span>| <span data-ttu-id="a2791-167">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="a2791-167">Email address of the principal.</span></span>|
|<span data-ttu-id="a2791-168">principalName</span><span class="sxs-lookup"><span data-stu-id="a2791-168">principalName</span></span>| <span data-ttu-id="a2791-169">String</span><span class="sxs-lookup"><span data-stu-id="a2791-169">String</span></span> | <span data-ttu-id="a2791-170">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="a2791-170">Name of the principal.</span></span>|
|<span data-ttu-id="a2791-171">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a2791-171">externalPrincipalId</span></span>| <span data-ttu-id="a2791-172">String</span><span class="sxs-lookup"><span data-stu-id="a2791-172">String</span></span> | <span data-ttu-id="a2791-173">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a2791-173">ID of principal in syncing system.</span></span> |
|<span data-ttu-id="a2791-174">highestGrade</span><span class="sxs-lookup"><span data-stu-id="a2791-174">highestGrade</span></span>|<span data-ttu-id="a2791-175">String</span><span class="sxs-lookup"><span data-stu-id="a2791-175">String</span></span>| <span data-ttu-id="a2791-176">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="a2791-176">Highest grade taught.</span></span> |
|<span data-ttu-id="a2791-177">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="a2791-177">lowestGrade</span></span>|<span data-ttu-id="a2791-178">String</span><span class="sxs-lookup"><span data-stu-id="a2791-178">String</span></span>| <span data-ttu-id="a2791-179">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="a2791-179">Lowest grade taught.</span></span> |
|<span data-ttu-id="a2791-180">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="a2791-180">schoolNumber</span></span>|<span data-ttu-id="a2791-181">String</span><span class="sxs-lookup"><span data-stu-id="a2791-181">String</span></span>| <span data-ttu-id="a2791-182">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="a2791-182">School Number.</span></span>|
|<span data-ttu-id="a2791-183">externalId</span><span class="sxs-lookup"><span data-stu-id="a2791-183">externalId</span></span>|<span data-ttu-id="a2791-184">String</span><span class="sxs-lookup"><span data-stu-id="a2791-184">String</span></span>| <span data-ttu-id="a2791-185">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a2791-185">ID of school in syncing system.</span></span> |
|<span data-ttu-id="a2791-186">phone</span><span class="sxs-lookup"><span data-stu-id="a2791-186">phone</span></span>|<span data-ttu-id="a2791-187">String</span><span class="sxs-lookup"><span data-stu-id="a2791-187">String</span></span>| <span data-ttu-id="a2791-188">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-188">Phone number of school.</span></span> |
|<span data-ttu-id="a2791-189">fax</span><span class="sxs-lookup"><span data-stu-id="a2791-189">fax</span></span>|<span data-ttu-id="a2791-190">String</span><span class="sxs-lookup"><span data-stu-id="a2791-190">String</span></span>| <span data-ttu-id="a2791-191">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-191">Fax number of school.</span></span> |
|<span data-ttu-id="a2791-192">address</span><span class="sxs-lookup"><span data-stu-id="a2791-192">address</span></span>|[<span data-ttu-id="a2791-193">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="a2791-193">physicalAddress</span></span>](physicaladdress.md)| <span data-ttu-id="a2791-194">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-194">Address of the school.</span></span>|
|<span data-ttu-id="a2791-195">createdBy</span><span class="sxs-lookup"><span data-stu-id="a2791-195">createdBy</span></span>|[<span data-ttu-id="a2791-196">identitySet</span><span class="sxs-lookup"><span data-stu-id="a2791-196">identitySet</span></span>](identityset.md)|<span data-ttu-id="a2791-197">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-197">Entity who created the school.</span></span>|


## <a name="relationships"></a><span data-ttu-id="a2791-198">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a2791-198">Relationships</span></span>
| <span data-ttu-id="a2791-199">Relación</span><span class="sxs-lookup"><span data-stu-id="a2791-199">Relationship</span></span> | <span data-ttu-id="a2791-200">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2791-200">Type</span></span>   |<span data-ttu-id="a2791-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2791-201">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2791-202">classes</span><span class="sxs-lookup"><span data-stu-id="a2791-202">classes</span></span>|<span data-ttu-id="a2791-203">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="a2791-203">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="a2791-204">Clases impartidas en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-204">Classes taught at the school.</span></span> <span data-ttu-id="a2791-205">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="a2791-205">Nullable.</span></span>|
|<span data-ttu-id="a2791-206">users</span><span class="sxs-lookup"><span data-stu-id="a2791-206">users</span></span>|<span data-ttu-id="a2791-207">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="a2791-207">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="a2791-208">Usuarios del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a2791-208">Users in the school.</span></span> <span data-ttu-id="a2791-209">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="a2791-209">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a2791-210">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2791-210">JSON representation</span></span>

<span data-ttu-id="a2791-211">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a2791-211">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSchool"
}-->

```json
{
  "id": "String",
  "displayName": "String",
  "description": "String",
  "status": "String",
  "externalSource": "String",
  "principalEmail": "String",
  "principalName": "String",
  "externalPrincipalId": "String",
  "highestGrade": "String",
  "lowestGrade": "String",
  "schoolNumber": "String",
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "externalId": "String",
  "fax": "String",
  "phone": "String",
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSchool resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
