# <a name="security-api-error-responses"></a><span data-ttu-id="f1838-101">Respuestas de error de la API de seguridad</span><span class="sxs-lookup"><span data-stu-id="f1838-101">Security API error responses</span></span>

<span data-ttu-id="f1838-102">Los errores en la API de seguridad en Microsoft Graph se devuelven mediante códigos de estado HTTP estándar y se entregan por medio de un encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="f1838-102">Errors in the security API in Microsoft Graph are returned using standard HTTP status codes and are delivered by way of a warning header.</span></span>

<span data-ttu-id="f1838-103">La API de seguridad es un servicio federado que recibe varias respuestas de todos los proveedores de datos.</span><span class="sxs-lookup"><span data-stu-id="f1838-103">The security API is a federated service that receives multiple responses from all data providers.</span></span> <span data-ttu-id="f1838-104">Cuando la API de seguridad recibe un error HTTP, devolverá un encabezado de advertencia con el siguiente formato: <!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="f1838-104">When an HTTP error is received by the security API, it will send back a warning header in the following format: <!-- { "blockType": "ignored" } --></span></span>

```http
{Vendor}/{Provider}/{StatusCode}/{LatencyInMs}
```

<span data-ttu-id="f1838-105">Este encabezado de advertencia sólo se envía a los clientes cuando uno de los proveedores de datos devuelve un código de error que no sea 2xx o 404.</span><span class="sxs-lookup"><span data-stu-id="f1838-105">This warning header is only sent back to clients when one of the data providers returns an error code other than 2xx or 404.</span></span> <span data-ttu-id="f1838-106">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f1838-106">For example:</span></span>

- <span data-ttu-id="f1838-107">Es posible que se devuelva HttpStatusCode.Forbidden (403) si no se ha concedido el acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="f1838-107">HttpStatusCode.Forbidden (403) might be returned if the access to the resource is not granted.</span></span>
- <span data-ttu-id="f1838-108">Si un proveedor excede el tiempo espera, se devuelve HttpStatusCode.GatewayTimeout (504) en el encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="f1838-108">If a provider times out, HttpStatusCode.GatewayTimeout (504) is returned in the warning header.</span></span>
- <span data-ttu-id="f1838-109">Si se produce un error interno del proveedor, se usa HttpStatusCode.InternalServerError (500) en el encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="f1838-109">If an internal provider error happens, HttpStatusCode.InternalServerError (500) is used in the warning header.</span></span>

<span data-ttu-id="f1838-110">Si un proveedor de datos devuelve 2xx o 404, no se muestra en el encabezado de advertencia debido a que estos códigos se preven, respectivamente, cuando el resultado es correcto o cuando no se han encontrado datos.</span><span class="sxs-lookup"><span data-stu-id="f1838-110">If a data provider returns 2xx or 404, it’s not shown in the warning header because these codes are expected for success or when data is not found respectively.</span></span> <span data-ttu-id="f1838-111">En un sistema federado, se prevé un error 404 de no encontrado tantas veces como los datos solo los conozcan uno o varios proveedores, pero no todos.</span><span class="sxs-lookup"><span data-stu-id="f1838-111">In a federated system, a 404 not found is expected as many times the data is only known to one or several, but not all, providers.</span></span>

## <a name="example"></a><span data-ttu-id="f1838-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1838-112">Example</span></span>

<span data-ttu-id="f1838-113">Un usuario solicita `security/alerts/{alert_id}`.</span><span class="sxs-lookup"><span data-stu-id="f1838-113">A user asks for `security/alerts/{alert_id}`.</span></span>

    Provider 1: 404 (provider does not have a record of this alert ID)
    Provider 2: 504 (provider timed out)
    Provider 3: 200 (success)
    Provider 4: 403 (customer has not licensed this provider)

<span data-ttu-id="f1838-114">Dado que 404 y 200 son las condiciones previstas, el encabezado de advertencia contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f1838-114">Because both 404 and 200 are expected conditions, the warning header contains the following:</span></span> 

```HTTP
Warning : 199 - "{Vendor2}/{Provider 2}/504/29000",    (usual timeout limit is set at 29 seconds)
          199 - "{Vendor4}/{Provider 4}/403/10"       (Provider 4 rejected the request in 10 ms)
```

> <span data-ttu-id="f1838-115">**Nota:** Cada encabezado HTTP es una colección de subelementos, por lo que los usuarios pueden enumerar el encabezado de advertencia y comprobar todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="f1838-115">**Note:** Each HTTP header is a collection of subitems, so users can enumerate the Warning header and check all items.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1838-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f1838-116">See also</span></span>

<span data-ttu-id="f1838-117">Si tiene problemas con la autorización, consulte nuestra [entrada de blog](https://techcommunity.microsoft.com/t5/Using-Microsoft-Graph-Security/Authorization-and-Microsoft-Graph-Security-API/m-p/184376#M2).</span><span class="sxs-lookup"><span data-stu-id="f1838-117">If you’re having trouble with authorization, see our [blog post](https://techcommunity.microsoft.com/t5/Using-Microsoft-Graph-Security/Authorization-and-Microsoft-Graph-Security-API/m-p/184376#M2).</span></span>
