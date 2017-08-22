# <a name="update-contact"></a><span data-ttu-id="bfe12-101">Actualizar contacto</span><span class="sxs-lookup"><span data-stu-id="bfe12-101">Update contact</span></span>

<span data-ttu-id="bfe12-102">Actualice las propiedades de un objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-102">Update the properties of a contact object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bfe12-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bfe12-103">Prerequisites</span></span>
<span data-ttu-id="bfe12-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="bfe12-104">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="bfe12-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bfe12-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="bfe12-106">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="bfe12-106">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="bfe12-107">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="bfe12-107">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="bfe12-p101">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p101">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="bfe12-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe12-110">Request headers</span></span>
| <span data-ttu-id="bfe12-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfe12-111">Header</span></span>       | <span data-ttu-id="bfe12-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe12-112">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bfe12-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="bfe12-113">Authorization</span></span>  | <span data-ttu-id="bfe12-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="bfe12-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bfe12-116">Content-Type</span></span>  | <span data-ttu-id="bfe12-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="bfe12-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe12-119">Request body</span></span>
<span data-ttu-id="bfe12-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="bfe12-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe12-123">Property</span></span>     | <span data-ttu-id="bfe12-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe12-124">Type</span></span>   |<span data-ttu-id="bfe12-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfe12-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bfe12-126">assistantName</span><span class="sxs-lookup"><span data-stu-id="bfe12-126">assistantName</span></span>|<span data-ttu-id="bfe12-127">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-127">String</span></span>|<span data-ttu-id="bfe12-128">El nombre del ayudante del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-128">The name of the contact's assistant.</span></span>|
|<span data-ttu-id="bfe12-129">birthday</span><span class="sxs-lookup"><span data-stu-id="bfe12-129">birthday</span></span>|<span data-ttu-id="bfe12-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bfe12-130">DateTimeOffset</span></span>|<span data-ttu-id="bfe12-131">El cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-131">The contact's birthday.</span></span>|
|<span data-ttu-id="bfe12-132">businessAddress</span><span class="sxs-lookup"><span data-stu-id="bfe12-132">businessAddress</span></span>|[<span data-ttu-id="bfe12-133">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="bfe12-133">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="bfe12-134">La dirección del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-134">The contact's business address.</span></span>|
|<span data-ttu-id="bfe12-135">businessHomePage</span><span class="sxs-lookup"><span data-stu-id="bfe12-135">businessHomePage</span></span>|<span data-ttu-id="bfe12-136">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-136">String</span></span>|<span data-ttu-id="bfe12-137">La página principal de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-137">The business home page of the contact.</span></span>|
|<span data-ttu-id="bfe12-138">businessPhones</span><span class="sxs-lookup"><span data-stu-id="bfe12-138">businessPhones</span></span>|<span data-ttu-id="bfe12-139">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-139">String</span></span>|<span data-ttu-id="bfe12-140">Los números de teléfono del trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-140">The contact's business phone numbers.</span></span>|
|<span data-ttu-id="bfe12-141">categories</span><span class="sxs-lookup"><span data-stu-id="bfe12-141">categories</span></span>|<span data-ttu-id="bfe12-142">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-142">String</span></span>|<span data-ttu-id="bfe12-143">Las categorías asociadas con el contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-143">The categories associated with the contact.</span></span>|
|<span data-ttu-id="bfe12-144">children</span><span class="sxs-lookup"><span data-stu-id="bfe12-144">children</span></span>|<span data-ttu-id="bfe12-145">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-145">String</span></span>|<span data-ttu-id="bfe12-146">Los nombres de los hijos del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-146">The names of the contact's children.</span></span>|
|<span data-ttu-id="bfe12-147">companyName</span><span class="sxs-lookup"><span data-stu-id="bfe12-147">companyName</span></span>|<span data-ttu-id="bfe12-148">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-148">String</span></span>|<span data-ttu-id="bfe12-149">El nombre de la empresa del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-149">The name of the contact's company.</span></span>|
|<span data-ttu-id="bfe12-150">department</span><span class="sxs-lookup"><span data-stu-id="bfe12-150">department</span></span>|<span data-ttu-id="bfe12-151">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-151">String</span></span>|<span data-ttu-id="bfe12-152">El departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-152">The contact's department.</span></span>|
|<span data-ttu-id="bfe12-153">displayName</span><span class="sxs-lookup"><span data-stu-id="bfe12-153">displayName</span></span>|<span data-ttu-id="bfe12-154">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-154">String</span></span>|<span data-ttu-id="bfe12-155">El nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-155">The contact's display name.</span></span>|
|<span data-ttu-id="bfe12-156">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="bfe12-156">emailAddresses</span></span>|<span data-ttu-id="bfe12-157">Colección [EmailAddress](../resources/emailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="bfe12-157">[EmailAddress](../resources/emailaddress.md) collection</span></span>|<span data-ttu-id="bfe12-158">Las direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-158">The contact's email addresses.</span></span>|
|<span data-ttu-id="bfe12-159">fileAs</span><span class="sxs-lookup"><span data-stu-id="bfe12-159">fileAs</span></span>|<span data-ttu-id="bfe12-160">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-160">String</span></span>|<span data-ttu-id="bfe12-161">El nombre con el que se ha archivado el contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-161">The name the contact is filed under.</span></span>|
|<span data-ttu-id="bfe12-162">generation</span><span class="sxs-lookup"><span data-stu-id="bfe12-162">generation</span></span>|<span data-ttu-id="bfe12-163">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-163">String</span></span>|<span data-ttu-id="bfe12-164">La generación del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-164">The contact's generation.</span></span>|
|<span data-ttu-id="bfe12-165">givenName</span><span class="sxs-lookup"><span data-stu-id="bfe12-165">givenName</span></span>|<span data-ttu-id="bfe12-166">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-166">String</span></span>|<span data-ttu-id="bfe12-167">El nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-167">The contact's given name.</span></span>|
|<span data-ttu-id="bfe12-168">homeAddress</span><span class="sxs-lookup"><span data-stu-id="bfe12-168">homeAddress</span></span>|[<span data-ttu-id="bfe12-169">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="bfe12-169">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="bfe12-170">La dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-170">The contact's home address.</span></span>|
|<span data-ttu-id="bfe12-171">homePhones</span><span class="sxs-lookup"><span data-stu-id="bfe12-171">homePhones</span></span>|<span data-ttu-id="bfe12-172">Colección String</span><span class="sxs-lookup"><span data-stu-id="bfe12-172">String collection</span></span>|<span data-ttu-id="bfe12-173">Los números de teléfono particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-173">The contact's home phone numbers.</span></span>|
|<span data-ttu-id="bfe12-174">imAddresses</span><span class="sxs-lookup"><span data-stu-id="bfe12-174">imAddresses</span></span>|<span data-ttu-id="bfe12-175">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-175">String</span></span>|<span data-ttu-id="bfe12-176">Las direcciones de mensajería instantánea (MI) del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-176">The contact's instant messaging (IM) addresses.</span></span>|
|<span data-ttu-id="bfe12-177">initials</span><span class="sxs-lookup"><span data-stu-id="bfe12-177">initials</span></span>|<span data-ttu-id="bfe12-178">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-178">String</span></span>|<span data-ttu-id="bfe12-179">Las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-179">The contact's initials.</span></span>|
|<span data-ttu-id="bfe12-180">jobTitle</span><span class="sxs-lookup"><span data-stu-id="bfe12-180">jobTitle</span></span>|<span data-ttu-id="bfe12-181">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-181">String</span></span>|<span data-ttu-id="bfe12-182">El puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-182">The contact’s job title.</span></span>|
|<span data-ttu-id="bfe12-183">manager</span><span class="sxs-lookup"><span data-stu-id="bfe12-183">manager</span></span>|<span data-ttu-id="bfe12-184">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-184">String</span></span>|<span data-ttu-id="bfe12-185">El nombre del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-185">The name of the contact's manager.</span></span>
|<span data-ttu-id="bfe12-186">middleName</span><span class="sxs-lookup"><span data-stu-id="bfe12-186">middleName</span></span>|<span data-ttu-id="bfe12-187">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-187">String</span></span>|<span data-ttu-id="bfe12-188">El segundo nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-188">The contact's middle name.</span></span>|
|<span data-ttu-id="bfe12-189">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="bfe12-189">mobilePhone</span></span>|<span data-ttu-id="bfe12-190">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-190">String</span></span>|<span data-ttu-id="bfe12-191">El número de teléfono móvil del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-191">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="bfe12-192">nickName</span><span class="sxs-lookup"><span data-stu-id="bfe12-192">nickName</span></span>|<span data-ttu-id="bfe12-193">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-193">String</span></span>|<span data-ttu-id="bfe12-194">El sobrenombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-194">The contact's nickname.</span></span>|
|<span data-ttu-id="bfe12-195">officeLocation</span><span class="sxs-lookup"><span data-stu-id="bfe12-195">officeLocation</span></span>|<span data-ttu-id="bfe12-196">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-196">String</span></span>|<span data-ttu-id="bfe12-197">La ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-197">The location of the contact's office.</span></span>|
|<span data-ttu-id="bfe12-198">otherAddress</span><span class="sxs-lookup"><span data-stu-id="bfe12-198">otherAddress</span></span>|[<span data-ttu-id="bfe12-199">PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="bfe12-199">PhysicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="bfe12-200">Otras direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-200">Other addresses for the contact.</span></span>|
|<span data-ttu-id="bfe12-201">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="bfe12-201">parentFolderId</span></span>|<span data-ttu-id="bfe12-202">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-202">String</span></span>|<span data-ttu-id="bfe12-203">El identificador de la carpeta principal del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-203">The ID of the contact's parent folder.</span></span>|
|<span data-ttu-id="bfe12-204">personalNotes</span><span class="sxs-lookup"><span data-stu-id="bfe12-204">personalNotes</span></span>|<span data-ttu-id="bfe12-205">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-205">String</span></span>|<span data-ttu-id="bfe12-206">Las notas del usuario sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-206">The user's notes about the contact.</span></span>|
|<span data-ttu-id="bfe12-207">profession</span><span class="sxs-lookup"><span data-stu-id="bfe12-207">profession</span></span>|<span data-ttu-id="bfe12-208">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-208">String</span></span>|<span data-ttu-id="bfe12-209">La profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-209">The contact's profession.</span></span>|
|<span data-ttu-id="bfe12-210">spouseName</span><span class="sxs-lookup"><span data-stu-id="bfe12-210">spouseName</span></span>|<span data-ttu-id="bfe12-211">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-211">String</span></span>|<span data-ttu-id="bfe12-212">El nombre del cónyuge del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-212">The name of the contact's spouse.</span></span>|
|<span data-ttu-id="bfe12-213">surname</span><span class="sxs-lookup"><span data-stu-id="bfe12-213">surname</span></span>|<span data-ttu-id="bfe12-214">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-214">String</span></span>|<span data-ttu-id="bfe12-215">Los apellidos del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-215">The contact's surname.</span></span>|
|<span data-ttu-id="bfe12-216">title</span><span class="sxs-lookup"><span data-stu-id="bfe12-216">title</span></span>|<span data-ttu-id="bfe12-217">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-217">String</span></span>|<span data-ttu-id="bfe12-218">El título del contacto.</span><span class="sxs-lookup"><span data-stu-id="bfe12-218">The contact's title.</span></span>|
|<span data-ttu-id="bfe12-219">yomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="bfe12-219">yomiCompanyName</span></span>|<span data-ttu-id="bfe12-220">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-220">String</span></span>|<span data-ttu-id="bfe12-p105">El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p105">The phonetic Japanese company name of the contact. This property is optional.</span></span>|
|<span data-ttu-id="bfe12-223">yomiGivenName</span><span class="sxs-lookup"><span data-stu-id="bfe12-223">yomiGivenName</span></span>|<span data-ttu-id="bfe12-224">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-224">String</span></span>|<span data-ttu-id="bfe12-p106">El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p106">The phonetic Japanese given name (first name) of the contact. This property is optional.</span></span>|
|<span data-ttu-id="bfe12-227">yomiSurname</span><span class="sxs-lookup"><span data-stu-id="bfe12-227">yomiSurname</span></span>|<span data-ttu-id="bfe12-228">String</span><span class="sxs-lookup"><span data-stu-id="bfe12-228">String</span></span>|<span data-ttu-id="bfe12-p107">El apellido fonético japonés del contacto. Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p107">The phonetic Japanese surname (last name)  of the contact. This property is optional.</span></span>|

## <a name="response"></a><span data-ttu-id="bfe12-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe12-231">Response</span></span>

<span data-ttu-id="bfe12-232">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [contact](../resources/contact.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfe12-232">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bfe12-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfe12-233">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bfe12-234">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe12-234">Request</span></span>
<span data-ttu-id="bfe12-235">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe12-235">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="bfe12-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe12-236">Response</span></span>
<span data-ttu-id="bfe12-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bfe12-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
