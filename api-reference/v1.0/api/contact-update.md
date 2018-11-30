---
title: Actualizar contacto
description: Actualiza las propiedades de un objeto de contacto.
ms.openlocfilehash: baf563530dc174418169efdd7f7bb48d81048a6b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031010"
---
# <a name="update-contact"></a><span data-ttu-id="b26ac-103">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="b26ac-103">Update contact</span></span>

<span data-ttu-id="b26ac-104">Actualiza las propiedades de un objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-104">Update the properties of a contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="b26ac-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b26ac-105">Permissions</span></span>
<span data-ttu-id="b26ac-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b26ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b26ac-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b26ac-108">Permission type</span></span>      | <span data-ttu-id="b26ac-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b26ac-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b26ac-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b26ac-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b26ac-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b26ac-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="b26ac-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b26ac-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b26ac-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b26ac-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="b26ac-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b26ac-114">Application</span></span> | <span data-ttu-id="b26ac-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b26ac-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="b26ac-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b26ac-116">HTTP request</span></span>
<span data-ttu-id="b26ac-117"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde predeterminado de un usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="b26ac-117"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="b26ac-118">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="b26ac-118">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="b26ac-p102">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="b26ac-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b26ac-121">Request headers</span></span>
| <span data-ttu-id="b26ac-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b26ac-122">Header</span></span>       | <span data-ttu-id="b26ac-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b26ac-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b26ac-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b26ac-124">Authorization</span></span>  | <span data-ttu-id="b26ac-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b26ac-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b26ac-127">Content-Type</span></span>  | <span data-ttu-id="b26ac-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b26ac-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b26ac-130">Request body</span></span>
<span data-ttu-id="b26ac-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b26ac-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b26ac-134">Property</span></span>     | <span data-ttu-id="b26ac-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="b26ac-135">Type</span></span>   |<span data-ttu-id="b26ac-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="b26ac-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b26ac-137">assistantName</span><span class="sxs-lookup"><span data-stu-id="b26ac-137">assistantName</span></span>|<span data-ttu-id="b26ac-138">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-138">String</span></span>|<span data-ttu-id="b26ac-139">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-139">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="b26ac-140">birthday</span><span class="sxs-lookup"><span data-stu-id="b26ac-140">birthday</span></span>|<span data-ttu-id="b26ac-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b26ac-141">DateTimeOffset</span></span>|<span data-ttu-id="b26ac-142">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-142">The contact's birthday.</span></span>|
|<span data-ttu-id="b26ac-143">businessAddress</span><span class="sxs-lookup"><span data-stu-id="b26ac-143">businessAddress</span></span>|[<span data-ttu-id="b26ac-144">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="b26ac-144">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="b26ac-145">La dirección del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-145">The contact's business address.</span></span>|
|<span data-ttu-id="b26ac-146">businessHomePage</span><span class="sxs-lookup"><span data-stu-id="b26ac-146">businessHomePage</span></span>|<span data-ttu-id="b26ac-147">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-147">String</span></span>|<span data-ttu-id="b26ac-148">La página principal de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-148">The business home page of the contact.</span></span>|
|<span data-ttu-id="b26ac-149">businessPhones</span><span class="sxs-lookup"><span data-stu-id="b26ac-149">businessPhones</span></span>|<span data-ttu-id="b26ac-150">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-150">String</span></span>|<span data-ttu-id="b26ac-151">Los números de teléfono del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-151">The contact's business phone numbers.</span></span>|
|<span data-ttu-id="b26ac-152">categories</span><span class="sxs-lookup"><span data-stu-id="b26ac-152">categories</span></span>|<span data-ttu-id="b26ac-153">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-153">String</span></span>|<span data-ttu-id="b26ac-154">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-154">The categories associated with the contact.</span></span>|
|<span data-ttu-id="b26ac-155">children</span><span class="sxs-lookup"><span data-stu-id="b26ac-155">children</span></span>|<span data-ttu-id="b26ac-156">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-156">String</span></span>|<span data-ttu-id="b26ac-157">Los nombres de los hijos del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-157">The names of the contact's children.</span></span>|
|<span data-ttu-id="b26ac-158">companyName</span><span class="sxs-lookup"><span data-stu-id="b26ac-158">companyName</span></span>|<span data-ttu-id="b26ac-159">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-159">String</span></span>|<span data-ttu-id="b26ac-160">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-160">The name of the contact's company.</span></span>|
|<span data-ttu-id="b26ac-161">department</span><span class="sxs-lookup"><span data-stu-id="b26ac-161">department</span></span>|<span data-ttu-id="b26ac-162">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-162">String</span></span>|<span data-ttu-id="b26ac-163">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-163">The contact's department.</span></span>|
|<span data-ttu-id="b26ac-164">displayName</span><span class="sxs-lookup"><span data-stu-id="b26ac-164">displayName</span></span>|<span data-ttu-id="b26ac-165">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-165">String</span></span>|<span data-ttu-id="b26ac-166">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-166">The contact's display name.</span></span> <span data-ttu-id="b26ac-167">Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado.</span><span class="sxs-lookup"><span data-stu-id="b26ac-167">Note that later updates to other properties may cause an automatically generated value to overwrite the displayName value you have specified.</span></span> <span data-ttu-id="b26ac-168">Para conservar un valor existente, siempre incluirla como displayName en una operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="b26ac-168">To preserve a pre-existing value, always include it as displayName in an update operation.</span></span>|
|<span data-ttu-id="b26ac-169">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="b26ac-169">emailAddresses</span></span>|<span data-ttu-id="b26ac-170">Colección [EmailAddress](../resources/emailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="b26ac-170">[EmailAddress](../resources/emailaddress.md) collection</span></span>|<span data-ttu-id="b26ac-171">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-171">The contact's email addresses.</span></span>|
|<span data-ttu-id="b26ac-172">fileAs</span><span class="sxs-lookup"><span data-stu-id="b26ac-172">fileAs</span></span>|<span data-ttu-id="b26ac-173">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-173">String</span></span>|<span data-ttu-id="b26ac-174">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-174">The name the contact is filed under.</span></span>|
|<span data-ttu-id="b26ac-175">generation</span><span class="sxs-lookup"><span data-stu-id="b26ac-175">generation</span></span>|<span data-ttu-id="b26ac-176">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-176">String</span></span>|<span data-ttu-id="b26ac-177">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-177">The contact's generation.</span></span>|
|<span data-ttu-id="b26ac-178">givenName</span><span class="sxs-lookup"><span data-stu-id="b26ac-178">givenName</span></span>|<span data-ttu-id="b26ac-179">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-179">String</span></span>|<span data-ttu-id="b26ac-180">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-180">The contact's given name.</span></span>|
|<span data-ttu-id="b26ac-181">homeAddress</span><span class="sxs-lookup"><span data-stu-id="b26ac-181">homeAddress</span></span>|[<span data-ttu-id="b26ac-182">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="b26ac-182">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="b26ac-183">La dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-183">The contact's home address.</span></span>|
|<span data-ttu-id="b26ac-184">homePhones</span><span class="sxs-lookup"><span data-stu-id="b26ac-184">homePhones</span></span>|<span data-ttu-id="b26ac-185">Colección String</span><span class="sxs-lookup"><span data-stu-id="b26ac-185">String collection</span></span>|<span data-ttu-id="b26ac-186">Los números de teléfono particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-186">The contact's home phone numbers.</span></span>|
|<span data-ttu-id="b26ac-187">imAddresses</span><span class="sxs-lookup"><span data-stu-id="b26ac-187">imAddresses</span></span>|<span data-ttu-id="b26ac-188">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-188">String</span></span>|<span data-ttu-id="b26ac-189">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-189">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="b26ac-190">initials</span><span class="sxs-lookup"><span data-stu-id="b26ac-190">initials</span></span>|<span data-ttu-id="b26ac-191">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-191">String</span></span>|<span data-ttu-id="b26ac-192">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-192">The contact's initials.</span></span>|
|<span data-ttu-id="b26ac-193">jobTitle</span><span class="sxs-lookup"><span data-stu-id="b26ac-193">jobTitle</span></span>|<span data-ttu-id="b26ac-194">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-194">String</span></span>|<span data-ttu-id="b26ac-195">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-195">The contact’s job title.</span></span>|
|<span data-ttu-id="b26ac-196">manager</span><span class="sxs-lookup"><span data-stu-id="b26ac-196">manager</span></span>|<span data-ttu-id="b26ac-197">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-197">String</span></span>|<span data-ttu-id="b26ac-198">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-198">The name of the contact's manager.</span></span>
|<span data-ttu-id="b26ac-199">middleName</span><span class="sxs-lookup"><span data-stu-id="b26ac-199">middleName</span></span>|<span data-ttu-id="b26ac-200">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-200">String</span></span>|<span data-ttu-id="b26ac-201">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-201">The contact's middle name.</span></span>|
|<span data-ttu-id="b26ac-202">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="b26ac-202">mobilePhone</span></span>|<span data-ttu-id="b26ac-203">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-203">String</span></span>|<span data-ttu-id="b26ac-204">El número de teléfono móvil del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-204">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="b26ac-205">nickName</span><span class="sxs-lookup"><span data-stu-id="b26ac-205">nickName</span></span>|<span data-ttu-id="b26ac-206">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-206">String</span></span>|<span data-ttu-id="b26ac-207">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-207">The contact's nickname.</span></span>|
|<span data-ttu-id="b26ac-208">officeLocation</span><span class="sxs-lookup"><span data-stu-id="b26ac-208">officeLocation</span></span>|<span data-ttu-id="b26ac-209">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-209">String</span></span>|<span data-ttu-id="b26ac-210">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-210">The location of the contact's office.</span></span>|
|<span data-ttu-id="b26ac-211">otherAddress</span><span class="sxs-lookup"><span data-stu-id="b26ac-211">otherAddress</span></span>|[<span data-ttu-id="b26ac-212">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="b26ac-212">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="b26ac-213">Otras direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-213">Other addresses for the contact.</span></span>|
|<span data-ttu-id="b26ac-214">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="b26ac-214">parentFolderId</span></span>|<span data-ttu-id="b26ac-215">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-215">String</span></span>|<span data-ttu-id="b26ac-216">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-216">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="b26ac-217">personalNotes</span><span class="sxs-lookup"><span data-stu-id="b26ac-217">personalNotes</span></span>|<span data-ttu-id="b26ac-218">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-218">String</span></span>|<span data-ttu-id="b26ac-219">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-219">The user's notes about the contact.</span></span>|
|<span data-ttu-id="b26ac-220">profession</span><span class="sxs-lookup"><span data-stu-id="b26ac-220">profession</span></span>|<span data-ttu-id="b26ac-221">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-221">String</span></span>|<span data-ttu-id="b26ac-222">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-222">The contact's profession.</span></span>|
|<span data-ttu-id="b26ac-223">spouseName</span><span class="sxs-lookup"><span data-stu-id="b26ac-223">spouseName</span></span>|<span data-ttu-id="b26ac-224">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-224">String</span></span>|<span data-ttu-id="b26ac-225">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-225">The name of the contact's spouse/partner.</span></span>|
|<span data-ttu-id="b26ac-226">surname</span><span class="sxs-lookup"><span data-stu-id="b26ac-226">surname</span></span>|<span data-ttu-id="b26ac-227">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-227">String</span></span>|<span data-ttu-id="b26ac-228">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-228">The contact's surname.</span></span>|
|<span data-ttu-id="b26ac-229">title</span><span class="sxs-lookup"><span data-stu-id="b26ac-229">title</span></span>|<span data-ttu-id="b26ac-230">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-230">String</span></span>|<span data-ttu-id="b26ac-231">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="b26ac-231">The contact's title.</span></span>|
|<span data-ttu-id="b26ac-232">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="b26ac-232">yomiCompanyName</span></span>|<span data-ttu-id="b26ac-233">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-233">String</span></span>|<span data-ttu-id="b26ac-p107">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p107">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="b26ac-236">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="b26ac-236">yomiGivenName</span></span>|<span data-ttu-id="b26ac-237">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-237">String</span></span>|<span data-ttu-id="b26ac-p108">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p108">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="b26ac-240">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="b26ac-240">yomiSurname</span></span>|<span data-ttu-id="b26ac-241">String</span><span class="sxs-lookup"><span data-stu-id="b26ac-241">String</span></span>|<span data-ttu-id="b26ac-p109">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p109">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

## <a name="response"></a><span data-ttu-id="b26ac-244">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b26ac-244">Response</span></span>

<span data-ttu-id="b26ac-245">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [contact](../resources/contact.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b26ac-245">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b26ac-246">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b26ac-246">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b26ac-247">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b26ac-247">Request</span></span>
<span data-ttu-id="b26ac-248">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b26ac-248">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_contact"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/contacts/{id}
Content-type: application/json
Content-length: 1977

{
  "homeAddress": {
    "street": "123 Some street",
    "city": "Seattle",
    "state": "WA",
    "postalCode": "98121"
  },
  "birthday": "1974-07-22"
}
```
##### <a name="response"></a><span data-ttu-id="b26ac-249">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b26ac-249">Response</span></span>
<span data-ttu-id="b26ac-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b26ac-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1977

{
  "id": "AAMkAGI2THk0AAA=",
  "createdDateTime": "2014-10-19T23:08:24Z",
  "lastModifiedDateTime": "2014-10-19T23:08:24Z",
  "changeKey": "EQAAABYAAACd9nJ/tVysQos2hTfspaWRAAADTIa4",
  "categories": [],
  "parentFolderId": "AAMkAGI2AAEOAAA=",
  "birthday": "1974-07-22",
  "fileAs": "Fort, Garth",
  "displayName": "Garth Fort",
  "givenName": "Garth",
  "initials": "G.F.",
  "middleName": null,
  "nickName": "Garth",
  "surname": "Fort",
  "title": null,
  "yomiGivenName": null,
  "yomiSurname": null,
  "yomiCompanyName": null,
  "generation": null,
  "emailAddresses": [
    {
      "name": "Garth",
      "address": "garth@a830edad9050849NDA1.onmicrosoft.com"
    }
  ],
  "imAddresses": [
    "sip:garthf@a830edad9050849nda1.onmicrosoft.com"
  ],
  "jobTitle": "Web Marketing Manager",
  "companyName": "Contoso, Inc.",
  "department": "Sales & Marketing",
  "officeLocation": "20/1101",
  "profession": null,
  "businessHomePage": "https://www.contoso.com",
  "assistantName": null,
  "manager": null,
  "homePhones": [],
  "mobilePhone": null,
  "businessPhones": [
    "+1 918 555 0101"
  ],
  "homeAddress": {
    "street": "123 Some street",
    "city": "Seattle",
    "state": "WA",
    "postalCode": "98121"
  },
  "businessAddress": {
      "street": "10 Contoso Way",
      "city": "Redmond",
      "state": "WA",
      "countryOrRegion": "USA",
      "postalCode": "98075"  
  },
  "otherAddress": {},
  "spouseName": null,
  "personalNotes": null,
  "children": []
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
