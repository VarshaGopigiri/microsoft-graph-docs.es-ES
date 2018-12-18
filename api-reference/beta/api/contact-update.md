---
title: Actualizar contacto
description: Actualizar las propiedades del objeto de contacto.
author: angelgolfer-ms
ms.openlocfilehash: d25efb55a090c4c0b5fa750b64a0b2a905327a76
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334107"
---
# <a name="update-contact"></a><span data-ttu-id="90451-103">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="90451-103">Update contact</span></span>

> <span data-ttu-id="90451-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90451-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90451-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90451-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="90451-106">Actualizar las propiedades del objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-106">Update the properties of contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="90451-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="90451-107">Permissions</span></span>
<span data-ttu-id="90451-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90451-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90451-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90451-110">Permission type</span></span>      | <span data-ttu-id="90451-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90451-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90451-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90451-112">Delegated (work or school account)</span></span> | <span data-ttu-id="90451-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90451-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="90451-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90451-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90451-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90451-115">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="90451-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90451-116">Application</span></span> | <span data-ttu-id="90451-117">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90451-117">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="90451-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90451-118">HTTP request</span></span>
<span data-ttu-id="90451-119"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde de predeterminado del usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="90451-119"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="90451-120">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="90451-120">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="90451-121">[Póngase en contacto con](../resources/contact.md) contenidos en una carpeta secundaria de un [contactFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="90451-121">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md).</span></span>  <span data-ttu-id="90451-122">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="90451-122">The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="90451-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90451-123">Request headers</span></span>
| <span data-ttu-id="90451-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90451-124">Header</span></span>       | <span data-ttu-id="90451-125">Valor</span><span class="sxs-lookup"><span data-stu-id="90451-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="90451-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="90451-126">Authorization</span></span>  | <span data-ttu-id="90451-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90451-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="90451-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="90451-129">Content-Type</span></span>  | <span data-ttu-id="90451-p105">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90451-p105">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="90451-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90451-132">Request body</span></span>
<span data-ttu-id="90451-p106">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="90451-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="90451-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90451-136">Property</span></span>     | <span data-ttu-id="90451-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="90451-137">Type</span></span>   |<span data-ttu-id="90451-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="90451-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="90451-139">assistantName</span><span class="sxs-lookup"><span data-stu-id="90451-139">assistantName</span></span>|<span data-ttu-id="90451-140">String</span><span class="sxs-lookup"><span data-stu-id="90451-140">String</span></span>|<span data-ttu-id="90451-141">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-141">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="90451-142">birthday</span><span class="sxs-lookup"><span data-stu-id="90451-142">birthday</span></span>|<span data-ttu-id="90451-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="90451-143">DateTimeOffset</span></span>|<span data-ttu-id="90451-144">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-144">The contact's birthday.</span></span>|
|<span data-ttu-id="90451-145">categories</span><span class="sxs-lookup"><span data-stu-id="90451-145">categories</span></span>|<span data-ttu-id="90451-146">String</span><span class="sxs-lookup"><span data-stu-id="90451-146">String</span></span>|<span data-ttu-id="90451-147">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-147">The categories associated with the contact.</span></span>|
|<span data-ttu-id="90451-148">children</span><span class="sxs-lookup"><span data-stu-id="90451-148">children</span></span>|<span data-ttu-id="90451-149">String</span><span class="sxs-lookup"><span data-stu-id="90451-149">String</span></span>||
|<span data-ttu-id="90451-150">companyName</span><span class="sxs-lookup"><span data-stu-id="90451-150">companyName</span></span>|<span data-ttu-id="90451-151">String</span><span class="sxs-lookup"><span data-stu-id="90451-151">String</span></span>|<span data-ttu-id="90451-152">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-152">The name of the contact's company.</span></span>|
|<span data-ttu-id="90451-153">department</span><span class="sxs-lookup"><span data-stu-id="90451-153">department</span></span>|<span data-ttu-id="90451-154">String</span><span class="sxs-lookup"><span data-stu-id="90451-154">String</span></span>|<span data-ttu-id="90451-155">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-155">The contact's department.</span></span>|
|<span data-ttu-id="90451-156">displayName</span><span class="sxs-lookup"><span data-stu-id="90451-156">displayName</span></span>|<span data-ttu-id="90451-157">String</span><span class="sxs-lookup"><span data-stu-id="90451-157">String</span></span>|<span data-ttu-id="90451-158">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-158">The contact's display name.</span></span> <span data-ttu-id="90451-159">Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado.</span><span class="sxs-lookup"><span data-stu-id="90451-159">Note that later updates to other properties may cause an automatically generated value to overwrite the displayName value you have specified.</span></span> <span data-ttu-id="90451-160">Para conservar un valor existente, siempre incluirla como displayName en una operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="90451-160">To preserve a pre-existing value, always include it as displayName in an update operation.</span></span>|
|<span data-ttu-id="90451-161">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="90451-161">emailAddresses</span></span>|<span data-ttu-id="90451-162">colección de [typedEmailAddress](../resources/typedemailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="90451-162">[typedEmailAddress](../resources/typedemailaddress.md) collection</span></span>|<span data-ttu-id="90451-163">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-163">The contact's email addresses.</span></span>|
|<span data-ttu-id="90451-164">fileAs</span><span class="sxs-lookup"><span data-stu-id="90451-164">fileAs</span></span>|<span data-ttu-id="90451-165">String</span><span class="sxs-lookup"><span data-stu-id="90451-165">String</span></span>|<span data-ttu-id="90451-166">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-166">The name the contact is filed under.</span></span>|
|<span data-ttu-id="90451-167">gender</span><span class="sxs-lookup"><span data-stu-id="90451-167">gender</span></span> |<span data-ttu-id="90451-168">String</span><span class="sxs-lookup"><span data-stu-id="90451-168">String</span></span> |<span data-ttu-id="90451-169">Género del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-169">The contact's gender.</span></span> |
|<span data-ttu-id="90451-170">generation</span><span class="sxs-lookup"><span data-stu-id="90451-170">generation</span></span>|<span data-ttu-id="90451-171">String</span><span class="sxs-lookup"><span data-stu-id="90451-171">String</span></span>|<span data-ttu-id="90451-172">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-172">The contact's generation.</span></span>|
|<span data-ttu-id="90451-173">givenName</span><span class="sxs-lookup"><span data-stu-id="90451-173">givenName</span></span>|<span data-ttu-id="90451-174">String</span><span class="sxs-lookup"><span data-stu-id="90451-174">String</span></span>|<span data-ttu-id="90451-175">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-175">The contact's given name.</span></span>|
|<span data-ttu-id="90451-176">imAddresses</span><span class="sxs-lookup"><span data-stu-id="90451-176">imAddresses</span></span>|<span data-ttu-id="90451-177">String</span><span class="sxs-lookup"><span data-stu-id="90451-177">String</span></span>|<span data-ttu-id="90451-178">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-178">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="90451-179">initials</span><span class="sxs-lookup"><span data-stu-id="90451-179">initials</span></span>|<span data-ttu-id="90451-180">String</span><span class="sxs-lookup"><span data-stu-id="90451-180">String</span></span>|<span data-ttu-id="90451-181">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-181">The contact's initials.</span></span>|
|<span data-ttu-id="90451-182">jobTitle</span><span class="sxs-lookup"><span data-stu-id="90451-182">jobTitle</span></span>|<span data-ttu-id="90451-183">String</span><span class="sxs-lookup"><span data-stu-id="90451-183">String</span></span>|<span data-ttu-id="90451-184">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-184">The contact’s job title.</span></span>|
|<span data-ttu-id="90451-185">manager</span><span class="sxs-lookup"><span data-stu-id="90451-185">manager</span></span>|<span data-ttu-id="90451-186">String</span><span class="sxs-lookup"><span data-stu-id="90451-186">String</span></span>|<span data-ttu-id="90451-187">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-187">The name of the contact's manager.</span></span>
|<span data-ttu-id="90451-188">middleName</span><span class="sxs-lookup"><span data-stu-id="90451-188">middleName</span></span>|<span data-ttu-id="90451-189">String</span><span class="sxs-lookup"><span data-stu-id="90451-189">String</span></span>|<span data-ttu-id="90451-190">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-190">The contact's middle name.</span></span>|
|<span data-ttu-id="90451-191">nickName</span><span class="sxs-lookup"><span data-stu-id="90451-191">nickName</span></span>|<span data-ttu-id="90451-192">String</span><span class="sxs-lookup"><span data-stu-id="90451-192">String</span></span>|<span data-ttu-id="90451-193">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-193">The contact's nickname.</span></span>|
|<span data-ttu-id="90451-194">officeLocation</span><span class="sxs-lookup"><span data-stu-id="90451-194">officeLocation</span></span>|<span data-ttu-id="90451-195">String</span><span class="sxs-lookup"><span data-stu-id="90451-195">String</span></span>|<span data-ttu-id="90451-196">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-196">The location of the contact's office.</span></span>|
|<span data-ttu-id="90451-197">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="90451-197">parentFolderId</span></span>|<span data-ttu-id="90451-198">String</span><span class="sxs-lookup"><span data-stu-id="90451-198">String</span></span>|<span data-ttu-id="90451-199">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-199">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="90451-200">personalNotes</span><span class="sxs-lookup"><span data-stu-id="90451-200">personalNotes</span></span>|<span data-ttu-id="90451-201">String</span><span class="sxs-lookup"><span data-stu-id="90451-201">String</span></span>|<span data-ttu-id="90451-202">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-202">The user's notes about the contact.</span></span>|
|<span data-ttu-id="90451-203">phones</span><span class="sxs-lookup"><span data-stu-id="90451-203">phones</span></span> |<span data-ttu-id="90451-204">Colección [phone](../resources/phone.md)</span><span class="sxs-lookup"><span data-stu-id="90451-204">[phone](../resources/phone.md) collection</span></span> |<span data-ttu-id="90451-205">Números de teléfono asociados con el contacto, por ejemplo, teléfono particular, teléfono móvil y teléfono del trabajo.</span><span class="sxs-lookup"><span data-stu-id="90451-205">Phone numbers associated with the contact, for example, home phone, mobile phone, and business phone.</span></span> |
|<span data-ttu-id="90451-206">postalAddresses</span><span class="sxs-lookup"><span data-stu-id="90451-206">postalAddresses</span></span> |<span data-ttu-id="90451-207">colección [physicalAddress](../resources/physicaladdress.md)</span><span class="sxs-lookup"><span data-stu-id="90451-207">[physicalAddress](../resources/physicaladdress.md) collection</span></span> |<span data-ttu-id="90451-208">Direcciones asociadas con el contacto, por ejemplo, home dirección y dirección de la empresa.</span><span class="sxs-lookup"><span data-stu-id="90451-208">Addresses associated with the contact, for example, home address and business address.</span></span> |
|<span data-ttu-id="90451-209">profession</span><span class="sxs-lookup"><span data-stu-id="90451-209">profession</span></span>|<span data-ttu-id="90451-210">String</span><span class="sxs-lookup"><span data-stu-id="90451-210">String</span></span>|<span data-ttu-id="90451-211">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-211">The contact's profession.</span></span>|
|<span data-ttu-id="90451-212">spouseName</span><span class="sxs-lookup"><span data-stu-id="90451-212">spouseName</span></span>|<span data-ttu-id="90451-213">String</span><span class="sxs-lookup"><span data-stu-id="90451-213">String</span></span>|<span data-ttu-id="90451-214">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-214">The name of the contact's spouse/partner.</span></span>|
|<span data-ttu-id="90451-215">surname</span><span class="sxs-lookup"><span data-stu-id="90451-215">surname</span></span>|<span data-ttu-id="90451-216">String</span><span class="sxs-lookup"><span data-stu-id="90451-216">String</span></span>|<span data-ttu-id="90451-217">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-217">The contact's surname.</span></span>|
|<span data-ttu-id="90451-218">title</span><span class="sxs-lookup"><span data-stu-id="90451-218">title</span></span>|<span data-ttu-id="90451-219">String</span><span class="sxs-lookup"><span data-stu-id="90451-219">String</span></span>|<span data-ttu-id="90451-220">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-220">The contact's title.</span></span>|
|<span data-ttu-id="90451-221">websites</span><span class="sxs-lookup"><span data-stu-id="90451-221">websites</span></span> |<span data-ttu-id="90451-222">Colección [website](../resources/website.md)</span><span class="sxs-lookup"><span data-stu-id="90451-222">[website](../resources/website.md) collection</span></span>|<span data-ttu-id="90451-223">Sitios Web asociados con el contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-223">Web sites associated with the contact.</span></span> |
|<span data-ttu-id="90451-224">weddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="90451-224">weddingAnniversary</span></span> |<span data-ttu-id="90451-225">Date</span><span class="sxs-lookup"><span data-stu-id="90451-225">Date</span></span> |<span data-ttu-id="90451-226">Aniversario de boda del contacto.</span><span class="sxs-lookup"><span data-stu-id="90451-226">The contact's wedding anniversary.</span></span> |
|<span data-ttu-id="90451-227">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="90451-227">yomiCompanyName</span></span>|<span data-ttu-id="90451-228">String</span><span class="sxs-lookup"><span data-stu-id="90451-228">String</span></span>|<span data-ttu-id="90451-p108">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="90451-p108">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="90451-231">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="90451-231">yomiGivenName</span></span>|<span data-ttu-id="90451-232">String</span><span class="sxs-lookup"><span data-stu-id="90451-232">String</span></span>|<span data-ttu-id="90451-p109">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="90451-p109">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="90451-235">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="90451-235">yomiSurname</span></span>|<span data-ttu-id="90451-236">String</span><span class="sxs-lookup"><span data-stu-id="90451-236">String</span></span>|<span data-ttu-id="90451-p110">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="90451-p110">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

<span data-ttu-id="90451-239">Puesto que el recurso **póngase en contacto con** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicas de la aplicación en las propiedades personalizadas de una extensión en una instancia **de contacto** existente.</span><span class="sxs-lookup"><span data-stu-id="90451-239">Since the **contact** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **contact** instance.</span></span>

## <a name="response"></a><span data-ttu-id="90451-240">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90451-240">Response</span></span>

<span data-ttu-id="90451-241">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [póngase en contacto con](../resources/contact.md) el objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90451-241">If successful, this method returns a `200 OK` response code and updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="90451-242">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90451-242">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90451-243">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90451-243">Request</span></span>
<span data-ttu-id="90451-244">En el ejemplo siguiente se actualiza la dirección de correo electrónico personal del contacto especificado.</span><span class="sxs-lookup"><span data-stu-id="90451-244">The following example updates the personal email address of the specified contact.</span></span>
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
##### <a name="response"></a><span data-ttu-id="90451-245">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90451-245">Response</span></span>
<span data-ttu-id="90451-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90451-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="90451-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="90451-249">See also</span></span>

- [<span data-ttu-id="90451-250">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="90451-250">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="90451-251">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="90451-251">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
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