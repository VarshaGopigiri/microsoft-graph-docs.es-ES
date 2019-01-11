---
title: Actualizar propiedades de educationschool
description: Actualice las propiedades de un objeto de centro educativo.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: a0a3ee2ea291cf48224d6dfa6294f0a1e521435c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862282"
---
# <a name="update-educationschool-properties"></a><span data-ttu-id="7455f-103">Actualizar propiedades de educationschool</span><span class="sxs-lookup"><span data-stu-id="7455f-103">Update educationschool properties</span></span>

<span data-ttu-id="7455f-104">Actualice las propiedades de un objeto de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="7455f-104">Update the properties of a school object.</span></span>

## <a name="permissions"></a><span data-ttu-id="7455f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7455f-105">Permissions</span></span>
<span data-ttu-id="7455f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7455f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7455f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7455f-108">Permission type</span></span>      | <span data-ttu-id="7455f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7455f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7455f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7455f-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="7455f-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7455f-111">Not supported.</span></span>  |
|<span data-ttu-id="7455f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7455f-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="7455f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7455f-113">Not supported.</span></span>  |
|<span data-ttu-id="7455f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7455f-114">Application</span></span> | <span data-ttu-id="7455f-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7455f-115">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7455f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7455f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/schools/{id}
```
## <a name="request-headers"></a><span data-ttu-id="7455f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7455f-117">Request headers</span></span>
| <span data-ttu-id="7455f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7455f-118">Header</span></span>       | <span data-ttu-id="7455f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7455f-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7455f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="7455f-120">Authorization</span></span>  | <span data-ttu-id="7455f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7455f-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7455f-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7455f-123">Content-Type</span></span>  | <span data-ttu-id="7455f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7455f-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7455f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7455f-125">Request body</span></span>
<span data-ttu-id="7455f-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="7455f-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="7455f-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7455f-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="7455f-128">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="7455f-128">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="7455f-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7455f-129">Property</span></span>     | <span data-ttu-id="7455f-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="7455f-130">Type</span></span>   |<span data-ttu-id="7455f-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7455f-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7455f-132">displayName</span><span class="sxs-lookup"><span data-stu-id="7455f-132">displayName</span></span>| <span data-ttu-id="7455f-133">String</span><span class="sxs-lookup"><span data-stu-id="7455f-133">String</span></span>| <span data-ttu-id="7455f-134">Nombre para mostrar del centro educativo</span><span class="sxs-lookup"><span data-stu-id="7455f-134">Display name of the school</span></span>| 
|<span data-ttu-id="7455f-135">description</span><span class="sxs-lookup"><span data-stu-id="7455f-135">description</span></span>| <span data-ttu-id="7455f-136">String</span><span class="sxs-lookup"><span data-stu-id="7455f-136">String</span></span> | <span data-ttu-id="7455f-137">Descripción del centro educativo</span><span class="sxs-lookup"><span data-stu-id="7455f-137">Description of the school</span></span>| 
|<span data-ttu-id="7455f-138">principalEmail</span><span class="sxs-lookup"><span data-stu-id="7455f-138">principalEmail</span></span>| <span data-ttu-id="7455f-139">String</span><span class="sxs-lookup"><span data-stu-id="7455f-139">String</span></span>| <span data-ttu-id="7455f-140">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="7455f-140">Email address of the principal</span></span>|
|<span data-ttu-id="7455f-141">principalName</span><span class="sxs-lookup"><span data-stu-id="7455f-141">principalName</span></span>| <span data-ttu-id="7455f-142">String</span><span class="sxs-lookup"><span data-stu-id="7455f-142">String</span></span> | <span data-ttu-id="7455f-143">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="7455f-143">Name of the principal</span></span>|
|<span data-ttu-id="7455f-144">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="7455f-144">externalPrincipalId</span></span>| <span data-ttu-id="7455f-145">String</span><span class="sxs-lookup"><span data-stu-id="7455f-145">String</span></span> | <span data-ttu-id="7455f-146">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="7455f-146">Id of principal in syncing system.</span></span> |
|<span data-ttu-id="7455f-147">highestGrade</span><span class="sxs-lookup"><span data-stu-id="7455f-147">highestGrade</span></span>|<span data-ttu-id="7455f-148">String</span><span class="sxs-lookup"><span data-stu-id="7455f-148">String</span></span>| <span data-ttu-id="7455f-149">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="7455f-149">Highest grade taught.</span></span> |
|<span data-ttu-id="7455f-150">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="7455f-150">lowestGrade</span></span>|<span data-ttu-id="7455f-151">String</span><span class="sxs-lookup"><span data-stu-id="7455f-151">String</span></span>| <span data-ttu-id="7455f-152">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="7455f-152">Lowest grade taught.</span></span> |
|<span data-ttu-id="7455f-153">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="7455f-153">schoolNumber</span></span>|<span data-ttu-id="7455f-154">String</span><span class="sxs-lookup"><span data-stu-id="7455f-154">String</span></span>| <span data-ttu-id="7455f-155">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="7455f-155">School Number.</span></span>|
|<span data-ttu-id="7455f-156">externalId</span><span class="sxs-lookup"><span data-stu-id="7455f-156">externalId</span></span>|<span data-ttu-id="7455f-157">String</span><span class="sxs-lookup"><span data-stu-id="7455f-157">String</span></span>| <span data-ttu-id="7455f-158">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="7455f-158">Id of school in syncing system.</span></span> |
|<span data-ttu-id="7455f-159">phone</span><span class="sxs-lookup"><span data-stu-id="7455f-159">phone</span></span>|<span data-ttu-id="7455f-160">String</span><span class="sxs-lookup"><span data-stu-id="7455f-160">String</span></span>| <span data-ttu-id="7455f-161">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="7455f-161">Phone number of school.</span></span> |
|<span data-ttu-id="7455f-162">fax</span><span class="sxs-lookup"><span data-stu-id="7455f-162">fax</span></span>|<span data-ttu-id="7455f-163">String</span><span class="sxs-lookup"><span data-stu-id="7455f-163">String</span></span>| <span data-ttu-id="7455f-164">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="7455f-164">Fax number of school.</span></span> |
|<span data-ttu-id="7455f-165">address</span><span class="sxs-lookup"><span data-stu-id="7455f-165">address</span></span>|[<span data-ttu-id="7455f-166">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="7455f-166">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="7455f-167">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="7455f-167">Address of the School.</span></span>|
|<span data-ttu-id="7455f-168">createdBy</span><span class="sxs-lookup"><span data-stu-id="7455f-168">createdBy</span></span>|[<span data-ttu-id="7455f-169">identitySet</span><span class="sxs-lookup"><span data-stu-id="7455f-169">identitySet</span></span>](../resources/identityset.md)|<span data-ttu-id="7455f-170">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="7455f-170">Entity who created the school.</span></span>|

## <a name="response"></a><span data-ttu-id="7455f-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7455f-171">Response</span></span>
<span data-ttu-id="7455f-172">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationSchool](../resources/educationschool.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7455f-172">If successful, this method returns a `200 OK` response code and an updated [educationSchool](../resources/educationschool.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7455f-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7455f-173">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7455f-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7455f-174">Request</span></span>
<span data-ttu-id="7455f-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7455f-175">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationschool"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/schools/{school-id}
Content-type: application/json
Content-length: 292

{
  "displayName": "Fabrikam Arts High School",
  "description": "Magnate school for the arts. Los Angeles School District"
}
```
##### <a name="response"></a><span data-ttu-id="7455f-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7455f-176">Response</span></span>
<span data-ttu-id="7455f-177">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7455f-177">The following is an example of the response.</span></span> 

><span data-ttu-id="7455f-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7455f-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
