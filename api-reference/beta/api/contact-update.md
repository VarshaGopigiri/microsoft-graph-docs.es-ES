---
title: Actualizar contacto
description: Actualizar las propiedades del objeto de contacto.
ms.openlocfilehash: 2fbf597ebc8a6c65141c64ae42ae42266f14cbde
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085640"
---
# <a name="update-contact"></a><span data-ttu-id="380bc-103">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="380bc-103">Update contact</span></span>

> <span data-ttu-id="380bc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="380bc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="380bc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="380bc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="380bc-106">Actualizar las propiedades del objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-106">Update the properties of contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="380bc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="380bc-107">Permissions</span></span>
<span data-ttu-id="380bc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="380bc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="380bc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="380bc-110">Permission type</span></span>      | <span data-ttu-id="380bc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="380bc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="380bc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="380bc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="380bc-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="380bc-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="380bc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="380bc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="380bc-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="380bc-115">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="380bc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="380bc-116">Application</span></span> | <span data-ttu-id="380bc-117">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="380bc-117">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="380bc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="380bc-118">HTTP request</span></span>
<span data-ttu-id="380bc-119"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde de predeterminado del usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="380bc-119"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="380bc-120">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="380bc-120">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="380bc-121">[Póngase en contacto con](../resources/contact.md) contenidos en una carpeta secundaria de un [contactFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="380bc-121">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md).</span></span>  <span data-ttu-id="380bc-122">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="380bc-122">The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="380bc-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="380bc-123">Request headers</span></span>
| <span data-ttu-id="380bc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="380bc-124">Header</span></span>       | <span data-ttu-id="380bc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="380bc-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="380bc-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="380bc-126">Authorization</span></span>  | <span data-ttu-id="380bc-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="380bc-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="380bc-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="380bc-129">Content-Type</span></span>  | <span data-ttu-id="380bc-p105">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="380bc-p105">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="380bc-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="380bc-132">Request body</span></span>
<span data-ttu-id="380bc-p106">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="380bc-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="380bc-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="380bc-136">Property</span></span>     | <span data-ttu-id="380bc-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="380bc-137">Type</span></span>   |<span data-ttu-id="380bc-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="380bc-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="380bc-139">assistantName</span><span class="sxs-lookup"><span data-stu-id="380bc-139">assistantName</span></span>|<span data-ttu-id="380bc-140">String</span><span class="sxs-lookup"><span data-stu-id="380bc-140">String</span></span>|<span data-ttu-id="380bc-141">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-141">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="380bc-142">birthday</span><span class="sxs-lookup"><span data-stu-id="380bc-142">birthday</span></span>|<span data-ttu-id="380bc-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="380bc-143">DateTimeOffset</span></span>|<span data-ttu-id="380bc-144">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-144">The contact's birthday.</span></span>|
|<span data-ttu-id="380bc-145">categories</span><span class="sxs-lookup"><span data-stu-id="380bc-145">categories</span></span>|<span data-ttu-id="380bc-146">String</span><span class="sxs-lookup"><span data-stu-id="380bc-146">String</span></span>|<span data-ttu-id="380bc-147">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-147">The categories associated with the contact.</span></span>|
|<span data-ttu-id="380bc-148">children</span><span class="sxs-lookup"><span data-stu-id="380bc-148">children</span></span>|<span data-ttu-id="380bc-149">String</span><span class="sxs-lookup"><span data-stu-id="380bc-149">String</span></span>||
|<span data-ttu-id="380bc-150">companyName</span><span class="sxs-lookup"><span data-stu-id="380bc-150">companyName</span></span>|<span data-ttu-id="380bc-151">String</span><span class="sxs-lookup"><span data-stu-id="380bc-151">String</span></span>|<span data-ttu-id="380bc-152">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-152">The name of the contact's company.</span></span>|
|<span data-ttu-id="380bc-153">department</span><span class="sxs-lookup"><span data-stu-id="380bc-153">department</span></span>|<span data-ttu-id="380bc-154">String</span><span class="sxs-lookup"><span data-stu-id="380bc-154">String</span></span>|<span data-ttu-id="380bc-155">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-155">The contact's department.</span></span>|
|<span data-ttu-id="380bc-156">displayName</span><span class="sxs-lookup"><span data-stu-id="380bc-156">displayName</span></span>|<span data-ttu-id="380bc-157">String</span><span class="sxs-lookup"><span data-stu-id="380bc-157">String</span></span>|<span data-ttu-id="380bc-158">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-158">The contact's display name.</span></span> <span data-ttu-id="380bc-159">Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado.</span><span class="sxs-lookup"><span data-stu-id="380bc-159">Note that later updates to other properties may cause an automatically generated value to overwrite the displayName value you have specified.</span></span> <span data-ttu-id="380bc-160">Para conservar un valor existente, siempre incluirla como displayName en una operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="380bc-160">To preserve a pre-existing value, always include it as displayName in an update operation.</span></span>|
|<span data-ttu-id="380bc-161">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="380bc-161">emailAddresses</span></span>|<span data-ttu-id="380bc-162">colección de [typedEmailAddress](../resources/typedemailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="380bc-162">[typedEmailAddress](../resources/typedemailaddress.md) collection</span></span>|<span data-ttu-id="380bc-163">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-163">The contact's email addresses.</span></span>|
|<span data-ttu-id="380bc-164">fileAs</span><span class="sxs-lookup"><span data-stu-id="380bc-164">fileAs</span></span>|<span data-ttu-id="380bc-165">String</span><span class="sxs-lookup"><span data-stu-id="380bc-165">String</span></span>|<span data-ttu-id="380bc-166">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-166">The name the contact is filed under.</span></span>|
|<span data-ttu-id="380bc-167">gender</span><span class="sxs-lookup"><span data-stu-id="380bc-167">gender</span></span> |<span data-ttu-id="380bc-168">String</span><span class="sxs-lookup"><span data-stu-id="380bc-168">String</span></span> |<span data-ttu-id="380bc-169">Género del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-169">The contact's gender.</span></span> |
|<span data-ttu-id="380bc-170">generation</span><span class="sxs-lookup"><span data-stu-id="380bc-170">generation</span></span>|<span data-ttu-id="380bc-171">String</span><span class="sxs-lookup"><span data-stu-id="380bc-171">String</span></span>|<span data-ttu-id="380bc-172">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-172">The contact's generation.</span></span>|
|<span data-ttu-id="380bc-173">givenName</span><span class="sxs-lookup"><span data-stu-id="380bc-173">givenName</span></span>|<span data-ttu-id="380bc-174">String</span><span class="sxs-lookup"><span data-stu-id="380bc-174">String</span></span>|<span data-ttu-id="380bc-175">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-175">The contact's given name.</span></span>|
|<span data-ttu-id="380bc-176">imAddresses</span><span class="sxs-lookup"><span data-stu-id="380bc-176">imAddresses</span></span>|<span data-ttu-id="380bc-177">String</span><span class="sxs-lookup"><span data-stu-id="380bc-177">String</span></span>|<span data-ttu-id="380bc-178">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-178">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="380bc-179">initials</span><span class="sxs-lookup"><span data-stu-id="380bc-179">initials</span></span>|<span data-ttu-id="380bc-180">String</span><span class="sxs-lookup"><span data-stu-id="380bc-180">String</span></span>|<span data-ttu-id="380bc-181">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-181">The contact's initials.</span></span>|
|<span data-ttu-id="380bc-182">jobTitle</span><span class="sxs-lookup"><span data-stu-id="380bc-182">jobTitle</span></span>|<span data-ttu-id="380bc-183">String</span><span class="sxs-lookup"><span data-stu-id="380bc-183">String</span></span>|<span data-ttu-id="380bc-184">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-184">The contact’s job title.</span></span>|
|<span data-ttu-id="380bc-185">manager</span><span class="sxs-lookup"><span data-stu-id="380bc-185">manager</span></span>|<span data-ttu-id="380bc-186">String</span><span class="sxs-lookup"><span data-stu-id="380bc-186">String</span></span>|<span data-ttu-id="380bc-187">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-187">The name of the contact's manager.</span></span>
|<span data-ttu-id="380bc-188">middleName</span><span class="sxs-lookup"><span data-stu-id="380bc-188">middleName</span></span>|<span data-ttu-id="380bc-189">String</span><span class="sxs-lookup"><span data-stu-id="380bc-189">String</span></span>|<span data-ttu-id="380bc-190">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-190">The contact's middle name.</span></span>|
|<span data-ttu-id="380bc-191">nickName</span><span class="sxs-lookup"><span data-stu-id="380bc-191">nickName</span></span>|<span data-ttu-id="380bc-192">String</span><span class="sxs-lookup"><span data-stu-id="380bc-192">String</span></span>|<span data-ttu-id="380bc-193">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-193">The contact's nickname.</span></span>|
|<span data-ttu-id="380bc-194">officeLocation</span><span class="sxs-lookup"><span data-stu-id="380bc-194">officeLocation</span></span>|<span data-ttu-id="380bc-195">String</span><span class="sxs-lookup"><span data-stu-id="380bc-195">String</span></span>|<span data-ttu-id="380bc-196">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-196">The location of the contact's office.</span></span>|
|<span data-ttu-id="380bc-197">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="380bc-197">parentFolderId</span></span>|<span data-ttu-id="380bc-198">String</span><span class="sxs-lookup"><span data-stu-id="380bc-198">String</span></span>|<span data-ttu-id="380bc-199">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-199">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="380bc-200">personalNotes</span><span class="sxs-lookup"><span data-stu-id="380bc-200">personalNotes</span></span>|<span data-ttu-id="380bc-201">String</span><span class="sxs-lookup"><span data-stu-id="380bc-201">String</span></span>|<span data-ttu-id="380bc-202">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-202">The user's notes about the contact.</span></span>|
|<span data-ttu-id="380bc-203">phones</span><span class="sxs-lookup"><span data-stu-id="380bc-203">phones</span></span> |<span data-ttu-id="380bc-204">Colección [phone](../resources/phone.md)</span><span class="sxs-lookup"><span data-stu-id="380bc-204">[phone](../resources/phone.md) collection</span></span> |<span data-ttu-id="380bc-205">Números de teléfono asociados con el contacto, por ejemplo, teléfono particular, teléfono móvil y teléfono del trabajo.</span><span class="sxs-lookup"><span data-stu-id="380bc-205">Phone numbers associated with the contact, for example, home phone, mobile phone, and business phone.</span></span> |
|<span data-ttu-id="380bc-206">postalAddresses</span><span class="sxs-lookup"><span data-stu-id="380bc-206">postalAddresses</span></span> |<span data-ttu-id="380bc-207">colección [physicalAddress](../resources/physicaladdress.md)</span><span class="sxs-lookup"><span data-stu-id="380bc-207">[physicalAddress](../resources/physicaladdress.md) collection</span></span> |<span data-ttu-id="380bc-208">Direcciones asociadas con el contacto, por ejemplo, home dirección y dirección de la empresa.</span><span class="sxs-lookup"><span data-stu-id="380bc-208">Addresses associated with the contact, for example, home address and business address.</span></span> |
|<span data-ttu-id="380bc-209">profession</span><span class="sxs-lookup"><span data-stu-id="380bc-209">profession</span></span>|<span data-ttu-id="380bc-210">String</span><span class="sxs-lookup"><span data-stu-id="380bc-210">String</span></span>|<span data-ttu-id="380bc-211">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-211">The contact's profession.</span></span>|
|<span data-ttu-id="380bc-212">spouseName</span><span class="sxs-lookup"><span data-stu-id="380bc-212">spouseName</span></span>|<span data-ttu-id="380bc-213">String</span><span class="sxs-lookup"><span data-stu-id="380bc-213">String</span></span>|<span data-ttu-id="380bc-214">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-214">The name of the contact's spouse/partner.</span></span>|
|<span data-ttu-id="380bc-215">surname</span><span class="sxs-lookup"><span data-stu-id="380bc-215">surname</span></span>|<span data-ttu-id="380bc-216">String</span><span class="sxs-lookup"><span data-stu-id="380bc-216">String</span></span>|<span data-ttu-id="380bc-217">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-217">The contact's surname.</span></span>|
|<span data-ttu-id="380bc-218">title</span><span class="sxs-lookup"><span data-stu-id="380bc-218">title</span></span>|<span data-ttu-id="380bc-219">String</span><span class="sxs-lookup"><span data-stu-id="380bc-219">String</span></span>|<span data-ttu-id="380bc-220">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-220">The contact's title.</span></span>|
|<span data-ttu-id="380bc-221">websites</span><span class="sxs-lookup"><span data-stu-id="380bc-221">websites</span></span> |<span data-ttu-id="380bc-222">Colección [website](../resources/website.md)</span><span class="sxs-lookup"><span data-stu-id="380bc-222">[website](../resources/website.md) collection</span></span>|<span data-ttu-id="380bc-223">Sitios Web asociados con el contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-223">Web sites associated with the contact.</span></span> |
|<span data-ttu-id="380bc-224">weddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="380bc-224">weddingAnniversary</span></span> |<span data-ttu-id="380bc-225">Fecha</span><span class="sxs-lookup"><span data-stu-id="380bc-225">Date</span></span> |<span data-ttu-id="380bc-226">Aniversario de boda del contacto.</span><span class="sxs-lookup"><span data-stu-id="380bc-226">The contact's wedding anniversary.</span></span> |
|<span data-ttu-id="380bc-227">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="380bc-227">yomiCompanyName</span></span>|<span data-ttu-id="380bc-228">String</span><span class="sxs-lookup"><span data-stu-id="380bc-228">String</span></span>|<span data-ttu-id="380bc-p108">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="380bc-p108">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="380bc-231">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="380bc-231">yomiGivenName</span></span>|<span data-ttu-id="380bc-232">String</span><span class="sxs-lookup"><span data-stu-id="380bc-232">String</span></span>|<span data-ttu-id="380bc-p109">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="380bc-p109">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="380bc-235">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="380bc-235">yomiSurname</span></span>|<span data-ttu-id="380bc-236">String</span><span class="sxs-lookup"><span data-stu-id="380bc-236">String</span></span>|<span data-ttu-id="380bc-p110">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="380bc-p110">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

<span data-ttu-id="380bc-239">Puesto que el recurso **póngase en contacto con** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicas de la aplicación en las propiedades personalizadas de una extensión en una instancia **de contacto** existente.</span><span class="sxs-lookup"><span data-stu-id="380bc-239">Since the **contact** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **contact** instance.</span></span>

## <a name="response"></a><span data-ttu-id="380bc-240">Respuesta</span><span class="sxs-lookup"><span data-stu-id="380bc-240">Response</span></span>

<span data-ttu-id="380bc-241">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [póngase en contacto con](../resources/contact.md) el objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="380bc-241">If successful, this method returns a `200 OK` response code and updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="380bc-242">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="380bc-242">Example</span></span>
##### <a name="request"></a><span data-ttu-id="380bc-243">Solicitud</span><span class="sxs-lookup"><span data-stu-id="380bc-243">Request</span></span>
<span data-ttu-id="380bc-244">En el ejemplo siguiente se actualiza la dirección de correo electrónico personal del contacto especificado.</span><span class="sxs-lookup"><span data-stu-id="380bc-244">The following example updates the personal email address of the specified contact.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_contact"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/contacts/AAMkADh6v5AAAvgTCEAAA=
Content-type: application/json

{
    "emailAddresses":[
        {
            "type":"personal",
            "name":"Pavel Bansky",
            "address":"pavelb@adatum.onmicrosoft.com"
        },
        {
          "address": "pavelb@fabrikam.onmicrosoft.com",
          "name": "Pavel Bansky",
          "type": "other",
          "otherLabel": "Volunteer work"
        }
    ]
}
```
##### <a name="response"></a><span data-ttu-id="380bc-245">Respuesta</span><span class="sxs-lookup"><span data-stu-id="380bc-245">Response</span></span>
<span data-ttu-id="380bc-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="380bc-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('c3e1fcd2-db78-42a8-aec5-1f2cd59abb5c')/contacts/$entity",
    "@odata.etag":"W/\"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7fh\"",
    "id":"AAMkADh6v5AAAvgTCEAAA=",
    "createdDateTime":"2018-06-11T19:56:07Z",
    "lastModifiedDateTime":"2018-06-11T20:26:23Z",
    "changeKey":"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7fh",
    "categories":[

    ],
    "parentFolderId":"AAMkADh6v5AAAAAAEOAAA=",
    "birthday":null,
    "fileAs":"",
    "displayName":"Pavel Bansky",
    "givenName":"Pavel",
    "initials":null,
    "middleName":null,
    "nickName":null,
    "surname":"Bansky",
    "title":null,
    "yomiGivenName":null,
    "yomiSurname":null,
    "yomiCompanyName":null,
    "generation":null,
    "imAddresses":[

    ],
    "jobTitle":null,
    "companyName":null,
    "department":null,
    "officeLocation":null,
    "profession":null,
    "assistantName":null,
    "manager":null,
    "spouseName":null,
    "personalNotes":"",
    "children":[

    ],
    "gender":null,
    "isFavorite":null,
    "emailAddresses":[
        {
            "type":"personal",
            "name":"Pavel Bansky",
            "address":"pavelb@adatum.onmicrosoft.com"
        },
        {
            "type":"other",
            "otherLabel":"Volunteer work",
            "name":"Pavel Bansky",
            "address":"pavelb@fabrikam.onmicrosoft.com"
        }
    ],
    "websites":[

    ],
    "phones":[
        {
            "type":"business",
            "number":"+1 732 555 0102"
        }
    ],
    "postalAddresses":[

    ],
    "flag":{
        "flagStatus":"notFlagged"
    }
}
```

## <a name="see-also"></a><span data-ttu-id="380bc-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="380bc-249">See also</span></span>

- [<span data-ttu-id="380bc-250">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="380bc-250">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="380bc-251">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="380bc-251">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->