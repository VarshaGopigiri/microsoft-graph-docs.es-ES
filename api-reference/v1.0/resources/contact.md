---
title: Tipo de recurso contact
description: Un contacto es un elemento de Outlook donde puede organizar y guardar información sobre las personas y organizaciones con las que se comunica. Los contactos se contienen en carpetas de contactos.
author: angelgolfer-ms
ms.openlocfilehash: 13eb3b1e3f88c5018031176cffbcc89a038073ed
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334975"
---
# <a name="contact-resource-type"></a><span data-ttu-id="784ba-104">Tipo de recurso contact</span><span class="sxs-lookup"><span data-stu-id="784ba-104">contact resource type</span></span>

<span data-ttu-id="784ba-p102">Un contacto es un elemento de Outlook donde puede organizar y guardar información sobre las personas y organizaciones con las que se comunica. Los contactos se contienen en carpetas de contactos.</span><span class="sxs-lookup"><span data-stu-id="784ba-p102">A contact is an item in Outlook where you can organize and save information about the people and organizations you communicate with. Contacts are contained in contact folders.</span></span>

<span data-ttu-id="784ba-107">Este recurso admite:</span><span class="sxs-lookup"><span data-stu-id="784ba-107">This resource supports:</span></span>

- <span data-ttu-id="784ba-108">Adición de sus propios datos a las propiedades personalizadas como [extensiones](/graph/extensibility-overview).</span><span class="sxs-lookup"><span data-stu-id="784ba-108">Adding your own data to custom properties as [extensions](/graph/extensibility-overview).</span></span>
- <span data-ttu-id="784ba-109">Suscribirse a [las notificaciones de cambios](/graph/webhooks).</span><span class="sxs-lookup"><span data-stu-id="784ba-109">Subscribing to [change notifications](/graph/webhooks).</span></span>
- <span data-ttu-id="784ba-110">que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/contact-delta.md).</span><span class="sxs-lookup"><span data-stu-id="784ba-110">Using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/contact-delta.md) function.</span></span>


## <a name="methods"></a><span data-ttu-id="784ba-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="784ba-111">Methods</span></span>

| <span data-ttu-id="784ba-112">Método</span><span class="sxs-lookup"><span data-stu-id="784ba-112">Method</span></span>       | <span data-ttu-id="784ba-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="784ba-113">Return Type</span></span>  |<span data-ttu-id="784ba-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="784ba-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="784ba-115">Obtener contacto</span><span class="sxs-lookup"><span data-stu-id="784ba-115">Get contact</span></span>](../api/contact-get.md) | [<span data-ttu-id="784ba-116">contact</span><span class="sxs-lookup"><span data-stu-id="784ba-116">contact</span></span>](contact.md) |<span data-ttu-id="784ba-117">Lea las propiedades y las relaciones del objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-117">Read properties and relationships of contact object.</span></span>|
|[<span data-ttu-id="784ba-118">Crear</span><span class="sxs-lookup"><span data-stu-id="784ba-118">Create</span></span>](../api/user-post-contacts.md) | [<span data-ttu-id="784ba-119">contact</span><span class="sxs-lookup"><span data-stu-id="784ba-119">contact</span></span>](contact.md) |<span data-ttu-id="784ba-120">Agregue un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="784ba-120">Add a contact to the root Contacts folder or to the contacts endpoint of another contact folder.</span></span>|
|[<span data-ttu-id="784ba-121">Actualizar</span><span class="sxs-lookup"><span data-stu-id="784ba-121">Update</span></span>](../api/contact-update.md) | [<span data-ttu-id="784ba-122">contact</span><span class="sxs-lookup"><span data-stu-id="784ba-122">contact</span></span>](contact.md) |<span data-ttu-id="784ba-123">Actualice el objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-123">Update contact object.</span></span> |
|[<span data-ttu-id="784ba-124">Eliminar</span><span class="sxs-lookup"><span data-stu-id="784ba-124">Delete</span></span>](../api/contact-delete.md) | <span data-ttu-id="784ba-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="784ba-125">None</span></span> |<span data-ttu-id="784ba-126">Elimine el objeto contact.</span><span class="sxs-lookup"><span data-stu-id="784ba-126">Delete contact object.</span></span> |
|[<span data-ttu-id="784ba-127">delta</span><span class="sxs-lookup"><span data-stu-id="784ba-127">delta</span></span>](../api/contact-delta.md)|<span data-ttu-id="784ba-128">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="784ba-128">[contact](contact.md) collection</span></span>| <span data-ttu-id="784ba-129">Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="784ba-129">Get a set of contacts that have been added, deleted, or updated in a specified folder.</span></span>|
|<span data-ttu-id="784ba-130">**Extensiones abiertas**</span><span class="sxs-lookup"><span data-stu-id="784ba-130">**Open extensions**</span></span>| | |
|[<span data-ttu-id="784ba-131">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="784ba-131">Create open extension</span></span>](../api/opentypeextension-post-opentypeextension.md) |[<span data-ttu-id="784ba-132">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="784ba-132">openTypeExtension</span></span>](opentypeextension.md)| <span data-ttu-id="784ba-133">Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="784ba-133">Create an open extension and add custom properties in a new or existing instance of a resource.</span></span>|
|[<span data-ttu-id="784ba-134">Obtener extensión abierta</span><span class="sxs-lookup"><span data-stu-id="784ba-134">Get open extension</span></span>](../api/opentypeextension-get.md) |<span data-ttu-id="784ba-135">Colección [openTypeExtension](opentypeextension.md)</span><span class="sxs-lookup"><span data-stu-id="784ba-135">[openTypeExtension](opentypeextension.md) collection</span></span>| <span data-ttu-id="784ba-136">Obtenga un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.</span><span class="sxs-lookup"><span data-stu-id="784ba-136">Get an open extension object or objects identified by name or fully qualified name.</span></span>|
|<span data-ttu-id="784ba-137">**Extensiones de esquema**</span><span class="sxs-lookup"><span data-stu-id="784ba-137">**Schema extensions**</span></span>| | |
|[<span data-ttu-id="784ba-138">Agregar valores de extensión de esquema</span><span class="sxs-lookup"><span data-stu-id="784ba-138">Add schema extension values</span></span>](/graph/extensibility-schema-groups) || <span data-ttu-id="784ba-139">Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.</span><span class="sxs-lookup"><span data-stu-id="784ba-139">Create a schema extension definition and then use it to add custom typed data to a resource.</span></span>|
|<span data-ttu-id="784ba-140">**Propiedades extendidas**</span><span class="sxs-lookup"><span data-stu-id="784ba-140">**Extended properties**</span></span>| | |
|[<span data-ttu-id="784ba-141">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="784ba-141">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[<span data-ttu-id="784ba-142">contact</span><span class="sxs-lookup"><span data-stu-id="784ba-142">contact</span></span>](contact.md)  |<span data-ttu-id="784ba-143">Cree una o varias propiedades extendidas de valor único en un contacto nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="784ba-143">Create one or more single-value extended properties in a new or existing contact.</span></span>   |
|[<span data-ttu-id="784ba-144">Obtener contacto con propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="784ba-144">Get contact with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="784ba-145">contact</span><span class="sxs-lookup"><span data-stu-id="784ba-145">contact</span></span>](contact.md) | <span data-ttu-id="784ba-146">Obtenga contactos que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="784ba-146">Get contacts that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="784ba-147">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="784ba-147">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [<span data-ttu-id="784ba-148">contact</span><span class="sxs-lookup"><span data-stu-id="784ba-148">contact</span></span>](contact.md) | <span data-ttu-id="784ba-149">Cree una o varias propiedades extendidas de varios valores en un contacto nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="784ba-149">Create one or more multi-value extended properties in a new or existing contact.</span></span>  |
|[<span data-ttu-id="784ba-150">Obtener contacto con propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="784ba-150">Get contact with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="784ba-151">contact</span><span class="sxs-lookup"><span data-stu-id="784ba-151">contact</span></span>](contact.md) | <span data-ttu-id="784ba-152">Obtenga un contacto que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="784ba-152">Get a contact that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="784ba-153">Propiedades</span><span class="sxs-lookup"><span data-stu-id="784ba-153">Properties</span></span>
| <span data-ttu-id="784ba-154">Propiedad</span><span class="sxs-lookup"><span data-stu-id="784ba-154">Property</span></span>     | <span data-ttu-id="784ba-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="784ba-155">Type</span></span>   |<span data-ttu-id="784ba-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="784ba-156">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="784ba-157">assistantName</span><span class="sxs-lookup"><span data-stu-id="784ba-157">assistantName</span></span>|<span data-ttu-id="784ba-158">String</span><span class="sxs-lookup"><span data-stu-id="784ba-158">String</span></span>|<span data-ttu-id="784ba-159">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-159">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="784ba-160">birthday</span><span class="sxs-lookup"><span data-stu-id="784ba-160">birthday</span></span>|<span data-ttu-id="784ba-161">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="784ba-161">DateTimeOffset</span></span>|<span data-ttu-id="784ba-p103">El cumpleaños del contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="784ba-p103">The contact's birthday. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="784ba-165">businessAddress</span><span class="sxs-lookup"><span data-stu-id="784ba-165">businessAddress</span></span>|[<span data-ttu-id="784ba-166">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="784ba-166">PhysicalAddress</span></span>](physicaladdress.md)|<span data-ttu-id="784ba-167">La dirección del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-167">The contact's business address.</span></span>|
|<span data-ttu-id="784ba-168">businessHomePage</span><span class="sxs-lookup"><span data-stu-id="784ba-168">businessHomePage</span></span>|<span data-ttu-id="784ba-169">String</span><span class="sxs-lookup"><span data-stu-id="784ba-169">String</span></span>|<span data-ttu-id="784ba-170">La página principal de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-170">The business home page of the contact.</span></span>|
|<span data-ttu-id="784ba-171">businessPhones</span><span class="sxs-lookup"><span data-stu-id="784ba-171">businessPhones</span></span>|<span data-ttu-id="784ba-172">Colección String</span><span class="sxs-lookup"><span data-stu-id="784ba-172">String collection</span></span>|<span data-ttu-id="784ba-173">Los números de teléfono del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-173">The contact's business phone numbers.</span></span>|
|<span data-ttu-id="784ba-174">categories</span><span class="sxs-lookup"><span data-stu-id="784ba-174">categories</span></span>|<span data-ttu-id="784ba-175">Colección String</span><span class="sxs-lookup"><span data-stu-id="784ba-175">String collection</span></span>|<span data-ttu-id="784ba-176">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-176">The categories associated with the contact.</span></span>|
|<span data-ttu-id="784ba-177">changeKey</span><span class="sxs-lookup"><span data-stu-id="784ba-177">changeKey</span></span>|<span data-ttu-id="784ba-178">String</span><span class="sxs-lookup"><span data-stu-id="784ba-178">String</span></span>|<span data-ttu-id="784ba-p104">Identifica la versión del contacto. Cada vez que cambia el contacto, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="784ba-p104">Identifies the version of the contact. Every time the contact is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="784ba-182">children</span><span class="sxs-lookup"><span data-stu-id="784ba-182">children</span></span>|<span data-ttu-id="784ba-183">Colección String</span><span class="sxs-lookup"><span data-stu-id="784ba-183">String collection</span></span>|<span data-ttu-id="784ba-184">Los nombres de los hijos del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-184">The names of the contact's children.</span></span>|
|<span data-ttu-id="784ba-185">companyName</span><span class="sxs-lookup"><span data-stu-id="784ba-185">companyName</span></span>|<span data-ttu-id="784ba-186">String</span><span class="sxs-lookup"><span data-stu-id="784ba-186">String</span></span>|<span data-ttu-id="784ba-187">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-187">The name of the contact's company.</span></span>|
|<span data-ttu-id="784ba-188">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="784ba-188">createdDateTime</span></span>|<span data-ttu-id="784ba-189">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="784ba-189">DateTimeOffset</span></span>|<span data-ttu-id="784ba-p105">La hora en que se ha creado el contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="784ba-p105">The time the contact was created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="784ba-193">departamento</span><span class="sxs-lookup"><span data-stu-id="784ba-193">department</span></span>|<span data-ttu-id="784ba-194">String</span><span class="sxs-lookup"><span data-stu-id="784ba-194">String</span></span>|<span data-ttu-id="784ba-195">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-195">The contact's department.</span></span>|
|<span data-ttu-id="784ba-196">displayName</span><span class="sxs-lookup"><span data-stu-id="784ba-196">displayName</span></span>|<span data-ttu-id="784ba-197">String</span><span class="sxs-lookup"><span data-stu-id="784ba-197">String</span></span>|<span data-ttu-id="784ba-198">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-198">The contact's display name.</span></span> <span data-ttu-id="784ba-199">Puede especificar el nombre para mostrar en una operación de [creación](../api/user-post-contacts.md) o [actualización](../api/contact-update.md) .</span><span class="sxs-lookup"><span data-stu-id="784ba-199">You can specify the display name in a [create](../api/user-post-contacts.md) or [update](../api/contact-update.md) operation.</span></span> <span data-ttu-id="784ba-200">Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado.</span><span class="sxs-lookup"><span data-stu-id="784ba-200">Note that later updates to other properties may cause an automatically generated value to overwrite the displayName value you have specified.</span></span> <span data-ttu-id="784ba-201">Para conservar un valor existente, siempre incluirla como displayName en una operación [de actualización](../api/contact-update.md) .</span><span class="sxs-lookup"><span data-stu-id="784ba-201">To preserve a pre-existing value, always include it as displayName in an [update](../api/contact-update.md) operation.</span></span>|
|<span data-ttu-id="784ba-202">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="784ba-202">emailAddresses</span></span>|<span data-ttu-id="784ba-203">Colección [EmailAddress](emailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="784ba-203">[EmailAddress](emailaddress.md) collection</span></span>|<span data-ttu-id="784ba-204">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-204">The contact's email addresses.</span></span>|
|<span data-ttu-id="784ba-205">fileAs</span><span class="sxs-lookup"><span data-stu-id="784ba-205">fileAs</span></span>|<span data-ttu-id="784ba-206">String</span><span class="sxs-lookup"><span data-stu-id="784ba-206">String</span></span>|<span data-ttu-id="784ba-207">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-207">The name the contact is filed under.</span></span>|
|<span data-ttu-id="784ba-208">generation</span><span class="sxs-lookup"><span data-stu-id="784ba-208">generation</span></span>|<span data-ttu-id="784ba-209">String</span><span class="sxs-lookup"><span data-stu-id="784ba-209">String</span></span>|<span data-ttu-id="784ba-210">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-210">The contact's generation.</span></span>|
|<span data-ttu-id="784ba-211">givenName</span><span class="sxs-lookup"><span data-stu-id="784ba-211">givenName</span></span>|<span data-ttu-id="784ba-212">String</span><span class="sxs-lookup"><span data-stu-id="784ba-212">String</span></span>|<span data-ttu-id="784ba-213">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-213">The contact's given name.</span></span>|
|<span data-ttu-id="784ba-214">homeAddress</span><span class="sxs-lookup"><span data-stu-id="784ba-214">homeAddress</span></span>|[<span data-ttu-id="784ba-215">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="784ba-215">PhysicalAddress</span></span>](physicaladdress.md)|<span data-ttu-id="784ba-216">La dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-216">The contact's home address.</span></span>|
|<span data-ttu-id="784ba-217">homePhones</span><span class="sxs-lookup"><span data-stu-id="784ba-217">homePhones</span></span>|<span data-ttu-id="784ba-218">Colección String</span><span class="sxs-lookup"><span data-stu-id="784ba-218">String collection</span></span>|<span data-ttu-id="784ba-219">Los números de teléfono particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-219">The contact's home phone numbers.</span></span>|
|<span data-ttu-id="784ba-220">id</span><span class="sxs-lookup"><span data-stu-id="784ba-220">id</span></span>|<span data-ttu-id="784ba-221">String</span><span class="sxs-lookup"><span data-stu-id="784ba-221">String</span></span>|<span data-ttu-id="784ba-p107">El identificador único del contacto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="784ba-p107">The contact's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="784ba-224">imAddresses</span><span class="sxs-lookup"><span data-stu-id="784ba-224">imAddresses</span></span>|<span data-ttu-id="784ba-225">Colección String</span><span class="sxs-lookup"><span data-stu-id="784ba-225">String collection</span></span>|<span data-ttu-id="784ba-226">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-226">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="784ba-227">initials</span><span class="sxs-lookup"><span data-stu-id="784ba-227">initials</span></span>|<span data-ttu-id="784ba-228">String</span><span class="sxs-lookup"><span data-stu-id="784ba-228">String</span></span>|<span data-ttu-id="784ba-229">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-229">The contact's initials.</span></span>|
|<span data-ttu-id="784ba-230">jobTitle</span><span class="sxs-lookup"><span data-stu-id="784ba-230">jobTitle</span></span>|<span data-ttu-id="784ba-231">String</span><span class="sxs-lookup"><span data-stu-id="784ba-231">String</span></span>|<span data-ttu-id="784ba-232">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-232">The contact’s job title.</span></span>|
|<span data-ttu-id="784ba-233">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="784ba-233">lastModifiedDateTime</span></span>|<span data-ttu-id="784ba-234">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="784ba-234">DateTimeOffset</span></span>|<span data-ttu-id="784ba-p108">La hora en que se ha modificado el contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="784ba-p108">The time the contact was modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="784ba-238">manager</span><span class="sxs-lookup"><span data-stu-id="784ba-238">manager</span></span>|<span data-ttu-id="784ba-239">String</span><span class="sxs-lookup"><span data-stu-id="784ba-239">String</span></span>|<span data-ttu-id="784ba-240">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-240">The name of the contact's manager.</span></span>
|<span data-ttu-id="784ba-241">middleName</span><span class="sxs-lookup"><span data-stu-id="784ba-241">middleName</span></span>|<span data-ttu-id="784ba-242">String</span><span class="sxs-lookup"><span data-stu-id="784ba-242">String</span></span>|<span data-ttu-id="784ba-243">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-243">The contact's middle name.</span></span>|
|<span data-ttu-id="784ba-244">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="784ba-244">mobilePhone</span></span>|<span data-ttu-id="784ba-245">String</span><span class="sxs-lookup"><span data-stu-id="784ba-245">String</span></span>|<span data-ttu-id="784ba-246">El número de teléfono móvil del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-246">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="784ba-247">nickName</span><span class="sxs-lookup"><span data-stu-id="784ba-247">nickName</span></span>|<span data-ttu-id="784ba-248">String</span><span class="sxs-lookup"><span data-stu-id="784ba-248">String</span></span>|<span data-ttu-id="784ba-249">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-249">The contact's nickname.</span></span>|
|<span data-ttu-id="784ba-250">officeLocation</span><span class="sxs-lookup"><span data-stu-id="784ba-250">officeLocation</span></span>|<span data-ttu-id="784ba-251">String</span><span class="sxs-lookup"><span data-stu-id="784ba-251">String</span></span>|<span data-ttu-id="784ba-252">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-252">The location of the contact's office.</span></span>|
|<span data-ttu-id="784ba-253">otherAddress</span><span class="sxs-lookup"><span data-stu-id="784ba-253">otherAddress</span></span>|[<span data-ttu-id="784ba-254">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="784ba-254">PhysicalAddress</span></span>](physicaladdress.md)|<span data-ttu-id="784ba-255">Otras direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-255">Other addresses for the contact.</span></span>|
|<span data-ttu-id="784ba-256">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="784ba-256">parentFolderId</span></span>|<span data-ttu-id="784ba-257">String</span><span class="sxs-lookup"><span data-stu-id="784ba-257">String</span></span>|<span data-ttu-id="784ba-258">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-258">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="784ba-259">personalNotes</span><span class="sxs-lookup"><span data-stu-id="784ba-259">personalNotes</span></span>|<span data-ttu-id="784ba-260">String</span><span class="sxs-lookup"><span data-stu-id="784ba-260">String</span></span>|<span data-ttu-id="784ba-261">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-261">The user's notes about the contact.</span></span>|
|<span data-ttu-id="784ba-262">profession</span><span class="sxs-lookup"><span data-stu-id="784ba-262">profession</span></span>|<span data-ttu-id="784ba-263">String</span><span class="sxs-lookup"><span data-stu-id="784ba-263">String</span></span>|<span data-ttu-id="784ba-264">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-264">The contact's profession.</span></span>|
|<span data-ttu-id="784ba-265">spouseName</span><span class="sxs-lookup"><span data-stu-id="784ba-265">spouseName</span></span>|<span data-ttu-id="784ba-266">String</span><span class="sxs-lookup"><span data-stu-id="784ba-266">String</span></span>|<span data-ttu-id="784ba-267">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-267">The name of the contact's spouse/partner.</span></span>|
|<span data-ttu-id="784ba-268">surname</span><span class="sxs-lookup"><span data-stu-id="784ba-268">surname</span></span>|<span data-ttu-id="784ba-269">String</span><span class="sxs-lookup"><span data-stu-id="784ba-269">String</span></span>|<span data-ttu-id="784ba-270">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-270">The contact's surname.</span></span>|
|<span data-ttu-id="784ba-271">title</span><span class="sxs-lookup"><span data-stu-id="784ba-271">title</span></span>|<span data-ttu-id="784ba-272">String</span><span class="sxs-lookup"><span data-stu-id="784ba-272">String</span></span>|<span data-ttu-id="784ba-273">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-273">The contact's title.</span></span>|
|<span data-ttu-id="784ba-274">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="784ba-274">yomiCompanyName</span></span>|<span data-ttu-id="784ba-275">String</span><span class="sxs-lookup"><span data-stu-id="784ba-275">String</span></span>|<span data-ttu-id="784ba-276">El nombre fonético japonés de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-276">The phonetic Japanese company name of the contact.</span></span>|
|<span data-ttu-id="784ba-277">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="784ba-277">yomiGivenName</span></span>|<span data-ttu-id="784ba-278">String</span><span class="sxs-lookup"><span data-stu-id="784ba-278">String</span></span>|<span data-ttu-id="784ba-279">El nombre (nombre de pila) fonético japonés del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-279">The phonetic Japanese given name (first name) of the contact.</span></span>|
|<span data-ttu-id="784ba-280">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="784ba-280">yomiSurname</span></span>|<span data-ttu-id="784ba-281">String</span><span class="sxs-lookup"><span data-stu-id="784ba-281">String</span></span>|<span data-ttu-id="784ba-282">El apellido fonético japonés del contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-282">The phonetic Japanese surname (last name)  of the contact.</span></span>|

## <a name="relationships"></a><span data-ttu-id="784ba-283">Relaciones</span><span class="sxs-lookup"><span data-stu-id="784ba-283">Relationships</span></span>
| <span data-ttu-id="784ba-284">Relación</span><span class="sxs-lookup"><span data-stu-id="784ba-284">Relationship</span></span> | <span data-ttu-id="784ba-285">Tipo</span><span class="sxs-lookup"><span data-stu-id="784ba-285">Type</span></span>   |<span data-ttu-id="784ba-286">Descripción</span><span class="sxs-lookup"><span data-stu-id="784ba-286">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="784ba-287">extensions</span><span class="sxs-lookup"><span data-stu-id="784ba-287">extensions</span></span>|<span data-ttu-id="784ba-288">Colección [Extension](extension.md)</span><span class="sxs-lookup"><span data-stu-id="784ba-288">[extension](extension.md) collection</span></span>|<span data-ttu-id="784ba-p109">La colección de extensiones abiertas definidas para el contacto. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="784ba-p109">The collection of open extensions defined for the contact. Read-only. Nullable.</span></span>|
|<span data-ttu-id="784ba-292">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="784ba-292">multiValueExtendedProperties</span></span>|<span data-ttu-id="784ba-293">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="784ba-293">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="784ba-p110">La colección de propiedades extendidas de varios valores definidas para el contacto. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="784ba-p110">The collection of multi-value extended properties defined for the contact. Read-only. Nullable.</span></span>|
|<span data-ttu-id="784ba-297">photo</span><span class="sxs-lookup"><span data-stu-id="784ba-297">photo</span></span>|[<span data-ttu-id="784ba-298">profilePhoto</span><span class="sxs-lookup"><span data-stu-id="784ba-298">profilePhoto</span></span>](profilephoto.md)| <span data-ttu-id="784ba-p111">Imagen de contacto opcional. Puede obtener o establecer una foto para un contacto.</span><span class="sxs-lookup"><span data-stu-id="784ba-p111">Optional contact picture. You can get or set a photo for a contact.</span></span>|
|<span data-ttu-id="784ba-301">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="784ba-301">singleValueExtendedProperties</span></span>|<span data-ttu-id="784ba-302">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="784ba-302">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="784ba-p112">La colección de propiedades extendidas de valor único definidas para el contacto. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="784ba-p112">The collection of single-value extended properties defined for the contact. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="784ba-306">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="784ba-306">JSON representation</span></span>

<span data-ttu-id="784ba-307">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="784ba-307">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.outlookItem",
  "openType": true,
  "optionalProperties": [
    "extensions",
    "multiValueExtendedProperties",
    "photo",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.contact",
  "@odata.annotations": [
    {
      "property": "extensions",
      "capabilities": {
        "changeTracking": false,
        "searchable": false
      }
    },
    {
      "property": "photo",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "assistantName": "string",
  "birthday": "String (timestamp)",
  "businessAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "businessHomePage": "string",
  "businessPhones": ["string"],
  "categories": ["string"],
  "changeKey": "string",
  "children": ["string"],
  "companyName": "string",
  "createdDateTime": "String (timestamp)",
  "department": "string",
  "displayName": "string",
  "emailAddresses": [{"@odata.type": "microsoft.graph.emailAddress"}],
  "fileAs": "string",
  "generation": "string",
  "givenName": "string",
  "homeAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "homePhones": ["string"],
  "id": "string (identifier)",
  "imAddresses": ["string"],
  "initials": "string",
  "jobTitle": "string",
  "lastModifiedDateTime": "String (timestamp)",
  "manager": "string",
  "middleName": "string",
  "mobilePhone": "string",
  "nickName": "string",
  "officeLocation": "string",
  "otherAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "parentFolderId": "string",
  "personalNotes": "string",
  "profession": "string",
  "spouseName": "string",
  "surname": "string",
  "title": "string",
  "yomiCompanyName": "string",
  "yomiGivenName": "string",
  "yomiSurname": "string",

  "photo": { "@odata.type": "microsoft.graph.profilePhoto" }
}

```

## <a name="see-also"></a><span data-ttu-id="784ba-308">Consulte también</span><span class="sxs-lookup"><span data-stu-id="784ba-308">See also</span></span>

- [<span data-ttu-id="784ba-309">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="784ba-309">Use delta query to track changes in Microsoft Graph data</span></span>](/graph/delta-query-overview)
- [<span data-ttu-id="784ba-310">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="784ba-310">Get incremental changes to messages in a folder</span></span>](/graph/delta-query-messages)
- [<span data-ttu-id="784ba-311">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="784ba-311">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="784ba-312">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="784ba-312">Add custom data to users using open extensions</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="784ba-313">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="784ba-313">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
