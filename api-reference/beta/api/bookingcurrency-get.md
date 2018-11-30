---
title: Obtener bookingCurrency
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 14238d40dc61b64ccca976830c68d093f401e214
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084697"
---
# <a name="get-bookingcurrency"></a><span data-ttu-id="5b3c5-104">Obtener bookingCurrency</span><span class="sxs-lookup"><span data-stu-id="5b3c5-104">Get bookingCurrency</span></span>

 > <span data-ttu-id="5b3c5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5b3c5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="5b3c5-107">Obtener las propiedades de un objeto [bookingCurrency](../resources/bookingcurrency.md) que está disponible para una empresa de Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-107">Get the properties of a [bookingCurrency](../resources/bookingcurrency.md) object that is available to a Microsoft Bookings business.</span></span> <span data-ttu-id="5b3c5-108">Utilice la propiedad **id** , que es el código de moneda, para especificar la moneda.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-108">Use the **id** property, which is the currency code, to specify the currency.</span></span>

## <a name="permissions"></a><span data-ttu-id="5b3c5-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5b3c5-109">Permissions</span></span>
<span data-ttu-id="5b3c5-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5b3c5-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5b3c5-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5b3c5-112">Permission type</span></span>      | <span data-ttu-id="5b3c5-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5b3c5-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5b3c5-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5b3c5-114">Delegated (work or school account)</span></span> | <span data-ttu-id="5b3c5-115">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="5b3c5-115">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="5b3c5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5b3c5-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5b3c5-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-117">Not supported.</span></span>   |
|<span data-ttu-id="5b3c5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5b3c5-118">Application</span></span> | <span data-ttu-id="5b3c5-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-119">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="5b3c5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5b3c5-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingCurrencies/<id>
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5b3c5-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5b3c5-121">Optional query parameters</span></span>
<span data-ttu-id="5b3c5-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5b3c5-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5b3c5-123">Request headers</span></span>
| <span data-ttu-id="5b3c5-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="5b3c5-124">Name</span></span>      |<span data-ttu-id="5b3c5-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b3c5-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="5b3c5-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="5b3c5-126">Authorization</span></span>  | <span data-ttu-id="5b3c5-127">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="5b3c5-127">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="5b3c5-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5b3c5-128">Request body</span></span>
<span data-ttu-id="5b3c5-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-129">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="5b3c5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b3c5-130">Response</span></span>
<span data-ttu-id="5b3c5-131">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [bookingCurrency](../resources/bookingcurrency.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-131">If successful, this method returns a `200 OK` response code and [bookingCurrency](../resources/bookingcurrency.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5b3c5-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b3c5-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5b3c5-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5b3c5-133">Request</span></span>
<span data-ttu-id="5b3c5-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_bookingcurrency"
}-->
```http
GET https://graph.microsoft.com/beta/bookingCurrencies/USD
```
##### <a name="response"></a><span data-ttu-id="5b3c5-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b3c5-135">Response</span></span>
<span data-ttu-id="5b3c5-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-136">The following is an example of the response.</span></span> <span data-ttu-id="5b3c5-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="5b3c5-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5b3c5-138">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCurrency"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 50

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingCurrencies/$entity",
    "id": "USD",
    "symbol": "$"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get bookingCurrency",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->