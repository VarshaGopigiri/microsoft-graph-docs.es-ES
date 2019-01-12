---
title: Lista bookingBusinesses
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 51b8e049b45542de9940168c994bed8fbd273b60
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951456"
---
# <a name="list-bookingbusinesses"></a><span data-ttu-id="45e23-104">Lista bookingBusinesses</span><span class="sxs-lookup"><span data-stu-id="45e23-104">List bookingBusinesses</span></span>

 > <span data-ttu-id="45e23-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45e23-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45e23-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45e23-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="45e23-107">Para obtener una colección de objetos [bookingbusiness](../resources/bookingbusiness.md) que se ha creado para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="45e23-107">Get a collection of [bookingbusiness](../resources/bookingbusiness.md) objects that has been created for the tenant.</span></span> 

<span data-ttu-id="45e23-108">Esta operación devuelve solo el **identificador** y **displayName** de cada empresa de reservas en la colección.</span><span class="sxs-lookup"><span data-stu-id="45e23-108">This operation returns only the **id** and **displayName** of each Bookings business in the collection.</span></span> <span data-ttu-id="45e23-109">Por motivos de rendimiento, no devolver otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="45e23-109">For performance considerations, it does not return other properties.</span></span> <span data-ttu-id="45e23-110">Puede obtener las demás propiedades de una empresa de reservas especificando su **identificador** en una operación [GET](bookingbusiness-get.md) .</span><span class="sxs-lookup"><span data-stu-id="45e23-110">You can get the other properties of a Bookings business by specifying its **id** in a [GET](bookingbusiness-get.md) operation.</span></span>

<span data-ttu-id="45e23-111">También puede consultar para empresas de reservas mediante la especificación de una cadena en un `query` parámetro a la coincidencia entre las empresas de un inquilino de subcadenas.</span><span class="sxs-lookup"><span data-stu-id="45e23-111">You can also query for Bookings businesses by specifying a string in a `query` parameter to do substring matching among the businesses of a tenant.</span></span> <span data-ttu-id="45e23-112">Ver un [ejemplo](#request-2) que aparece a continuación.</span><span class="sxs-lookup"><span data-stu-id="45e23-112">See an [example](#request-2) below.</span></span>


## <a name="permissions"></a><span data-ttu-id="45e23-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="45e23-113">Permissions</span></span>
<span data-ttu-id="45e23-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="45e23-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45e23-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45e23-116">Permission type</span></span>      | <span data-ttu-id="45e23-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45e23-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="45e23-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45e23-118">Delegated (work or school account)</span></span> |  <span data-ttu-id="45e23-119">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="45e23-119">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="45e23-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45e23-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="45e23-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45e23-121">Not supported.</span></span>   |
|<span data-ttu-id="45e23-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45e23-122">Application</span></span> | <span data-ttu-id="45e23-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45e23-123">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="45e23-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45e23-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses
```
## <a name="optional-query-parameters"></a><span data-ttu-id="45e23-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="45e23-125">Optional query parameters</span></span>
<span data-ttu-id="45e23-126">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45e23-126">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="45e23-127">Este método también admite la `query` parámetro que acepta un valor de tipo string.</span><span class="sxs-lookup"><span data-stu-id="45e23-127">This method also supports the `query` parameter which accepts a string value.</span></span> <span data-ttu-id="45e23-128">Este parámetro limita los resultados GET a empresas que coinciden con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="45e23-128">This parameter limits the GET results to businesses that match the specified string.</span></span> <span data-ttu-id="45e23-129">Puede ver un [ejemplo](#request-2) que aparece a continuación.</span><span class="sxs-lookup"><span data-stu-id="45e23-129">You can see an [example](#request-2) below.</span></span>


## <a name="request-headers"></a><span data-ttu-id="45e23-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45e23-130">Request headers</span></span>
| <span data-ttu-id="45e23-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="45e23-131">Name</span></span>      |<span data-ttu-id="45e23-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="45e23-132">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="45e23-133">Autorización</span><span class="sxs-lookup"><span data-stu-id="45e23-133">Authorization</span></span>  | <span data-ttu-id="45e23-134">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="45e23-134">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="45e23-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45e23-135">Request body</span></span>
<span data-ttu-id="45e23-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="45e23-136">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="45e23-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45e23-137">Response</span></span>
<span data-ttu-id="45e23-138">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [bookingBusiness](../resources/bookingbusiness.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45e23-138">If successful, this method returns a `200 OK` response code and collection of [bookingBusiness](../resources/bookingbusiness.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="45e23-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45e23-139">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="45e23-140">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="45e23-140">Request 1</span></span>
<span data-ttu-id="45e23-141">En el ejemplo siguiente se obtiene la empresas de reservas en un inquilino.</span><span class="sxs-lookup"><span data-stu-id="45e23-141">The following example gets the Bookings businesses in a tenant.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_bookingbusinesses"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses
```
##### <a name="response-1"></a><span data-ttu-id="45e23-142">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="45e23-142">Response 1</span></span>
<span data-ttu-id="45e23-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45e23-143">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingBusiness",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#bookingBusinesses",
    "value":[
        {
            "id":"Contosolunchdelivery@M365B489948.onmicrosoft.com",
            "displayName":"Contoso lunch delivery",
        },
        {
            "id":"Fabrikam@M365B489948.onmicrosoft.com",
            "displayName":"Fabrikam",
        }
    ]
}
```


##### <a name="request-2"></a><span data-ttu-id="45e23-144">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="45e23-144">Request 2</span></span>
<span data-ttu-id="45e23-145">En el ejemplo siguiente se muestra cómo usar la `query` parámetro para obtener una o más empresas reservas coincidentes en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="45e23-145">The following example shows how to use the `query` parameter to get one or more matching Bookings businesses in the tenant.</span></span>
<!-- {
  "blockType": "request",
  "name": "query_bookingbusinesses"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses?query=Adventure
```
##### <a name="response-2"></a><span data-ttu-id="45e23-146">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="45e23-146">Response 2</span></span>
<span data-ttu-id="45e23-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45e23-147">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingBusiness",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#bookingBusinesses",
    "value":[
        {
            "id":"AdventureWorksCycles@M365B960066.onmicrosoft.com",
            "displayName":"Adventure Works Cycles",
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List bookingBusinesses",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
