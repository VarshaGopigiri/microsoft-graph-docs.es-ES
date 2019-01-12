---
title: Actualizar propiedades de educationUser
description: Actualice las propiedades de un objeto **educationuser**.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 0c93ecd601e941cd68f0b6f8d668775e7de3feef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975963"
---
# <a name="update-educationuser-properties"></a><span data-ttu-id="27844-103">Actualizar propiedades de educationUser</span><span class="sxs-lookup"><span data-stu-id="27844-103">Update educationUser properties</span></span>

<span data-ttu-id="27844-104">Actualice las propiedades de un objeto **educationuser**.</span><span class="sxs-lookup"><span data-stu-id="27844-104">Update the properties of an **educationuser** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="27844-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="27844-105">Permissions</span></span>
<span data-ttu-id="27844-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27844-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="27844-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27844-108">Permission type</span></span>      | <span data-ttu-id="27844-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27844-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="27844-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27844-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="27844-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27844-111">Not supported.</span></span>  |
|<span data-ttu-id="27844-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27844-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="27844-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27844-113">Not supported.</span></span>  |
|<span data-ttu-id="27844-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27844-114">Application</span></span> | <span data-ttu-id="27844-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27844-115">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="27844-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27844-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/me
PATCH /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="27844-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27844-117">Request headers</span></span>
| <span data-ttu-id="27844-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27844-118">Header</span></span>       | <span data-ttu-id="27844-119">Valor</span><span class="sxs-lookup"><span data-stu-id="27844-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="27844-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="27844-120">Authorization</span></span>  | <span data-ttu-id="27844-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27844-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="27844-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="27844-123">Content-Type</span></span>  | <span data-ttu-id="27844-124">application/json</span><span class="sxs-lookup"><span data-stu-id="27844-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="27844-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27844-125">Request body</span></span>
<span data-ttu-id="27844-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="27844-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="27844-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="27844-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="27844-128">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="27844-128">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="27844-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27844-129">Property</span></span>     | <span data-ttu-id="27844-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="27844-130">Type</span></span>   |<span data-ttu-id="27844-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="27844-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="27844-132">displayName</span><span class="sxs-lookup"><span data-stu-id="27844-132">displayName</span></span>| <span data-ttu-id="27844-133">String</span><span class="sxs-lookup"><span data-stu-id="27844-133">String</span></span>| <span data-ttu-id="27844-134">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-134">Display Name of User</span></span>|
|<span data-ttu-id="27844-135">givenName</span><span class="sxs-lookup"><span data-stu-id="27844-135">givenName</span></span>| <span data-ttu-id="27844-136">String</span><span class="sxs-lookup"><span data-stu-id="27844-136">String</span></span> | <span data-ttu-id="27844-137">Nombre.</span><span class="sxs-lookup"><span data-stu-id="27844-137">First Name</span></span> |
|<span data-ttu-id="27844-138">middleName</span><span class="sxs-lookup"><span data-stu-id="27844-138">middleName</span></span>| <span data-ttu-id="27844-139">String</span><span class="sxs-lookup"><span data-stu-id="27844-139">String</span></span> | <span data-ttu-id="27844-140">Segundo nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-140">Middle Name of user</span></span>|
|<span data-ttu-id="27844-141">surname</span><span class="sxs-lookup"><span data-stu-id="27844-141">surname</span></span>| <span data-ttu-id="27844-142">String</span><span class="sxs-lookup"><span data-stu-id="27844-142">String</span></span> | <span data-ttu-id="27844-143">Apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-143">Surname of user</span></span>|
|<span data-ttu-id="27844-144">mail</span><span class="sxs-lookup"><span data-stu-id="27844-144">mail</span></span>| <span data-ttu-id="27844-145">String</span><span class="sxs-lookup"><span data-stu-id="27844-145">String</span></span>| <span data-ttu-id="27844-146">Dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="27844-146">email address</span></span>|
|<span data-ttu-id="27844-147">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="27844-147">mobilePhone</span></span>| <span data-ttu-id="27844-148">String</span><span class="sxs-lookup"><span data-stu-id="27844-148">String</span></span> | <span data-ttu-id="27844-149">Número de móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-149">Mobile number of user</span></span> |
|<span data-ttu-id="27844-150">externalSource</span><span class="sxs-lookup"><span data-stu-id="27844-150">externalSource</span></span>|<span data-ttu-id="27844-151">string</span><span class="sxs-lookup"><span data-stu-id="27844-151">string</span></span>| <span data-ttu-id="27844-152">Los valores posibles son: `sis`, `manual`, `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="27844-152">The possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="27844-153">externalSource</span><span class="sxs-lookup"><span data-stu-id="27844-153">externalSource</span></span>|<span data-ttu-id="27844-154">string</span><span class="sxs-lookup"><span data-stu-id="27844-154">string</span></span>| <span data-ttu-id="27844-155">Indica desde dónde se ha creado este usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-155">Where this user was created from.</span></span>  <span data-ttu-id="27844-156">Los valores posibles son: `sis`, `manual`, `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="27844-156">The possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="27844-157">mailingAddress</span><span class="sxs-lookup"><span data-stu-id="27844-157">mailingAddress</span></span>|[<span data-ttu-id="27844-158">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="27844-158">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="27844-159">Dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-159">Mail address of user.</span></span>|
|<span data-ttu-id="27844-160">residenceAddress</span><span class="sxs-lookup"><span data-stu-id="27844-160">residenceAddress</span></span>|[<span data-ttu-id="27844-161">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="27844-161">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="27844-162">Dirección donde reside el usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-162">Address where user lives.</span></span>|
|<span data-ttu-id="27844-163">primaryRole</span><span class="sxs-lookup"><span data-stu-id="27844-163">primaryRole</span></span>|<span data-ttu-id="27844-164">string</span><span class="sxs-lookup"><span data-stu-id="27844-164">string</span></span>| <span data-ttu-id="27844-165">Rol predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="27844-165">Default Role for a user.</span></span>  <span data-ttu-id="27844-166">Puede que el rol del usuario sea distinto en una clase individual.</span><span class="sxs-lookup"><span data-stu-id="27844-166">The user's role might be different in an individual class.</span></span> <span data-ttu-id="27844-167">Los valores posibles son: `student`, `teacher`, `enum_sentinel`.</span><span class="sxs-lookup"><span data-stu-id="27844-167">The possible values are: `student`, `teacher`, `enum_sentinel`.</span></span>|
|<span data-ttu-id="27844-168">student</span><span class="sxs-lookup"><span data-stu-id="27844-168">student</span></span>|[<span data-ttu-id="27844-169">educationStudent</span><span class="sxs-lookup"><span data-stu-id="27844-169">educationStudent</span></span>](../resources/educationstudent.md)| <span data-ttu-id="27844-170">Si el rol principal es alumno, este bloque contendrá datos específicos de alumnos.</span><span class="sxs-lookup"><span data-stu-id="27844-170">If the primary role is student, this block will contain student specific data.</span></span>|
|<span data-ttu-id="27844-171">teacher</span><span class="sxs-lookup"><span data-stu-id="27844-171">teacher</span></span>|[<span data-ttu-id="27844-172">educationTeacher</span><span class="sxs-lookup"><span data-stu-id="27844-172">educationTeacher</span></span>](../resources/educationteacher.md)| <span data-ttu-id="27844-173">Si el rol principal es profesor, este bloque contendrá datos específicos de profesores.</span><span class="sxs-lookup"><span data-stu-id="27844-173">If the primary role is teacher, this block will conatin teacher specific data.</span></span>|


## <a name="response"></a><span data-ttu-id="27844-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27844-174">Response</span></span>
<span data-ttu-id="27844-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [educationUser](../resources/educationuser.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27844-175">If successful, this method returns a `200 OK` response code and updated [educationUser](../resources/educationuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="27844-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27844-176">Example</span></span>
##### <a name="request"></a><span data-ttu-id="27844-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27844-177">Request</span></span>
<span data-ttu-id="27844-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27844-178">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="27844-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27844-179">Response</span></span>
<span data-ttu-id="27844-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27844-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
