---
title: Actualizar propiedades de educationUser
description: Actualice las propiedades de un objeto **educationuser**.
ms.openlocfilehash: bd8d8f95cf1c8475a5c52946d0cf0d1eaa5240ed
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084930"
---
# <a name="update-educationuser-properties"></a><span data-ttu-id="90f4f-103">Actualizar propiedades de educationUser</span><span class="sxs-lookup"><span data-stu-id="90f4f-103">Update educationUser properties</span></span>

> <span data-ttu-id="90f4f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90f4f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90f4f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90f4f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="90f4f-106">Actualice las propiedades de un objeto **educationuser**.</span><span class="sxs-lookup"><span data-stu-id="90f4f-106">Update the properties of an **educationuser** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="90f4f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="90f4f-107">Permissions</span></span>
<span data-ttu-id="90f4f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90f4f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90f4f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90f4f-110">Permission type</span></span>      | <span data-ttu-id="90f4f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90f4f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90f4f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90f4f-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="90f4f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90f4f-113">Not supported.</span></span>  |
|<span data-ttu-id="90f4f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90f4f-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="90f4f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90f4f-115">Not supported.</span></span>  |
|<span data-ttu-id="90f4f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90f4f-116">Application</span></span> | <span data-ttu-id="90f4f-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="90f4f-117">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="90f4f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90f4f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/me
PATCH /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="90f4f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90f4f-119">Request headers</span></span>
| <span data-ttu-id="90f4f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90f4f-120">Header</span></span>       | <span data-ttu-id="90f4f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="90f4f-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="90f4f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="90f4f-122">Authorization</span></span>  | <span data-ttu-id="90f4f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90f4f-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="90f4f-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="90f4f-125">Content-Type</span></span>  | <span data-ttu-id="90f4f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="90f4f-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="90f4f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90f4f-127">Request body</span></span>
<span data-ttu-id="90f4f-128">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="90f4f-128">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="90f4f-129">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="90f4f-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="90f4f-130">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="90f4f-130">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="90f4f-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90f4f-131">Property</span></span>     | <span data-ttu-id="90f4f-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="90f4f-132">Type</span></span>   |<span data-ttu-id="90f4f-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="90f4f-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="90f4f-134">displayName</span><span class="sxs-lookup"><span data-stu-id="90f4f-134">displayName</span></span>| <span data-ttu-id="90f4f-135">String</span><span class="sxs-lookup"><span data-stu-id="90f4f-135">String</span></span>| <span data-ttu-id="90f4f-136">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-136">Display Name of User</span></span>|
|<span data-ttu-id="90f4f-137">givenName</span><span class="sxs-lookup"><span data-stu-id="90f4f-137">givenName</span></span>| <span data-ttu-id="90f4f-138">String</span><span class="sxs-lookup"><span data-stu-id="90f4f-138">String</span></span> | <span data-ttu-id="90f4f-139">Nombre.</span><span class="sxs-lookup"><span data-stu-id="90f4f-139">First Name</span></span> |
|<span data-ttu-id="90f4f-140">middleName</span><span class="sxs-lookup"><span data-stu-id="90f4f-140">middleName</span></span>| <span data-ttu-id="90f4f-141">String</span><span class="sxs-lookup"><span data-stu-id="90f4f-141">String</span></span> | <span data-ttu-id="90f4f-142">Segundo nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-142">Middle Name of user</span></span>|
|<span data-ttu-id="90f4f-143">surname</span><span class="sxs-lookup"><span data-stu-id="90f4f-143">surname</span></span>| <span data-ttu-id="90f4f-144">String</span><span class="sxs-lookup"><span data-stu-id="90f4f-144">String</span></span> | <span data-ttu-id="90f4f-145">Apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-145">Surname of user</span></span>|
|<span data-ttu-id="90f4f-146">mail</span><span class="sxs-lookup"><span data-stu-id="90f4f-146">mail</span></span>| <span data-ttu-id="90f4f-147">String</span><span class="sxs-lookup"><span data-stu-id="90f4f-147">String</span></span>| <span data-ttu-id="90f4f-148">Dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="90f4f-148">email address</span></span>|
|<span data-ttu-id="90f4f-149">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="90f4f-149">mobilePhone</span></span>| <span data-ttu-id="90f4f-150">String</span><span class="sxs-lookup"><span data-stu-id="90f4f-150">String</span></span> | <span data-ttu-id="90f4f-151">Número de móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-151">Mobile number of user</span></span> |
|<span data-ttu-id="90f4f-152">externalSource</span><span class="sxs-lookup"><span data-stu-id="90f4f-152">externalSource</span></span>|<span data-ttu-id="90f4f-153">string</span><span class="sxs-lookup"><span data-stu-id="90f4f-153">string</span></span>| <span data-ttu-id="90f4f-154">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="90f4f-154">Possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="90f4f-155">externalSource</span><span class="sxs-lookup"><span data-stu-id="90f4f-155">externalSource</span></span>|<span data-ttu-id="90f4f-156">string</span><span class="sxs-lookup"><span data-stu-id="90f4f-156">string</span></span>| <span data-ttu-id="90f4f-157">Indica desde dónde se ha creado este usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-157">Where this user was created from.</span></span>  <span data-ttu-id="90f4f-158">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="90f4f-158">Possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="90f4f-159">mailingAddress</span><span class="sxs-lookup"><span data-stu-id="90f4f-159">mailingAddress</span></span>|[<span data-ttu-id="90f4f-160">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="90f4f-160">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="90f4f-161">Dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-161">Mail address of user.</span></span>|
|<span data-ttu-id="90f4f-162">residenceAddress</span><span class="sxs-lookup"><span data-stu-id="90f4f-162">residenceAddress</span></span>|[<span data-ttu-id="90f4f-163">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="90f4f-163">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="90f4f-164">Dirección donde reside el usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-164">Address where user lives.</span></span>|
|<span data-ttu-id="90f4f-165">primaryRole</span><span class="sxs-lookup"><span data-stu-id="90f4f-165">primaryRole</span></span>|<span data-ttu-id="90f4f-166">string</span><span class="sxs-lookup"><span data-stu-id="90f4f-166">string</span></span>| <span data-ttu-id="90f4f-167">Rol predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="90f4f-167">Default Role for a user.</span></span>  <span data-ttu-id="90f4f-168">Puede que el rol del usuario sea distinto en una clase individual.</span><span class="sxs-lookup"><span data-stu-id="90f4f-168">The user's role might be different in an individual class.</span></span> <span data-ttu-id="90f4f-169">Los valores posibles son: `student`, `teacher` y `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="90f4f-169">Possible values are: `student`, `teacher`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="90f4f-170">student</span><span class="sxs-lookup"><span data-stu-id="90f4f-170">student</span></span>|[<span data-ttu-id="90f4f-171">educationStudent</span><span class="sxs-lookup"><span data-stu-id="90f4f-171">educationStudent</span></span>](../resources/educationstudent.md)| <span data-ttu-id="90f4f-172">Si el rol principal es alumno, este bloque contendrá datos específicos de alumnos.</span><span class="sxs-lookup"><span data-stu-id="90f4f-172">If the primary role is student, this block will contain student specific data.</span></span>|
|<span data-ttu-id="90f4f-173">teacher</span><span class="sxs-lookup"><span data-stu-id="90f4f-173">teacher</span></span>|[<span data-ttu-id="90f4f-174">educationTeacher</span><span class="sxs-lookup"><span data-stu-id="90f4f-174">educationTeacher</span></span>](../resources/educationteacher.md)| <span data-ttu-id="90f4f-175">Si el rol principal es profesor, este bloque contendrá datos específicos de profesores.</span><span class="sxs-lookup"><span data-stu-id="90f4f-175">If the primary role is teacher, this block will conatin teacher specific data.</span></span>|


## <a name="response"></a><span data-ttu-id="90f4f-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90f4f-176">Response</span></span>
<span data-ttu-id="90f4f-177">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [educationUser](../resources/educationuser.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90f4f-177">If successful, this method returns a `200 OK` response code and updated [educationUser](../resources/educationuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="90f4f-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90f4f-178">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90f4f-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90f4f-179">Request</span></span>
<span data-ttu-id="90f4f-180">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90f4f-180">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationuser"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/users/13020
Content-type: application/json
Content-length: 508

{
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
}
```
##### <a name="response"></a><span data-ttu-id="90f4f-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90f4f-181">Response</span></span>
<span data-ttu-id="90f4f-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90f4f-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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