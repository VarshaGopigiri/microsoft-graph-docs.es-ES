---
title: Actualizar bookingbusiness
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: c0d92e0ddf792e28cb488cf466a1462272086c8f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085042"
---
# <a name="update-bookingbusiness"></a><span data-ttu-id="f7402-104">Actualizar bookingbusiness</span><span class="sxs-lookup"><span data-stu-id="f7402-104">Update bookingbusiness</span></span>

 > <span data-ttu-id="f7402-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f7402-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f7402-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f7402-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="f7402-107">Actualizar las propiedades de un objeto [bookingBusiness](../resources/bookingbusiness.md) .</span><span class="sxs-lookup"><span data-stu-id="f7402-107">Update the properties of a [bookingBusiness](../resources/bookingbusiness.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="f7402-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="f7402-108">Permissions</span></span>
<span data-ttu-id="f7402-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f7402-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f7402-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7402-111">Permission type</span></span>      | <span data-ttu-id="f7402-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7402-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f7402-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7402-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="f7402-114">Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="f7402-114">Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="f7402-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7402-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f7402-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7402-116">Not supported.</span></span>   |
|<span data-ttu-id="f7402-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7402-117">Application</span></span> | <span data-ttu-id="f7402-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7402-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="f7402-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7402-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /bookingBusinesses/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="f7402-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="f7402-120">Optional request headers</span></span>
| <span data-ttu-id="f7402-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7402-121">Name</span></span>       | <span data-ttu-id="f7402-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7402-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="f7402-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f7402-123">Authorization</span></span>  | <span data-ttu-id="f7402-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="f7402-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="f7402-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7402-125">Request body</span></span>
<span data-ttu-id="f7402-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="f7402-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="f7402-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f7402-129">Property</span></span>     | <span data-ttu-id="f7402-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7402-130">Type</span></span>   |<span data-ttu-id="f7402-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7402-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f7402-132">address</span><span class="sxs-lookup"><span data-stu-id="f7402-132">address</span></span>|[<span data-ttu-id="f7402-133">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="f7402-133">physicalAddress</span></span>](../resources/physicaladdress.md)|<span data-ttu-id="f7402-134">La dirección de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f7402-134">The street address of the business.</span></span>|
|<span data-ttu-id="f7402-135">businessHours</span><span class="sxs-lookup"><span data-stu-id="f7402-135">businessHours</span></span>|<span data-ttu-id="f7402-136">colección de [bookingWorkHours](../resources/bookingworkhours.md)</span><span class="sxs-lookup"><span data-stu-id="f7402-136">[bookingWorkHours](../resources/bookingworkhours.md) collection</span></span>|<span data-ttu-id="f7402-137">Las horas de operación para la empresa.</span><span class="sxs-lookup"><span data-stu-id="f7402-137">The hours of operation for the business.</span></span>|
|<span data-ttu-id="f7402-138">businessType</span><span class="sxs-lookup"><span data-stu-id="f7402-138">businessType</span></span>|<span data-ttu-id="f7402-139">String</span><span class="sxs-lookup"><span data-stu-id="f7402-139">String</span></span>|<span data-ttu-id="f7402-140">El tipo de negocio.</span><span class="sxs-lookup"><span data-stu-id="f7402-140">The type of business.</span></span>|
|<span data-ttu-id="f7402-141">defaultCurrencyIso</span><span class="sxs-lookup"><span data-stu-id="f7402-141">defaultCurrencyIso</span></span>|<span data-ttu-id="f7402-142">String</span><span class="sxs-lookup"><span data-stu-id="f7402-142">String</span></span>|<span data-ttu-id="f7402-143">El código para la moneda que la empresa opera en Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="f7402-143">The code for the currency that the business operates in on Microsoft Bookings.</span></span>|
|<span data-ttu-id="f7402-144">displayName</span><span class="sxs-lookup"><span data-stu-id="f7402-144">displayName</span></span>|<span data-ttu-id="f7402-145">String</span><span class="sxs-lookup"><span data-stu-id="f7402-145">String</span></span>|<span data-ttu-id="f7402-146">Un nombre para la empresa que interactúa con los clientes.</span><span class="sxs-lookup"><span data-stu-id="f7402-146">A name for the business that interfaces with customers.</span></span>|
|<span data-ttu-id="f7402-147">email</span><span class="sxs-lookup"><span data-stu-id="f7402-147">email</span></span>|<span data-ttu-id="f7402-148">String</span><span class="sxs-lookup"><span data-stu-id="f7402-148">String</span></span>|<span data-ttu-id="f7402-149">La dirección de correo electrónico para el negocio.</span><span class="sxs-lookup"><span data-stu-id="f7402-149">The email address for the business.</span></span>|
|<span data-ttu-id="f7402-150">phone</span><span class="sxs-lookup"><span data-stu-id="f7402-150">phone</span></span>|<span data-ttu-id="f7402-151">String</span><span class="sxs-lookup"><span data-stu-id="f7402-151">String</span></span>|<span data-ttu-id="f7402-152">El número de teléfono para el negocio.</span><span class="sxs-lookup"><span data-stu-id="f7402-152">The telephone number for the business.</span></span>|
|<span data-ttu-id="f7402-153">schedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="f7402-153">schedulingPolicy</span></span>|[<span data-ttu-id="f7402-154">bookingSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="f7402-154">bookingSchedulingPolicy</span></span>](../resources/bookingschedulingpolicy.md)|<span data-ttu-id="f7402-155">Especifica cómo se pueden crear reservas para este negocio.</span><span class="sxs-lookup"><span data-stu-id="f7402-155">Specifies how bookings can be created for this business.</span></span>|
|<span data-ttu-id="f7402-156">webSiteUrl</span><span class="sxs-lookup"><span data-stu-id="f7402-156">webSiteUrl</span></span>|<span data-ttu-id="f7402-157">String</span><span class="sxs-lookup"><span data-stu-id="f7402-157">String</span></span>|<span data-ttu-id="f7402-158">La dirección URL del sitio web de negocio.</span><span class="sxs-lookup"><span data-stu-id="f7402-158">The URL of the business web site.</span></span>|

## <a name="response"></a><span data-ttu-id="f7402-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7402-159">Response</span></span>
<span data-ttu-id="f7402-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7402-p105">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f7402-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7402-162">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f7402-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7402-163">Request</span></span>
<span data-ttu-id="f7402-164">En el ejemplo siguiente se actualiza la dirección de correo electrónico del trabajo y programación de directiva, para cambiar el intervalo de tiempo de reserva de negocio predeterminado para una hora y avance hasta 30 días de reserva.</span><span class="sxs-lookup"><span data-stu-id="f7402-164">The following example updates the business email address and scheduling policy, to change the business default booking time slot to an hour, and advance booking up to 30 days.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_bookingbusiness"
}-->
```http
PATCH https://graph.microsoft.com/beta/bookingBusinesses/fabrikam@M365B489948.onmicrosoft.com
Content-type: application/json

{
  "email": "admin@fabrikam.com",
  "schedulingPolicy": {
      "timeSlotInterval": "PT60M",
      "minimumLeadTime": "P1D",
      "maximumAdvance": "P30D",
      "sendConfirmationsToOwner": true,
      "allowStaffSelection": true
  }
}
```
##### <a name="response"></a><span data-ttu-id="f7402-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7402-165">Response</span></span>
<span data-ttu-id="f7402-166">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7402-166">The following is an example of the response.</span></span> <span data-ttu-id="f7402-167">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f7402-167">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f7402-168">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f7402-168">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update bookingbusiness",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->