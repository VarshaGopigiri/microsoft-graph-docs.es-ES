---
title: Actualizar contacto
description: Actualiza las propiedades de un objeto de contacto.
author: angelgolfer-ms
ms.openlocfilehash: 386f0d3f7673733de805893e16ab049d85d120a6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351236"
---
# <a name="update-contact"></a><span data-ttu-id="fe9f5-103">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="fe9f5-103">Update contact</span></span>

<span data-ttu-id="fe9f5-104">Actualiza las propiedades de un objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-104">Update the properties of a contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="fe9f5-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fe9f5-105">Permissions</span></span>
<span data-ttu-id="fe9f5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fe9f5-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fe9f5-108">Permission type</span></span>      | <span data-ttu-id="fe9f5-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fe9f5-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fe9f5-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fe9f5-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fe9f5-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe9f5-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="fe9f5-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fe9f5-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fe9f5-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe9f5-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="fe9f5-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fe9f5-114">Application</span></span> | <span data-ttu-id="fe9f5-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe9f5-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fe9f5-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fe9f5-116">HTTP request</span></span>
<span data-ttu-id="fe9f5-117"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde predeterminado de un usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="fe9f5-117"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="fe9f5-118">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-118">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="fe9f5-p102">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="fe9f5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fe9f5-121">Request headers</span></span>
| <span data-ttu-id="fe9f5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe9f5-122">Header</span></span>       | <span data-ttu-id="fe9f5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fe9f5-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="fe9f5-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="fe9f5-124">Authorization</span></span>  | <span data-ttu-id="fe9f5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="fe9f5-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fe9f5-127">Content-Type</span></span>  | <span data-ttu-id="fe9f5-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="fe9f5-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fe9f5-130">Request body</span></span>
<span data-ttu-id="fe9f5-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="fe9f5-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe9f5-134">Property</span></span>     | <span data-ttu-id="fe9f5-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe9f5-135">Type</span></span>   |<span data-ttu-id="fe9f5-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe9f5-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fe9f5-137">assistantName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-137">assistantName</span></span>|<span data-ttu-id="fe9f5-138">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-138">String</span></span>|<span data-ttu-id="fe9f5-139">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-139">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="fe9f5-140">birthday</span><span class="sxs-lookup"><span data-stu-id="fe9f5-140">birthday</span></span>|<span data-ttu-id="fe9f5-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fe9f5-141">DateTimeOffset</span></span>|<span data-ttu-id="fe9f5-142">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-142">The contact's birthday.</span></span>|
|<span data-ttu-id="fe9f5-143">businessAddress</span><span class="sxs-lookup"><span data-stu-id="fe9f5-143">businessAddress</span></span>|[<span data-ttu-id="fe9f5-144">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="fe9f5-144">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="fe9f5-145">La dirección del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-145">The contact's business address.</span></span>|
|<span data-ttu-id="fe9f5-146">businessHomePage</span><span class="sxs-lookup"><span data-stu-id="fe9f5-146">businessHomePage</span></span>|<span data-ttu-id="fe9f5-147">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-147">String</span></span>|<span data-ttu-id="fe9f5-148">La página principal de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-148">The business home page of the contact.</span></span>|
|<span data-ttu-id="fe9f5-149">businessPhones</span><span class="sxs-lookup"><span data-stu-id="fe9f5-149">businessPhones</span></span>|<span data-ttu-id="fe9f5-150">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-150">String</span></span>|<span data-ttu-id="fe9f5-151">Los números de teléfono del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-151">The contact's business phone numbers.</span></span>|
|<span data-ttu-id="fe9f5-152">categories</span><span class="sxs-lookup"><span data-stu-id="fe9f5-152">categories</span></span>|<span data-ttu-id="fe9f5-153">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-153">String</span></span>|<span data-ttu-id="fe9f5-154">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-154">The categories associated with the contact.</span></span>|
|<span data-ttu-id="fe9f5-155">children</span><span class="sxs-lookup"><span data-stu-id="fe9f5-155">children</span></span>|<span data-ttu-id="fe9f5-156">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-156">String</span></span>|<span data-ttu-id="fe9f5-157">Los nombres de los hijos del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-157">The names of the contact's children.</span></span>|
|<span data-ttu-id="fe9f5-158">companyName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-158">companyName</span></span>|<span data-ttu-id="fe9f5-159">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-159">String</span></span>|<span data-ttu-id="fe9f5-160">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-160">The name of the contact's company.</span></span>|
|<span data-ttu-id="fe9f5-161">department</span><span class="sxs-lookup"><span data-stu-id="fe9f5-161">department</span></span>|<span data-ttu-id="fe9f5-162">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-162">String</span></span>|<span data-ttu-id="fe9f5-163">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-163">The contact's department.</span></span>|
|<span data-ttu-id="fe9f5-164">displayName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-164">displayName</span></span>|<span data-ttu-id="fe9f5-165">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-165">String</span></span>|<span data-ttu-id="fe9f5-166">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-166">The contact's display name.</span></span> <span data-ttu-id="fe9f5-167">Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-167">Note that later updates to other properties may cause an automatically generated value to overwrite the displayName value you have specified.</span></span> <span data-ttu-id="fe9f5-168">Para conservar un valor existente, siempre incluirla como displayName en una operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-168">To preserve a pre-existing value, always include it as displayName in an update operation.</span></span>|
|<span data-ttu-id="fe9f5-169">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="fe9f5-169">emailAddresses</span></span>|<span data-ttu-id="fe9f5-170">Colección [EmailAddress](../resources/emailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="fe9f5-170">[EmailAddress](../resources/emailaddress.md) collection</span></span>|<span data-ttu-id="fe9f5-171">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-171">The contact's email addresses.</span></span>|
|<span data-ttu-id="fe9f5-172">fileAs</span><span class="sxs-lookup"><span data-stu-id="fe9f5-172">fileAs</span></span>|<span data-ttu-id="fe9f5-173">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-173">String</span></span>|<span data-ttu-id="fe9f5-174">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-174">The name the contact is filed under.</span></span>|
|<span data-ttu-id="fe9f5-175">generation</span><span class="sxs-lookup"><span data-stu-id="fe9f5-175">generation</span></span>|<span data-ttu-id="fe9f5-176">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-176">String</span></span>|<span data-ttu-id="fe9f5-177">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-177">The contact's generation.</span></span>|
|<span data-ttu-id="fe9f5-178">givenName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-178">givenName</span></span>|<span data-ttu-id="fe9f5-179">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-179">String</span></span>|<span data-ttu-id="fe9f5-180">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-180">The contact's given name.</span></span>|
|<span data-ttu-id="fe9f5-181">homeAddress</span><span class="sxs-lookup"><span data-stu-id="fe9f5-181">homeAddress</span></span>|[<span data-ttu-id="fe9f5-182">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="fe9f5-182">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="fe9f5-183">La dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-183">The contact's home address.</span></span>|
|<span data-ttu-id="fe9f5-184">homePhones</span><span class="sxs-lookup"><span data-stu-id="fe9f5-184">homePhones</span></span>|<span data-ttu-id="fe9f5-185">Colección String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-185">String collection</span></span>|<span data-ttu-id="fe9f5-186">Los números de teléfono particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-186">The contact's home phone numbers.</span></span>|
|<span data-ttu-id="fe9f5-187">imAddresses</span><span class="sxs-lookup"><span data-stu-id="fe9f5-187">imAddresses</span></span>|<span data-ttu-id="fe9f5-188">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-188">String</span></span>|<span data-ttu-id="fe9f5-189">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-189">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="fe9f5-190">initials</span><span class="sxs-lookup"><span data-stu-id="fe9f5-190">initials</span></span>|<span data-ttu-id="fe9f5-191">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-191">String</span></span>|<span data-ttu-id="fe9f5-192">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-192">The contact's initials.</span></span>|
|<span data-ttu-id="fe9f5-193">jobTitle</span><span class="sxs-lookup"><span data-stu-id="fe9f5-193">jobTitle</span></span>|<span data-ttu-id="fe9f5-194">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-194">String</span></span>|<span data-ttu-id="fe9f5-195">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-195">The contact’s job title.</span></span>|
|<span data-ttu-id="fe9f5-196">manager</span><span class="sxs-lookup"><span data-stu-id="fe9f5-196">manager</span></span>|<span data-ttu-id="fe9f5-197">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-197">String</span></span>|<span data-ttu-id="fe9f5-198">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-198">The name of the contact's manager.</span></span>
|<span data-ttu-id="fe9f5-199">middleName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-199">middleName</span></span>|<span data-ttu-id="fe9f5-200">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-200">String</span></span>|<span data-ttu-id="fe9f5-201">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-201">The contact's middle name.</span></span>|
|<span data-ttu-id="fe9f5-202">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="fe9f5-202">mobilePhone</span></span>|<span data-ttu-id="fe9f5-203">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-203">String</span></span>|<span data-ttu-id="fe9f5-204">El número de teléfono móvil del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-204">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="fe9f5-205">nickName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-205">nickName</span></span>|<span data-ttu-id="fe9f5-206">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-206">String</span></span>|<span data-ttu-id="fe9f5-207">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-207">The contact's nickname.</span></span>|
|<span data-ttu-id="fe9f5-208">officeLocation</span><span class="sxs-lookup"><span data-stu-id="fe9f5-208">officeLocation</span></span>|<span data-ttu-id="fe9f5-209">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-209">String</span></span>|<span data-ttu-id="fe9f5-210">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-210">The location of the contact's office.</span></span>|
|<span data-ttu-id="fe9f5-211">otherAddress</span><span class="sxs-lookup"><span data-stu-id="fe9f5-211">otherAddress</span></span>|[<span data-ttu-id="fe9f5-212">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="fe9f5-212">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="fe9f5-213">Otras direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-213">Other addresses for the contact.</span></span>|
|<span data-ttu-id="fe9f5-214">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="fe9f5-214">parentFolderId</span></span>|<span data-ttu-id="fe9f5-215">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-215">String</span></span>|<span data-ttu-id="fe9f5-216">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-216">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="fe9f5-217">personalNotes</span><span class="sxs-lookup"><span data-stu-id="fe9f5-217">personalNotes</span></span>|<span data-ttu-id="fe9f5-218">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-218">String</span></span>|<span data-ttu-id="fe9f5-219">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-219">The user's notes about the contact.</span></span>|
|<span data-ttu-id="fe9f5-220">profession</span><span class="sxs-lookup"><span data-stu-id="fe9f5-220">profession</span></span>|<span data-ttu-id="fe9f5-221">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-221">String</span></span>|<span data-ttu-id="fe9f5-222">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-222">The contact's profession.</span></span>|
|<span data-ttu-id="fe9f5-223">spouseName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-223">spouseName</span></span>|<span data-ttu-id="fe9f5-224">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-224">String</span></span>|<span data-ttu-id="fe9f5-225">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-225">The name of the contact's spouse/partner.</span></span>|
|<span data-ttu-id="fe9f5-226">surname</span><span class="sxs-lookup"><span data-stu-id="fe9f5-226">surname</span></span>|<span data-ttu-id="fe9f5-227">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-227">String</span></span>|<span data-ttu-id="fe9f5-228">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-228">The contact's surname.</span></span>|
|<span data-ttu-id="fe9f5-229">title</span><span class="sxs-lookup"><span data-stu-id="fe9f5-229">title</span></span>|<span data-ttu-id="fe9f5-230">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-230">String</span></span>|<span data-ttu-id="fe9f5-231">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-231">The contact's title.</span></span>|
|<span data-ttu-id="fe9f5-232">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-232">yomiCompanyName</span></span>|<span data-ttu-id="fe9f5-233">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-233">String</span></span>|<span data-ttu-id="fe9f5-p107">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p107">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="fe9f5-236">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="fe9f5-236">yomiGivenName</span></span>|<span data-ttu-id="fe9f5-237">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-237">String</span></span>|<span data-ttu-id="fe9f5-p108">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p108">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="fe9f5-240">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="fe9f5-240">yomiSurname</span></span>|<span data-ttu-id="fe9f5-241">String</span><span class="sxs-lookup"><span data-stu-id="fe9f5-241">String</span></span>|<span data-ttu-id="fe9f5-p109">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p109">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

## <a name="response"></a><span data-ttu-id="fe9f5-244">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe9f5-244">Response</span></span>

<span data-ttu-id="fe9f5-245">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [contact](../resources/contact.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-245">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fe9f5-246">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe9f5-246">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fe9f5-247">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe9f5-247">Request</span></span>
<span data-ttu-id="fe9f5-248">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-248">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="fe9f5-249">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe9f5-249">Response</span></span>
<span data-ttu-id="fe9f5-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fe9f5-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
