---
title: Eliminar bookingAppointment
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 076c08b240ee3bd9b0648a000f1399fa2f6060b3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083702"
---
# <a name="delete-bookingappointment"></a><span data-ttu-id="ff223-104">Eliminar bookingAppointment</span><span class="sxs-lookup"><span data-stu-id="ff223-104">Delete bookingAppointment</span></span>

 > <span data-ttu-id="ff223-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff223-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff223-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff223-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="ff223-107">Eliminar un [bookingAppointment](../resources/bookingappointment.md) en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="ff223-107">Delete a [bookingAppointment](../resources/bookingappointment.md) in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="ff223-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ff223-108">Permissions</span></span>
<span data-ttu-id="ff223-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ff223-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ff223-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff223-111">Permission type</span></span>      | <span data-ttu-id="ff223-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ff223-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ff223-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff223-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="ff223-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="ff223-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="ff223-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff223-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ff223-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff223-116">Not supported.</span></span>   |
|<span data-ttu-id="ff223-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff223-117">Application</span></span> | <span data-ttu-id="ff223-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff223-118">Not supported.</span></span>  |

## <a name="http-request"></a><span data-ttu-id="ff223-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff223-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /bookingBusinesses/{id}/appointments/{id}

```
## <a name="request-headers"></a><span data-ttu-id="ff223-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff223-120">Request headers</span></span>
| <span data-ttu-id="ff223-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff223-121">Name</span></span>       | <span data-ttu-id="ff223-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff223-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ff223-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ff223-123">Authorization</span></span>  | <span data-ttu-id="ff223-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="ff223-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="ff223-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff223-125">Request body</span></span>
<span data-ttu-id="ff223-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ff223-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="ff223-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff223-127">Response</span></span>
<span data-ttu-id="ff223-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff223-p104">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ff223-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff223-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ff223-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff223-131">Request</span></span>
<span data-ttu-id="ff223-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ff223-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_bookingappointment"
}-->
```http
DELETE https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/appointments/AAMkADKqAAA=
```
##### <a name="response"></a><span data-ttu-id="ff223-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff223-133">Response</span></span>
<span data-ttu-id="ff223-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff223-134">The following is an example of the response.</span></span> <span data-ttu-id="ff223-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="ff223-135">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="ff223-136">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ff223-136">All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete bookingAppointment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->