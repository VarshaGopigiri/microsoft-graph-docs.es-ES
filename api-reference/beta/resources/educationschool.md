---
title: Tipo de recurso educationSchool
description: 'Centro educativo. El recurso **educationSchool** actualmente corresponde a un recurso administrativeUnit y comparte el mismo identificador.  '
localization_priority: Normal
ms.openlocfilehash: 20eacb87b68cbf490131b98a15d3ab3239d73478
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830453"
---
# <a name="educationschool-resource-type"></a><span data-ttu-id="826ed-104">Tipo de recurso educationSchool</span><span class="sxs-lookup"><span data-stu-id="826ed-104">educationSchool resource type</span></span>

> <span data-ttu-id="826ed-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="826ed-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="826ed-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="826ed-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="826ed-107">Centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-107">A school.</span></span> <span data-ttu-id="826ed-108">El recurso **educationSchool** actualmente corresponde a un recurso [administrativeUnit](administrativeunit.md) y comparte el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="826ed-108">The **educationSchool** resource currently corresponds to an [administrativeUnit](administrativeunit.md) resource and shares the same ID.</span></span>  

<span data-ttu-id="826ed-109">Este recurso es un subtipo de [educationOrganization](educationorganization.md).</span><span class="sxs-lookup"><span data-stu-id="826ed-109">This resource is a subtype of [educationOrganization](educationorganization.md).</span></span>




## <a name="methods"></a><span data-ttu-id="826ed-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="826ed-110">Methods</span></span>

| <span data-ttu-id="826ed-111">Método</span><span class="sxs-lookup"><span data-stu-id="826ed-111">Method</span></span>           | <span data-ttu-id="826ed-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="826ed-112">Return Type</span></span>    |<span data-ttu-id="826ed-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="826ed-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="826ed-114">Get</span><span class="sxs-lookup"><span data-stu-id="826ed-114">Get</span></span>](../api/educationschool-get.md) | [<span data-ttu-id="826ed-115">educationSchool</span><span class="sxs-lookup"><span data-stu-id="826ed-115">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="826ed-116">Lea las propiedades y relaciones de un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="826ed-116">Read properties and relationships of an **educationSchool** object.</span></span>|
|[<span data-ttu-id="826ed-117">Agregar clase</span><span class="sxs-lookup"><span data-stu-id="826ed-117">Add class</span></span>](../api/educationschool-post-classes.md) |[<span data-ttu-id="826ed-118">educationClass</span><span class="sxs-lookup"><span data-stu-id="826ed-118">educationClass</span></span>](educationclass.md)| <span data-ttu-id="826ed-119">Agregue un nuevo **educationClass** en el centro educativo publicando en la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="826ed-119">Add a new **educationClass** for the school by posting to the classes navigation property.</span></span>|
|[<span data-ttu-id="826ed-120">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="826ed-120">List classes</span></span>](../api/educationschool-list-classes.md) |<span data-ttu-id="826ed-121">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="826ed-121">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="826ed-122">Obtenga la colección de objetos **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="826ed-122">Get the **educationClass** object collection.</span></span>|
|[<span data-ttu-id="826ed-123">Quitar clase</span><span class="sxs-lookup"><span data-stu-id="826ed-123">Remove class</span></span>](../api/educationschool-delete-classes.md) |[<span data-ttu-id="826ed-124">educationClass</span><span class="sxs-lookup"><span data-stu-id="826ed-124">educationClass</span></span>](educationclass.md)| <span data-ttu-id="826ed-125">Quite un **educationClass** del centro educativo mediante la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="826ed-125">Remove an **educationClass** from the school through the classes navigation property.</span></span>|
|[<span data-ttu-id="826ed-126">Agregar usuario</span><span class="sxs-lookup"><span data-stu-id="826ed-126">Add user</span></span>](../api/educationschool-post-users.md) |[<span data-ttu-id="826ed-127">educationUser</span><span class="sxs-lookup"><span data-stu-id="826ed-127">educationUser</span></span>](educationuser.md)| <span data-ttu-id="826ed-128">Agregue un nuevo **educationUser** en el centro educativo publicando en la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="826ed-128">Add a new **educationUser** for the school by posting to the **users** navigation property.</span></span>|
|[<span data-ttu-id="826ed-129">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="826ed-129">List users</span></span>](../api/educationschool-list-users.md) |<span data-ttu-id="826ed-130">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="826ed-130">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="826ed-131">Obtenga la colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="826ed-131">Get the **educationUser** object collection.</span></span>|
|[<span data-ttu-id="826ed-132">Quitar usuario</span><span class="sxs-lookup"><span data-stu-id="826ed-132">Remove user</span></span>](../api/educationschool-delete-users.md) |[<span data-ttu-id="826ed-133">educationUser</span><span class="sxs-lookup"><span data-stu-id="826ed-133">educationUser</span></span>](educationuser.md)| <span data-ttu-id="826ed-134">Quite un **educationUser** del centro educativo mediante la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="826ed-134">Remove an **educationUser** from the school through the **users** navigation property.</span></span>|
|[<span data-ttu-id="826ed-135">Obtener administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="826ed-135">Get administrativeUnit</span></span>](../api/educationschool-get-administrativeunit.md) |[<span data-ttu-id="826ed-136">administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="826ed-136">administrativeUnit</span></span>](administrativeunit.md)| <span data-ttu-id="826ed-137">Obtenga el directorio simple **administrativeUnit** correspondiente a este objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="826ed-137">Get the **administrativeUnit** that corresponds to this **educationSchool**.</span></span>|
|[<span data-ttu-id="826ed-138">Actualizar</span><span class="sxs-lookup"><span data-stu-id="826ed-138">Update</span></span>](../api/educationschool-update.md) | [<span data-ttu-id="826ed-139">educationSchool</span><span class="sxs-lookup"><span data-stu-id="826ed-139">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="826ed-140">Actualice un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="826ed-140">Update an **educationSchool** object.</span></span> |
|[<span data-ttu-id="826ed-141">Eliminar</span><span class="sxs-lookup"><span data-stu-id="826ed-141">Delete</span></span>](../api/educationschool-delete.md) | <span data-ttu-id="826ed-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="826ed-142">None</span></span> |<span data-ttu-id="826ed-143">Elimine un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="826ed-143">Delete an **educationSchool** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="826ed-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="826ed-144">Properties</span></span>
| <span data-ttu-id="826ed-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="826ed-145">Property</span></span>     | <span data-ttu-id="826ed-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="826ed-146">Type</span></span>   |<span data-ttu-id="826ed-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="826ed-147">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="826ed-148">id</span><span class="sxs-lookup"><span data-stu-id="826ed-148">id</span></span>|<span data-ttu-id="826ed-149">String</span><span class="sxs-lookup"><span data-stu-id="826ed-149">String</span></span>|<span data-ttu-id="826ed-150">GUID de este centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-150">GUID of this school.</span></span>|
|<span data-ttu-id="826ed-151">displayName</span><span class="sxs-lookup"><span data-stu-id="826ed-151">displayName</span></span>| <span data-ttu-id="826ed-152">String</span><span class="sxs-lookup"><span data-stu-id="826ed-152">String</span></span>| <span data-ttu-id="826ed-153">Nombre para mostrar del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-153">Display name of the school.</span></span>| 
|<span data-ttu-id="826ed-154">description</span><span class="sxs-lookup"><span data-stu-id="826ed-154">description</span></span>| <span data-ttu-id="826ed-155">String</span><span class="sxs-lookup"><span data-stu-id="826ed-155">String</span></span> | <span data-ttu-id="826ed-156">Descripción del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-156">Description of the school.</span></span>| 
|<span data-ttu-id="826ed-157">status</span><span class="sxs-lookup"><span data-stu-id="826ed-157">status</span></span>| <span data-ttu-id="826ed-158">string</span><span class="sxs-lookup"><span data-stu-id="826ed-158">string</span></span>| <span data-ttu-id="826ed-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="826ed-159">Read-Only.</span></span> <span data-ttu-id="826ed-160">Los valores posibles son: `inactive`, `active`, `expired` y `deleteable`.</span><span class="sxs-lookup"><span data-stu-id="826ed-160">Possible values are: `inactive`, `active`, `expired`, `deleteable`.</span></span>|
|<span data-ttu-id="826ed-161">externalSource</span><span class="sxs-lookup"><span data-stu-id="826ed-161">externalSource</span></span>| <span data-ttu-id="826ed-162">string</span><span class="sxs-lookup"><span data-stu-id="826ed-162">string</span></span>| <span data-ttu-id="826ed-163">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="826ed-163">Read-Only.</span></span>  <span data-ttu-id="826ed-164">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="826ed-164">Possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="826ed-165">principalEmail</span><span class="sxs-lookup"><span data-stu-id="826ed-165">principalEmail</span></span>| <span data-ttu-id="826ed-166">String</span><span class="sxs-lookup"><span data-stu-id="826ed-166">String</span></span>| <span data-ttu-id="826ed-167">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="826ed-167">Email address of the principal.</span></span>|
|<span data-ttu-id="826ed-168">principalName</span><span class="sxs-lookup"><span data-stu-id="826ed-168">principalName</span></span>| <span data-ttu-id="826ed-169">String</span><span class="sxs-lookup"><span data-stu-id="826ed-169">String</span></span> | <span data-ttu-id="826ed-170">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="826ed-170">Name of the principal.</span></span>|
|<span data-ttu-id="826ed-171">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="826ed-171">externalPrincipalId</span></span>| <span data-ttu-id="826ed-172">String</span><span class="sxs-lookup"><span data-stu-id="826ed-172">String</span></span> | <span data-ttu-id="826ed-173">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="826ed-173">ID of principal in syncing system.</span></span> |
|<span data-ttu-id="826ed-174">highestGrade</span><span class="sxs-lookup"><span data-stu-id="826ed-174">highestGrade</span></span>|<span data-ttu-id="826ed-175">String</span><span class="sxs-lookup"><span data-stu-id="826ed-175">String</span></span>| <span data-ttu-id="826ed-176">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="826ed-176">Highest grade taught.</span></span> |
|<span data-ttu-id="826ed-177">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="826ed-177">lowestGrade</span></span>|<span data-ttu-id="826ed-178">String</span><span class="sxs-lookup"><span data-stu-id="826ed-178">String</span></span>| <span data-ttu-id="826ed-179">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="826ed-179">Lowest grade taught.</span></span> |
|<span data-ttu-id="826ed-180">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="826ed-180">schoolNumber</span></span>|<span data-ttu-id="826ed-181">String</span><span class="sxs-lookup"><span data-stu-id="826ed-181">String</span></span>| <span data-ttu-id="826ed-182">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="826ed-182">School Number.</span></span>|
|<span data-ttu-id="826ed-183">externalId</span><span class="sxs-lookup"><span data-stu-id="826ed-183">externalId</span></span>|<span data-ttu-id="826ed-184">String</span><span class="sxs-lookup"><span data-stu-id="826ed-184">String</span></span>| <span data-ttu-id="826ed-185">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="826ed-185">ID of school in syncing system.</span></span> |
|<span data-ttu-id="826ed-186">phone</span><span class="sxs-lookup"><span data-stu-id="826ed-186">phone</span></span>|<span data-ttu-id="826ed-187">String</span><span class="sxs-lookup"><span data-stu-id="826ed-187">String</span></span>| <span data-ttu-id="826ed-188">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-188">Phone number of school.</span></span> |
|<span data-ttu-id="826ed-189">fax</span><span class="sxs-lookup"><span data-stu-id="826ed-189">fax</span></span>|<span data-ttu-id="826ed-190">String</span><span class="sxs-lookup"><span data-stu-id="826ed-190">String</span></span>| <span data-ttu-id="826ed-191">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-191">Fax number of school.</span></span> |
|<span data-ttu-id="826ed-192">address</span><span class="sxs-lookup"><span data-stu-id="826ed-192">address</span></span>|[<span data-ttu-id="826ed-193">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="826ed-193">physicalAddress</span></span>](physicaladdress.md)| <span data-ttu-id="826ed-194">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-194">Address of the school.</span></span>|
|<span data-ttu-id="826ed-195">createdBy</span><span class="sxs-lookup"><span data-stu-id="826ed-195">createdBy</span></span>|[<span data-ttu-id="826ed-196">identitySet</span><span class="sxs-lookup"><span data-stu-id="826ed-196">identitySet</span></span>](identityset.md)|<span data-ttu-id="826ed-197">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-197">Entity who created the school.</span></span>|


## <a name="relationships"></a><span data-ttu-id="826ed-198">Relaciones</span><span class="sxs-lookup"><span data-stu-id="826ed-198">Relationships</span></span>
| <span data-ttu-id="826ed-199">Relación</span><span class="sxs-lookup"><span data-stu-id="826ed-199">Relationship</span></span> | <span data-ttu-id="826ed-200">Tipo</span><span class="sxs-lookup"><span data-stu-id="826ed-200">Type</span></span>   |<span data-ttu-id="826ed-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="826ed-201">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="826ed-202">classes</span><span class="sxs-lookup"><span data-stu-id="826ed-202">classes</span></span>|<span data-ttu-id="826ed-203">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="826ed-203">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="826ed-204">Clases impartidas en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-204">Classes taught at the school.</span></span> <span data-ttu-id="826ed-205">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="826ed-205">Nullable.</span></span>|
|<span data-ttu-id="826ed-206">users</span><span class="sxs-lookup"><span data-stu-id="826ed-206">users</span></span>|<span data-ttu-id="826ed-207">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="826ed-207">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="826ed-208">Usuarios del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="826ed-208">Users in the school.</span></span> <span data-ttu-id="826ed-209">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="826ed-209">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="826ed-210">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="826ed-210">JSON representation</span></span>

<span data-ttu-id="826ed-211">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="826ed-211">The following is a JSON representation of the resource.</span></span>

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
