---
title: Tipo de recurso educationClass
description: 'Representa una clase en un centro educativo. El recurso **educationClass** corresponde al grupo de Office 365 y comparte el mismo identificador. Los alumnos son miembros normales de la clase y los profesores son propietarios y tienen los derechos adecuados. Para que las experiencias de Office funcionen correctamente, los profesores deben ser miembros de las colecciones de profesores y de miembros.  '
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: c5b145d12dd99293eef9c338ff840d5781c5ef3f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933991"
---
# <a name="educationclass-resource-type"></a><span data-ttu-id="bbccb-106">Tipo de recurso educationClass</span><span class="sxs-lookup"><span data-stu-id="bbccb-106">educationClass resource type</span></span>

<span data-ttu-id="bbccb-107">Representa una clase en un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="bbccb-107">Represents a class within a school.</span></span> <span data-ttu-id="bbccb-108">El recurso **educationClass** corresponde al grupo de Office 365 y comparte el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="bbccb-108">The **educationClass** resource corresponds to the Office 365 group and shares the same ID.</span></span> <span data-ttu-id="bbccb-109">Los alumnos son miembros normales de la clase y los profesores son propietarios y tienen los derechos adecuados.</span><span class="sxs-lookup"><span data-stu-id="bbccb-109">Students are regular members of the class, and teachers are owners and have appropriate rights.</span></span> <span data-ttu-id="bbccb-110">Para que las experiencias de Office funcionen correctamente, los profesores deben ser miembros de las colecciones de profesores y de miembros.</span><span class="sxs-lookup"><span data-stu-id="bbccb-110">For Office experiences to work correctly, teachers must be members of both the teachers and members collections.</span></span>  


## <a name="methods"></a><span data-ttu-id="bbccb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bbccb-111">Methods</span></span>

| <span data-ttu-id="bbccb-112">Método</span><span class="sxs-lookup"><span data-stu-id="bbccb-112">Method</span></span>           | <span data-ttu-id="bbccb-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbccb-113">Return Type</span></span>    |<span data-ttu-id="bbccb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbccb-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bbccb-115">Obtener educationClass</span><span class="sxs-lookup"><span data-stu-id="bbccb-115">Get educationClass</span></span>](../api/educationclass-get.md) | [<span data-ttu-id="bbccb-116">educationClass</span><span class="sxs-lookup"><span data-stu-id="bbccb-116">educationClass</span></span>](educationclass.md) |<span data-ttu-id="bbccb-117">Lea las propiedades y relaciones de un objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="bbccb-117">Read properties and relationships of an **educationClass** object.</span></span>|
|[<span data-ttu-id="bbccb-118">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="bbccb-118">Add member</span></span>](../api/educationclass-post-members.md) |[<span data-ttu-id="bbccb-119">educationUser</span><span class="sxs-lookup"><span data-stu-id="bbccb-119">educationUser</span></span>](educationuser.md)| <span data-ttu-id="bbccb-120">Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="bbccb-120">Add a new **educationUser** for the class by posting to the members navigation property.</span></span>|
|[<span data-ttu-id="bbccb-121">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="bbccb-121">List members</span></span>](../api/educationclass-list-members.md) |<span data-ttu-id="bbccb-122">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="bbccb-122">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="bbccb-123">Obtenga una colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="bbccb-123">Get an **educationUser** object collection.</span></span>|
|[<span data-ttu-id="bbccb-124">Quitar alumnos</span><span class="sxs-lookup"><span data-stu-id="bbccb-124">Remove student</span></span>](../api/educationclass-delete-members.md) |[<span data-ttu-id="bbccb-125">educationUser</span><span class="sxs-lookup"><span data-stu-id="bbccb-125">educationUser</span></span>](educationuser.md)| <span data-ttu-id="bbccb-126">Quite un **educationUser** de la clase mediante la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="bbccb-126">Remove an **educationUser** from the class through the members navigation property.</span></span>|
|[<span data-ttu-id="bbccb-127">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="bbccb-127">List schools</span></span>](../api/educationclass-list-schools.md) |<span data-ttu-id="bbccb-128">Colección [educationSchool](educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="bbccb-128">[educationSchool](educationschool.md) collection</span></span>| <span data-ttu-id="bbccb-129">Obtenga una colección de objetos **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="bbccb-129">Get an **educationSchool** object collection.</span></span>|
|[<span data-ttu-id="bbccb-130">Agregar profesor</span><span class="sxs-lookup"><span data-stu-id="bbccb-130">Add teacher</span></span>](../api/educationclass-post-teachers.md) |[<span data-ttu-id="bbccb-131">educationUser</span><span class="sxs-lookup"><span data-stu-id="bbccb-131">educationUser</span></span>](educationuser.md)| <span data-ttu-id="bbccb-132">Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de profesores.</span><span class="sxs-lookup"><span data-stu-id="bbccb-132">Add a new **educationUser** for the class by posting to the teachers navigation property.</span></span>|
|[<span data-ttu-id="bbccb-133">Enumerar profesores</span><span class="sxs-lookup"><span data-stu-id="bbccb-133">List teachers</span></span>](../api/educationclass-list-teachers.md) |<span data-ttu-id="bbccb-134">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="bbccb-134">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="bbccb-135">Obtenga una lista de los profesores de la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-135">Get a list of teachers for the class.</span></span>|
|[<span data-ttu-id="bbccb-136">Quitar profesor</span><span class="sxs-lookup"><span data-stu-id="bbccb-136">Remove teacher</span></span>](../api/educationclass-delete-teachers.md) |[<span data-ttu-id="bbccb-137">educationUser</span><span class="sxs-lookup"><span data-stu-id="bbccb-137">educationUser</span></span>](educationuser.md)| <span data-ttu-id="bbccb-138">Quite un **educationUser** de la clase mediante la propiedad de navegación de profesores.</span><span class="sxs-lookup"><span data-stu-id="bbccb-138">Remove an **educationUser** from the class through the teachers navigation property.</span></span>|
|[<span data-ttu-id="bbccb-139">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="bbccb-139">Get group</span></span>](../api/educationclass-get-group.md) |[<span data-ttu-id="bbccb-140">group</span><span class="sxs-lookup"><span data-stu-id="bbccb-140">group</span></span>](group.md)| <span data-ttu-id="bbccb-141">Obtenga el **group** de Office 365 correspondiente a este objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="bbccb-141">Get the Office 365 **group** that corresponds to this **educationClass**.</span></span>|
|[<span data-ttu-id="bbccb-142">Actualizar</span><span class="sxs-lookup"><span data-stu-id="bbccb-142">Update</span></span>](../api/educationclass-update.md) | [<span data-ttu-id="bbccb-143">educationClass</span><span class="sxs-lookup"><span data-stu-id="bbccb-143">educationClass</span></span>](educationclass.md)    |<span data-ttu-id="bbccb-144">Actualice un objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="bbccb-144">Update **educationClass** object.</span></span> |
|[<span data-ttu-id="bbccb-145">Eliminar</span><span class="sxs-lookup"><span data-stu-id="bbccb-145">Delete</span></span>](../api/educationclass-delete.md) | <span data-ttu-id="bbccb-146">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bbccb-146">None</span></span> |<span data-ttu-id="bbccb-147">Elimine un objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="bbccb-147">Delete **educationClass** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="bbccb-148">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbccb-148">Properties</span></span>
| <span data-ttu-id="bbccb-149">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bbccb-149">Property</span></span>     | <span data-ttu-id="bbccb-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbccb-150">Type</span></span>   |<span data-ttu-id="bbccb-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbccb-151">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bbccb-152">id</span><span class="sxs-lookup"><span data-stu-id="bbccb-152">id</span></span>| <span data-ttu-id="bbccb-153">String</span><span class="sxs-lookup"><span data-stu-id="bbccb-153">String</span></span>| <span data-ttu-id="bbccb-154">Identificador único de la clase</span><span class="sxs-lookup"><span data-stu-id="bbccb-154">Unique identifier for the class.</span></span>|
|<span data-ttu-id="bbccb-155">description</span><span class="sxs-lookup"><span data-stu-id="bbccb-155">description</span></span>|<span data-ttu-id="bbccb-156">String</span><span class="sxs-lookup"><span data-stu-id="bbccb-156">String</span></span>| <span data-ttu-id="bbccb-157">Descripción de la clase</span><span class="sxs-lookup"><span data-stu-id="bbccb-157">Description of the class.</span></span>|
|<span data-ttu-id="bbccb-158">displayName</span><span class="sxs-lookup"><span data-stu-id="bbccb-158">displayName</span></span>|<span data-ttu-id="bbccb-159">String</span><span class="sxs-lookup"><span data-stu-id="bbccb-159">String</span></span>| <span data-ttu-id="bbccb-160">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-160">Name of the class.</span></span>|
|<span data-ttu-id="bbccb-161">mailNickname</span><span class="sxs-lookup"><span data-stu-id="bbccb-161">mailNickname</span></span>|<span data-ttu-id="bbccb-162">String</span><span class="sxs-lookup"><span data-stu-id="bbccb-162">String</span></span>| <span data-ttu-id="bbccb-163">Nombre de correo para enviar correo electrónico a todos los miembros, si esta opción está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bbccb-163">Mail name for sending email to all members, if this is enabled.</span></span> |
|<span data-ttu-id="bbccb-164">createdBy</span><span class="sxs-lookup"><span data-stu-id="bbccb-164">createdBy</span></span>|[<span data-ttu-id="bbccb-165">identitySet</span><span class="sxs-lookup"><span data-stu-id="bbccb-165">identitySet</span></span>](identityset.md)| <span data-ttu-id="bbccb-166">Entidad que ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-166">Entity who created the class</span></span> |
|<span data-ttu-id="bbccb-167">classCode</span><span class="sxs-lookup"><span data-stu-id="bbccb-167">classCode</span></span>|<span data-ttu-id="bbccb-168">String</span><span class="sxs-lookup"><span data-stu-id="bbccb-168">String</span></span>| <span data-ttu-id="bbccb-169">Código de clase que usa el centro educativo para identificar la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-169">Class code used by the school to identify the class.</span></span>|
|<span data-ttu-id="bbccb-170">externalId</span><span class="sxs-lookup"><span data-stu-id="bbccb-170">externalId</span></span>|<span data-ttu-id="bbccb-171">String</span><span class="sxs-lookup"><span data-stu-id="bbccb-171">String</span></span>| <span data-ttu-id="bbccb-172">Identificador de la clase en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="bbccb-172">ID of the class from the syncing system.</span></span> |
|<span data-ttu-id="bbccb-173">externalName</span><span class="sxs-lookup"><span data-stu-id="bbccb-173">externalName</span></span>|<span data-ttu-id="bbccb-174">String</span><span class="sxs-lookup"><span data-stu-id="bbccb-174">String</span></span>|<span data-ttu-id="bbccb-175">Nombre de la clase en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="bbccb-175">Name of the class in the syncing system.</span></span>|
|<span data-ttu-id="bbccb-176">externalSource</span><span class="sxs-lookup"><span data-stu-id="bbccb-176">externalSource</span></span>|<span data-ttu-id="bbccb-177">educationExternalSource</span><span class="sxs-lookup"><span data-stu-id="bbccb-177">educationExternalSource</span></span>| <span data-ttu-id="bbccb-178">Forma en que se ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-178">How this class was created.</span></span> <span data-ttu-id="bbccb-179">Los valores posibles son: `sis`, `manual`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="bbccb-179">The possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="bbccb-180">term</span><span class="sxs-lookup"><span data-stu-id="bbccb-180">term</span></span>|[<span data-ttu-id="bbccb-181">educationTerm</span><span class="sxs-lookup"><span data-stu-id="bbccb-181">educationTerm</span></span>](educationterm.md)|<span data-ttu-id="bbccb-182">Período de la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-182">Term for this class.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bbccb-183">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bbccb-183">Relationships</span></span>
| <span data-ttu-id="bbccb-184">Relación</span><span class="sxs-lookup"><span data-stu-id="bbccb-184">Relationship</span></span> | <span data-ttu-id="bbccb-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbccb-185">Type</span></span>   |<span data-ttu-id="bbccb-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbccb-186">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bbccb-187">members</span><span class="sxs-lookup"><span data-stu-id="bbccb-187">members</span></span>|<span data-ttu-id="bbccb-188">Colección [educationUser](../resources/educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="bbccb-188">[educationUser](../resources/educationuser.md) collection</span></span>| <span data-ttu-id="bbccb-189">Todos los usuarios de la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-189">All users in the class.</span></span> <span data-ttu-id="bbccb-190">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="bbccb-190">Nullable.</span></span>|
|<span data-ttu-id="bbccb-191">schools</span><span class="sxs-lookup"><span data-stu-id="bbccb-191">schools</span></span>|<span data-ttu-id="bbccb-192">Colección [educationSchool](../resources/educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="bbccb-192">[educationSchool](../resources/educationschool.md) collection</span></span>| <span data-ttu-id="bbccb-193">Todos los centros educativos a los que está asociada la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-193">All schools that this class is associated with.</span></span> <span data-ttu-id="bbccb-194">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="bbccb-194">Nullable.</span></span>|
|<span data-ttu-id="bbccb-195">teachers</span><span class="sxs-lookup"><span data-stu-id="bbccb-195">teachers</span></span>|<span data-ttu-id="bbccb-196">Colección [educationUser](../resources/educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="bbccb-196">[educationUser](../resources/educationuser.md) collection</span></span>|  <span data-ttu-id="bbccb-197">Todos los profesores de la clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-197">All teachers in the class.</span></span> <span data-ttu-id="bbccb-198">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="bbccb-198">Nullable.</span></span>|
|<span data-ttu-id="bbccb-199">grupo</span><span class="sxs-lookup"><span data-stu-id="bbccb-199">group</span></span>|[<span data-ttu-id="bbccb-200">grupo</span><span class="sxs-lookup"><span data-stu-id="bbccb-200">group</span></span>](../resources/group.md)| <span data-ttu-id="bbccb-201">El grupo de Active directory correspondiente a esta clase.</span><span class="sxs-lookup"><span data-stu-id="bbccb-201">The directory group corresponding to this class.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bbccb-202">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bbccb-202">JSON representation</span></span>

<span data-ttu-id="bbccb-203">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bbccb-203">The following is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.educationClass"
}-->

```json
{
  "id": "String",
  "description": "String",
  "classCode": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "displayName": "String",
  "externalId": "String",
  "externalName": "String",
  "externalSource": "string",
  "mailNickname": "String",
  "term": {"@odata.type": "microsoft.graph.educationTerm"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationClass resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
