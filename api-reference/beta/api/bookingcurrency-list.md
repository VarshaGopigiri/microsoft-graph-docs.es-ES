---
title: Lista bookingCurrencies
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: e08385c887b1da6972caab83da068b0e537586db
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941523"
---
# <a name="list-bookingcurrencies"></a><span data-ttu-id="1c001-104">Lista bookingCurrencies</span><span class="sxs-lookup"><span data-stu-id="1c001-104">List bookingCurrencies</span></span>

 > <span data-ttu-id="1c001-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c001-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1c001-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1c001-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="1c001-107">Obtener una lista de objetos de [bookingCurrency](../resources/bookingcurrency.md) disponibles para una empresa de Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="1c001-107">Get a list of [bookingCurrency](../resources/bookingcurrency.md) objects available to a Microsoft Bookings business.</span></span>
## <a name="permissions"></a><span data-ttu-id="1c001-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="1c001-108">Permissions</span></span>
<span data-ttu-id="1c001-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c001-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1c001-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c001-111">Permission type</span></span>      | <span data-ttu-id="1c001-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c001-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1c001-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c001-113">Delegated (work or school account)</span></span> | <span data-ttu-id="1c001-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="1c001-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="1c001-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c001-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1c001-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c001-116">Not supported.</span></span>   |
|<span data-ttu-id="1c001-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c001-117">Application</span></span> | <span data-ttu-id="1c001-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c001-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="1c001-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c001-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingCurrencies
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1c001-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1c001-120">Optional query parameters</span></span>
<span data-ttu-id="1c001-121">Este método es compatible con los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta, incluida la $count, $filter, $select, $skip y $top.</span><span class="sxs-lookup"><span data-stu-id="1c001-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response, including $count, $filter, $select, $skip, and $top.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1c001-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c001-122">Request headers</span></span>
| <span data-ttu-id="1c001-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c001-123">Name</span></span>      |<span data-ttu-id="1c001-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c001-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1c001-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="1c001-125">Authorization</span></span>  | <span data-ttu-id="1c001-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="1c001-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="1c001-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c001-127">Request body</span></span>
<span data-ttu-id="1c001-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1c001-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="1c001-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c001-129">Response</span></span>
<span data-ttu-id="1c001-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [bookingCurrency](../resources/bookingcurrency.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c001-130">If successful, this method returns a `200 OK` response code and collection of [bookingCurrency](../resources/bookingcurrency.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1c001-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c001-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1c001-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c001-132">Request</span></span>
<span data-ttu-id="1c001-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c001-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_bookingcurrencies"
}-->
```http
GET https://graph.microsoft.com/beta/bookingCurrencies
```
##### <a name="response"></a><span data-ttu-id="1c001-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c001-134">Response</span></span>
<span data-ttu-id="1c001-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c001-135">The following is an example of the response.</span></span> <span data-ttu-id="1c001-136">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="1c001-136">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="1c001-137">Se devolverán todas las monedas compatibles y las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c001-137">All of the supported currencies and properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCurrency",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#bookingCurrencies",
    "value":[
        {
            "id":"AED",
            "symbol":"د.إ.‏"
        },
        {
            "id":"AFN",
            "symbol":"؋"
        },
        {
            "id":"ALL",
            "symbol":"Lekë"
        },
        {
            "id":"AMD",
            "symbol":"֏"
        },
        {
            "id":"USD",
            "symbol":"$"
        },
        {
            "id":"YER",
            "symbol":"ر.ي.‏"
        },
        {
            "id":"ZAR",
            "symbol":"R"
        },
        {
            "id":"ZMW",
            "symbol":"K"
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List bookingCurrencies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
