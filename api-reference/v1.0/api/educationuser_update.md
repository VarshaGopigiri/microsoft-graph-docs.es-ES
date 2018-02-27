# <a name="update-educationuser-properties"></a><span data-ttu-id="956d5-101">Actualizar propiedades de educationUser</span><span class="sxs-lookup"><span data-stu-id="956d5-101">Update educationUser properties</span></span>

<span data-ttu-id="956d5-102">Actualice las propiedades de un objeto **educationuser**.</span><span class="sxs-lookup"><span data-stu-id="956d5-102">Update the properties of an **eventMessage** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="956d5-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="956d5-103">Permissions</span></span>
<span data-ttu-id="956d5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="956d5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="956d5-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="956d5-106">Permission type</span></span>      | <span data-ttu-id="956d5-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="956d5-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="956d5-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="956d5-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="956d5-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="956d5-109">Not supported.</span></span>  |
|<span data-ttu-id="956d5-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="956d5-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="956d5-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="956d5-111">Not supported.</span></span>  |
|<span data-ttu-id="956d5-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="956d5-112">Application</span></span> | <span data-ttu-id="956d5-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="956d5-113">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="956d5-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="956d5-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/me
PATCH /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="956d5-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="956d5-115">Request headers</span></span>
| <span data-ttu-id="956d5-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="956d5-116">Header</span></span>       | <span data-ttu-id="956d5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="956d5-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="956d5-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="956d5-118">Authorization</span></span>  | <span data-ttu-id="956d5-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="956d5-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="956d5-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="956d5-121">Content-Type</span></span>  | <span data-ttu-id="956d5-122">application/json</span><span class="sxs-lookup"><span data-stu-id="956d5-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="956d5-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="956d5-123">Request body</span></span>
<span data-ttu-id="956d5-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="956d5-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="956d5-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="956d5-125">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="956d5-126">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="956d5-126">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="956d5-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="956d5-127">Property</span></span>     | <span data-ttu-id="956d5-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="956d5-128">Type</span></span>   |<span data-ttu-id="956d5-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="956d5-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="956d5-130">displayName</span><span class="sxs-lookup"><span data-stu-id="956d5-130">displayName</span></span>| <span data-ttu-id="956d5-131">String</span><span class="sxs-lookup"><span data-stu-id="956d5-131">String</span></span>| <span data-ttu-id="956d5-132">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-132">Display Name of User</span></span>|
|<span data-ttu-id="956d5-133">givenName</span><span class="sxs-lookup"><span data-stu-id="956d5-133">givenName</span></span>| <span data-ttu-id="956d5-134">String</span><span class="sxs-lookup"><span data-stu-id="956d5-134">String</span></span> | <span data-ttu-id="956d5-135">Nombre.</span><span class="sxs-lookup"><span data-stu-id="956d5-135">First Name</span></span> |
|<span data-ttu-id="956d5-136">middleName</span><span class="sxs-lookup"><span data-stu-id="956d5-136">middleName</span></span>| <span data-ttu-id="956d5-137">String</span><span class="sxs-lookup"><span data-stu-id="956d5-137">String</span></span> | <span data-ttu-id="956d5-138">Segundo nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-138">Middle Name of user</span></span>|
|<span data-ttu-id="956d5-139">surname</span><span class="sxs-lookup"><span data-stu-id="956d5-139">surname</span></span>| <span data-ttu-id="956d5-140">String</span><span class="sxs-lookup"><span data-stu-id="956d5-140">String</span></span> | <span data-ttu-id="956d5-141">Apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-141">Surname of user</span></span>|
|<span data-ttu-id="956d5-142">mail</span><span class="sxs-lookup"><span data-stu-id="956d5-142">mail</span></span>| <span data-ttu-id="956d5-143">String</span><span class="sxs-lookup"><span data-stu-id="956d5-143">String</span></span>| <span data-ttu-id="956d5-144">Dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="956d5-144">Email Address</span></span>|
|<span data-ttu-id="956d5-145">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="956d5-145">mobilePhone</span></span>| <span data-ttu-id="956d5-146">String</span><span class="sxs-lookup"><span data-stu-id="956d5-146">String</span></span> | <span data-ttu-id="956d5-147">Número de móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-147">Mobile number of user</span></span> |
|<span data-ttu-id="956d5-148">externalSource</span><span class="sxs-lookup"><span data-stu-id="956d5-148">externalSource</span></span>|<span data-ttu-id="956d5-149">string</span><span class="sxs-lookup"><span data-stu-id="956d5-149">string</span></span>| <span data-ttu-id="956d5-150">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="956d5-150">Possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="956d5-151">externalSource</span><span class="sxs-lookup"><span data-stu-id="956d5-151">externalSource</span></span>|<span data-ttu-id="956d5-152">string</span><span class="sxs-lookup"><span data-stu-id="956d5-152">string</span></span>| <span data-ttu-id="956d5-153">Indica desde dónde se ha creado este usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-153">Where this user was created from.</span></span>  <span data-ttu-id="956d5-154">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="956d5-154">Possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="956d5-155">mailingAddress</span><span class="sxs-lookup"><span data-stu-id="956d5-155">mailingAddress</span></span>|[<span data-ttu-id="956d5-156">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="956d5-156">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="956d5-157">Dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-157">Mail address of user.</span></span>|
|<span data-ttu-id="956d5-158">residenceAddress</span><span class="sxs-lookup"><span data-stu-id="956d5-158">residenceAddress</span></span>|[<span data-ttu-id="956d5-159">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="956d5-159">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="956d5-160">Dirección donde reside el usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-160">Address where user lives.</span></span>|
|<span data-ttu-id="956d5-161">primaryRole</span><span class="sxs-lookup"><span data-stu-id="956d5-161">primaryRole</span></span>|<span data-ttu-id="956d5-162">string</span><span class="sxs-lookup"><span data-stu-id="956d5-162">string</span></span>| <span data-ttu-id="956d5-163">Rol predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="956d5-163">Default Role for a user.</span></span>  <span data-ttu-id="956d5-164">Puede que el rol del usuario sea distinto en una clase individual.</span><span class="sxs-lookup"><span data-stu-id="956d5-164">The user's role might be different in an individual class.</span></span> <span data-ttu-id="956d5-165">Los valores posibles son: `student`, `teacher` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="956d5-165">Possible values are: `student`, `teacher`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="956d5-166">student</span><span class="sxs-lookup"><span data-stu-id="956d5-166">student</span></span>|[<span data-ttu-id="956d5-167">educationStudent</span><span class="sxs-lookup"><span data-stu-id="956d5-167">educationStudent</span></span>](../resources/educationstudent.md)| <span data-ttu-id="956d5-168">Si el rol principal es alumno, este bloque contendrá datos específicos de alumnos.</span><span class="sxs-lookup"><span data-stu-id="956d5-168">If the primary role is student, this block will contain student specific data.</span></span>|
|<span data-ttu-id="956d5-169">teacher</span><span class="sxs-lookup"><span data-stu-id="956d5-169">teacher</span></span>|[<span data-ttu-id="956d5-170">educationTeacher</span><span class="sxs-lookup"><span data-stu-id="956d5-170">educationTeacher</span></span>](../resources/educationteacher.md)| <span data-ttu-id="956d5-171">Si el rol principal es profesor, este bloque contendrá datos específicos de profesores.</span><span class="sxs-lookup"><span data-stu-id="956d5-171">If the primary role is teacher, this block will conatin teacher specific data.</span></span>|


## <a name="response"></a><span data-ttu-id="956d5-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="956d5-172">Response</span></span>
<span data-ttu-id="956d5-173">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [educationUser](../resources/educationuser.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="956d5-173">If successful, this method returns a `200 OK` response code and updated [ChartFont](../resources/educationuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="956d5-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="956d5-174">Example</span></span>
##### <a name="request"></a><span data-ttu-id="956d5-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="956d5-175">Request</span></span>
<span data-ttu-id="956d5-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="956d5-176">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationuser"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/users/13020
Content-type: application/json
Content-length: 508

{
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
}
```
##### <a name="response"></a><span data-ttu-id="956d5-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="956d5-177">Response</span></span>
<span data-ttu-id="956d5-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="956d5-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 508

{
  "id": "13020",
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
  "mail": "rogelioC@contoso.com",
  "mobilePhone": "+1 (253) 555-0101",
  "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
  },
  "externalSource": "sis",
  "mailingAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
  "primaryRole": "string",
  "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
  "student": {
      "primaryRole": "student",
      "externalId": "13005",
      "birthDate": "2001-01-01T00:00:00Z"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationuser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->