---
title: Crear bookingCustomer
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 555723fdb4eb7bacb2c876ed3fd87eb539a5239d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922259"
---
# <a name="create-bookingcustomer"></a><span data-ttu-id="37e10-104">Crear bookingCustomer</span><span class="sxs-lookup"><span data-stu-id="37e10-104">Create bookingCustomer</span></span>

 > <span data-ttu-id="37e10-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37e10-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37e10-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37e10-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="37e10-107">Crear un nuevo objeto [bookingCustomer](../resources/bookingcustomer.md) .</span><span class="sxs-lookup"><span data-stu-id="37e10-107">Create a new [bookingCustomer](../resources/bookingcustomer.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="37e10-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="37e10-108">Permissions</span></span>
<span data-ttu-id="37e10-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37e10-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37e10-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37e10-111">Permission type</span></span>      | <span data-ttu-id="37e10-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37e10-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="37e10-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37e10-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="37e10-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="37e10-114">BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="37e10-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37e10-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="37e10-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37e10-116">Not supported.</span></span>   |
|<span data-ttu-id="37e10-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37e10-117">Application</span></span> | <span data-ttu-id="37e10-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37e10-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="37e10-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37e10-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /bookingBusinesses/{id}/customers

```
## <a name="request-headers"></a><span data-ttu-id="37e10-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37e10-120">Request headers</span></span>
| <span data-ttu-id="37e10-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="37e10-121">Name</span></span>       | <span data-ttu-id="37e10-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="37e10-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="37e10-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="37e10-123">Authorization</span></span>  | <span data-ttu-id="37e10-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="37e10-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="37e10-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37e10-125">Request body</span></span>
<span data-ttu-id="37e10-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingCustomer](../resources/bookingcustomer.md) .</span><span class="sxs-lookup"><span data-stu-id="37e10-126">In the request body, supply a JSON representation of [bookingCustomer](../resources/bookingcustomer.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="37e10-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37e10-127">Response</span></span>
<span data-ttu-id="37e10-128">Si tiene éxito, este método devuelve `201, Created` objeto de código y [bookingCustomer](../resources/bookingcustomer.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37e10-128">If successful, this method returns `201, Created` response code and [bookingCustomer](../resources/bookingcustomer.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37e10-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37e10-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="37e10-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37e10-130">Request</span></span>
<span data-ttu-id="37e10-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37e10-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_bookingcustomer_from_bookingbusiness"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/customers

Content-type: application/json

{
    "displayName": "Joni Sherman",
    "emailAddress": "jonis@relecloud.com"
}
```
<span data-ttu-id="37e10-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingCustomer](../resources/bookingcustomer.md) .</span><span class="sxs-lookup"><span data-stu-id="37e10-132">In the request body, supply a JSON representation of [bookingCustomer](../resources/bookingcustomer.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="37e10-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37e10-133">Response</span></span>
<span data-ttu-id="37e10-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37e10-134">The following is an example of the response.</span></span> <span data-ttu-id="37e10-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="37e10-135">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="37e10-136">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37e10-136">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCustomer"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/customers/$entity",
    "id": "36038f36-634e-44e4-9415-d7d59c2347aa",
    "displayName": "Joni Sherman",
    "emailAddress": "jonis@relecloud.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create bookingCustomer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
