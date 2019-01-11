---
title: Actualizar bookingcustomer
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: ccfd7d496f796ea71568a58d48e62ed84c29abc4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844348"
---
# <a name="update-bookingcustomer"></a><span data-ttu-id="49ea3-104">Actualizar bookingcustomer</span><span class="sxs-lookup"><span data-stu-id="49ea3-104">Update bookingcustomer</span></span>

 > <span data-ttu-id="49ea3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="49ea3-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="49ea3-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="49ea3-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="49ea3-107">Actualizar las propiedades de un objeto [bookingCustomer](../resources/bookingcustomer.md) .</span><span class="sxs-lookup"><span data-stu-id="49ea3-107">Update the properties of a [bookingCustomer](../resources/bookingcustomer.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="49ea3-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="49ea3-108">Permissions</span></span>
<span data-ttu-id="49ea3-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49ea3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="49ea3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49ea3-111">Permission type</span></span>      | <span data-ttu-id="49ea3-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="49ea3-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="49ea3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49ea3-113">Delegated (work or school account)</span></span> | <span data-ttu-id="49ea3-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="49ea3-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="49ea3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49ea3-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="49ea3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49ea3-116">Not supported.</span></span>   |
|<span data-ttu-id="49ea3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49ea3-117">Application</span></span> | <span data-ttu-id="49ea3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49ea3-118">Not supported.</span></span>  |  

## <a name="http-request"></a><span data-ttu-id="49ea3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49ea3-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /bookingBusinesses/{id}/customers/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="49ea3-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="49ea3-120">Optional request headers</span></span>
| <span data-ttu-id="49ea3-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="49ea3-121">Name</span></span>       | <span data-ttu-id="49ea3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ea3-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="49ea3-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="49ea3-123">Authorization</span></span>  | <span data-ttu-id="49ea3-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="49ea3-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="49ea3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49ea3-125">Request body</span></span>
<span data-ttu-id="49ea3-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="49ea3-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="49ea3-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="49ea3-129">Property</span></span>     | <span data-ttu-id="49ea3-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="49ea3-130">Type</span></span>   |<span data-ttu-id="49ea3-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ea3-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="49ea3-132">displayName</span><span class="sxs-lookup"><span data-stu-id="49ea3-132">displayName</span></span>|<span data-ttu-id="49ea3-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="49ea3-133">String</span></span>|<span data-ttu-id="49ea3-134">El nombre del cliente.</span><span class="sxs-lookup"><span data-stu-id="49ea3-134">The name of the customer.</span></span>|
|<span data-ttu-id="49ea3-135">emailAddress</span><span class="sxs-lookup"><span data-stu-id="49ea3-135">emailAddress</span></span>|<span data-ttu-id="49ea3-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="49ea3-136">String</span></span>|<span data-ttu-id="49ea3-137">La dirección SMTP del cliente.</span><span class="sxs-lookup"><span data-stu-id="49ea3-137">The SMTP address of the customer.</span></span>|

## <a name="response"></a><span data-ttu-id="49ea3-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49ea3-138">Response</span></span>
<span data-ttu-id="49ea3-139">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [bookingCustomer](../resources/bookingcustomer.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49ea3-139">If successful, this method returns a `200 OK` response code and updated [bookingCustomer](../resources/bookingcustomer.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="49ea3-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49ea3-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="49ea3-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49ea3-141">Request</span></span>
<span data-ttu-id="49ea3-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ea3-142">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_bookingcustomer"
}-->
```http
PATCH https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/customers/8bb19078-0f45-4efb-b2c5-da78b860f73a
Content-type: application/json

{
    "displayName": "Adele",
    "emailAddress": "adele@relecloud.com"
}
```
##### <a name="response"></a><span data-ttu-id="49ea3-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49ea3-143">Response</span></span>
<span data-ttu-id="49ea3-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49ea3-144">The following is an example of the response.</span></span> <span data-ttu-id="49ea3-145">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="49ea3-145">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="49ea3-146">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="49ea3-146">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCustomer"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/customers/$entity",
    "id": "8bb19078-0f45-4efb-b2c5-da78b860f73a",
    "displayName": "Adele",
    "emailAddress": "adele@relecloud.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update bookingcustomer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
