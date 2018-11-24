# <a name="update-contact"></a><span data-ttu-id="c1670-101">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="c1670-101">Update contact</span></span>

<span data-ttu-id="c1670-102">Actualiza las propiedades de un objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-102">Update the properties of a contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c1670-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c1670-103">Permissions</span></span>
<span data-ttu-id="c1670-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c1670-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c1670-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c1670-106">Permission type</span></span>      | <span data-ttu-id="c1670-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c1670-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c1670-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c1670-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c1670-109">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c1670-109">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="c1670-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c1670-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c1670-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c1670-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="c1670-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c1670-112">Application</span></span> | <span data-ttu-id="c1670-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c1670-113">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c1670-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c1670-114">HTTP request</span></span>
<span data-ttu-id="c1670-115"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde predeterminado de un usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="c1670-115"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="c1670-116">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c1670-116">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="c1670-p102">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="c1670-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c1670-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c1670-119">Request headers</span></span>
| <span data-ttu-id="c1670-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1670-120">Header</span></span>       | <span data-ttu-id="c1670-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c1670-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c1670-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c1670-122">Authorization</span></span>  | <span data-ttu-id="c1670-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1670-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c1670-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c1670-125">Content-Type</span></span>  | <span data-ttu-id="c1670-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1670-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c1670-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c1670-128">Request body</span></span>
<span data-ttu-id="c1670-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c1670-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c1670-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c1670-132">Property</span></span>     | <span data-ttu-id="c1670-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1670-133">Type</span></span>   |<span data-ttu-id="c1670-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1670-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c1670-135">assistantName</span><span class="sxs-lookup"><span data-stu-id="c1670-135">assistantName</span></span>|<span data-ttu-id="c1670-136">String</span><span class="sxs-lookup"><span data-stu-id="c1670-136">String</span></span>|<span data-ttu-id="c1670-137">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-137">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="c1670-138">birthday</span><span class="sxs-lookup"><span data-stu-id="c1670-138">birthday</span></span>|<span data-ttu-id="c1670-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c1670-139">DateTimeOffset</span></span>|<span data-ttu-id="c1670-140">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-140">The contact's birthday.</span></span>|
|<span data-ttu-id="c1670-141">businessAddress</span><span class="sxs-lookup"><span data-stu-id="c1670-141">businessAddress</span></span>|[<span data-ttu-id="c1670-142">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="c1670-142">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="c1670-143">La dirección del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-143">The contact's business address.</span></span>|
|<span data-ttu-id="c1670-144">businessHomePage</span><span class="sxs-lookup"><span data-stu-id="c1670-144">businessHomePage</span></span>|<span data-ttu-id="c1670-145">String</span><span class="sxs-lookup"><span data-stu-id="c1670-145">String</span></span>|<span data-ttu-id="c1670-146">La página principal de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-146">The business home page of the contact.</span></span>|
|<span data-ttu-id="c1670-147">businessPhones</span><span class="sxs-lookup"><span data-stu-id="c1670-147">businessPhones</span></span>|<span data-ttu-id="c1670-148">String</span><span class="sxs-lookup"><span data-stu-id="c1670-148">String</span></span>|<span data-ttu-id="c1670-149">Los números de teléfono del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-149">The contact's business phone numbers.</span></span>|
|<span data-ttu-id="c1670-150">categories</span><span class="sxs-lookup"><span data-stu-id="c1670-150">categories</span></span>|<span data-ttu-id="c1670-151">String</span><span class="sxs-lookup"><span data-stu-id="c1670-151">String</span></span>|<span data-ttu-id="c1670-152">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-152">The categories associated with the contact.</span></span>|
|<span data-ttu-id="c1670-153">children</span><span class="sxs-lookup"><span data-stu-id="c1670-153">children</span></span>|<span data-ttu-id="c1670-154">String</span><span class="sxs-lookup"><span data-stu-id="c1670-154">String</span></span>|<span data-ttu-id="c1670-155">Los nombres de los hijos del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-155">The names of the contact's children.</span></span>|
|<span data-ttu-id="c1670-156">companyName</span><span class="sxs-lookup"><span data-stu-id="c1670-156">companyName</span></span>|<span data-ttu-id="c1670-157">String</span><span class="sxs-lookup"><span data-stu-id="c1670-157">String</span></span>|<span data-ttu-id="c1670-158">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-158">The name of the contact's company.</span></span>|
|<span data-ttu-id="c1670-159">department</span><span class="sxs-lookup"><span data-stu-id="c1670-159">department</span></span>|<span data-ttu-id="c1670-160">String</span><span class="sxs-lookup"><span data-stu-id="c1670-160">String</span></span>|<span data-ttu-id="c1670-161">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-161">The contact's department.</span></span>|
|<span data-ttu-id="c1670-162">displayName</span><span class="sxs-lookup"><span data-stu-id="c1670-162">displayName</span></span>|<span data-ttu-id="c1670-163">String</span><span class="sxs-lookup"><span data-stu-id="c1670-163">String</span></span>|<span data-ttu-id="c1670-164">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-164">The contact's display name.</span></span> <span data-ttu-id="c1670-165">Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado.</span><span class="sxs-lookup"><span data-stu-id="c1670-165">Note that later updates to other properties may cause an automatically generated value to overwrite the displayName value you have specified.</span></span> <span data-ttu-id="c1670-166">Para conservar un valor existente, siempre incluirla como displayName en una operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="c1670-166">To preserve a pre-existing value, always include it as displayName in an update operation.</span></span>|
|<span data-ttu-id="c1670-167">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="c1670-167">emailAddresses</span></span>|<span data-ttu-id="c1670-168">Colección [EmailAddress](../resources/emailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="c1670-168">[EmailAddress](../resources/emailaddress.md) collection</span></span>|<span data-ttu-id="c1670-169">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-169">The contact's email addresses.</span></span>|
|<span data-ttu-id="c1670-170">fileAs</span><span class="sxs-lookup"><span data-stu-id="c1670-170">fileAs</span></span>|<span data-ttu-id="c1670-171">String</span><span class="sxs-lookup"><span data-stu-id="c1670-171">String</span></span>|<span data-ttu-id="c1670-172">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-172">The name the contact is filed under.</span></span>|
|<span data-ttu-id="c1670-173">generation</span><span class="sxs-lookup"><span data-stu-id="c1670-173">generation</span></span>|<span data-ttu-id="c1670-174">String</span><span class="sxs-lookup"><span data-stu-id="c1670-174">String</span></span>|<span data-ttu-id="c1670-175">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-175">The contact's generation.</span></span>|
|<span data-ttu-id="c1670-176">givenName</span><span class="sxs-lookup"><span data-stu-id="c1670-176">givenName</span></span>|<span data-ttu-id="c1670-177">String</span><span class="sxs-lookup"><span data-stu-id="c1670-177">String</span></span>|<span data-ttu-id="c1670-178">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-178">The contact's given name.</span></span>|
|<span data-ttu-id="c1670-179">homeAddress</span><span class="sxs-lookup"><span data-stu-id="c1670-179">homeAddress</span></span>|[<span data-ttu-id="c1670-180">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="c1670-180">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="c1670-181">La dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-181">The contact's home address.</span></span>|
|<span data-ttu-id="c1670-182">homePhones</span><span class="sxs-lookup"><span data-stu-id="c1670-182">homePhones</span></span>|<span data-ttu-id="c1670-183">Colección String</span><span class="sxs-lookup"><span data-stu-id="c1670-183">String collection</span></span>|<span data-ttu-id="c1670-184">Los números de teléfono particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-184">The contact's home phone numbers.</span></span>|
|<span data-ttu-id="c1670-185">imAddresses</span><span class="sxs-lookup"><span data-stu-id="c1670-185">imAddresses</span></span>|<span data-ttu-id="c1670-186">String</span><span class="sxs-lookup"><span data-stu-id="c1670-186">String</span></span>|<span data-ttu-id="c1670-187">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-187">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="c1670-188">initials</span><span class="sxs-lookup"><span data-stu-id="c1670-188">initials</span></span>|<span data-ttu-id="c1670-189">String</span><span class="sxs-lookup"><span data-stu-id="c1670-189">String</span></span>|<span data-ttu-id="c1670-190">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-190">The contact's initials.</span></span>|
|<span data-ttu-id="c1670-191">jobTitle</span><span class="sxs-lookup"><span data-stu-id="c1670-191">jobTitle</span></span>|<span data-ttu-id="c1670-192">String</span><span class="sxs-lookup"><span data-stu-id="c1670-192">String</span></span>|<span data-ttu-id="c1670-193">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-193">The contact’s job title.</span></span>|
|<span data-ttu-id="c1670-194">manager</span><span class="sxs-lookup"><span data-stu-id="c1670-194">manager</span></span>|<span data-ttu-id="c1670-195">String</span><span class="sxs-lookup"><span data-stu-id="c1670-195">String</span></span>|<span data-ttu-id="c1670-196">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-196">The name of the contact's manager.</span></span>
|<span data-ttu-id="c1670-197">middleName</span><span class="sxs-lookup"><span data-stu-id="c1670-197">middleName</span></span>|<span data-ttu-id="c1670-198">String</span><span class="sxs-lookup"><span data-stu-id="c1670-198">String</span></span>|<span data-ttu-id="c1670-199">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-199">The contact's middle name.</span></span>|
|<span data-ttu-id="c1670-200">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="c1670-200">mobilePhone</span></span>|<span data-ttu-id="c1670-201">String</span><span class="sxs-lookup"><span data-stu-id="c1670-201">String</span></span>|<span data-ttu-id="c1670-202">El número de teléfono móvil del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-202">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="c1670-203">nickName</span><span class="sxs-lookup"><span data-stu-id="c1670-203">nickName</span></span>|<span data-ttu-id="c1670-204">String</span><span class="sxs-lookup"><span data-stu-id="c1670-204">String</span></span>|<span data-ttu-id="c1670-205">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-205">The contact's nickname.</span></span>|
|<span data-ttu-id="c1670-206">officeLocation</span><span class="sxs-lookup"><span data-stu-id="c1670-206">officeLocation</span></span>|<span data-ttu-id="c1670-207">String</span><span class="sxs-lookup"><span data-stu-id="c1670-207">String</span></span>|<span data-ttu-id="c1670-208">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-208">The location of the contact's office.</span></span>|
|<span data-ttu-id="c1670-209">otherAddress</span><span class="sxs-lookup"><span data-stu-id="c1670-209">otherAddress</span></span>|[<span data-ttu-id="c1670-210">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="c1670-210">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="c1670-211">Otras direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-211">Other addresses for the contact.</span></span>|
|<span data-ttu-id="c1670-212">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="c1670-212">parentFolderId</span></span>|<span data-ttu-id="c1670-213">String</span><span class="sxs-lookup"><span data-stu-id="c1670-213">String</span></span>|<span data-ttu-id="c1670-214">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-214">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="c1670-215">personalNotes</span><span class="sxs-lookup"><span data-stu-id="c1670-215">personalNotes</span></span>|<span data-ttu-id="c1670-216">String</span><span class="sxs-lookup"><span data-stu-id="c1670-216">String</span></span>|<span data-ttu-id="c1670-217">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-217">The user's notes about the contact.</span></span>|
|<span data-ttu-id="c1670-218">profession</span><span class="sxs-lookup"><span data-stu-id="c1670-218">profession</span></span>|<span data-ttu-id="c1670-219">String</span><span class="sxs-lookup"><span data-stu-id="c1670-219">String</span></span>|<span data-ttu-id="c1670-220">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-220">The contact's profession.</span></span>|
|<span data-ttu-id="c1670-221">spouseName</span><span class="sxs-lookup"><span data-stu-id="c1670-221">spouseName</span></span>|<span data-ttu-id="c1670-222">String</span><span class="sxs-lookup"><span data-stu-id="c1670-222">String</span></span>|<span data-ttu-id="c1670-223">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-223">The name of the contact's spouse/partner.</span></span>|
|<span data-ttu-id="c1670-224">surname</span><span class="sxs-lookup"><span data-stu-id="c1670-224">surname</span></span>|<span data-ttu-id="c1670-225">String</span><span class="sxs-lookup"><span data-stu-id="c1670-225">String</span></span>|<span data-ttu-id="c1670-226">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-226">The contact's surname.</span></span>|
|<span data-ttu-id="c1670-227">title</span><span class="sxs-lookup"><span data-stu-id="c1670-227">title</span></span>|<span data-ttu-id="c1670-228">String</span><span class="sxs-lookup"><span data-stu-id="c1670-228">String</span></span>|<span data-ttu-id="c1670-229">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="c1670-229">The contact's title.</span></span>|
|<span data-ttu-id="c1670-230">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="c1670-230">yomiCompanyName</span></span>|<span data-ttu-id="c1670-231">String</span><span class="sxs-lookup"><span data-stu-id="c1670-231">String</span></span>|<span data-ttu-id="c1670-p107">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1670-p107">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="c1670-234">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="c1670-234">yomiGivenName</span></span>|<span data-ttu-id="c1670-235">String</span><span class="sxs-lookup"><span data-stu-id="c1670-235">String</span></span>|<span data-ttu-id="c1670-p108">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1670-p108">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="c1670-238">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="c1670-238">yomiSurname</span></span>|<span data-ttu-id="c1670-239">String</span><span class="sxs-lookup"><span data-stu-id="c1670-239">String</span></span>|<span data-ttu-id="c1670-p109">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1670-p109">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

## <a name="response"></a><span data-ttu-id="c1670-242">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1670-242">Response</span></span>

<span data-ttu-id="c1670-243">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [contact](../resources/contact.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1670-243">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c1670-244">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c1670-244">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c1670-245">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c1670-245">Request</span></span>
<span data-ttu-id="c1670-246">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c1670-246">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="c1670-247">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1670-247">Response</span></span>
<span data-ttu-id="c1670-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c1670-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
