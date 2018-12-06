---
title: Guía de limitación de Microsoft Graph
description: La limitación restringe el número de llamadas simultáneas a un servicio para evitar el uso excesivo de los recursos. Microsoft Graph está diseñado para admitir un gran volumen de solicitudes. Si se produce un número abrumador de solicitudes, la limitación ayuda a mantener un rendimiento y fiabilidad óptimos del servicio Microsoft Graph.
ms.openlocfilehash: dfe7fed3efc01932137df00d6d62ad069faf64cd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092824"
---
# <a name="microsoft-graph-throttling-guidance"></a><span data-ttu-id="d05e9-105">Guía de limitación de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="d05e9-105">Microsoft Graph throttling guidance</span></span>


<span data-ttu-id="d05e9-p102">La limitación restringe el número de llamadas simultáneas a un servicio para evitar el uso excesivo de los recursos. Microsoft Graph está diseñado para admitir un gran volumen de solicitudes. Si se produce un número abrumador de solicitudes, la limitación ayuda a mantener un rendimiento y fiabilidad óptimos del servicio Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="d05e9-p102">Throttling limits the number of concurrent calls to a service to prevent overuse of resources. Microsoft Graph is designed to handle a high volume of requests. If an overwhelming number of requests occurs, throttling helps maintain optimal performance and reliability of the Microsoft Graph service.</span></span>

<span data-ttu-id="d05e9-p103">Los márgenes de la limitación varían en función del escenario. Por ejemplo, si va a realizar un gran volumen de escrituras, la posibilidad de limitación es mayor que si solo va a realizar lecturas.</span><span class="sxs-lookup"><span data-stu-id="d05e9-p103">Throttling limits vary based on the scenario. For example, if you are performing a large volume of writes, the possibility for throttling is higher than if you are only performing reads.</span></span>

## <a name="what-happens-when-throttling-occurs"></a><span data-ttu-id="d05e9-111">¿Qué sucede cuando se produce la limitación?</span><span class="sxs-lookup"><span data-stu-id="d05e9-111">What happens when throttling occurs?</span></span>

<span data-ttu-id="d05e9-p104">Cuando se supera un umbral límite, Microsoft Graph limita las solicitudes sucesivas de ese cliente durante un período de tiempo. Cuando se produce la limitación, Microsoft Graph devuelve el código de estado HTTP 429 (demasiadas solicitudes) y las solicitudes proporcionan errores. Se devuelve un tiempo de espera sugerido en el encabezado de la respuesta de la solicitud con errores. El comportamiento de la limitación puede depender del tipo y el número de solicitudes. Por ejemplo, si tiene un gran volumen de solicitudes, se regulan todos los tipos de estas. Los límites del umbral varían según el tipo de solicitud. Por lo tanto, podría encontrarse un escenario donde se limiten las escrituras pero se sigan permitiendo las lecturas.</span><span class="sxs-lookup"><span data-stu-id="d05e9-p104">When a throttling threshold is exceeded, Microsoft Graph limits any further requests from that client for a period of time. When throttling occurs, Microsoft Graph returns HTTP status code 429 (Too many requests), and the requests fail. A suggested wait time is returned in the response header of the failed request. Throttling behavior can depend on the type and number of requests. For example, if you have a high volume of requests, all requests types are throttled. Threshold limits vary based on the request type. Therefore, you could encounter a scenario where writes are throttled but reads are still permitted.</span></span> 

## <a name="common-throttling-scenarios"></a><span data-ttu-id="d05e9-119">Escenarios de limitación comunes</span><span class="sxs-lookup"><span data-stu-id="d05e9-119">Common throttling scenarios</span></span>

<span data-ttu-id="d05e9-120">Las causas más comunes de limitación de los clientes incluyen:</span><span class="sxs-lookup"><span data-stu-id="d05e9-120">The most common causes of throttling of clients include:</span></span>

* <span data-ttu-id="d05e9-121">Un gran número de solicitudes en todas las aplicaciones de un espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="d05e9-121">A large number of requests across all applications in a tenant.</span></span>
* <span data-ttu-id="d05e9-122">Un gran número de solicitudes de una aplicación determinada a través de todos los espacios empresariales.</span><span class="sxs-lookup"><span data-stu-id="d05e9-122">A large number of requests from a particular application across all tenants.</span></span>

## <a name="best-practices-to-handle-throttling"></a><span data-ttu-id="d05e9-123">Procedimientos recomendados para tratar la limitación</span><span class="sxs-lookup"><span data-stu-id="d05e9-123">Best practices to handle throttling</span></span>

<span data-ttu-id="d05e9-124">Las siguientes son recomendaciones para el tratamiento de la limitación:</span><span class="sxs-lookup"><span data-stu-id="d05e9-124">The following are best practices for handling throttling:</span></span>

* <span data-ttu-id="d05e9-125">Reduzca el número de operaciones por solicitud.</span><span class="sxs-lookup"><span data-stu-id="d05e9-125">Reduce the number of operations per request.</span></span>
* <span data-ttu-id="d05e9-126">Reduzca la frecuencia de llamadas.</span><span class="sxs-lookup"><span data-stu-id="d05e9-126">Reduce the frequency of calls.</span></span>
* <span data-ttu-id="d05e9-127">Evite los reintentos inmediatos, dado que todas las solicitudes se acumulan contra los límites de uso.</span><span class="sxs-lookup"><span data-stu-id="d05e9-127">Avoid immediate retries, because all requests accrue against your usage limits.</span></span>

<span data-ttu-id="d05e9-p105">Cuando se implementa el control de errores, utilice el código de error HTTP 429 para detectar la limitación. La respuesta de error incluye el campo *Retry-After* (volver a intentar más adelante) en el encabezado de la respuesta. Interrumpir las solicitudes mediante el retraso *Retry-After* es la forma más rápida de recuperar la limitación, porque Microsoft Graph sigue registrando el uso de recursos mientras que a un cliente se le está limitando.</span><span class="sxs-lookup"><span data-stu-id="d05e9-p105">When you implement error handling, use the HTTP error code 429 to detect throttling. The failed response includes the *Retry-After* field in the response header. Backing off requests using the *Retry-After* delay is the fastest way to recover from throttling because Microsoft Graph continues to log resource usage while a client is being throttled.</span></span>

1. <span data-ttu-id="d05e9-131">Espere el número de segundos especificado en el campo *Retry-After*.</span><span class="sxs-lookup"><span data-stu-id="d05e9-131">Wait the number of seconds specified in the *Retry-After* field.</span></span>
2. <span data-ttu-id="d05e9-132">Vuelva a intentar realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d05e9-132">Retry the request.</span></span>
3. <span data-ttu-id="d05e9-p106">Si la solicitud vuelve a proporcionar errores con un código de error 429, todavía se le está limitando. Siga utilizando el retraso recomendado Retry-After y vuelva a intentar la solicitud hasta que lo logre.</span><span class="sxs-lookup"><span data-stu-id="d05e9-p106">If the request fails again with a 429 error code, you are still being throttled. Continue to use the recommended Retry-After delay and retry the request until it succeeds.</span></span>

<span data-ttu-id="d05e9-135">Actualmente, los siguientes recursos proporcionan un encabezado retry-after:</span><span class="sxs-lookup"><span data-stu-id="d05e9-135">The following resources currently provide a retry-after header:</span></span>
- [<span data-ttu-id="d05e9-136">Usuario</span><span class="sxs-lookup"><span data-stu-id="d05e9-136">User</span></span>](/graph/api/resources/user?view=graph-rest-1.0)
- [<span data-ttu-id="d05e9-137">Foto</span><span class="sxs-lookup"><span data-stu-id="d05e9-137">Photo</span></span>](/graph/api/resources/profilephoto?view=graph-rest-1.0)
- [<span data-ttu-id="d05e9-138">Correo</span><span class="sxs-lookup"><span data-stu-id="d05e9-138">Mail</span></span>](/graph/api/resources/message?view=graph-rest-1.0)
- [<span data-ttu-id="d05e9-139">Calendario (usuarios y grupos)</span><span class="sxs-lookup"><span data-stu-id="d05e9-139">Calendar (users and groups)</span></span>](/graph/api/resources/event?view=graph-rest-1.0)
- [<span data-ttu-id="d05e9-140">Contacto</span><span class="sxs-lookup"><span data-stu-id="d05e9-140">Contact</span></span>](/graph/api/resources/contact?view=graph-rest-1.0)
- [<span data-ttu-id="d05e9-141">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="d05e9-141">Attachment</span></span>](/graph/api/resources/attachment?view=graph-rest-1.0)
- [<span data-ttu-id="d05e9-142">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="d05e9-142">Group conversations</span></span>](/graph/api/resources/conversation?view=graph-rest-1.0)
- [<span data-ttu-id="d05e9-143">Contactos y redes sociales</span><span class="sxs-lookup"><span data-stu-id="d05e9-143">People and social</span></span>](/graph/api/resources/social-overview?view=graph-rest-beta)
- [<span data-ttu-id="d05e9-144">Unidad (OneDrive)</span><span class="sxs-lookup"><span data-stu-id="d05e9-144">Drive (OneDrive)</span></span>](/graph/api/resources/drive?view=graph-rest-1.0)

<span data-ttu-id="d05e9-145">Para obtener una explicación más amplia de la limitación en Microsoft Cloud, vea [Patrón Throttling](https://msdn.microsoft.com/library/office/dn589798.aspx).</span><span class="sxs-lookup"><span data-stu-id="d05e9-145">For a broader discussion of throttling on the Microsoft Cloud, see [Throttling Pattern](https://msdn.microsoft.com/library/office/dn589798.aspx).</span></span>
