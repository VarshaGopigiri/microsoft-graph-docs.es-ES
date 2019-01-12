---
title: Actualizar propiedades de educationschool
description: Actualice las propiedades de un objeto de centro educativo.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 3f44d6f8de1685c0c825be8781c1450baad5231e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975802"
---
# <a name="update-educationschool-properties"></a><span data-ttu-id="715ce-103">Actualizar propiedades de educationschool</span><span class="sxs-lookup"><span data-stu-id="715ce-103">Update educationschool properties</span></span>

> <span data-ttu-id="715ce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="715ce-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="715ce-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="715ce-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="715ce-106">Actualice las propiedades de un objeto de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="715ce-106">Update the properties of a school object.</span></span>

## <a name="permissions"></a><span data-ttu-id="715ce-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="715ce-107">Permissions</span></span>
<span data-ttu-id="715ce-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="715ce-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="715ce-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="715ce-110">Permission type</span></span>      | <span data-ttu-id="715ce-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="715ce-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="715ce-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="715ce-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="715ce-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="715ce-113">Not supported.</span></span>  |
|<span data-ttu-id="715ce-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="715ce-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="715ce-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="715ce-115">Not supported.</span></span>  |
|<span data-ttu-id="715ce-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="715ce-116">Application</span></span> | <span data-ttu-id="715ce-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="715ce-117">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="715ce-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="715ce-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/schools/{id}
```
## <a name="request-headers"></a><span data-ttu-id="715ce-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="715ce-119">Request headers</span></span>
| <span data-ttu-id="715ce-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="715ce-120">Header</span></span>       | <span data-ttu-id="715ce-121">Valor</span><span class="sxs-lookup"><span data-stu-id="715ce-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="715ce-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="715ce-122">Authorization</span></span>  | <span data-ttu-id="715ce-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="715ce-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="715ce-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="715ce-125">Content-Type</span></span>  | <span data-ttu-id="715ce-126">application/json</span><span class="sxs-lookup"><span data-stu-id="715ce-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="715ce-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="715ce-127">Request body</span></span>
<span data-ttu-id="715ce-128">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="715ce-128">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="715ce-129">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="715ce-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="715ce-130">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="715ce-130">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="715ce-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="715ce-131">Property</span></span>     | <span data-ttu-id="715ce-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="715ce-132">Type</span></span>   |<span data-ttu-id="715ce-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="715ce-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="715ce-134">displayName</span><span class="sxs-lookup"><span data-stu-id="715ce-134">displayName</span></span>| <span data-ttu-id="715ce-135">String</span><span class="sxs-lookup"><span data-stu-id="715ce-135">String</span></span>| <span data-ttu-id="715ce-136">Nombre para mostrar del centro educativo</span><span class="sxs-lookup"><span data-stu-id="715ce-136">Display name of the school</span></span>| 
|<span data-ttu-id="715ce-137">description</span><span class="sxs-lookup"><span data-stu-id="715ce-137">description</span></span>| <span data-ttu-id="715ce-138">String</span><span class="sxs-lookup"><span data-stu-id="715ce-138">String</span></span> | <span data-ttu-id="715ce-139">Descripción del centro educativo</span><span class="sxs-lookup"><span data-stu-id="715ce-139">Description of the school</span></span>| 
|<span data-ttu-id="715ce-140">principalEmail</span><span class="sxs-lookup"><span data-stu-id="715ce-140">principalEmail</span></span>| <span data-ttu-id="715ce-141">String</span><span class="sxs-lookup"><span data-stu-id="715ce-141">String</span></span>| <span data-ttu-id="715ce-142">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="715ce-142">Email address of the principal</span></span>|
|<span data-ttu-id="715ce-143">principalName</span><span class="sxs-lookup"><span data-stu-id="715ce-143">principalName</span></span>| <span data-ttu-id="715ce-144">String</span><span class="sxs-lookup"><span data-stu-id="715ce-144">String</span></span> | <span data-ttu-id="715ce-145">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="715ce-145">Name of the principal</span></span>|
|<span data-ttu-id="715ce-146">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="715ce-146">externalPrincipalId</span></span>| <span data-ttu-id="715ce-147">String</span><span class="sxs-lookup"><span data-stu-id="715ce-147">String</span></span> | <span data-ttu-id="715ce-148">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="715ce-148">Id of principal in syncing system.</span></span> |
|<span data-ttu-id="715ce-149">highestGrade</span><span class="sxs-lookup"><span data-stu-id="715ce-149">highestGrade</span></span>|<span data-ttu-id="715ce-150">String</span><span class="sxs-lookup"><span data-stu-id="715ce-150">String</span></span>| <span data-ttu-id="715ce-151">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="715ce-151">Highest grade taught.</span></span> |
|<span data-ttu-id="715ce-152">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="715ce-152">lowestGrade</span></span>|<span data-ttu-id="715ce-153">String</span><span class="sxs-lookup"><span data-stu-id="715ce-153">String</span></span>| <span data-ttu-id="715ce-154">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="715ce-154">Lowest grade taught.</span></span> |
|<span data-ttu-id="715ce-155">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="715ce-155">schoolNumber</span></span>|<span data-ttu-id="715ce-156">String</span><span class="sxs-lookup"><span data-stu-id="715ce-156">String</span></span>| <span data-ttu-id="715ce-157">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="715ce-157">School Number.</span></span>|
|<span data-ttu-id="715ce-158">externalId</span><span class="sxs-lookup"><span data-stu-id="715ce-158">externalId</span></span>|<span data-ttu-id="715ce-159">String</span><span class="sxs-lookup"><span data-stu-id="715ce-159">String</span></span>| <span data-ttu-id="715ce-160">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="715ce-160">Id of school in syncing system.</span></span> |
|<span data-ttu-id="715ce-161">phone</span><span class="sxs-lookup"><span data-stu-id="715ce-161">phone</span></span>|<span data-ttu-id="715ce-162">String</span><span class="sxs-lookup"><span data-stu-id="715ce-162">String</span></span>| <span data-ttu-id="715ce-163">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="715ce-163">Phone number of school.</span></span> |
|<span data-ttu-id="715ce-164">fax</span><span class="sxs-lookup"><span data-stu-id="715ce-164">fax</span></span>|<span data-ttu-id="715ce-165">String</span><span class="sxs-lookup"><span data-stu-id="715ce-165">String</span></span>| <span data-ttu-id="715ce-166">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="715ce-166">Fax number of school.</span></span> |
|<span data-ttu-id="715ce-167">address</span><span class="sxs-lookup"><span data-stu-id="715ce-167">address</span></span>|[<span data-ttu-id="715ce-168">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="715ce-168">physicalAddress</span></span>](../resources/physicaladdress.md)| <span data-ttu-id="715ce-169">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="715ce-169">Address of the School.</span></span>|
|<span data-ttu-id="715ce-170">createdBy</span><span class="sxs-lookup"><span data-stu-id="715ce-170">createdBy</span></span>|[<span data-ttu-id="715ce-171">identitySet</span><span class="sxs-lookup"><span data-stu-id="715ce-171">identitySet</span></span>](../resources/identityset.md)|<span data-ttu-id="715ce-172">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="715ce-172">Entity who created the school.</span></span>|

## <a name="response"></a><span data-ttu-id="715ce-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="715ce-173">Response</span></span>
<span data-ttu-id="715ce-174">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationSchool](../resources/educationschool.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="715ce-174">If successful, this method returns a `200 OK` response code and an updated [educationSchool](../resources/educationschool.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="715ce-175">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="715ce-175">Example</span></span>
##### <a name="request"></a><span data-ttu-id="715ce-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="715ce-176">Request</span></span>
<span data-ttu-id="715ce-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="715ce-177">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationschool"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/schools/10002
Content-type: application/json
Content-length: 292

{
  "displayName": "Fabrikam Arts High School",
  "description": "Magnate school for the arts. Los Angeles School District"
}
```
##### <a name="response"></a><span data-ttu-id="715ce-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="715ce-178">Response</span></span>
<span data-ttu-id="715ce-179">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="715ce-179">The following is an example of the response.</span></span> 

><span data-ttu-id="715ce-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="715ce-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
