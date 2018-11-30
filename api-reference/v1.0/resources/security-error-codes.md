---
title: Respuestas de error de la API de seguridad de Microsoft Graph
description: Errores en la API de seguridad de Microsoft Graph en Microsoft Graph se devuelven mediante código de estado HTTP 206 parcial contenido estándar y se entregan por medio de un encabezado de advertencia.
ms.openlocfilehash: 35af0a1ed4c4bf7f6e1afb36039f812ab59f64dd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032406"
---
# <a name="microsoft-graph-security-api-error-responses"></a><span data-ttu-id="be2d7-103">Respuestas de error de la API de seguridad de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="be2d7-103">Microsoft Graph Security API error responses</span></span>

<span data-ttu-id="be2d7-104">Errores en la API de seguridad de Microsoft Graph en Microsoft Graph se devuelven mediante código de estado HTTP 206 parcial contenido estándar y se entregan por medio de un encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="be2d7-104">Errors in the Microsoft Graph Security API in Microsoft Graph are returned using standard HTTP 206 Partial Content status code and are delivered by way of a warning header.</span></span>

<span data-ttu-id="be2d7-105">La API de seguridad de Microsoft Graph es un servicio federado que recibe varias respuestas de todos los proveedores de datos.</span><span class="sxs-lookup"><span data-stu-id="be2d7-105">The Microsoft Graph Security API is a federated service that receives multiple responses from all data providers.</span></span> <span data-ttu-id="be2d7-106">Cuando se recibe un error HTTP por la API de seguridad de Microsoft Graph, bien va a volver a enviar un encabezado de advertencia en el siguiente formato:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="be2d7-106">When an HTTP error is received by the Microsoft Graph Security API, it will send back a warning header in the following format: <!-- { "blockType": "ignored" } --></span></span>

```http
{Vendor}/{Provider}/{StatusCode}/{LatencyInMs}
```

<span data-ttu-id="be2d7-107">Este encabezado de advertencia sólo se envía a los clientes cuando uno de los proveedores de datos devuelve un código de error que no sean 2xx o 404.</span><span class="sxs-lookup"><span data-stu-id="be2d7-107">This warning header is only sent back to clients when one of the data providers returns an error code other than 2xx or 404.</span></span> <span data-ttu-id="be2d7-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="be2d7-108">For example:</span></span>

- <span data-ttu-id="be2d7-109">Es posible que se devuelva HttpStatusCode.Forbidden (403) si no se concede el acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="be2d7-109">HttpStatusCode.Forbidden (403) might be returned if the access to the resource is not granted.</span></span>
- <span data-ttu-id="be2d7-110">Si un proveedor de tiempo de espera, se devuelve HttpStatusCode.GatewayTimeout (504) en el encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="be2d7-110">If a provider times out, HttpStatusCode.GatewayTimeout (504) is returned in the warning header.</span></span>
- <span data-ttu-id="be2d7-111">Si se produce un error interno del proveedor, se usa HttpStatusCode.InternalServerError (500) en el encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="be2d7-111">If an internal provider error happens, HttpStatusCode.InternalServerError (500) is used in the warning header.</span></span>

<span data-ttu-id="be2d7-112">Si un proveedor de datos devuelve 2xx o 404, no se muestra en el encabezado de advertencia debido a que se esperan que estos códigos para el éxito o cuando no se encontraron datos respectivamente.</span><span class="sxs-lookup"><span data-stu-id="be2d7-112">If a data provider returns 2xx or 404, it’s not shown in the warning header because these codes are expected for success or when data is not found respectively.</span></span> <span data-ttu-id="be2d7-113">En un sistema federado, se prevé un error 404 no se encontró como número de veces que los datos sólo se conocen a uno o varios, pero no todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="be2d7-113">In a federated system, a 404 not found is expected as many times the data is only known to one or several, but not all, providers.</span></span>

## <a name="example"></a><span data-ttu-id="be2d7-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be2d7-114">Example</span></span>

<span data-ttu-id="be2d7-115">Un usuario solicita `security/alerts/{alert_id}`.</span><span class="sxs-lookup"><span data-stu-id="be2d7-115">A user asks for `security/alerts/{alert_id}`.</span></span>

    Provider 1: 404 (provider does not have a record of this alert ID)
    Provider 2: 504 (provider timed out)
    Provider 3: 200 (success)
    Provider 4: 403 (customer has not licensed this provider)

<span data-ttu-id="be2d7-116">Dado que 404 y 200 son las condiciones previstas, el encabezado de advertencia contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="be2d7-116">Because both 404 and 200 are expected conditions, the warning header contains the following:</span></span> 

```HTTP
Warning : 199 - "{Vendor2}/{Provider 2}/504/10000",    (usual timeout limit is set at 10 seconds)
          199 - "{Vendor4}/{Provider 4}/403/10"       (Provider 4 rejected the request in 10 ms)
```

> <span data-ttu-id="be2d7-117">**Nota:** Cada encabezado HTTP es una colección de subelementos, por lo que los usuarios pueden enumerar el encabezado de advertencia y compruebe todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="be2d7-117">**Note:** Each HTTP header is a collection of subitems, so users can enumerate the Warning header and check all items.</span></span>

## <a name="see-also"></a><span data-ttu-id="be2d7-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="be2d7-118">See also</span></span>

<span data-ttu-id="be2d7-119">Si tiene problemas con la autorización, consulte nuestro [blog post](https://techcommunity.microsoft.com/t5/Using-Microsoft-Graph-Security/Authorization-and-Microsoft-Graph-Security-API/m-p/184376#M2).</span><span class="sxs-lookup"><span data-stu-id="be2d7-119">If you’re having trouble with authorization, see our [blog post](https://techcommunity.microsoft.com/t5/Using-Microsoft-Graph-Security/Authorization-and-Microsoft-Graph-Security-API/m-p/184376#M2).</span></span>
