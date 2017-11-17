# <a name="update-contact"></a><span data-ttu-id="8a384-101">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="8a384-101">Update contact</span></span>

<span data-ttu-id="8a384-102">Actualiza las propiedades de un objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-102">Update the properties of a contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8a384-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8a384-103">Permissions</span></span>
<span data-ttu-id="8a384-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8a384-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8a384-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a384-106">Permission type</span></span>      | <span data-ttu-id="8a384-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a384-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8a384-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a384-108">Delegated (work or school account)</span></span> | <span data-ttu-id="8a384-109">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a384-109">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="8a384-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a384-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8a384-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a384-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="8a384-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a384-112">Application</span></span> | <span data-ttu-id="8a384-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a384-113">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="8a384-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a384-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="8a384-115">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8a384-115">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="8a384-116">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8a384-116">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="8a384-p102">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="8a384-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="8a384-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a384-119">Request headers</span></span>
| <span data-ttu-id="8a384-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a384-120">Header</span></span>       | <span data-ttu-id="8a384-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8a384-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8a384-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a384-122">Authorization</span></span>  | <span data-ttu-id="8a384-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a384-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8a384-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8a384-125">Content-Type</span></span>  | <span data-ttu-id="8a384-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a384-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8a384-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a384-128">Request body</span></span>
<span data-ttu-id="8a384-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8a384-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8a384-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a384-132">Property</span></span>     | <span data-ttu-id="8a384-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a384-133">Type</span></span>   |<span data-ttu-id="8a384-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a384-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8a384-135">assistantName</span><span class="sxs-lookup"><span data-stu-id="8a384-135">assistantName</span></span>|<span data-ttu-id="8a384-136">String</span><span class="sxs-lookup"><span data-stu-id="8a384-136">String</span></span>|<span data-ttu-id="8a384-137">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-137">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="8a384-138">birthday</span><span class="sxs-lookup"><span data-stu-id="8a384-138">birthday</span></span>|<span data-ttu-id="8a384-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a384-139">DateTimeOffset</span></span>|<span data-ttu-id="8a384-140">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-140">The contact's birthday.</span></span>|
|<span data-ttu-id="8a384-141">businessAddress</span><span class="sxs-lookup"><span data-stu-id="8a384-141">businessAddress</span></span>|[<span data-ttu-id="8a384-142">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="8a384-142">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="8a384-143">La dirección del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-143">The contact's business address.</span></span>|
|<span data-ttu-id="8a384-144">businessHomePage</span><span class="sxs-lookup"><span data-stu-id="8a384-144">businessHomePage</span></span>|<span data-ttu-id="8a384-145">String</span><span class="sxs-lookup"><span data-stu-id="8a384-145">String</span></span>|<span data-ttu-id="8a384-146">La página principal de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-146">The business home page of the contact.</span></span>|
|<span data-ttu-id="8a384-147">businessPhones</span><span class="sxs-lookup"><span data-stu-id="8a384-147">businessPhones</span></span>|<span data-ttu-id="8a384-148">String</span><span class="sxs-lookup"><span data-stu-id="8a384-148">String</span></span>|<span data-ttu-id="8a384-149">Los números de teléfono del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-149">The contact's business phone numbers.</span></span>|
|<span data-ttu-id="8a384-150">categories</span><span class="sxs-lookup"><span data-stu-id="8a384-150">categories</span></span>|<span data-ttu-id="8a384-151">String</span><span class="sxs-lookup"><span data-stu-id="8a384-151">String</span></span>|<span data-ttu-id="8a384-152">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-152">The categories associated with the contact.</span></span>|
|<span data-ttu-id="8a384-153">children</span><span class="sxs-lookup"><span data-stu-id="8a384-153">children</span></span>|<span data-ttu-id="8a384-154">String</span><span class="sxs-lookup"><span data-stu-id="8a384-154">String</span></span>|<span data-ttu-id="8a384-155">Los nombres de los hijos del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-155">The names of the contact's children.</span></span>|
|<span data-ttu-id="8a384-156">companyName</span><span class="sxs-lookup"><span data-stu-id="8a384-156">companyName</span></span>|<span data-ttu-id="8a384-157">String</span><span class="sxs-lookup"><span data-stu-id="8a384-157">String</span></span>|<span data-ttu-id="8a384-158">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-158">The name of the contact's company.</span></span>|
|<span data-ttu-id="8a384-159">department</span><span class="sxs-lookup"><span data-stu-id="8a384-159">department</span></span>|<span data-ttu-id="8a384-160">String</span><span class="sxs-lookup"><span data-stu-id="8a384-160">String</span></span>|<span data-ttu-id="8a384-161">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-161">The contact's department.</span></span>|
|<span data-ttu-id="8a384-162">displayName</span><span class="sxs-lookup"><span data-stu-id="8a384-162">displayName</span></span>|<span data-ttu-id="8a384-163">String</span><span class="sxs-lookup"><span data-stu-id="8a384-163">String</span></span>|<span data-ttu-id="8a384-164">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-164">The contact's display name.</span></span>|
|<span data-ttu-id="8a384-165">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="8a384-165">emailAddresses</span></span>|<span data-ttu-id="8a384-166">Colección [EmailAddress](../resources/emailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="8a384-166">[EmailAddress](../resources/emailaddress.md) collection</span></span>|<span data-ttu-id="8a384-167">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-167">The contact's email addresses.</span></span>|
|<span data-ttu-id="8a384-168">fileAs</span><span class="sxs-lookup"><span data-stu-id="8a384-168">fileAs</span></span>|<span data-ttu-id="8a384-169">String</span><span class="sxs-lookup"><span data-stu-id="8a384-169">String</span></span>|<span data-ttu-id="8a384-170">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-170">The name the contact is filed under.</span></span>|
|<span data-ttu-id="8a384-171">generation</span><span class="sxs-lookup"><span data-stu-id="8a384-171">generation</span></span>|<span data-ttu-id="8a384-172">String</span><span class="sxs-lookup"><span data-stu-id="8a384-172">String</span></span>|<span data-ttu-id="8a384-173">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-173">The contact's generation.</span></span>|
|<span data-ttu-id="8a384-174">givenName</span><span class="sxs-lookup"><span data-stu-id="8a384-174">givenName</span></span>|<span data-ttu-id="8a384-175">String</span><span class="sxs-lookup"><span data-stu-id="8a384-175">String</span></span>|<span data-ttu-id="8a384-176">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-176">The contact's given name.</span></span>|
|<span data-ttu-id="8a384-177">homeAddress</span><span class="sxs-lookup"><span data-stu-id="8a384-177">homeAddress</span></span>|[<span data-ttu-id="8a384-178">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="8a384-178">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="8a384-179">La dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-179">The contact's home address.</span></span>|
|<span data-ttu-id="8a384-180">homePhones</span><span class="sxs-lookup"><span data-stu-id="8a384-180">homePhones</span></span>|<span data-ttu-id="8a384-181">Colección String</span><span class="sxs-lookup"><span data-stu-id="8a384-181">String collection</span></span>|<span data-ttu-id="8a384-182">Los números de teléfono particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-182">The contact's home phone numbers.</span></span>|
|<span data-ttu-id="8a384-183">imAddresses</span><span class="sxs-lookup"><span data-stu-id="8a384-183">imAddresses</span></span>|<span data-ttu-id="8a384-184">String</span><span class="sxs-lookup"><span data-stu-id="8a384-184">String</span></span>|<span data-ttu-id="8a384-185">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-185">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="8a384-186">initials</span><span class="sxs-lookup"><span data-stu-id="8a384-186">initials</span></span>|<span data-ttu-id="8a384-187">String</span><span class="sxs-lookup"><span data-stu-id="8a384-187">String</span></span>|<span data-ttu-id="8a384-188">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-188">The contact's initials.</span></span>|
|<span data-ttu-id="8a384-189">jobTitle</span><span class="sxs-lookup"><span data-stu-id="8a384-189">jobTitle</span></span>|<span data-ttu-id="8a384-190">String</span><span class="sxs-lookup"><span data-stu-id="8a384-190">String</span></span>|<span data-ttu-id="8a384-191">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-191">The contact’s job title.</span></span>|
|<span data-ttu-id="8a384-192">manager</span><span class="sxs-lookup"><span data-stu-id="8a384-192">manager</span></span>|<span data-ttu-id="8a384-193">String</span><span class="sxs-lookup"><span data-stu-id="8a384-193">String</span></span>|<span data-ttu-id="8a384-194">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-194">The name of the contact's manager.</span></span>
|<span data-ttu-id="8a384-195">middleName</span><span class="sxs-lookup"><span data-stu-id="8a384-195">middleName</span></span>|<span data-ttu-id="8a384-196">String</span><span class="sxs-lookup"><span data-stu-id="8a384-196">String</span></span>|<span data-ttu-id="8a384-197">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-197">The contact's middle name.</span></span>|
|<span data-ttu-id="8a384-198">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="8a384-198">mobilePhone</span></span>|<span data-ttu-id="8a384-199">String</span><span class="sxs-lookup"><span data-stu-id="8a384-199">String</span></span>|<span data-ttu-id="8a384-200">El número de teléfono móvil del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-200">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="8a384-201">nickName</span><span class="sxs-lookup"><span data-stu-id="8a384-201">nickName</span></span>|<span data-ttu-id="8a384-202">String</span><span class="sxs-lookup"><span data-stu-id="8a384-202">String</span></span>|<span data-ttu-id="8a384-203">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-203">The contact's nickname.</span></span>|
|<span data-ttu-id="8a384-204">officeLocation</span><span class="sxs-lookup"><span data-stu-id="8a384-204">officeLocation</span></span>|<span data-ttu-id="8a384-205">String</span><span class="sxs-lookup"><span data-stu-id="8a384-205">String</span></span>|<span data-ttu-id="8a384-206">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-206">The location of the contact's office.</span></span>|
|<span data-ttu-id="8a384-207">otherAddress</span><span class="sxs-lookup"><span data-stu-id="8a384-207">otherAddress</span></span>|[<span data-ttu-id="8a384-208">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="8a384-208">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="8a384-209">Otras direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-209">Other addresses for the contact.</span></span>|
|<span data-ttu-id="8a384-210">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="8a384-210">parentFolderId</span></span>|<span data-ttu-id="8a384-211">String</span><span class="sxs-lookup"><span data-stu-id="8a384-211">String</span></span>|<span data-ttu-id="8a384-212">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-212">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="8a384-213">personalNotes</span><span class="sxs-lookup"><span data-stu-id="8a384-213">personalNotes</span></span>|<span data-ttu-id="8a384-214">String</span><span class="sxs-lookup"><span data-stu-id="8a384-214">String</span></span>|<span data-ttu-id="8a384-215">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-215">The user's notes about the contact.</span></span>|
|<span data-ttu-id="8a384-216">profession</span><span class="sxs-lookup"><span data-stu-id="8a384-216">profession</span></span>|<span data-ttu-id="8a384-217">String</span><span class="sxs-lookup"><span data-stu-id="8a384-217">String</span></span>|<span data-ttu-id="8a384-218">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-218">The contact's profession.</span></span>|
|<span data-ttu-id="8a384-219">spouseName</span><span class="sxs-lookup"><span data-stu-id="8a384-219">spouseName</span></span>|<span data-ttu-id="8a384-220">String</span><span class="sxs-lookup"><span data-stu-id="8a384-220">String</span></span>|<span data-ttu-id="8a384-221">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-221">The name of the contact's spouse.</span></span>|
|<span data-ttu-id="8a384-222">surname</span><span class="sxs-lookup"><span data-stu-id="8a384-222">surname</span></span>|<span data-ttu-id="8a384-223">String</span><span class="sxs-lookup"><span data-stu-id="8a384-223">String</span></span>|<span data-ttu-id="8a384-224">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-224">The contact's surname.</span></span>|
|<span data-ttu-id="8a384-225">title</span><span class="sxs-lookup"><span data-stu-id="8a384-225">title</span></span>|<span data-ttu-id="8a384-226">String</span><span class="sxs-lookup"><span data-stu-id="8a384-226">String</span></span>|<span data-ttu-id="8a384-227">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="8a384-227">The contact's title.</span></span>|
|<span data-ttu-id="8a384-228">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="8a384-228">yomiCompanyName</span></span>|<span data-ttu-id="8a384-229">String</span><span class="sxs-lookup"><span data-stu-id="8a384-229">String</span></span>|<span data-ttu-id="8a384-p106">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="8a384-p106">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="8a384-232">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="8a384-232">yomiGivenName</span></span>|<span data-ttu-id="8a384-233">String</span><span class="sxs-lookup"><span data-stu-id="8a384-233">String</span></span>|<span data-ttu-id="8a384-p107">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="8a384-p107">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="8a384-236">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="8a384-236">yomiSurname</span></span>|<span data-ttu-id="8a384-237">String</span><span class="sxs-lookup"><span data-stu-id="8a384-237">String</span></span>|<span data-ttu-id="8a384-p108">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="8a384-p108">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

## <a name="response"></a><span data-ttu-id="8a384-240">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a384-240">Response</span></span>

<span data-ttu-id="8a384-241">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [contact](../resources/contact.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a384-241">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8a384-242">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a384-242">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8a384-243">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a384-243">Request</span></span>
<span data-ttu-id="8a384-244">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a384-244">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="8a384-245">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a384-245">Response</span></span>
<span data-ttu-id="8a384-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a384-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "businessHomePage": "http://www.contoso.com",
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
