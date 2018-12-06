---
title: Combinación de varias solicitudes en una llamada HTTP mediante el procesamiento por lotes de JSON
description: 'El procesamiento por lotes de JSON le permite optimizar la aplicación mediante la combinación de varias solicitudes en un solo objeto JSON. Por ejemplo, un cliente desea crear una vista de datos no relacionados, como:'
ms.openlocfilehash: 875f5f8758d37e84498446876eb863f474e00f21
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092772"
---
# <a name="combine-multiple-requests-in-one-http-call-using-json-batching"></a><span data-ttu-id="88048-104">Combinación de varias solicitudes en una llamada HTTP mediante el procesamiento por lotes de JSON</span><span class="sxs-lookup"><span data-stu-id="88048-104">Combine multiple requests in one HTTP call using JSON batching</span></span>

<span data-ttu-id="88048-p102">El procesamiento por lotes de JSON le permite optimizar la aplicación mediante la combinación de varias solicitudes en un solo objeto JSON. Por ejemplo, un cliente desea crear una vista de datos no relacionados, como:</span><span class="sxs-lookup"><span data-stu-id="88048-p102">JSON batching allows you to optimize your application by combining multiple requests into a single JSON object. For example, a client might want to compose a view of unrelated data such as:</span></span>

1. <span data-ttu-id="88048-107">Una imagen almacenada en OneDrive</span><span class="sxs-lookup"><span data-stu-id="88048-107">An image stored in OneDrive</span></span>
2. <span data-ttu-id="88048-108">Una lista de tareas de Planner</span><span class="sxs-lookup"><span data-stu-id="88048-108">A list of Planner tasks</span></span>
3. <span data-ttu-id="88048-109">El calendario de un grupo</span><span class="sxs-lookup"><span data-stu-id="88048-109">The calendar for a group</span></span>

<span data-ttu-id="88048-110">La combinación de estas tres solicitudes individuales en una sola solicitud por lotes puede ahorrarle a la aplicación una importante latencia de red.</span><span class="sxs-lookup"><span data-stu-id="88048-110">Combining these three individual requests into a single batch request can save the application significant network latency.</span></span>

## <a name="first-json-batch-request"></a><span data-ttu-id="88048-111">Primera solicitud por lotes JSON</span><span class="sxs-lookup"><span data-stu-id="88048-111">First JSON batch request</span></span>

<span data-ttu-id="88048-p103">En primer lugar, se construye la solicitud por lotes JSON para el ejemplo anterior. En este escenario, las solicitudes individuales no son interdependientes de ningún modo y, por lo tanto, se pueden colocar en la solicitud por lotes en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="88048-p103">First you construct the JSON batch request for the previous example. In this scenario, the individual requests are not interdependent in any way and therefore can be placed into the batch request in any order.</span></span>

```http
POST https://graph.microsoft.com/v1.0/$batch
Accept: application/json
Content-Type: application/json
```

```json
{
  "requests": [
    {
      "id": "1",
      "method": "GET",
      "url": "/me/drive/root:/{file}:/content"
    },
    {
      "id": "2",
      "method": "GET",
      "url": "/me/planner/tasks"
    },
    {
      "id": "3",
      "method": "GET",
      "url": "/groups/{id}/events"
    },
    {
      "id": "4",
      "url": "/me",
      "method": "PATCH",
      "body": {
        "city" : "Redmond"
      },
      "headers": {
        "Content-Type": "application/json"
      }
    }
  ]
}
```

<span data-ttu-id="88048-p104">Las respuestas a las solicitudes por lotes pueden aparecer en un orden diferente. La propiedad `id` puede utilizarse para poner en correlación las respuestas y solicitudes individuales.</span><span class="sxs-lookup"><span data-stu-id="88048-p104">Responses to the batched requests might appear in a different order. The `id` property can be used to correlate individual requests and responses.</span></span>

```http
200 OK
Content-Type: application/json
```

```json
{
  "responses": [
    {
      "id": "1",
      "status": 302,
      "headers": {
        "location": "https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi"
      }
    },
    {
      "id": "3",
      "status": 401,
      "body": {
        "error": {
          "code": "Forbidden",
          "message": "..."
        }
      }
    },
    {
      "id": "2",
      "status": 200,
      "body": {
        "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(microsoft.graph.plannerTask)",
        "value": []
      }
    },
    {
      "id": "4",
      "status": 204,
      "body": null
    }
  ]
}
```

## <a name="request-format"></a><span data-ttu-id="88048-116">Formato de solicitud</span><span class="sxs-lookup"><span data-stu-id="88048-116">Request format</span></span>

<span data-ttu-id="88048-117">Las solicitudes por lotes se envían siempre mediante el método `POST` al punto de conexión `/$batch`.</span><span class="sxs-lookup"><span data-stu-id="88048-117">Batch requests are always sent using `POST` to the `/$batch` endpoint.</span></span>

<span data-ttu-id="88048-p105">Un cuerpo de solicitud por lotes JSON consta de un único objeto JSON con una propiedad requerida: `requests`. La propiedad `requests` es una matriz de solicitudes individuales. Para cada solicitud individual, son necesarias las propiedades `id`, `method` y `url`.</span><span class="sxs-lookup"><span data-stu-id="88048-p105">A JSON batch request body consists of a single JSON object with one required property: `requests`. The `requests` property is an array of individual requests. For each individual request, the `id`, `method`, and `url` properties are required.</span></span>

<span data-ttu-id="88048-p106">La propiedad `id` funciona principalmente como un valor de correlación para asociar las respuestas individuales a las solicitudes. Esto permite que el servidor procese las solicitudes en el lote en el orden más eficaz.</span><span class="sxs-lookup"><span data-stu-id="88048-p106">The `id` property functions primarily as a correlation value to associate individual responses with requests. This allows the server to process requests in the batch in the most efficient order.</span></span>

<span data-ttu-id="88048-p107">Las propiedades `method` y `url` son exactamente lo que vería al principio de cualquier solicitud HTTP determinada. El método es el método HTTP y la dirección URL es la URL de recurso a la que normalmente se enviaría la solicitud individual.</span><span class="sxs-lookup"><span data-stu-id="88048-p107">The `method` and `url` properties are exactly what you would see at the start of any given HTTP request. The method is the HTTP method, and the URL is the resource URL the individual request would typically be sent to.</span></span>

<span data-ttu-id="88048-125">Opcionalmente, las solicitudes individuales también contienen una propiedad `headers` y una propiedad `body`.</span><span class="sxs-lookup"><span data-stu-id="88048-125">Individual requests can optionally also contain a `headers` property and a `body` property.</span></span> <span data-ttu-id="88048-126">Ambas propiedades normalmente son objetos JSON, tal y como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="88048-126">Both of these properties are typically JSON objects, as shown in the previous example.</span></span> <span data-ttu-id="88048-127">En algunos casos, `body` puede ser un valor de dirección URL codificada en base64 en lugar de un objeto JSON, por ejemplo, cuando el cuerpo es una imagen.</span><span class="sxs-lookup"><span data-stu-id="88048-127">In some cases, the `body` might be a base64 URL-encoded value rather than a JSON object - for example, when the body is an image.</span></span> <span data-ttu-id="88048-128">Cuando se incluye un `body` con la solicitud, el objeto `headers` debe contener un valor para `Content-Type`.</span><span class="sxs-lookup"><span data-stu-id="88048-128">When a `body` is included with the request, the `headers` object must contain a value for `Content-Type`.</span></span>

## <a name="response-format"></a><span data-ttu-id="88048-129">Formato de respuesta</span><span class="sxs-lookup"><span data-stu-id="88048-129">Response format</span></span>

<span data-ttu-id="88048-p109">El formato de respuesta para las solicitudes por lotes JSON es similar al formato de solicitud. Estas son las diferencias clave:</span><span class="sxs-lookup"><span data-stu-id="88048-p109">The response format for JSON batch requests is similar to the request format. The following are the key differences:</span></span>

* <span data-ttu-id="88048-132">La propiedad en el objeto principal JSON se denomina `responses` como contraposición a `requests`.</span><span class="sxs-lookup"><span data-stu-id="88048-132">The property in the main JSON object is named `responses` as opposed to `requests`.</span></span>
* <span data-ttu-id="88048-133">Las respuestas individuales pueden aparecer en un orden diferente a las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="88048-133">Individual responses might appear in a different order than the requests.</span></span>
* <span data-ttu-id="88048-p110">En lugar de `method` y `url`, las respuestas individuales tienen una propiedad `status`. El valor de `status` es un número que representa el código de estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="88048-p110">Rather than `method` and `url`, individual responses have a `status` property. The value of `status` is a number that represents the HTTP status code.</span></span>

<span data-ttu-id="88048-p111">Normalmente, el código de estado en una respuesta por lotes es `200` o `400`. Si la misma solicitud por lotes está mal formada, el código de estado es `400`. Si la solicitud por lotes se puede analizar, el código de estado es `200`. Un código de estado `200` en la respuesta por lotes no indica que las solicitudes individuales dentro del lote se hayan realizado correctamente. Por ello, cada respuesta individual en la propiedad `responses` tiene un código de estado.</span><span class="sxs-lookup"><span data-stu-id="88048-p111">The status code on a batch response is typically `200` or `400`. If the batch request itself is malformed, the status code is `400`. If the batch request is parseable, the status code is `200`. A `200` status code on the batch response does not indicate that the individual requests inside the batch succeeded. This is why each individual response in the `responses` property has a status code.</span></span>

<span data-ttu-id="88048-p112">Además de la propiedad `responses`, podría haber una propiedad `nextLink` en la respuesta por lotes. Esto permite a Microsoft Graph devolver una respuesta por lotes tan pronto como cualquiera de las solicitudes individuales se haya completado. Para asegurarse de que se recibieron todas las respuestas individuales, continúe con el `nextLink` en caso de que exista.</span><span class="sxs-lookup"><span data-stu-id="88048-p112">In addition to the `responses` property, there might be a `nextLink` property in the batch response. This allows Microsoft Graph to return a batch response as soon as any of the individual requests has completed. To ensure that all individual responses have been received, continue to follow the `nextLink` as long as it exists.</span></span>

## <a name="sequencing-requests-with-the-dependson-property"></a><span data-ttu-id="88048-144">Secuenciar solicitudes con la propiedad dependsOn</span><span class="sxs-lookup"><span data-stu-id="88048-144">Sequencing requests with the dependsOn property</span></span>

<span data-ttu-id="88048-p113">Las solicitudes individuales se pueden ejecutar en un orden especificado utilizando la propiedad `dependsOn`. Esta propiedad es una matriz de cadenas que hace referencia a la `id` de una solicitud individual diferente. Por este motivo, los valores de `id` deben ser únicos. Por ejemplo, en la siguiente solicitud, el cliente especifica que las solicitudes 1 y 3 se deben ejecutar en primer lugar, después, la solicitud 2 y, a continuación, la solicitud 4.</span><span class="sxs-lookup"><span data-stu-id="88048-p113">Individual requests can be executed in a specified order by using the `dependsOn` property. This property is an array of strings that reference the `id` of a different individual request. For this reason, the values for `id` must be unique. For example, in the following request, the client is specifying that requests 1 and 3 should be run first, then request 2, then request 4.</span></span>

```json
{
  "requests": [
    {
      "id": "1",
      "method": "GET",
      "url": "..."
    },
    {
      "id": "2",
      "dependsOn": [ "1" ],
      "method": "GET",
      "url": "..."
    },
    {
      "id": "3",
      "method": "GET",
      "url": "..."
    },
    {
      "id": "4",
      "dependsOn": [ "2" ],
      "method": "GET",
      "url": "..."
    }
  ]
}
```

<span data-ttu-id="88048-149">Si se produce un error en una solicitud individual, cualquier solicitud que dependa de dicha solicitud producirá un error con código de estado `424` (dependencia errónea).</span><span class="sxs-lookup"><span data-stu-id="88048-149">If an individual request fails, any request that depends on that request fails with status code `424` (Failed Dependency).</span></span>

## <a name="bypassing-url-length-limitations-with-batching"></a><span data-ttu-id="88048-150">Omitir las limitaciones de longitud de URL con el procesamiento por lotes</span><span class="sxs-lookup"><span data-stu-id="88048-150">Bypassing URL length limitations with batching</span></span>

<span data-ttu-id="88048-p114">Un caso de uso adicional para el procesamiento por lotes de JSON es omitir las limitaciones de longitud de dirección URL. En los casos donde la cláusula de filtro es compleja, la longitud de la dirección URL podría superar las limitaciones integradas en los navegadores u otros clientes HTTP. Puede utilizar el procesamiento por lotes de JSON como solución alternativa para ejecutar estas solicitudes porque la longitud de la URL simplemente pasa a formar parte de la carga de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88048-p114">An additional use case for JSON batching is to bypass URL length limitations. In cases where the filter clause is complex, the URL length might surpass limitations built into browsers or other HTTP clients. You can use JSON batching as a workaround for running these requests because the lengthy URL simply becomes part of the request payload.</span></span>

## <a name="known-issues"></a><span data-ttu-id="88048-154">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="88048-154">Known issues</span></span>

<span data-ttu-id="88048-155">Para obtener una lista de las limitaciones actuales relacionadas con el procesamiento por lotes, consulte [problemas conocidos][batching-known-issues].</span><span class="sxs-lookup"><span data-stu-id="88048-155">For a list of current limitations related to batching, see [known issues][batching-known-issues].</span></span>

[batching-known-issues]: known-issues.md#json-batching
[odata-4.01-json]: https://www.oasis-open.org/committees/download.php/60365/odata-json-format-v4.01-wd02-2017-03-24.docx


## <a name="see-also"></a><span data-ttu-id="88048-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="88048-156">See also</span></span>

<span data-ttu-id="88048-p115">Para obtener más información sobre el formato de solicitud o respuesta por lotes JSON, consulte la [especificación OData JSON, versión de formato 4.01][odata-4.01-json], sección 18. Tenga en cuenta que actualmente esta especificación es un borrador, pero no se espera que cambie.</span><span class="sxs-lookup"><span data-stu-id="88048-p115">For more information about the JSON batch request/response format, see the [OData JSON Format Version 4.01 specification][odata-4.01-json], section 18. Note that this specification is currently in a draft version, but is not expected to change.</span></span>

