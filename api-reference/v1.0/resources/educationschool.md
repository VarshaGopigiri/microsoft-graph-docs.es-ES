---
title: Tipo de recurso educationSchool
description: 'Un recurso que representa una escuela y que se usa para administrar las clases, los profesores y los alumnos de la escuela representada.  '
ms.openlocfilehash: 8a87b3a0ceebf9a3dd66978da1bdde2d677ef63e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032312"
---
# <a name="educationschool-resource-type"></a><span data-ttu-id="e690e-103">Tipo de recurso educationSchool</span><span class="sxs-lookup"><span data-stu-id="e690e-103">educationSchool resource type</span></span>

<span data-ttu-id="e690e-104">Un recurso que representa una escuela y que se usa para administrar las clases, los profesores y los alumnos de la escuela representada.</span><span class="sxs-lookup"><span data-stu-id="e690e-104">A resource representing a school and used to manage the classes, teachers, and students of the represented school.</span></span>  


## <a name="methods"></a><span data-ttu-id="e690e-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="e690e-105">Methods</span></span>

| <span data-ttu-id="e690e-106">Método</span><span class="sxs-lookup"><span data-stu-id="e690e-106">Method</span></span>           | <span data-ttu-id="e690e-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e690e-107">Return Type</span></span>    |<span data-ttu-id="e690e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e690e-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e690e-109">Get</span><span class="sxs-lookup"><span data-stu-id="e690e-109">Get</span></span>](../api/educationschool-get.md) | [<span data-ttu-id="e690e-110">educationSchool</span><span class="sxs-lookup"><span data-stu-id="e690e-110">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="e690e-111">Lea las propiedades y relaciones de un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="e690e-111">Read properties and relationships of an **educationSchool** object.</span></span>|
|[<span data-ttu-id="e690e-112">Agregar clase</span><span class="sxs-lookup"><span data-stu-id="e690e-112">Add class</span></span>](../api/educationschool-post-classes.md) |[<span data-ttu-id="e690e-113">educationClass</span><span class="sxs-lookup"><span data-stu-id="e690e-113">educationClass</span></span>](educationclass.md)| <span data-ttu-id="e690e-114">Agregue un nuevo **educationClass** en el centro educativo publicando en la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="e690e-114">Add a new **educationClass** for the school by posting to the classes navigation property.</span></span>|
|[<span data-ttu-id="e690e-115">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="e690e-115">List classes</span></span>](../api/educationschool-list-classes.md) |<span data-ttu-id="e690e-116">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="e690e-116">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="e690e-117">Obtenga la colección de objetos **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="e690e-117">Get the **educationClass** object collection.</span></span>|
|[<span data-ttu-id="e690e-118">Quitar clase</span><span class="sxs-lookup"><span data-stu-id="e690e-118">Remove class</span></span>](../api/educationschool-delete-classes.md) |[<span data-ttu-id="e690e-119">educationClass</span><span class="sxs-lookup"><span data-stu-id="e690e-119">educationClass</span></span>](educationclass.md)| <span data-ttu-id="e690e-120">Quite un **educationClass** del centro educativo mediante la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="e690e-120">Remove an **educationClass** from the school through the classes navigation property.</span></span>|
|[<span data-ttu-id="e690e-121">Agregar usuario</span><span class="sxs-lookup"><span data-stu-id="e690e-121">Add user</span></span>](../api/educationschool-post-users.md) |[<span data-ttu-id="e690e-122">educationUser</span><span class="sxs-lookup"><span data-stu-id="e690e-122">educationUser</span></span>](educationuser.md)| <span data-ttu-id="e690e-123">Agregue un nuevo **educationUser** en el centro educativo publicando en la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="e690e-123">Add a new **educationUser** for the school by posting to the **users** navigation property.</span></span>|
|[<span data-ttu-id="e690e-124">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="e690e-124">List users</span></span>](../api/educationschool-list-users.md) |<span data-ttu-id="e690e-125">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="e690e-125">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="e690e-126">Obtenga la colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="e690e-126">Get the **educationUser** object collection.</span></span>|
|[<span data-ttu-id="e690e-127">Quitar usuario</span><span class="sxs-lookup"><span data-stu-id="e690e-127">Remove user</span></span>](../api/educationschool-delete-users.md) |[<span data-ttu-id="e690e-128">educationUser</span><span class="sxs-lookup"><span data-stu-id="e690e-128">educationUser</span></span>](educationuser.md)| <span data-ttu-id="e690e-129">Quite un elemento **educationUser** del centro educativo mediante la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="e690e-129">Remove an **educationUser** from the school through the **users** navigation property.</span></span>|
|[<span data-ttu-id="e690e-130">Actualizar</span><span class="sxs-lookup"><span data-stu-id="e690e-130">Update</span></span>](../api/educationschool-update.md) | [<span data-ttu-id="e690e-131">educationSchool</span><span class="sxs-lookup"><span data-stu-id="e690e-131">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="e690e-132">Actualice un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="e690e-132">Update an **educationSchool** object.</span></span> |
|[<span data-ttu-id="e690e-133">Eliminar</span><span class="sxs-lookup"><span data-stu-id="e690e-133">Delete</span></span>](../api/educationschool-delete.md) | <span data-ttu-id="e690e-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e690e-134">None</span></span> |<span data-ttu-id="e690e-135">Elimine un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="e690e-135">Delete an **educationSchool** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="e690e-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e690e-136">Properties</span></span>
| <span data-ttu-id="e690e-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e690e-137">Property</span></span>     | <span data-ttu-id="e690e-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="e690e-138">Type</span></span>   |<span data-ttu-id="e690e-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="e690e-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e690e-140">id</span><span class="sxs-lookup"><span data-stu-id="e690e-140">id</span></span>|<span data-ttu-id="e690e-141">String</span><span class="sxs-lookup"><span data-stu-id="e690e-141">String</span></span>|<span data-ttu-id="e690e-142">GUID de este centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-142">GUID of this school.</span></span>|
|<span data-ttu-id="e690e-143">displayName</span><span class="sxs-lookup"><span data-stu-id="e690e-143">displayName</span></span>| <span data-ttu-id="e690e-144">String</span><span class="sxs-lookup"><span data-stu-id="e690e-144">String</span></span>| <span data-ttu-id="e690e-145">Nombre para mostrar del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-145">Display name of the school.</span></span>| 
|<span data-ttu-id="e690e-146">description</span><span class="sxs-lookup"><span data-stu-id="e690e-146">description</span></span>| <span data-ttu-id="e690e-147">String</span><span class="sxs-lookup"><span data-stu-id="e690e-147">String</span></span> | <span data-ttu-id="e690e-148">Descripción del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-148">Description of the school.</span></span>| 
|<span data-ttu-id="e690e-149">status</span><span class="sxs-lookup"><span data-stu-id="e690e-149">status</span></span>| <span data-ttu-id="e690e-150">string</span><span class="sxs-lookup"><span data-stu-id="e690e-150">string</span></span>| <span data-ttu-id="e690e-151">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e690e-151">Read-Only.</span></span> <span data-ttu-id="e690e-152">Los valores posibles son: `inactive`, `active`, `expired`, `deleteable`.</span><span class="sxs-lookup"><span data-stu-id="e690e-152">The possible values are: `inactive`, `active`, `expired`, `deleteable`.</span></span>|
|<span data-ttu-id="e690e-153">externalSource</span><span class="sxs-lookup"><span data-stu-id="e690e-153">externalSource</span></span>| <span data-ttu-id="e690e-154">educationExternalSource</span><span class="sxs-lookup"><span data-stu-id="e690e-154">educationExternalSource</span></span>| <span data-ttu-id="e690e-155">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e690e-155">Read-Only.</span></span>  <span data-ttu-id="e690e-156">Los valores posibles son: `sis`, `manual`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="e690e-156">The possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="e690e-157">principalEmail</span><span class="sxs-lookup"><span data-stu-id="e690e-157">principalEmail</span></span>| <span data-ttu-id="e690e-158">String</span><span class="sxs-lookup"><span data-stu-id="e690e-158">String</span></span>| <span data-ttu-id="e690e-159">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="e690e-159">Email address of the principal.</span></span>|
|<span data-ttu-id="e690e-160">principalName</span><span class="sxs-lookup"><span data-stu-id="e690e-160">principalName</span></span>| <span data-ttu-id="e690e-161">String</span><span class="sxs-lookup"><span data-stu-id="e690e-161">String</span></span> | <span data-ttu-id="e690e-162">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="e690e-162">Name of the principal.</span></span>|
|<span data-ttu-id="e690e-163">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="e690e-163">externalPrincipalId</span></span>| <span data-ttu-id="e690e-164">String</span><span class="sxs-lookup"><span data-stu-id="e690e-164">String</span></span> | <span data-ttu-id="e690e-165">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="e690e-165">ID of principal in syncing system.</span></span> |
|<span data-ttu-id="e690e-166">highestGrade</span><span class="sxs-lookup"><span data-stu-id="e690e-166">highestGrade</span></span>|<span data-ttu-id="e690e-167">String</span><span class="sxs-lookup"><span data-stu-id="e690e-167">String</span></span>| <span data-ttu-id="e690e-168">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="e690e-168">Highest grade taught.</span></span> |
|<span data-ttu-id="e690e-169">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="e690e-169">lowestGrade</span></span>|<span data-ttu-id="e690e-170">String</span><span class="sxs-lookup"><span data-stu-id="e690e-170">String</span></span>| <span data-ttu-id="e690e-171">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="e690e-171">Lowest grade taught.</span></span> |
|<span data-ttu-id="e690e-172">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="e690e-172">schoolNumber</span></span>|<span data-ttu-id="e690e-173">String</span><span class="sxs-lookup"><span data-stu-id="e690e-173">String</span></span>| <span data-ttu-id="e690e-174">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="e690e-174">School Number.</span></span>|
|<span data-ttu-id="e690e-175">externalId</span><span class="sxs-lookup"><span data-stu-id="e690e-175">externalId</span></span>|<span data-ttu-id="e690e-176">String</span><span class="sxs-lookup"><span data-stu-id="e690e-176">String</span></span>| <span data-ttu-id="e690e-177">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="e690e-177">ID of school in syncing system.</span></span> |
|<span data-ttu-id="e690e-178">phone</span><span class="sxs-lookup"><span data-stu-id="e690e-178">phone</span></span>|<span data-ttu-id="e690e-179">String</span><span class="sxs-lookup"><span data-stu-id="e690e-179">String</span></span>| <span data-ttu-id="e690e-180">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-180">Phone number of school.</span></span> |
|<span data-ttu-id="e690e-181">fax</span><span class="sxs-lookup"><span data-stu-id="e690e-181">fax</span></span>|<span data-ttu-id="e690e-182">String</span><span class="sxs-lookup"><span data-stu-id="e690e-182">String</span></span>| <span data-ttu-id="e690e-183">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-183">Fax number of school.</span></span> |
|<span data-ttu-id="e690e-184">address</span><span class="sxs-lookup"><span data-stu-id="e690e-184">address</span></span>|[<span data-ttu-id="e690e-185">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="e690e-185">physicalAddress</span></span>](physicaladdress.md)| <span data-ttu-id="e690e-186">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-186">Address of the school.</span></span>|
|<span data-ttu-id="e690e-187">createdBy</span><span class="sxs-lookup"><span data-stu-id="e690e-187">createdBy</span></span>|[<span data-ttu-id="e690e-188">identitySet</span><span class="sxs-lookup"><span data-stu-id="e690e-188">identitySet</span></span>](identityset.md)|<span data-ttu-id="e690e-189">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-189">Entity who created the school.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e690e-190">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e690e-190">Relationships</span></span>
| <span data-ttu-id="e690e-191">Relación</span><span class="sxs-lookup"><span data-stu-id="e690e-191">Relationship</span></span> | <span data-ttu-id="e690e-192">Tipo</span><span class="sxs-lookup"><span data-stu-id="e690e-192">Type</span></span>   |<span data-ttu-id="e690e-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="e690e-193">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e690e-194">classes</span><span class="sxs-lookup"><span data-stu-id="e690e-194">classes</span></span>|<span data-ttu-id="e690e-195">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="e690e-195">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="e690e-196">Clases impartidas en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-196">Classes taught at the school.</span></span> <span data-ttu-id="e690e-197">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e690e-197">Nullable.</span></span>|
|<span data-ttu-id="e690e-198">users</span><span class="sxs-lookup"><span data-stu-id="e690e-198">users</span></span>|<span data-ttu-id="e690e-199">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="e690e-199">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="e690e-200">Usuarios del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="e690e-200">Users in the school.</span></span> <span data-ttu-id="e690e-201">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e690e-201">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e690e-202">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e690e-202">JSON representation</span></span>

<span data-ttu-id="e690e-203">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e690e-203">The following is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.educationOrganization",
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
