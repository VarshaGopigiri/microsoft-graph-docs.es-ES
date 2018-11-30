---
title: 'bookingAppointment: Cancelar'
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 4cd7b511f997f32c134f70a976cd94c2ed910fb1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083092"
---
# <a name="bookingappointment-cancel"></a><span data-ttu-id="51117-104">bookingAppointment: Cancelar</span><span class="sxs-lookup"><span data-stu-id="51117-104">bookingAppointment: cancel</span></span>

 > <span data-ttu-id="51117-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="51117-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="51117-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="51117-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="51117-107">Cancelar el especificado [bookingAppointment](../resources/bookingappointment.md) en el especificado [bookingbusiness](../resources/bookingbusiness.md)y enviar un mensaje para el cliente implicado y los miembros del personal.</span><span class="sxs-lookup"><span data-stu-id="51117-107">Cancel the specified [bookingAppointment](../resources/bookingappointment.md) in the specified [bookingbusiness](../resources/bookingbusiness.md), and send a message to the involved customer and staff members.</span></span>

## <a name="permissions"></a><span data-ttu-id="51117-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="51117-108">Permissions</span></span>
<span data-ttu-id="51117-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51117-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51117-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51117-111">Permission type</span></span>      | <span data-ttu-id="51117-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51117-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="51117-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51117-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="51117-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="51117-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="51117-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51117-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="51117-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51117-116">Not supported.</span></span>   |
|<span data-ttu-id="51117-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51117-117">Application</span></span> | <span data-ttu-id="51117-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51117-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="51117-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51117-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /bookingBusinesses/{id}/appointments/{id}/cancel

```
## <a name="request-headers"></a><span data-ttu-id="51117-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51117-120">Request headers</span></span>
| <span data-ttu-id="51117-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="51117-121">Name</span></span>       | <span data-ttu-id="51117-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="51117-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="51117-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="51117-123">Authorization</span></span>  | <span data-ttu-id="51117-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="51117-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="51117-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51117-125">Request body</span></span>
<span data-ttu-id="51117-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="51117-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="51117-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="51117-127">Parameter</span></span>    | <span data-ttu-id="51117-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="51117-128">Type</span></span>   |<span data-ttu-id="51117-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="51117-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="51117-130">cancellationMessage</span><span class="sxs-lookup"><span data-stu-id="51117-130">cancellationMessage</span></span>|<span data-ttu-id="51117-131">String</span><span class="sxs-lookup"><span data-stu-id="51117-131">String</span></span>|<span data-ttu-id="51117-132">Un mensaje para confirmar con el cliente que se ha cancelado la cita.</span><span class="sxs-lookup"><span data-stu-id="51117-132">A message to acknowledge with the customer that the appointment has been cancelled.</span></span>|

## <a name="response"></a><span data-ttu-id="51117-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51117-133">Response</span></span>
<span data-ttu-id="51117-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51117-p104">If successful, this method returns `204 No content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="51117-136">Si se intenta cancelar una cita que hace anota, este método devuelve `HTTP 404 Not found`.</span><span class="sxs-lookup"><span data-stu-id="51117-136">If you attempt to cancel an appointment that does not exisit, this method returns `HTTP 404 Not found`.</span></span>

## <a name="example"></a><span data-ttu-id="51117-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51117-137">Example</span></span>
<span data-ttu-id="51117-138">Este es un ejemplo de cómo realizar una llamada a esta API.</span><span class="sxs-lookup"><span data-stu-id="51117-138">The following is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="51117-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51117-139">Request</span></span>
<span data-ttu-id="51117-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51117-140">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "bookingappointment_cancel"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/appointments/AAMkADKoAAA=/cancel
Content-type: application/json

{
  "cancellationMessage": "Your appointment has been successfully cancelled. Please call us again."
}
```

##### <a name="response"></a><span data-ttu-id="51117-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51117-141">Response</span></span>
<span data-ttu-id="51117-142">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51117-142">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingAppointment: cancel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->