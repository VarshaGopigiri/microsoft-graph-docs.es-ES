# <a name="update-educationuser-properties"></a><span data-ttu-id="e2f99-101">Actualizar propiedades de educationUser</span><span class="sxs-lookup"><span data-stu-id="e2f99-101">Update educationUser properties</span></span>

<span data-ttu-id="e2f99-102">Actualice las propiedades de un objeto **educationuser**.</span><span class="sxs-lookup"><span data-stu-id="e2f99-102">Update the properties of an **educationuser** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="e2f99-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e2f99-103">Permissions</span></span>
<span data-ttu-id="e2f99-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e2f99-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e2f99-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e2f99-106">Permission type</span></span>      | <span data-ttu-id="e2f99-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e2f99-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e2f99-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e2f99-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="e2f99-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2f99-109">Not supported.</span></span>  |
|<span data-ttu-id="e2f99-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e2f99-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e2f99-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2f99-111">Not supported.</span></span>  |
|<span data-ttu-id="e2f99-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e2f99-112">Application</span></span> | <span data-ttu-id="e2f99-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e2f99-113">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e2f99-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e2f99-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/me
PATCH /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e2f99-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2f99-115">Request headers</span></span>
| <span data-ttu-id="e2f99-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2f99-116">Header</span></span>       | <span data-ttu-id="e2f99-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e2f99-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e2f99-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="e2f99-118">Authorization</span></span>  | <span data-ttu-id="e2f99-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e2f99-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e2f99-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e2f99-121">Content-Type</span></span>  | <span data-ttu-id="e2f99-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e2f99-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e2f99-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e2f99-123">Request body</span></span>
<span data-ttu-id="e2f99-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="e2f99-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="e2f99-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e2f99-125">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="e2f99-126">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e2f99-126">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e2f99-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2f99-127">Property</span></span>     | <span data-ttu-id="e2f99-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2f99-128">Type</span></span>   |<span data-ttu-id="e2f99-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2f99-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e2f99-130">displayName</span><span class="sxs-lookup"><span data-stu-id="e2f99-130">displayName</span></span>| <span data-ttu-id="e2f99-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-131">String</span></span>| <span data-ttu-id="e2f99-132">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-132">Display Name of User</span></span>|
|<span data-ttu-id="e2f99-133">givenName</span><span class="sxs-lookup"><span data-stu-id="e2f99-133">givenName</span></span>| <span data-ttu-id="e2f99-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-134">String</span></span> | <span data-ttu-id="e2f99-135">Nombre.</span><span class="sxs-lookup"><span data-stu-id="e2f99-135">First Name</span></span> |
|<span data-ttu-id="e2f99-136">middleName</span><span class="sxs-lookup"><span data-stu-id="e2f99-136">middleName</span></span>| <span data-ttu-id="e2f99-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-137">String</span></span> | <span data-ttu-id="e2f99-138">Segundo nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-138">Middle Name of user</span></span>|
|<span data-ttu-id="e2f99-139">surname</span><span class="sxs-lookup"><span data-stu-id="e2f99-139">surname</span></span>| <span data-ttu-id="e2f99-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-140">String</span></span> | <span data-ttu-id="e2f99-141">Apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-141">Surname of user</span></span>|
|<span data-ttu-id="e2f99-142">mail</span><span class="sxs-lookup"><span data-stu-id="e2f99-142">mail</span></span>| <span data-ttu-id="e2f99-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-143">String</span></span>| <span data-ttu-id="e2f99-144">Dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e2f99-144">email address</span></span>|
|<span data-ttu-id="e2f99-145">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="e2f99-145">mobilePhone</span></span>| <span data-ttu-id="e2f99-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-146">String</span></span> | <span data-ttu-id="e2f99-147">Número de móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-147">Mobile number of user</span></span> |
|<span data-ttu-id="e2f99-148">externalSource</span><span class="sxs-lookup"><span data-stu-id="e2f99-148">externalSource</span></span>|<span data-ttu-id="e2f99-149">cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-149">string</span></span>| <span data-ttu-id="e2f99-150">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="e2f99-150">The possible values are `sis`, `manual`, `enum_sentinel`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="e2f99-151">externalSource</span><span class="sxs-lookup"><span data-stu-id="e2f99-151">externalSource</span></span>|<span data-ttu-id="e2f99-152">cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-152">string</span></span>| <span data-ttu-id="e2f99-153">Indica desde dónde se ha creado este usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-153">Where this user was created from.</span></span>  <span data-ttu-id="e2f99-154">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="e2f99-154">The possible values are `sis`, `manual`, `enum_sentinel`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="e2f99-155">mailingAddress</span><span class="sxs-lookup"><span data-stu-id="e2f99-155">mailingAddress</span></span>|[<span data-ttu-id="e2f99-156">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="e2f99-156">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="e2f99-157">Dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-157">Mail address of user.</span></span>|
|<span data-ttu-id="e2f99-158">residenceAddress</span><span class="sxs-lookup"><span data-stu-id="e2f99-158">residenceAddress</span></span>|[<span data-ttu-id="e2f99-159">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="e2f99-159">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="e2f99-160">Dirección donde reside el usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-160">Address where user lives.</span></span>|
|<span data-ttu-id="e2f99-161">primaryRole</span><span class="sxs-lookup"><span data-stu-id="e2f99-161">primaryRole</span></span>|<span data-ttu-id="e2f99-162">cadena</span><span class="sxs-lookup"><span data-stu-id="e2f99-162">string</span></span>| <span data-ttu-id="e2f99-163">Rol predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e2f99-163">Default Role for a user.</span></span>  <span data-ttu-id="e2f99-164">Puede que el rol del usuario sea distinto en una clase individual.</span><span class="sxs-lookup"><span data-stu-id="e2f99-164">The user's role might be different in an individual class.</span></span> <span data-ttu-id="e2f99-165">Los valores posibles son: `student`, `teacher` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="e2f99-165">The possible values are `student`, `teacher`, `enum_sentinel`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="e2f99-166">student</span><span class="sxs-lookup"><span data-stu-id="e2f99-166">student</span></span>|[<span data-ttu-id="e2f99-167">educationStudent</span><span class="sxs-lookup"><span data-stu-id="e2f99-167">educationStudent</span></span>](../resources/educationstudent.md)| <span data-ttu-id="e2f99-168">Si el rol principal es alumno, este bloque contendrá datos específicos de alumnos.</span><span class="sxs-lookup"><span data-stu-id="e2f99-168">If the primary role is student, this block will contain student specific data.</span></span>|
|<span data-ttu-id="e2f99-169">teacher</span><span class="sxs-lookup"><span data-stu-id="e2f99-169">teacher</span></span>|[<span data-ttu-id="e2f99-170">educationTeacher</span><span class="sxs-lookup"><span data-stu-id="e2f99-170">educationTeacher</span></span>](../resources/educationteacher.md)| <span data-ttu-id="e2f99-171">Si el rol principal es profesor, este bloque contendrá datos específicos de profesores.</span><span class="sxs-lookup"><span data-stu-id="e2f99-171">If the primary role is teacher, this block will conatin teacher specific data.</span></span>|


## <a name="response"></a><span data-ttu-id="e2f99-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2f99-172">Response</span></span>
<span data-ttu-id="e2f99-173">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [educationUser](../resources/educationuser.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2f99-173">If successful, this method returns a `200 OK` response code and updated [educationUser](../resources/educationuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e2f99-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2f99-174">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e2f99-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e2f99-175">Request</span></span>
<span data-ttu-id="e2f99-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2f99-176">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationuser"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/users/{user-id}
Content-type: application/json
Content-length: 508

{
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
}
```
##### <a name="response"></a><span data-ttu-id="e2f99-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2f99-177">Response</span></span>
<span data-ttu-id="e2f99-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e2f99-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "primaryRole": "student",
  "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
  "student": {
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