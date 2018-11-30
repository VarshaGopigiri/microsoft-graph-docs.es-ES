---
title: Actualizar orgcontact
description: Actualizar las propiedades del objeto orgcontact.
ms.openlocfilehash: 04bc5bef07fb49c2c4fe730e89517de2f364628a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085370"
---
# <a name="update-orgcontact"></a><span data-ttu-id="c2677-103">Actualizar orgcontact</span><span class="sxs-lookup"><span data-stu-id="c2677-103">Update orgcontact</span></span>

> <span data-ttu-id="c2677-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2677-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2677-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2677-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c2677-106">Actualizar las propiedades del objeto orgcontact.</span><span class="sxs-lookup"><span data-stu-id="c2677-106">Update the properties of orgcontact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c2677-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2677-107">Permissions</span></span>
<span data-ttu-id="c2677-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2677-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2677-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2677-110">Permission type</span></span>      | <span data-ttu-id="c2677-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2677-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2677-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2677-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c2677-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2677-113">Not supported.</span></span>    |
|<span data-ttu-id="c2677-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2677-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2677-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2677-115">Not supported.</span></span>    |
|<span data-ttu-id="c2677-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2677-116">Application</span></span> | <span data-ttu-id="c2677-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2677-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2677-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2677-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c2677-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2677-119">Request headers</span></span>
| <span data-ttu-id="c2677-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2677-120">Name</span></span>       | <span data-ttu-id="c2677-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2677-121">Type</span></span> | <span data-ttu-id="c2677-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2677-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c2677-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2677-123">Authorization</span></span>  | <span data-ttu-id="c2677-124">string</span><span class="sxs-lookup"><span data-stu-id="c2677-124">string</span></span>  | <span data-ttu-id="c2677-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2677-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c2677-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2677-127">Request body</span></span>
<span data-ttu-id="c2677-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c2677-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c2677-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2677-131">Property</span></span>     | <span data-ttu-id="c2677-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2677-132">Type</span></span>   |<span data-ttu-id="c2677-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2677-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c2677-134">city</span><span class="sxs-lookup"><span data-stu-id="c2677-134">city</span></span>|<span data-ttu-id="c2677-135">String</span><span class="sxs-lookup"><span data-stu-id="c2677-135">String</span></span>||
|<span data-ttu-id="c2677-136">country</span><span class="sxs-lookup"><span data-stu-id="c2677-136">country</span></span>|<span data-ttu-id="c2677-137">String</span><span class="sxs-lookup"><span data-stu-id="c2677-137">String</span></span>||
|<span data-ttu-id="c2677-138">department</span><span class="sxs-lookup"><span data-stu-id="c2677-138">department</span></span>|<span data-ttu-id="c2677-139">String</span><span class="sxs-lookup"><span data-stu-id="c2677-139">String</span></span>||
|<span data-ttu-id="c2677-140">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="c2677-140">onPremisesSyncEnabled</span></span>|<span data-ttu-id="c2677-141">Booleano</span><span class="sxs-lookup"><span data-stu-id="c2677-141">Boolean</span></span>||
|<span data-ttu-id="c2677-142">displayName</span><span class="sxs-lookup"><span data-stu-id="c2677-142">displayName</span></span>|<span data-ttu-id="c2677-143">String</span><span class="sxs-lookup"><span data-stu-id="c2677-143">String</span></span>||
|<span data-ttu-id="c2677-144">givenName</span><span class="sxs-lookup"><span data-stu-id="c2677-144">givenName</span></span>|<span data-ttu-id="c2677-145">String</span><span class="sxs-lookup"><span data-stu-id="c2677-145">String</span></span>||
|<span data-ttu-id="c2677-146">jobTitle</span><span class="sxs-lookup"><span data-stu-id="c2677-146">jobTitle</span></span>|<span data-ttu-id="c2677-147">String</span><span class="sxs-lookup"><span data-stu-id="c2677-147">String</span></span>||
|<span data-ttu-id="c2677-148">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="c2677-148">onPremisesLastSyncDateTime</span></span>|<span data-ttu-id="c2677-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c2677-149">DateTimeOffset</span></span>||
|<span data-ttu-id="c2677-150">mail</span><span class="sxs-lookup"><span data-stu-id="c2677-150">mail</span></span>|<span data-ttu-id="c2677-151">String</span><span class="sxs-lookup"><span data-stu-id="c2677-151">String</span></span>||
|<span data-ttu-id="c2677-152">mailNickname</span><span class="sxs-lookup"><span data-stu-id="c2677-152">mailNickname</span></span>|<span data-ttu-id="c2677-153">String</span><span class="sxs-lookup"><span data-stu-id="c2677-153">String</span></span>||
|<span data-ttu-id="c2677-154">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="c2677-154">mobilePhone</span></span>|<span data-ttu-id="c2677-155">String</span><span class="sxs-lookup"><span data-stu-id="c2677-155">String</span></span>||
|<span data-ttu-id="c2677-156">officeLocation</span><span class="sxs-lookup"><span data-stu-id="c2677-156">officeLocation</span></span>|<span data-ttu-id="c2677-157">String</span><span class="sxs-lookup"><span data-stu-id="c2677-157">String</span></span>||
|<span data-ttu-id="c2677-158">postalCode</span><span class="sxs-lookup"><span data-stu-id="c2677-158">postalCode</span></span>|<span data-ttu-id="c2677-159">String</span><span class="sxs-lookup"><span data-stu-id="c2677-159">String</span></span>||
|<span data-ttu-id="c2677-160">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="c2677-160">proxyAddresses</span></span>|<span data-ttu-id="c2677-161">String</span><span class="sxs-lookup"><span data-stu-id="c2677-161">String</span></span>||
|<span data-ttu-id="c2677-162">state</span><span class="sxs-lookup"><span data-stu-id="c2677-162">state</span></span>|<span data-ttu-id="c2677-163">String</span><span class="sxs-lookup"><span data-stu-id="c2677-163">String</span></span>||
|<span data-ttu-id="c2677-164">streetAddress</span><span class="sxs-lookup"><span data-stu-id="c2677-164">streetAddress</span></span>|<span data-ttu-id="c2677-165">String</span><span class="sxs-lookup"><span data-stu-id="c2677-165">String</span></span>||
|<span data-ttu-id="c2677-166">surname</span><span class="sxs-lookup"><span data-stu-id="c2677-166">surname</span></span>|<span data-ttu-id="c2677-167">String</span><span class="sxs-lookup"><span data-stu-id="c2677-167">String</span></span>||
|<span data-ttu-id="c2677-168">businessPhones</span><span class="sxs-lookup"><span data-stu-id="c2677-168">businessPhones</span></span>|<span data-ttu-id="c2677-169">String</span><span class="sxs-lookup"><span data-stu-id="c2677-169">String</span></span>||

## <a name="response"></a><span data-ttu-id="c2677-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2677-170">Response</span></span>

<span data-ttu-id="c2677-171">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [orgContact](../resources/orgcontact.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2677-171">If successful, this method returns a `200 OK` response code and updated [orgContact](../resources/orgcontact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c2677-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2677-172">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c2677-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2677-173">Request</span></span>
<span data-ttu-id="c2677-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2677-174">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_orgcontact"
}-->
```http
PATCH https://graph.microsoft.com/beta/contacts/{id}
Content-type: application/json
Content-length: 222

{
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "companyName": "companyName-value",
  "country": "country-value",
  "department": "department-value",
  "displayName": "displayName-value"
}
```
##### <a name="response"></a><span data-ttu-id="c2677-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2677-175">Response</span></span>
<span data-ttu-id="c2677-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2677-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.orgcontact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 222

{
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "companyName": "companyName-value",
  "country": "country-value",
  "department": "department-value",
  "displayName": "displayName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update orgcontact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->