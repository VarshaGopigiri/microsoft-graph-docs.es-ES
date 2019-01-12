---
title: Clientes de la lista
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: de40a68981c7cf158b9082e93124f119d44d3ca0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946920"
---
# <a name="list-customers"></a><span data-ttu-id="e6a6b-104">Clientes de la lista</span><span class="sxs-lookup"><span data-stu-id="e6a6b-104">List customers</span></span>

 > <span data-ttu-id="e6a6b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6a6b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="e6a6b-107">Obtener una lista de objetos de [bookingCustomer](../resources/bookingcustomer.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a6b-107">Get a list of [bookingCustomer](../resources/bookingcustomer.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="e6a6b-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="e6a6b-108">Permissions</span></span>
<span data-ttu-id="e6a6b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6a6b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6a6b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6a6b-111">Permission type</span></span>      | <span data-ttu-id="e6a6b-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6a6b-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e6a6b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6a6b-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="e6a6b-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="e6a6b-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="e6a6b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6a6b-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e6a6b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-116">Not supported.</span></span>   |
|<span data-ttu-id="e6a6b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6a6b-117">Application</span></span> | <span data-ttu-id="e6a6b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-118">Not supported.</span></span>  |  

## <a name="http-request"></a><span data-ttu-id="e6a6b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6a6b-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses/{id}/customers
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e6a6b-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e6a6b-120">Optional query parameters</span></span>
<span data-ttu-id="e6a6b-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e6a6b-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a6b-122">Request headers</span></span>
| <span data-ttu-id="e6a6b-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6a6b-123">Name</span></span>      |<span data-ttu-id="e6a6b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6a6b-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="e6a6b-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="e6a6b-125">Authorization</span></span>  | <span data-ttu-id="e6a6b-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="e6a6b-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6a6b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a6b-127">Request body</span></span>
<span data-ttu-id="e6a6b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="e6a6b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6a6b-129">Response</span></span>
<span data-ttu-id="e6a6b-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [bookingCustomer](../resources/bookingcustomer.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-130">If successful, this method returns a `200 OK` response code and collection of [bookingCustomer](../resources/bookingcustomer.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e6a6b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6a6b-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e6a6b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a6b-132">Request</span></span>
<span data-ttu-id="e6a6b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_customers"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/customers
```
##### <a name="response"></a><span data-ttu-id="e6a6b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6a6b-134">Response</span></span>
<span data-ttu-id="e6a6b-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-135">The following is an example of the response.</span></span> <span data-ttu-id="e6a6b-136">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-136">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="e6a6b-137">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-137">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCustomer",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/customers",
    "value": [
        {
            "id": "80b5ddda-1e3b-4c9d-abe2-d606cc075e2e",
            "displayName": "Adele Vance",
            "emailAddress": "adelev@proseware.com"
        },
        {
            "id": "8bb19078-0f45-4efb-b2c5-da78b860f73a",
            "displayName": "Adele Vance",
            "emailAddress": "adelev@proseware.com"
        },
        {
            "id": "829e3cb5-3d4d-4319-a8de-1953aedaa166",
            "displayName": "Bob Kelly",
            "emailAddress": "bobk@tailspintoys.com"
        },
        {
            "id": "7ed53fa5-9ef2-4f2f-975b-27447440bc09",
            "displayName": "Jordan Miller",
            "emailAddress": "jordanm@contoso.com"
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List customers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
