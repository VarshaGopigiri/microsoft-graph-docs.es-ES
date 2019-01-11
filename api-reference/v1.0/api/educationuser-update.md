---
title: Actualizar propiedades de educationUser
description: Actualice las propiedades de un objeto **educationuser**.
localization_priority: Normal
ms.openlocfilehash: aef8640f49ad6ff4d91755fd5200000f4a0e856d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856662"
---
# <a name="update-educationuser-properties"></a><span data-ttu-id="62453-103">Actualizar propiedades de educationUser</span><span class="sxs-lookup"><span data-stu-id="62453-103">Update educationUser properties</span></span>

<span data-ttu-id="62453-104">Actualice las propiedades de un objeto **educationuser**.</span><span class="sxs-lookup"><span data-stu-id="62453-104">Update the properties of an **educationuser** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="62453-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="62453-105">Permissions</span></span>
<span data-ttu-id="62453-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62453-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="62453-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62453-108">Permission type</span></span>      | <span data-ttu-id="62453-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62453-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="62453-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62453-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="62453-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62453-111">Not supported.</span></span>  |
|<span data-ttu-id="62453-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62453-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="62453-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62453-113">Not supported.</span></span>  |
|<span data-ttu-id="62453-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62453-114">Application</span></span> | <span data-ttu-id="62453-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="62453-115">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="62453-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62453-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/me
PATCH /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="62453-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62453-117">Request headers</span></span>
| <span data-ttu-id="62453-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62453-118">Header</span></span>       | <span data-ttu-id="62453-119">Valor</span><span class="sxs-lookup"><span data-stu-id="62453-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="62453-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="62453-120">Authorization</span></span>  | <span data-ttu-id="62453-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="62453-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="62453-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="62453-123">Content-Type</span></span>  | <span data-ttu-id="62453-124">application/json</span><span class="sxs-lookup"><span data-stu-id="62453-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="62453-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62453-125">Request body</span></span>
<span data-ttu-id="62453-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="62453-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="62453-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="62453-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="62453-128">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="62453-128">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="62453-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="62453-129">Property</span></span>     | <span data-ttu-id="62453-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="62453-130">Type</span></span>   |<span data-ttu-id="62453-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="62453-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="62453-132">displayName</span><span class="sxs-lookup"><span data-stu-id="62453-132">displayName</span></span>| <span data-ttu-id="62453-133">String</span><span class="sxs-lookup"><span data-stu-id="62453-133">String</span></span>| <span data-ttu-id="62453-134">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-134">Display Name of User</span></span>|
|<span data-ttu-id="62453-135">givenName</span><span class="sxs-lookup"><span data-stu-id="62453-135">givenName</span></span>| <span data-ttu-id="62453-136">String</span><span class="sxs-lookup"><span data-stu-id="62453-136">String</span></span> | <span data-ttu-id="62453-137">Nombre.</span><span class="sxs-lookup"><span data-stu-id="62453-137">First Name</span></span> |
|<span data-ttu-id="62453-138">middleName</span><span class="sxs-lookup"><span data-stu-id="62453-138">middleName</span></span>| <span data-ttu-id="62453-139">String</span><span class="sxs-lookup"><span data-stu-id="62453-139">String</span></span> | <span data-ttu-id="62453-140">Segundo nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-140">Middle Name of user</span></span>|
|<span data-ttu-id="62453-141">surname</span><span class="sxs-lookup"><span data-stu-id="62453-141">surname</span></span>| <span data-ttu-id="62453-142">String</span><span class="sxs-lookup"><span data-stu-id="62453-142">String</span></span> | <span data-ttu-id="62453-143">Apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-143">Surname of user</span></span>|
|<span data-ttu-id="62453-144">mail</span><span class="sxs-lookup"><span data-stu-id="62453-144">mail</span></span>| <span data-ttu-id="62453-145">String</span><span class="sxs-lookup"><span data-stu-id="62453-145">String</span></span>| <span data-ttu-id="62453-146">Dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="62453-146">email address</span></span>|
|<span data-ttu-id="62453-147">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="62453-147">mobilePhone</span></span>| <span data-ttu-id="62453-148">String</span><span class="sxs-lookup"><span data-stu-id="62453-148">String</span></span> | <span data-ttu-id="62453-149">Número de móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-149">Mobile number of user</span></span> |
|<span data-ttu-id="62453-150">externalSource</span><span class="sxs-lookup"><span data-stu-id="62453-150">externalSource</span></span>|<span data-ttu-id="62453-151">string</span><span class="sxs-lookup"><span data-stu-id="62453-151">string</span></span>| <span data-ttu-id="62453-152">Los valores posibles son: `sis`, `manual`, `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="62453-152">The possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="62453-153">externalSource</span><span class="sxs-lookup"><span data-stu-id="62453-153">externalSource</span></span>|<span data-ttu-id="62453-154">string</span><span class="sxs-lookup"><span data-stu-id="62453-154">string</span></span>| <span data-ttu-id="62453-155">Indica desde dónde se ha creado este usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-155">Where this user was created from.</span></span>  <span data-ttu-id="62453-156">Los valores posibles son: `sis`, `manual`, `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="62453-156">The possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="62453-157">mailingAddress</span><span class="sxs-lookup"><span data-stu-id="62453-157">mailingAddress</span></span>|[<span data-ttu-id="62453-158">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="62453-158">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="62453-159">Dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-159">Mail address of user.</span></span>|
|<span data-ttu-id="62453-160">residenceAddress</span><span class="sxs-lookup"><span data-stu-id="62453-160">residenceAddress</span></span>|[<span data-ttu-id="62453-161">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="62453-161">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="62453-162">Dirección donde reside el usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-162">Address where user lives.</span></span>|
|<span data-ttu-id="62453-163">primaryRole</span><span class="sxs-lookup"><span data-stu-id="62453-163">primaryRole</span></span>|<span data-ttu-id="62453-164">string</span><span class="sxs-lookup"><span data-stu-id="62453-164">string</span></span>| <span data-ttu-id="62453-165">Rol predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="62453-165">Default Role for a user.</span></span>  <span data-ttu-id="62453-166">Puede que el rol del usuario sea distinto en una clase individual.</span><span class="sxs-lookup"><span data-stu-id="62453-166">The user's role might be different in an individual class.</span></span> <span data-ttu-id="62453-167">Los valores posibles son: `student`, `teacher`, `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="62453-167">The possible values are: `student`, `teacher`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="62453-168">student</span><span class="sxs-lookup"><span data-stu-id="62453-168">student</span></span>|[<span data-ttu-id="62453-169">educationStudent</span><span class="sxs-lookup"><span data-stu-id="62453-169">educationStudent</span></span>](../resources/educationstudent.md)| <span data-ttu-id="62453-170">Si el rol principal es alumno, este bloque contendrá datos específicos de alumnos.</span><span class="sxs-lookup"><span data-stu-id="62453-170">If the primary role is student, this block will contain student specific data.</span></span>|
|<span data-ttu-id="62453-171">teacher</span><span class="sxs-lookup"><span data-stu-id="62453-171">teacher</span></span>|[<span data-ttu-id="62453-172">educationTeacher</span><span class="sxs-lookup"><span data-stu-id="62453-172">educationTeacher</span></span>](../resources/educationteacher.md)| <span data-ttu-id="62453-173">Si el rol principal es profesor, este bloque contendrá datos específicos de profesores.</span><span class="sxs-lookup"><span data-stu-id="62453-173">If the primary role is teacher, this block will conatin teacher specific data.</span></span>|


## <a name="response"></a><span data-ttu-id="62453-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62453-174">Response</span></span>
<span data-ttu-id="62453-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [educationUser](../resources/educationuser.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62453-175">If successful, this method returns a `200 OK` response code and updated [educationUser](../resources/educationuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="62453-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62453-176">Example</span></span>
##### <a name="request"></a><span data-ttu-id="62453-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="62453-177">Request</span></span>
<span data-ttu-id="62453-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62453-178">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="62453-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62453-179">Response</span></span>
<span data-ttu-id="62453-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62453-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
