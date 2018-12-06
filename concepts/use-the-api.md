---
title: Usar la API de Microsoft Graph
description: Microsoft Graph es una API para web REST que permite tener acceso a los recursos del servicio Microsoft Cloud. Después de registrar su aplicación y obtener tokens de autenticación para un usuario o servicio, puede realizar solicitudes a la API de Microsoft Graph.
ms.openlocfilehash: 1a9d9bcefdfb302a9de602aa15aa642a0c57a793
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092906"
---
# <a name="use-the-microsoft-graph-api"></a><span data-ttu-id="9e129-104">Usar la API de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="9e129-104">Use the Microsoft Graph API</span></span>

<span data-ttu-id="9e129-p102">Microsoft Graph es una API para web REST que permite tener acceso a los recursos del servicio Microsoft Cloud. Después de [registrar su aplicación](auth-register-app-v2.md) y [obtener tokens de autenticación para un usuario](auth-v2-user.md) o [servicio](auth-v2-service.md), puede realizar solicitudes a la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="9e129-p102">Microsoft Graph is a RESTful web API that enables you to access Microsoft Cloud service resources. After you [register your app](auth-register-app-v2.md) and [get authentication tokens for a user](auth-v2-user.md) or [service](auth-v2-service.md), you can make requests to the Microsoft Graph API.</span></span>

> <span data-ttu-id="9e129-107">**Importante:** Cómo se aplican las directivas de acceso condicional a Microsoft Graph es algo que está cambiando.</span><span class="sxs-lookup"><span data-stu-id="9e129-107">**Important:**  How conditional access policies apply to Microsoft Graph is changing.</span></span> <span data-ttu-id="9e129-108">Las aplicaciones deben actualizarse para administrar los escenarios donde se configuran las directivas de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="9e129-108">Applications need to be updated to handle scenarios where conditional access policies are configured.</span></span> <span data-ttu-id="9e129-109">Para obtener más información y directrices, vea [Instrucciones para desarrolladores para Acceso condicional de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-conditional-access-developer).</span><span class="sxs-lookup"><span data-stu-id="9e129-109">For more information and guidance, see [Developer Guidance for Azure Active Directory Conditional Access](https://docs.microsoft.com/azure/active-directory/develop/active-directory-conditional-access-developer).</span></span>

<span data-ttu-id="9e129-110">Para leer o escribir en recursos como usuarios o mensajes de correo electrónico, se construye una solicitud similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="9e129-110">To read from or write to a resource such as a user or an email message, you construct a request that looks like the following.</span></span>

```http
https://graph.microsoft.com/{version}/{resource}?query-parameters
```

<span data-ttu-id="9e129-111">Los componentes de una solicitud incluyen:</span><span class="sxs-lookup"><span data-stu-id="9e129-111">The components of a request include:</span></span>

* <span data-ttu-id="9e129-112">[Método HTTP](#http-methods): método HTTP utilizado en la solicitud a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="9e129-112">[HTTP method](#http-methods) - The HTTP method used on the request to Microsoft Graph.</span></span>
* <span data-ttu-id="9e129-113">[`{version}`](#version): la versión de la API de Microsoft Graph utilizada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9e129-113">[`{version}`](#version) - The version of the Microsoft Graph API your application is using.</span></span>
* <span data-ttu-id="9e129-114">[`{resource}`](#resource): el recurso de Microsoft Graph al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="9e129-114">[`{resource}`](#resource) - The resource in Microsoft Graph that you're referencing.</span></span>
* <span data-ttu-id="9e129-115">[query-parameters](#query-parameters-optional): un conjunto opcional de parámetros para modificar la solicitud o la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e129-115">[query-parameters](#query-parameters-optional) - An optional set of parameters to modify the request or response.</span></span>

<span data-ttu-id="9e129-116">Después de realizar una solicitud, se devuelve una respuesta que incluye:</span><span class="sxs-lookup"><span data-stu-id="9e129-116">After you make a request, a response is returned that includes:</span></span> 

* <span data-ttu-id="9e129-p104">Código de estado: un código de estado HTTP que indica correcto o incorrecto. Para obtener más información sobre los códigos de error HTTP, consulte [Errores](errors.md).</span><span class="sxs-lookup"><span data-stu-id="9e129-p104">Status code - An HTTP status code that indicates success or failure. For details about HTTP error codes, see [Errors](errors.md).</span></span>
* <span data-ttu-id="9e129-p105">Mensaje de respuesta: los datos que ha solicitado o el resultado de la operación. Con algunas operaciones, el mensaje de respuesta puede estar vacío.</span><span class="sxs-lookup"><span data-stu-id="9e129-p105">Response message - The data that you requested or the result of the operation. The response message can be empty for some operations.</span></span>
* <span data-ttu-id="9e129-p106">Vínculo **Siguiente**: si su solicitud devuelve una gran cantidad de datos, debe recorrer las páginas usando **Siguiente**. Para más información, consulte [Paginación](paging.md).</span><span class="sxs-lookup"><span data-stu-id="9e129-p106">**Next** link - If your request returns a lot of data, you need to page through it by choosing **Next**. For details, see [Paging](paging.md).</span></span>

## <a name="http-methods"></a><span data-ttu-id="9e129-123">Métodos HTTP</span><span class="sxs-lookup"><span data-stu-id="9e129-123">HTTP methods</span></span>

<span data-ttu-id="9e129-p107">Microsoft Graph utiliza el método HTTP en la solicitud para determinar lo que está haciendo la solicitud. La API admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="9e129-p107">Microsoft Graph uses the HTTP method on your request to determine what your request is doing. The API supports the following methods.</span></span>


|<span data-ttu-id="9e129-126">**Método**</span><span class="sxs-lookup"><span data-stu-id="9e129-126">**Method**</span></span> |<span data-ttu-id="9e129-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e129-127">**Description**</span></span>                             |
| :----- | :------------------------------------------- |
| <span data-ttu-id="9e129-128">GET</span><span class="sxs-lookup"><span data-stu-id="9e129-128">GET</span></span>    | <span data-ttu-id="9e129-129">Lee datos de un recurso.</span><span class="sxs-lookup"><span data-stu-id="9e129-129">Read data from a resource.</span></span>                   |
| <span data-ttu-id="9e129-130">POST</span><span class="sxs-lookup"><span data-stu-id="9e129-130">POST</span></span>   | <span data-ttu-id="9e129-131">Crea un nuevo recurso o realiza una acción.</span><span class="sxs-lookup"><span data-stu-id="9e129-131">Create a new resource, or perform an action.</span></span> |
| <span data-ttu-id="9e129-132">PATCH</span><span class="sxs-lookup"><span data-stu-id="9e129-132">PATCH</span></span>  | <span data-ttu-id="9e129-133">Actualiza un recurso con nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="9e129-133">Update a resource with new values.</span></span>           |
| <span data-ttu-id="9e129-134">PUT</span><span class="sxs-lookup"><span data-stu-id="9e129-134">PUT</span></span>    | <span data-ttu-id="9e129-135">Reemplaza un recurso por otro nuevo.</span><span class="sxs-lookup"><span data-stu-id="9e129-135">Replace a resource with a new one.</span></span>           |
| <span data-ttu-id="9e129-136">DELETE</span><span class="sxs-lookup"><span data-stu-id="9e129-136">DELETE</span></span> | <span data-ttu-id="9e129-137">Elimina un recurso.</span><span class="sxs-lookup"><span data-stu-id="9e129-137">Remove a resource.</span></span>                           |

* <span data-ttu-id="9e129-138">Para los métodos **GET** y **DELETE**, no es necesario un cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e129-138">For the methods **GET** and **DELETE**, no request body is required.</span></span>
* <span data-ttu-id="9e129-139">Los métodos **POST**, **PATCH** y **PUT** requieren un cuerpo de la solicitud —generalmente especificado en formato JSON— que contiene información adicional, como los valores de las propiedades del recurso.</span><span class="sxs-lookup"><span data-stu-id="9e129-139">The **POST**, **PATCH**, and **PUT** methods require a request body, usually specified in JSON format, that contains additional information, such as the values for properties of the resource.</span></span>

## <a name="version"></a><span data-ttu-id="9e129-140">Versión</span><span class="sxs-lookup"><span data-stu-id="9e129-140">Version</span></span>

<span data-ttu-id="9e129-141">Microsoft Graph admite actualmente dos versiones: `v1.0` y `beta`.</span><span class="sxs-lookup"><span data-stu-id="9e129-141">Microsoft Graph currently supports two versions: `v1.0` and `beta`.</span></span>

* <span data-ttu-id="9e129-p108">`v1.0` incluye las API que por lo general están disponibles. Utilice la versión v1.0 para todas las aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9e129-p108">`v1.0` includes generally available APIs. Use the v1.0 version for all production apps.</span></span>
* <span data-ttu-id="9e129-p109">`beta` incluye las API que todavía están en versión preliminar. Debido a que podríamos introducir cambios importantes en nuestras API beta, recomendamos que utilice la versión beta solo para probar aplicaciones que están en desarrollo, y no en sus aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9e129-p109">`beta` includes APIs that are currently in preview. Because we might introduce breaking changes to our beta APIs, we recommend that you use the beta version only to test apps that are in development; do not use beta APIs in your production apps.</span></span>

<span data-ttu-id="9e129-p110">Siempre agradecemos los comentarios sobre nuestras API beta. Para dar su opinión o solicitar características, visite nuestra página [UserVoice](https://officespdev.uservoice.com/).</span><span class="sxs-lookup"><span data-stu-id="9e129-p110">We are always looking for feedback on our beta APIs. To provide feedback or request features, see our [UserVoice](https://officespdev.uservoice.com/) page.</span></span>

<span data-ttu-id="9e129-148">Para obtener más información sobre las versiones de API, consulte [Control de versiones y soporte](versioning-and-support.md).</span><span class="sxs-lookup"><span data-stu-id="9e129-148">For more information about API versions, see [Versioning and support](versioning-and-support.md).</span></span>

## <a name="resource"></a><span data-ttu-id="9e129-149">Recurso</span><span class="sxs-lookup"><span data-stu-id="9e129-149">Resource</span></span>

<span data-ttu-id="9e129-p111">La dirección URL incluirá el recurso o los recursos con los que interactúa en la solicitud, como `me`, `users`, `groups`, `drives` y `sites`. Cada uno de los recursos de nivel superior también incluye **relaciones** que se pueden usar para tener acceso a recursos adicionales, como `me/messages` o `me/drive`. También puede interactuar con los recursos mediante **métodos**, por ejemplo, para enviar un correo electrónico, utilice `me/sendMail`.</span><span class="sxs-lookup"><span data-stu-id="9e129-p111">Your URL will include the resource or resources you are interacting with in the request, such as `me`, `users`, `groups`, `drives`, and `sites`. Each of the top-level resources also include **relationships**, which you can use to access additional resources, like `me/messages` or `me/drive`. You can also interact with resources using **methods**; for example, to send an email, use `me/sendMail`.</span></span>

<span data-ttu-id="9e129-153">Para obtener más información sobre cómo desplazarse por los métodos y relaciones de recursos, consulte [Recorrido por Microsoft Graph](traverse-the-graph.md).</span><span class="sxs-lookup"><span data-stu-id="9e129-153">For more information about how to navigate resource relationships and methods, see [Traverse the graph](traverse-the-graph.md).</span></span> 

<span data-ttu-id="9e129-p112">Cada recurso podría necesitar diferentes permisos de acceso. A menudo necesitará un nivel de permisos mayor para crear o actualizar un recurso que para leerlo. Para obtener más información sobre los permisos necesarios, consulte el tema de referencia del método.</span><span class="sxs-lookup"><span data-stu-id="9e129-p112">Each resource might require different permissions to access it. You will often need a higher level of permissions to create or update a resource than to read it. For details about required permissions, see the method reference topic.</span></span> 

<span data-ttu-id="9e129-157">Para obtener más información acerca de los permisos, consulte [Referencia de permisos](permissions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9e129-157">For details about permissions, see [Permissions reference](permissions-reference.md).</span></span>

## <a name="query-parameters-optional"></a><span data-ttu-id="9e129-158">Parámetros de consulta (opcional)</span><span class="sxs-lookup"><span data-stu-id="9e129-158">Query parameters (optional)</span></span>

<span data-ttu-id="9e129-p113">Puede usar parámetros de consulta opcionales para personalizar la respuesta de la aplicación Microsoft Graph. Use parámetros de consulta para incluir más o menos propiedades que la respuesta predeterminada, filtrar la respuesta según los elementos que coincidan con una consulta personalizada o proporcionar parámetros adicionales para un método.</span><span class="sxs-lookup"><span data-stu-id="9e129-p113">You can use optional query parameters to customize the response in your Microsoft Graph app. Use query parameters to include more or fewer properties than the default response, filter the response for items that match a custom query, or provide additional parameters for a method.</span></span>

<span data-ttu-id="9e129-161">Por ejemplo, agregar el siguiente parámetro de filtro restringe los mensajes devueltos solo a aquellos que tengan la propiedad `emailAddress` de `jon@contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="9e129-161">For example, adding the following filter parameter restricts the messages returned to only those with the `emailAddress` property of `jon@contoso.com`.</span></span>

```http
https://graph.microsoft.com/v1.0/me/messages?filter=emailAddress eq 'jon@contoso.com'
```

<span data-ttu-id="9e129-162">Para obtener más información sobre los parámetros de consulta, vea [Personalizar respuestas](query-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9e129-162">For more information about query parameters, see [Customize responses](query-parameters.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="9e129-163">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="9e129-163">Next steps</span></span>

<span data-ttu-id="9e129-p114">Está listo para poner en funcionamiento Microsoft Graph. Para obtener más información, vaya a [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) y pruebe algunas solicitudes y el [Inicio rápido](https://developer.microsoft.com/graph/quick-start), o comience con uno de nuestros [ejemplos de código y SDK](https://developer.microsoft.com/graph/code-samples-and-sdks).</span><span class="sxs-lookup"><span data-stu-id="9e129-p114">You're ready to get up and running with Microsoft Graph. To learn more, go to the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) to try out some requests, try the [Quick Start](https://developer.microsoft.com/graph/quick-start), or get started using one of our [SDKs and code samples](https://developer.microsoft.com/graph/code-samples-and-sdks).</span></span>
