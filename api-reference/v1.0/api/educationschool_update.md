# <a name="update-educationschool-properties"></a><span data-ttu-id="9851d-101">Actualizar propiedades de educationschool</span><span class="sxs-lookup"><span data-stu-id="9851d-101">Update educationschool properties</span></span>

<span data-ttu-id="9851d-102">Actualice las propiedades de un objeto de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="9851d-102">Update the properties of a contact object.</span></span>

## <a name="permissions"></a><span data-ttu-id="9851d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9851d-103">Permissions</span></span>
<span data-ttu-id="9851d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9851d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9851d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9851d-106">Permission type</span></span>      | <span data-ttu-id="9851d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9851d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9851d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9851d-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="9851d-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9851d-109">Not supported.</span></span>  |
|<span data-ttu-id="9851d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9851d-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9851d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9851d-111">Not supported.</span></span>  |
|<span data-ttu-id="9851d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9851d-112">Application</span></span> | <span data-ttu-id="9851d-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9851d-113">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9851d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9851d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/schools/{id}
```
## <a name="request-headers"></a><span data-ttu-id="9851d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9851d-115">Request headers</span></span>
| <span data-ttu-id="9851d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9851d-116">Header</span></span>       | <span data-ttu-id="9851d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9851d-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9851d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9851d-118">Authorization</span></span>  | <span data-ttu-id="9851d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9851d-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="9851d-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9851d-121">Content-Type</span></span>  | <span data-ttu-id="9851d-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9851d-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9851d-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="9851d-123">Request body</span></span>
<span data-ttu-id="9851d-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="9851d-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="9851d-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9851d-125">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="9851d-126">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9851d-126">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9851d-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9851d-127">Property</span></span>     | <span data-ttu-id="9851d-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="9851d-128">Type</span></span>   |<span data-ttu-id="9851d-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="9851d-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9851d-130">displayName</span><span class="sxs-lookup"><span data-stu-id="9851d-130">displayName</span></span>| <span data-ttu-id="9851d-131">String</span><span class="sxs-lookup"><span data-stu-id="9851d-131">String</span></span>| <span data-ttu-id="9851d-132">Nombre para mostrar del centro educativo</span><span class="sxs-lookup"><span data-stu-id="9851d-132">Display name of the template.</span></span>| 
|<span data-ttu-id="9851d-133">description</span><span class="sxs-lookup"><span data-stu-id="9851d-133">description</span></span>| <span data-ttu-id="9851d-134">String</span><span class="sxs-lookup"><span data-stu-id="9851d-134">String</span></span> | <span data-ttu-id="9851d-135">Descripción del centro educativo</span><span class="sxs-lookup"><span data-stu-id="9851d-135">Description of the template.</span></span>| 
|<span data-ttu-id="9851d-136">principalEmail</span><span class="sxs-lookup"><span data-stu-id="9851d-136">principalEmail</span></span>| <span data-ttu-id="9851d-137">String</span><span class="sxs-lookup"><span data-stu-id="9851d-137">String</span></span>| <span data-ttu-id="9851d-138">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="9851d-138">Email address of the principal</span></span>|
|<span data-ttu-id="9851d-139">principalName</span><span class="sxs-lookup"><span data-stu-id="9851d-139">principalName</span></span>| <span data-ttu-id="9851d-140">String</span><span class="sxs-lookup"><span data-stu-id="9851d-140">String</span></span> | <span data-ttu-id="9851d-141">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="9851d-141">Name of the principal</span></span>|
|<span data-ttu-id="9851d-142">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="9851d-142">externalPrincipalId</span></span>| <span data-ttu-id="9851d-143">String</span><span class="sxs-lookup"><span data-stu-id="9851d-143">String</span></span> | <span data-ttu-id="9851d-144">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="9851d-144">Id of principal in syncing system.</span></span> |
|<span data-ttu-id="9851d-145">highestGrade</span><span class="sxs-lookup"><span data-stu-id="9851d-145">highestGrade</span></span>|<span data-ttu-id="9851d-146">String</span><span class="sxs-lookup"><span data-stu-id="9851d-146">String</span></span>| <span data-ttu-id="9851d-147">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="9851d-147">Highest grade taught.</span></span> |
|<span data-ttu-id="9851d-148">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="9851d-148">lowestGrade</span></span>|<span data-ttu-id="9851d-149">String</span><span class="sxs-lookup"><span data-stu-id="9851d-149">String</span></span>| <span data-ttu-id="9851d-150">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="9851d-150">Lowest grade taught.</span></span> |
|<span data-ttu-id="9851d-151">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="9851d-151">schoolNumber</span></span>|<span data-ttu-id="9851d-152">String</span><span class="sxs-lookup"><span data-stu-id="9851d-152">String</span></span>| <span data-ttu-id="9851d-153">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="9851d-153">School Number.</span></span>|
|<span data-ttu-id="9851d-154">externalId</span><span class="sxs-lookup"><span data-stu-id="9851d-154">externalId</span></span>|<span data-ttu-id="9851d-155">String</span><span class="sxs-lookup"><span data-stu-id="9851d-155">String</span></span>| <span data-ttu-id="9851d-156">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="9851d-156">Id of school in syncing system.</span></span> |
|<span data-ttu-id="9851d-157">phone</span><span class="sxs-lookup"><span data-stu-id="9851d-157">Phone</span></span>|<span data-ttu-id="9851d-158">String</span><span class="sxs-lookup"><span data-stu-id="9851d-158">String</span></span>| <span data-ttu-id="9851d-159">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="9851d-159">Phone number of school.</span></span> |
|<span data-ttu-id="9851d-160">fax</span><span class="sxs-lookup"><span data-stu-id="9851d-160">fax</span></span>|<span data-ttu-id="9851d-161">String</span><span class="sxs-lookup"><span data-stu-id="9851d-161">String</span></span>| <span data-ttu-id="9851d-162">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="9851d-162">Fax number of school.</span></span> |
|<span data-ttu-id="9851d-163">address</span><span class="sxs-lookup"><span data-stu-id="9851d-163">address</span></span>|[<span data-ttu-id="9851d-164">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="9851d-164">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="9851d-165">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="9851d-165">Address of the School.</span></span>|
|<span data-ttu-id="9851d-166">createdBy</span><span class="sxs-lookup"><span data-stu-id="9851d-166">createdBy</span></span>|[<span data-ttu-id="9851d-167">identitySet</span><span class="sxs-lookup"><span data-stu-id="9851d-167">identitySet</span></span>](../resources/identityset.md)|<span data-ttu-id="9851d-168">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="9851d-168">Entity who created the school.</span></span>|

## <a name="response"></a><span data-ttu-id="9851d-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9851d-169">Response</span></span>
<span data-ttu-id="9851d-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationSchool](../resources/educationschool.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9851d-170">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/educationschool.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9851d-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9851d-171">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9851d-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9851d-172">Request</span></span>
<span data-ttu-id="9851d-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9851d-173">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationschool"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/schools/10002
Content-type: application/json
Content-length: 292

{
  "displayName": "Fabrikam Arts High School",
  "description": "Magnate school for the arts. Los Angeles School District"
}
```
##### <a name="response"></a><span data-ttu-id="9851d-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9851d-174">Response</span></span>
<span data-ttu-id="9851d-175">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9851d-175">The following is an example of the response.</span></span> 

><span data-ttu-id="9851d-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9851d-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 292

{
  "id": "10002",
  "displayName": "Fabrikam Arts High School",
  "description": "Magnate school for the arts. Los Angeles School District",
  "status": "String",
  "externalSource": "String",
  "principalEmail": "AmyR@fabrikam.com",
  "principalName": "Amy Roebuck",
  "externalPrincipalId": "14007",
  "highestGrade": "12",
  "lowestGrade": "9",
  "schoolNumber": "10002",
  "address": {
    "city": "Los Angeles",
    "countryOrRegion": "United States",
    "postalCode": "98055",
    "state": "CA",
    "street": "12345 Main St."
  },
  "externalId": "10002",
  "fax": "+1 (253) 555-0101",
  "phone": "+1 (253) 555-0102"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationschool",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
