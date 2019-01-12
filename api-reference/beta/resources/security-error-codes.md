---
title: Respuestas de error de la API de seguridad de Microsoft Graph
description: Errores en la API de seguridad de Microsoft Graph se devuelven mediante el código de estado HTTP 206 parcial contenido estándar y se entregan a través de un encabezado de advertencia.
author: preetikr
localization_priority: Normal
ms.prod: security
ms.openlocfilehash: 52b7c375bd3e0c6a367f1150a21bb96ef84437ff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921433"
---
# <a name="microsoft-graph-security-api-error-responses"></a><span data-ttu-id="8eeff-103">Respuestas de error de la API de seguridad de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8eeff-103">Microsoft Graph Security API error responses</span></span>

<span data-ttu-id="8eeff-104">Errores en la API de seguridad de Microsoft Graph se devuelven mediante el código de estado HTTP 206 parcial contenido estándar y se entregan a través de un encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="8eeff-104">Errors in the Microsoft Graph Security API are returned using the standard HTTP 206 Partial Content status code and are delivered via a warning header.</span></span>

## <a name="errors"></a><span data-ttu-id="8eeff-105">Errores</span><span class="sxs-lookup"><span data-stu-id="8eeff-105">Errors</span></span>

<span data-ttu-id="8eeff-106">La API de seguridad de Microsoft Graph es un servicio federado que recibe varias respuestas de todos los proveedores de datos.</span><span class="sxs-lookup"><span data-stu-id="8eeff-106">The Microsoft Graph Security API is a federated service that receives multiple responses from all data providers.</span></span> <span data-ttu-id="8eeff-107">Cuando se recibe un error HTTP por la API de seguridad de Microsoft Graph, bien va a volver a enviar un encabezado de advertencia en el siguiente formato:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="8eeff-107">When an HTTP error is received by the Microsoft Graph Security API, it will send back a warning header in the following format: <!-- { "blockType": "ignored" } --></span></span>

```http
{Vendor}/{Provider}/{StatusCode}/{LatencyInMs}
```

<span data-ttu-id="8eeff-108">Este encabezado de advertencia sólo se envía a los clientes cuando uno de los proveedores de datos devuelve un código de error que no sean 2xx o 404.</span><span class="sxs-lookup"><span data-stu-id="8eeff-108">This warning header is only sent back to clients when one of the data providers returns an error code other than 2xx or 404.</span></span> <span data-ttu-id="8eeff-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8eeff-109">For example:</span></span>

- <span data-ttu-id="8eeff-110">Es posible que se devuelva HttpStatusCode.Forbidden (403) si no se concede el acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="8eeff-110">HttpStatusCode.Forbidden (403) might be returned if the access to the resource is not granted.</span></span>
- <span data-ttu-id="8eeff-111">Si un proveedor de tiempo de espera, se devuelve HttpStatusCode.GatewayTimeout (504) en el encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="8eeff-111">If a provider times out, HttpStatusCode.GatewayTimeout (504) is returned in the warning header.</span></span>
- <span data-ttu-id="8eeff-112">Si se produce un error interno del proveedor, se usa HttpStatusCode.InternalServerError (500) en el encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="8eeff-112">If an internal provider error happens, HttpStatusCode.InternalServerError (500) is used in the warning header.</span></span>

<span data-ttu-id="8eeff-113">Si un proveedor de datos devuelve 2xx o 404, no se muestra en el encabezado de advertencia debido a que se esperan que estos códigos para el éxito o cuando no se encontraron datos respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8eeff-113">If a data provider returns 2xx or 404, it’s not shown in the warning header because these codes are expected for success or when data is not found respectively.</span></span> <span data-ttu-id="8eeff-114">En un sistema federado, se prevé un error 404 no se encontró como número de veces que los datos sólo se conocen a uno o varios, pero no todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="8eeff-114">In a federated system, a 404 not found is expected as many times the data is only known to one or several, but not all, providers.</span></span>

## <a name="example"></a><span data-ttu-id="8eeff-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8eeff-115">Example</span></span>

<span data-ttu-id="8eeff-116">Un usuario solicita `security/alerts/{alert_id}`.</span><span class="sxs-lookup"><span data-stu-id="8eeff-116">A user asks for `security/alerts/{alert_id}`.</span></span>

    Provider 1: 404 (provider does not have a record of this alert ID)
    Provider 2: 504 (provider timed out)
    Provider 3: 200 (success)
    Provider 4: 403 (customer has not licensed this provider)

<span data-ttu-id="8eeff-117">Dado que 404 y 200 son las condiciones previstas, el encabezado de advertencia contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8eeff-117">Because both 404 and 200 are expected conditions, the warning header contains the following:</span></span>

```HTTP
Warning : 199 - "{Vendor2}/{Provider 2}/504/10000",    (usual timeout limit is set at 10 seconds)
          199 - "{Vendor4}/{Provider 4}/403/10"       (Provider 4 rejected the request in 10 ms)
```

> <span data-ttu-id="8eeff-118">**Nota:** Cada encabezado HTTP es una colección de subelementos, por lo que los usuarios pueden enumerar el encabezado de advertencia y compruebe todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="8eeff-118">**Note:** Each HTTP header is a collection of subitems, so users can enumerate the Warning header and check all items.</span></span>

## <a name="constraints"></a><span data-ttu-id="8eeff-119">Restricciones</span><span class="sxs-lookup"><span data-stu-id="8eeff-119">Constraints</span></span>

<span data-ttu-id="8eeff-120">El `$top` parámetro de consulta de OData tiene un límite de 1000 alertas y una combinación de `$top`  +  `$skip` parámetros no pueden superar los 6000 alertas de consulta de OData.</span><span class="sxs-lookup"><span data-stu-id="8eeff-120">The `$top` OData query parameter has a limit of 1000 alerts, and a combination of `$top` + `$skip` OData query parameters cannot exceed 6000 alerts.</span></span> <span data-ttu-id="8eeff-121">Por ejemplo, `/security/alerts?$top=10&$skip=5990` devolverá un `200 OK` código de respuesta, pero `/security/alerts?$top=10&$skip=5991` devolverá un `400 Bad Request` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8eeff-121">For example, `/security/alerts?$top=10&$skip=5990` will return a `200 OK` response code, but `/security/alerts?$top=10&$skip=5991` will return a `400 Bad Request` response code.</span></span>

<span data-ttu-id="8eeff-122">Una solución alternativa para este límite es usar el `$filter` parámetro de consulta de OData con la `eventDateTime` de la entidad de alerta de la API de seguridad de Microsoft Graph, con `?$filter=eventDateTime gt {YYYY-MM-DDT00:00:00.000Z}` y reemplazar el valor de fecha y hora con la última alerta (6000th).</span><span class="sxs-lookup"><span data-stu-id="8eeff-122">A work-around for this limit is to use the `$filter` OData query parameter with the `eventDateTime` of the alert entity from the Microsoft Graph Security API, using `?$filter=eventDateTime gt {YYYY-MM-DDT00:00:00.000Z}` and replacing the dateTime value with the last (6000th) alert.</span></span> <span data-ttu-id="8eeff-123">También puede establecer un intervalo para la `eventDateTime`; Por ejemplo, *filtro de $ alerts? = eventDateTime **gt** 2018-11 -**11**T00:00:00.000Z & eventDateTime **lt** 2018-11 -**12**T00:00:00.000Z*</span><span class="sxs-lookup"><span data-stu-id="8eeff-123">You can also set a range for the `eventDateTime`; for example, *alerts?$filter=eventDateTime **gt** 2018-11-**11**T00:00:00.000Z&eventDateTime **lt** 2018-11-**12**T00:00:00.000Z*</span></span>

## <a name="see-also"></a><span data-ttu-id="8eeff-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8eeff-124">See also</span></span>

<span data-ttu-id="8eeff-125">Si tiene problemas con la autorización, vea [autorización y la API de seguridad de Microsoft Graph](/graph/security-authorization).</span><span class="sxs-lookup"><span data-stu-id="8eeff-125">If you’re having trouble with authorization, see [Authorization and the Microsoft Graph Security API](/graph/security-authorization).</span></span>
