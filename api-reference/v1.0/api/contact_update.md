# <a name="update-contact"></a><span data-ttu-id="965ba-101">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="965ba-101">Update contact</span></span>

<span data-ttu-id="965ba-102">Actualiza las propiedades de un objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-102">Update the properties of a contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="965ba-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="965ba-103">Permissions</span></span>
<span data-ttu-id="965ba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="965ba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="965ba-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="965ba-106">Permission type</span></span>      | <span data-ttu-id="965ba-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="965ba-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="965ba-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="965ba-108">Delegated (work or school account)</span></span> | <span data-ttu-id="965ba-109">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="965ba-109">Contacts.ReadWrite</span></span>    | 
|<span data-ttu-id="965ba-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="965ba-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="965ba-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="965ba-111">Contacts.ReadWrite</span></span>    | 
|<span data-ttu-id="965ba-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="965ba-112">Application</span></span> | <span data-ttu-id="965ba-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="965ba-113">Contacts.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="965ba-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="965ba-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="965ba-115">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="965ba-115">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="965ba-116">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="965ba-116">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="965ba-p102">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="965ba-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="965ba-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="965ba-119">Request headers</span></span>
| <span data-ttu-id="965ba-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="965ba-120">Header</span></span>       | <span data-ttu-id="965ba-121">Valor</span><span class="sxs-lookup"><span data-stu-id="965ba-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="965ba-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="965ba-122">Authorization</span></span>  | <span data-ttu-id="965ba-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="965ba-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="965ba-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="965ba-125">Content-Type</span></span>  | <span data-ttu-id="965ba-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="965ba-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="965ba-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="965ba-128">Request body</span></span>
<span data-ttu-id="965ba-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="965ba-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="965ba-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="965ba-132">Property</span></span>     | <span data-ttu-id="965ba-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="965ba-133">Type</span></span>   |<span data-ttu-id="965ba-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="965ba-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="965ba-135">assistantName</span><span class="sxs-lookup"><span data-stu-id="965ba-135">assistantName</span></span>|<span data-ttu-id="965ba-136">String</span><span class="sxs-lookup"><span data-stu-id="965ba-136">String</span></span>|<span data-ttu-id="965ba-137">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-137">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="965ba-138">birthday</span><span class="sxs-lookup"><span data-stu-id="965ba-138">birthday</span></span>|<span data-ttu-id="965ba-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="965ba-139">DateTimeOffset</span></span>|<span data-ttu-id="965ba-140">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-140">The contact's birthday.</span></span>|
|<span data-ttu-id="965ba-141">businessAddress</span><span class="sxs-lookup"><span data-stu-id="965ba-141">businessAddress</span></span>|[<span data-ttu-id="965ba-142">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="965ba-142">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="965ba-143">La dirección del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-143">The contact's business address.</span></span>|
|<span data-ttu-id="965ba-144">businessHomePage</span><span class="sxs-lookup"><span data-stu-id="965ba-144">businessHomePage</span></span>|<span data-ttu-id="965ba-145">String</span><span class="sxs-lookup"><span data-stu-id="965ba-145">String</span></span>|<span data-ttu-id="965ba-146">La página principal de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-146">The business home page of the contact.</span></span>|
|<span data-ttu-id="965ba-147">businessPhones</span><span class="sxs-lookup"><span data-stu-id="965ba-147">businessPhones</span></span>|<span data-ttu-id="965ba-148">String</span><span class="sxs-lookup"><span data-stu-id="965ba-148">String</span></span>|<span data-ttu-id="965ba-149">Los números de teléfono del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-149">The contact's business phone numbers.</span></span>|
|<span data-ttu-id="965ba-150">categories</span><span class="sxs-lookup"><span data-stu-id="965ba-150">categories</span></span>|<span data-ttu-id="965ba-151">String</span><span class="sxs-lookup"><span data-stu-id="965ba-151">String</span></span>|<span data-ttu-id="965ba-152">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-152">The categories associated with the contact.</span></span>|
|<span data-ttu-id="965ba-153">children</span><span class="sxs-lookup"><span data-stu-id="965ba-153">children</span></span>|<span data-ttu-id="965ba-154">String</span><span class="sxs-lookup"><span data-stu-id="965ba-154">String</span></span>|<span data-ttu-id="965ba-155">Los nombres de los hijos del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-155">The names of the contact's children.</span></span>|
|<span data-ttu-id="965ba-156">companyName</span><span class="sxs-lookup"><span data-stu-id="965ba-156">companyName</span></span>|<span data-ttu-id="965ba-157">String</span><span class="sxs-lookup"><span data-stu-id="965ba-157">String</span></span>|<span data-ttu-id="965ba-158">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-158">The name of the contact's company.</span></span>|
|<span data-ttu-id="965ba-159">department</span><span class="sxs-lookup"><span data-stu-id="965ba-159">department</span></span>|<span data-ttu-id="965ba-160">String</span><span class="sxs-lookup"><span data-stu-id="965ba-160">String</span></span>|<span data-ttu-id="965ba-161">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-161">The contact's department.</span></span>|
|<span data-ttu-id="965ba-162">displayName</span><span class="sxs-lookup"><span data-stu-id="965ba-162">displayName</span></span>|<span data-ttu-id="965ba-163">String</span><span class="sxs-lookup"><span data-stu-id="965ba-163">String</span></span>|<span data-ttu-id="965ba-164">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-164">The contact's display name.</span></span>|
|<span data-ttu-id="965ba-165">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="965ba-165">emailAddresses</span></span>|<span data-ttu-id="965ba-166">Colección [EmailAddress](../resources/emailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="965ba-166">[EmailAddress](../resources/emailaddress.md) collection</span></span>|<span data-ttu-id="965ba-167">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-167">The contact's email addresses.</span></span>|
|<span data-ttu-id="965ba-168">fileAs</span><span class="sxs-lookup"><span data-stu-id="965ba-168">fileAs</span></span>|<span data-ttu-id="965ba-169">String</span><span class="sxs-lookup"><span data-stu-id="965ba-169">String</span></span>|<span data-ttu-id="965ba-170">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-170">The name the contact is filed under.</span></span>|
|<span data-ttu-id="965ba-171">generation</span><span class="sxs-lookup"><span data-stu-id="965ba-171">generation</span></span>|<span data-ttu-id="965ba-172">String</span><span class="sxs-lookup"><span data-stu-id="965ba-172">String</span></span>|<span data-ttu-id="965ba-173">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-173">The contact's generation.</span></span>|
|<span data-ttu-id="965ba-174">givenName</span><span class="sxs-lookup"><span data-stu-id="965ba-174">givenName</span></span>|<span data-ttu-id="965ba-175">String</span><span class="sxs-lookup"><span data-stu-id="965ba-175">String</span></span>|<span data-ttu-id="965ba-176">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-176">The contact's given name.</span></span>|
|<span data-ttu-id="965ba-177">homeAddress</span><span class="sxs-lookup"><span data-stu-id="965ba-177">homeAddress</span></span>|[<span data-ttu-id="965ba-178">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="965ba-178">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="965ba-179">La dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-179">The contact's home address.</span></span>|
|<span data-ttu-id="965ba-180">homePhones</span><span class="sxs-lookup"><span data-stu-id="965ba-180">homePhones</span></span>|<span data-ttu-id="965ba-181">Colección String</span><span class="sxs-lookup"><span data-stu-id="965ba-181">String collection</span></span>|<span data-ttu-id="965ba-182">Los números de teléfono particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-182">The contact's home phone numbers.</span></span>|
|<span data-ttu-id="965ba-183">imAddresses</span><span class="sxs-lookup"><span data-stu-id="965ba-183">imAddresses</span></span>|<span data-ttu-id="965ba-184">String</span><span class="sxs-lookup"><span data-stu-id="965ba-184">String</span></span>|<span data-ttu-id="965ba-185">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-185">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="965ba-186">initials</span><span class="sxs-lookup"><span data-stu-id="965ba-186">initials</span></span>|<span data-ttu-id="965ba-187">String</span><span class="sxs-lookup"><span data-stu-id="965ba-187">String</span></span>|<span data-ttu-id="965ba-188">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-188">The contact's initials.</span></span>|
|<span data-ttu-id="965ba-189">jobTitle</span><span class="sxs-lookup"><span data-stu-id="965ba-189">jobTitle</span></span>|<span data-ttu-id="965ba-190">String</span><span class="sxs-lookup"><span data-stu-id="965ba-190">String</span></span>|<span data-ttu-id="965ba-191">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-191">The contact’s job title.</span></span>|
|<span data-ttu-id="965ba-192">manager</span><span class="sxs-lookup"><span data-stu-id="965ba-192">manager</span></span>|<span data-ttu-id="965ba-193">String</span><span class="sxs-lookup"><span data-stu-id="965ba-193">String</span></span>|<span data-ttu-id="965ba-194">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-194">The name of the contact's manager.</span></span>
|<span data-ttu-id="965ba-195">middleName</span><span class="sxs-lookup"><span data-stu-id="965ba-195">middleName</span></span>|<span data-ttu-id="965ba-196">String</span><span class="sxs-lookup"><span data-stu-id="965ba-196">String</span></span>|<span data-ttu-id="965ba-197">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-197">The contact's middle name.</span></span>|
|<span data-ttu-id="965ba-198">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="965ba-198">mobilePhone</span></span>|<span data-ttu-id="965ba-199">String</span><span class="sxs-lookup"><span data-stu-id="965ba-199">String</span></span>|<span data-ttu-id="965ba-200">El número de teléfono móvil del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-200">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="965ba-201">nickName</span><span class="sxs-lookup"><span data-stu-id="965ba-201">nickName</span></span>|<span data-ttu-id="965ba-202">String</span><span class="sxs-lookup"><span data-stu-id="965ba-202">String</span></span>|<span data-ttu-id="965ba-203">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-203">The contact's nickname.</span></span>|
|<span data-ttu-id="965ba-204">officeLocation</span><span class="sxs-lookup"><span data-stu-id="965ba-204">officeLocation</span></span>|<span data-ttu-id="965ba-205">String</span><span class="sxs-lookup"><span data-stu-id="965ba-205">String</span></span>|<span data-ttu-id="965ba-206">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-206">The location of the contact's office.</span></span>|
|<span data-ttu-id="965ba-207">otherAddress</span><span class="sxs-lookup"><span data-stu-id="965ba-207">otherAddress</span></span>|[<span data-ttu-id="965ba-208">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="965ba-208">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="965ba-209">Otras direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-209">Other addresses for the contact.</span></span>|
|<span data-ttu-id="965ba-210">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="965ba-210">parentFolderId</span></span>|<span data-ttu-id="965ba-211">String</span><span class="sxs-lookup"><span data-stu-id="965ba-211">String</span></span>|<span data-ttu-id="965ba-212">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-212">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="965ba-213">personalNotes</span><span class="sxs-lookup"><span data-stu-id="965ba-213">personalNotes</span></span>|<span data-ttu-id="965ba-214">String</span><span class="sxs-lookup"><span data-stu-id="965ba-214">String</span></span>|<span data-ttu-id="965ba-215">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-215">The user's notes about the contact.</span></span>|
|<span data-ttu-id="965ba-216">profession</span><span class="sxs-lookup"><span data-stu-id="965ba-216">profession</span></span>|<span data-ttu-id="965ba-217">String</span><span class="sxs-lookup"><span data-stu-id="965ba-217">String</span></span>|<span data-ttu-id="965ba-218">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-218">The contact's profession.</span></span>|
|<span data-ttu-id="965ba-219">spouseName</span><span class="sxs-lookup"><span data-stu-id="965ba-219">spouseName</span></span>|<span data-ttu-id="965ba-220">String</span><span class="sxs-lookup"><span data-stu-id="965ba-220">String</span></span>|<span data-ttu-id="965ba-221">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-221">The name of the contact's spouse.</span></span>|
|<span data-ttu-id="965ba-222">surname</span><span class="sxs-lookup"><span data-stu-id="965ba-222">surname</span></span>|<span data-ttu-id="965ba-223">String</span><span class="sxs-lookup"><span data-stu-id="965ba-223">String</span></span>|<span data-ttu-id="965ba-224">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-224">The contact's surname.</span></span>|
|<span data-ttu-id="965ba-225">title</span><span class="sxs-lookup"><span data-stu-id="965ba-225">title</span></span>|<span data-ttu-id="965ba-226">String</span><span class="sxs-lookup"><span data-stu-id="965ba-226">String</span></span>|<span data-ttu-id="965ba-227">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="965ba-227">The contact's title.</span></span>|
|<span data-ttu-id="965ba-228">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="965ba-228">yomiCompanyName</span></span>|<span data-ttu-id="965ba-229">String</span><span class="sxs-lookup"><span data-stu-id="965ba-229">String</span></span>|<span data-ttu-id="965ba-p106">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="965ba-p106">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="965ba-232">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="965ba-232">yomiGivenName</span></span>|<span data-ttu-id="965ba-233">String</span><span class="sxs-lookup"><span data-stu-id="965ba-233">String</span></span>|<span data-ttu-id="965ba-p107">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="965ba-p107">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="965ba-236">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="965ba-236">yomiSurname</span></span>|<span data-ttu-id="965ba-237">String</span><span class="sxs-lookup"><span data-stu-id="965ba-237">String</span></span>|<span data-ttu-id="965ba-p108">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="965ba-p108">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

## <a name="response"></a><span data-ttu-id="965ba-240">Respuesta</span><span class="sxs-lookup"><span data-stu-id="965ba-240">Response</span></span>

<span data-ttu-id="965ba-241">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [contact](../resources/contact.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="965ba-241">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="965ba-242">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="965ba-242">Example</span></span>
##### <a name="request"></a><span data-ttu-id="965ba-243">Solicitud</span><span class="sxs-lookup"><span data-stu-id="965ba-243">Request</span></span>
<span data-ttu-id="965ba-244">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="965ba-244">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="965ba-245">Respuesta</span><span class="sxs-lookup"><span data-stu-id="965ba-245">Response</span></span>
<span data-ttu-id="965ba-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="965ba-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
