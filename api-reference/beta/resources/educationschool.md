---
title: Tipo de recurso educationSchool
description: 'Centro educativo. El recurso **educationSchool** actualmente corresponde a un recurso administrativeUnit y comparte el mismo identificador.  '
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 17a5c3ad2f28e802bb6cad3a97d1cb723b3407d6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918248"
---
# <a name="educationschool-resource-type"></a><span data-ttu-id="4b0f5-104">Tipo de recurso educationSchool</span><span class="sxs-lookup"><span data-stu-id="4b0f5-104">educationSchool resource type</span></span>

> <span data-ttu-id="4b0f5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4b0f5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4b0f5-107">Centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-107">A school.</span></span> <span data-ttu-id="4b0f5-108">El recurso **educationSchool** actualmente corresponde a un recurso [administrativeUnit](administrativeunit.md) y comparte el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-108">The **educationSchool** resource currently corresponds to an [administrativeUnit](administrativeunit.md) resource and shares the same ID.</span></span>  

<span data-ttu-id="4b0f5-109">Este recurso es un subtipo de [educationOrganization](educationorganization.md).</span><span class="sxs-lookup"><span data-stu-id="4b0f5-109">This resource is a subtype of [educationOrganization](educationorganization.md).</span></span>




## <a name="methods"></a><span data-ttu-id="4b0f5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b0f5-110">Methods</span></span>

| <span data-ttu-id="4b0f5-111">Método</span><span class="sxs-lookup"><span data-stu-id="4b0f5-111">Method</span></span>           | <span data-ttu-id="4b0f5-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b0f5-112">Return Type</span></span>    |<span data-ttu-id="4b0f5-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b0f5-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4b0f5-114">Get</span><span class="sxs-lookup"><span data-stu-id="4b0f5-114">Get</span></span>](../api/educationschool-get.md) | [<span data-ttu-id="4b0f5-115">educationSchool</span><span class="sxs-lookup"><span data-stu-id="4b0f5-115">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="4b0f5-116">Lea las propiedades y relaciones de un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-116">Read properties and relationships of an **educationSchool** object.</span></span>|
|[<span data-ttu-id="4b0f5-117">Agregar clase</span><span class="sxs-lookup"><span data-stu-id="4b0f5-117">Add class</span></span>](../api/educationschool-post-classes.md) |[<span data-ttu-id="4b0f5-118">educationClass</span><span class="sxs-lookup"><span data-stu-id="4b0f5-118">educationClass</span></span>](educationclass.md)| <span data-ttu-id="4b0f5-119">Agregue un nuevo **educationClass** en el centro educativo publicando en la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-119">Add a new **educationClass** for the school by posting to the classes navigation property.</span></span>|
|[<span data-ttu-id="4b0f5-120">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="4b0f5-120">List classes</span></span>](../api/educationschool-list-classes.md) |<span data-ttu-id="4b0f5-121">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="4b0f5-121">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="4b0f5-122">Obtenga la colección de objetos **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-122">Get the **educationClass** object collection.</span></span>|
|[<span data-ttu-id="4b0f5-123">Quitar clase</span><span class="sxs-lookup"><span data-stu-id="4b0f5-123">Remove class</span></span>](../api/educationschool-delete-classes.md) |[<span data-ttu-id="4b0f5-124">educationClass</span><span class="sxs-lookup"><span data-stu-id="4b0f5-124">educationClass</span></span>](educationclass.md)| <span data-ttu-id="4b0f5-125">Quite un **educationClass** del centro educativo mediante la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-125">Remove an **educationClass** from the school through the classes navigation property.</span></span>|
|[<span data-ttu-id="4b0f5-126">Agregar usuario</span><span class="sxs-lookup"><span data-stu-id="4b0f5-126">Add user</span></span>](../api/educationschool-post-users.md) |[<span data-ttu-id="4b0f5-127">educationUser</span><span class="sxs-lookup"><span data-stu-id="4b0f5-127">educationUser</span></span>](educationuser.md)| <span data-ttu-id="4b0f5-128">Agregue un nuevo **educationUser** en el centro educativo publicando en la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-128">Add a new **educationUser** for the school by posting to the **users** navigation property.</span></span>|
|[<span data-ttu-id="4b0f5-129">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="4b0f5-129">List users</span></span>](../api/educationschool-list-users.md) |<span data-ttu-id="4b0f5-130">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="4b0f5-130">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="4b0f5-131">Obtenga la colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-131">Get the **educationUser** object collection.</span></span>|
|[<span data-ttu-id="4b0f5-132">Quitar usuario</span><span class="sxs-lookup"><span data-stu-id="4b0f5-132">Remove user</span></span>](../api/educationschool-delete-users.md) |[<span data-ttu-id="4b0f5-133">educationUser</span><span class="sxs-lookup"><span data-stu-id="4b0f5-133">educationUser</span></span>](educationuser.md)| <span data-ttu-id="4b0f5-134">Quite un **educationUser** del centro educativo mediante la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-134">Remove an **educationUser** from the school through the **users** navigation property.</span></span>|
|[<span data-ttu-id="4b0f5-135">Obtener administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="4b0f5-135">Get administrativeUnit</span></span>](../api/educationschool-get-administrativeunit.md) |[<span data-ttu-id="4b0f5-136">administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="4b0f5-136">administrativeUnit</span></span>](administrativeunit.md)| <span data-ttu-id="4b0f5-137">Obtenga el directorio simple **administrativeUnit** correspondiente a este objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-137">Get the **administrativeUnit** that corresponds to this **educationSchool**.</span></span>|
|[<span data-ttu-id="4b0f5-138">Actualizar</span><span class="sxs-lookup"><span data-stu-id="4b0f5-138">Update</span></span>](../api/educationschool-update.md) | [<span data-ttu-id="4b0f5-139">educationSchool</span><span class="sxs-lookup"><span data-stu-id="4b0f5-139">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="4b0f5-140">Actualice un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-140">Update an **educationSchool** object.</span></span> |
|[<span data-ttu-id="4b0f5-141">Eliminar</span><span class="sxs-lookup"><span data-stu-id="4b0f5-141">Delete</span></span>](../api/educationschool-delete.md) | <span data-ttu-id="4b0f5-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4b0f5-142">None</span></span> |<span data-ttu-id="4b0f5-143">Elimine un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-143">Delete an **educationSchool** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="4b0f5-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b0f5-144">Properties</span></span>
| <span data-ttu-id="4b0f5-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b0f5-145">Property</span></span>     | <span data-ttu-id="4b0f5-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b0f5-146">Type</span></span>   |<span data-ttu-id="4b0f5-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b0f5-147">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4b0f5-148">id</span><span class="sxs-lookup"><span data-stu-id="4b0f5-148">id</span></span>|<span data-ttu-id="4b0f5-149">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-149">String</span></span>|<span data-ttu-id="4b0f5-150">GUID de este centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-150">GUID of this school.</span></span>|
|<span data-ttu-id="4b0f5-151">displayName</span><span class="sxs-lookup"><span data-stu-id="4b0f5-151">displayName</span></span>| <span data-ttu-id="4b0f5-152">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-152">String</span></span>| <span data-ttu-id="4b0f5-153">Nombre para mostrar del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-153">Display name of the school.</span></span>| 
|<span data-ttu-id="4b0f5-154">description</span><span class="sxs-lookup"><span data-stu-id="4b0f5-154">description</span></span>| <span data-ttu-id="4b0f5-155">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-155">String</span></span> | <span data-ttu-id="4b0f5-156">Descripción del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-156">Description of the school.</span></span>| 
|<span data-ttu-id="4b0f5-157">status</span><span class="sxs-lookup"><span data-stu-id="4b0f5-157">status</span></span>| <span data-ttu-id="4b0f5-158">string</span><span class="sxs-lookup"><span data-stu-id="4b0f5-158">string</span></span>| <span data-ttu-id="4b0f5-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-159">Read-Only.</span></span> <span data-ttu-id="4b0f5-160">Los valores posibles son: `inactive`, `active`, `expired` y `deleteable`.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-160">Possible values are: `inactive`, `active`, `expired`, `deleteable`.</span></span>|
|<span data-ttu-id="4b0f5-161">externalSource</span><span class="sxs-lookup"><span data-stu-id="4b0f5-161">externalSource</span></span>| <span data-ttu-id="4b0f5-162">string</span><span class="sxs-lookup"><span data-stu-id="4b0f5-162">string</span></span>| <span data-ttu-id="4b0f5-163">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-163">Read-Only.</span></span>  <span data-ttu-id="4b0f5-164">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-164">Possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="4b0f5-165">principalEmail</span><span class="sxs-lookup"><span data-stu-id="4b0f5-165">principalEmail</span></span>| <span data-ttu-id="4b0f5-166">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-166">String</span></span>| <span data-ttu-id="4b0f5-167">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-167">Email address of the principal.</span></span>|
|<span data-ttu-id="4b0f5-168">principalName</span><span class="sxs-lookup"><span data-stu-id="4b0f5-168">principalName</span></span>| <span data-ttu-id="4b0f5-169">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-169">String</span></span> | <span data-ttu-id="4b0f5-170">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-170">Name of the principal.</span></span>|
|<span data-ttu-id="4b0f5-171">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="4b0f5-171">externalPrincipalId</span></span>| <span data-ttu-id="4b0f5-172">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-172">String</span></span> | <span data-ttu-id="4b0f5-173">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-173">ID of principal in syncing system.</span></span> |
|<span data-ttu-id="4b0f5-174">highestGrade</span><span class="sxs-lookup"><span data-stu-id="4b0f5-174">highestGrade</span></span>|<span data-ttu-id="4b0f5-175">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-175">String</span></span>| <span data-ttu-id="4b0f5-176">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-176">Highest grade taught.</span></span> |
|<span data-ttu-id="4b0f5-177">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="4b0f5-177">lowestGrade</span></span>|<span data-ttu-id="4b0f5-178">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-178">String</span></span>| <span data-ttu-id="4b0f5-179">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-179">Lowest grade taught.</span></span> |
|<span data-ttu-id="4b0f5-180">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="4b0f5-180">schoolNumber</span></span>|<span data-ttu-id="4b0f5-181">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-181">String</span></span>| <span data-ttu-id="4b0f5-182">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="4b0f5-182">School Number.</span></span>|
|<span data-ttu-id="4b0f5-183">externalId</span><span class="sxs-lookup"><span data-stu-id="4b0f5-183">externalId</span></span>|<span data-ttu-id="4b0f5-184">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-184">String</span></span>| <span data-ttu-id="4b0f5-185">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-185">ID of school in syncing system.</span></span> |
|<span data-ttu-id="4b0f5-186">phone</span><span class="sxs-lookup"><span data-stu-id="4b0f5-186">phone</span></span>|<span data-ttu-id="4b0f5-187">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-187">String</span></span>| <span data-ttu-id="4b0f5-188">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-188">Phone number of school.</span></span> |
|<span data-ttu-id="4b0f5-189">fax</span><span class="sxs-lookup"><span data-stu-id="4b0f5-189">fax</span></span>|<span data-ttu-id="4b0f5-190">String</span><span class="sxs-lookup"><span data-stu-id="4b0f5-190">String</span></span>| <span data-ttu-id="4b0f5-191">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-191">Fax number of school.</span></span> |
|<span data-ttu-id="4b0f5-192">address</span><span class="sxs-lookup"><span data-stu-id="4b0f5-192">address</span></span>|[<span data-ttu-id="4b0f5-193">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="4b0f5-193">physicalAddress</span></span>](physicaladdress.md)| <span data-ttu-id="4b0f5-194">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-194">Address of the school.</span></span>|
|<span data-ttu-id="4b0f5-195">createdBy</span><span class="sxs-lookup"><span data-stu-id="4b0f5-195">createdBy</span></span>|[<span data-ttu-id="4b0f5-196">identitySet</span><span class="sxs-lookup"><span data-stu-id="4b0f5-196">identitySet</span></span>](identityset.md)|<span data-ttu-id="4b0f5-197">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-197">Entity who created the school.</span></span>|


## <a name="relationships"></a><span data-ttu-id="4b0f5-198">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4b0f5-198">Relationships</span></span>
| <span data-ttu-id="4b0f5-199">Relación</span><span class="sxs-lookup"><span data-stu-id="4b0f5-199">Relationship</span></span> | <span data-ttu-id="4b0f5-200">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b0f5-200">Type</span></span>   |<span data-ttu-id="4b0f5-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b0f5-201">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4b0f5-202">classes</span><span class="sxs-lookup"><span data-stu-id="4b0f5-202">classes</span></span>|<span data-ttu-id="4b0f5-203">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="4b0f5-203">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="4b0f5-204">Clases impartidas en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-204">Classes taught at the school.</span></span> <span data-ttu-id="4b0f5-205">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-205">Nullable.</span></span>|
|<span data-ttu-id="4b0f5-206">users</span><span class="sxs-lookup"><span data-stu-id="4b0f5-206">users</span></span>|<span data-ttu-id="4b0f5-207">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="4b0f5-207">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="4b0f5-208">Usuarios del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-208">Users in the school.</span></span> <span data-ttu-id="4b0f5-209">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4b0f5-209">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4b0f5-210">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4b0f5-210">JSON representation</span></span>

<span data-ttu-id="4b0f5-211">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4b0f5-211">The following is a JSON representation of the resource.</span></span>

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
