---
title: Códigos de error de las API de OneNote en Microsoft Graph
description: Este artículo describe los códigos de error que devuelven las API de OneNote en Microsoft Graph cuando se produce un error en una solicitud enviada a través de la API.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: f74f9be52756e068aa3e197f2de526b38c187266
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987856"
---
# <a name="error-codes-for-onenote-apis-in-microsoft-graph"></a><span data-ttu-id="a02ba-103">Códigos de error de las API de OneNote en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="a02ba-103">Error codes for OneNote APIs in Microsoft Graph</span></span>

<span data-ttu-id="a02ba-104">Este artículo describe los códigos de error que devuelven las API de OneNote en Microsoft Graph cuando se produce un error en una solicitud enviada a través de la API.</span><span class="sxs-lookup"><span data-stu-id="a02ba-104">This article describes error codes that are returned by the OneNote APIs in Microsoft Graph whenever a request sent through the API fails.</span></span>

## <a name="error-response-example"></a><span data-ttu-id="a02ba-105">Ejemplo de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="a02ba-105">Error response example</span></span>

<span data-ttu-id="a02ba-106">Cuando la solicitud genera un error, la API de OneNote deja de realizar la solicitud y devuelve una respuesta de error como un objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="a02ba-106">When your request generates an error, the OneNote API stops performing the request and returns an error response as a JSON object.</span></span> <span data-ttu-id="a02ba-107">Una respuesta de error contiene el código de error asociado, un mensaje y un vínculo a la sección correspondiente en este artículo.</span><span class="sxs-lookup"><span data-stu-id="a02ba-107">An error response contains the associated error code, a message, and a link to the appropriate section of this article.</span></span> <span data-ttu-id="a02ba-108">El ejemplo siguiente muestra el aspecto de una respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="a02ba-108">The following example shows how an error response looks.</span></span>

```json
{
   "error":{
      "code":"10002",
      "message":"The service is currently unavailable. Please try again later.",
      "innerError": {
        "requestId": "request-id",
        "date": "date-time"
      }
   }
}
```

<span data-ttu-id="a02ba-109">Para obtener más información sobre los errores de Microsoft Graph, consulte [Respuestas de error de Microsoft Graph y tipos de recursos](errors.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-109">For more information about Microsoft Graph errors, see [Microsoft Graph error responses and resource types](errors.md).</span></span>

## <a name="codes-from-10001-to-19999"></a><span data-ttu-id="a02ba-110">Códigos de 10001 a 19999</span><span class="sxs-lookup"><span data-stu-id="a02ba-110">Codes from 10001 to 19999</span></span>

<span data-ttu-id="a02ba-111">El servicio tiene problemas o está enviando información a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-111">The service is having problems or is sending information to the application.</span></span>

### <a name="10001"></a><span data-ttu-id="a02ba-112">10001</span><span class="sxs-lookup"><span data-stu-id="a02ba-112">10001</span></span>
<span data-ttu-id="a02ba-113">Se produjo un error inesperado y la solicitud ha fallado.</span><span class="sxs-lookup"><span data-stu-id="a02ba-113">An unexpected error occurred and the request failed.</span></span>

### <a name="10002"></a><span data-ttu-id="a02ba-114">10002</span><span class="sxs-lookup"><span data-stu-id="a02ba-114">10002</span></span>
<span data-ttu-id="a02ba-115">El servicio no está disponible en este momento.</span><span class="sxs-lookup"><span data-stu-id="a02ba-115">The service is not currently available.</span></span>

### <a name="10003"></a><span data-ttu-id="a02ba-116">10003</span><span class="sxs-lookup"><span data-stu-id="a02ba-116">10003</span></span>
<span data-ttu-id="a02ba-117">La cuenta de usuario actual ha superado el número máximo de solicitudes activas.</span><span class="sxs-lookup"><span data-stu-id="a02ba-117">The current user's account has exceeded the maximum number of active requests.</span></span> <span data-ttu-id="a02ba-118">La aplicación tendrá que repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-118">Your app will have to repeat the request.</span></span>

### <a name="10004"></a><span data-ttu-id="a02ba-119">10004</span><span class="sxs-lookup"><span data-stu-id="a02ba-119">10004</span></span>
<span data-ttu-id="a02ba-120">El servicio no puede crear una página en la sección solicitada porque la sección está protegida por contraseña.</span><span class="sxs-lookup"><span data-stu-id="a02ba-120">The service can't create a page in the requested section because that section is protected by a password.</span></span>

### <a name="10005"></a><span data-ttu-id="a02ba-121">10005</span><span class="sxs-lookup"><span data-stu-id="a02ba-121">10005</span></span>
<span data-ttu-id="a02ba-122">La solicitud contiene más del número máximo de etiquetas de imagen en las que el atributo **data-render-src** contiene un PDF.</span><span class="sxs-lookup"><span data-stu-id="a02ba-122">The request contains more than the maximum number of image tags in which the **data-render-src** attribute contains a PDF.</span></span> <span data-ttu-id="a02ba-123">Vea [Agregar imágenes y archivos](onenote-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-123">See [Add images and files](onenote-images-files.md).</span></span>

### <a name="10006"></a><span data-ttu-id="a02ba-124">10006</span><span class="sxs-lookup"><span data-stu-id="a02ba-124">10006</span></span>
<span data-ttu-id="a02ba-125">La API de OneNote no pudo crear una página en la sección especificada porque esta sección está dañada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-125">The OneNote API was unable to create a page in the specified section because that section is corrupt.</span></span>

### <a name="10007"></a><span data-ttu-id="a02ba-126">10007</span><span class="sxs-lookup"><span data-stu-id="a02ba-126">10007</span></span>
<span data-ttu-id="a02ba-p104">El servidor está demasiado ocupado para atender la solicitud entrante en este momento. Inténtelo de nuevo más tarde.</span><span class="sxs-lookup"><span data-stu-id="a02ba-p104">The server is too busy to handle the incoming request at this moment. Please try again later.</span></span>

### <a name="10008"></a><span data-ttu-id="a02ba-129">10008</span><span class="sxs-lookup"><span data-stu-id="a02ba-129">10008</span></span>
<span data-ttu-id="a02ba-130">Uno o más de las bibliotecas de documentos en OneDrive del usuario o del grupo contiene más de 5000 elementos de OneNote (blocs de notas, secciones, grupos de secciones) y no se puede consultar mediante la API.</span><span class="sxs-lookup"><span data-stu-id="a02ba-130">One or more of the document libraries on the user or group's OneDrive contains more than 5000 OneNote items (notebooks, sections, section groups), and cannot be queried using the API.</span></span> <span data-ttu-id="a02ba-131">Asegúrese de que ninguna de las bibliotecas de documentos del grupo o del usuario contiene más de 5000 elementos de OneNote.</span><span class="sxs-lookup"><span data-stu-id="a02ba-131">Please make sure that none of the user or group's document libraries contains more than 5000 OneNote items.</span></span> <span data-ttu-id="a02ba-132">Consulte el [blog de desarrollo de OneNote](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) para conocer los pasos de mitigación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-132">See the [OneNote Dev blog](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) for mitigation steps.</span></span>

### <a name="10012"></a><span data-ttu-id="a02ba-133">10012</span><span class="sxs-lookup"><span data-stu-id="a02ba-133">10012</span></span>
<span data-ttu-id="a02ba-p106">No se puede crear ni actualizar la entidad porque la biblioteca que contiene el bloc de notas necesita extraer del repositorio los elementos antes de editarlos. Para obtener más información, vea [Configurar una biblioteca para requerir la desprotección de archivos](https://support.office.com/es-ES/article/Configure-a-site-library-to-require-check-out-of-files-f63fcbdc-1db6-4eb7-a3eb-dd815500c9e7).</span><span class="sxs-lookup"><span data-stu-id="a02ba-p106">Unable to create or update the entity because the library that contains the notebook requires items to be checked out before they can be edited. For more information, see [Set up a library to require check-out of files](https://support.office.com/es-ES/article/Configure-a-site-library-to-require-check-out-of-files-f63fcbdc-1db6-4eb7-a3eb-dd815500c9e7).</span></span>

<span data-ttu-id="a02ba-136">Quite el requisito de desprotección de la biblioteca o mueva el bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="a02ba-136">Either remove the check-out requirement from the library, or move the notebook.</span></span>

### <a name="10013"></a><span data-ttu-id="a02ba-137">10013</span><span class="sxs-lookup"><span data-stu-id="a02ba-137">10013</span></span>
<span data-ttu-id="a02ba-p107">Una o más bibliotecas de documentos del OneDrive del usuario o del grupo contienen más de 20 000 elementos y no se pueden indexar para consultas usando la API. Asegúrese de que ninguna biblioteca de documentos del grupo o del usuario contiene más de 20 000 elementos. Consulte el blog [OneNote Dev](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) para ver los pasos de mitigación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-p107">One or more of the document libraries on the user or group's OneDrive contains more than 20,000 items and cannot be indexed for querying using the API. Please make sure that none of the user or group's document libraries contains more than 20,000 items. See the [OneNote Dev blog](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) for mitigation steps.</span></span>

### <a name="10014"></a><span data-ttu-id="a02ba-141">10014</span><span class="sxs-lookup"><span data-stu-id="a02ba-141">10014</span></span>
<span data-ttu-id="a02ba-142">Azure Key Vault está demasiado ocupado para atender la solicitud entrante en este momento.</span><span class="sxs-lookup"><span data-stu-id="a02ba-142">Azure Key Vault is too busy to handle the incoming request at this moment.</span></span> <span data-ttu-id="a02ba-143">Inténtelo de nuevo más tarde.</span><span class="sxs-lookup"><span data-stu-id="a02ba-143">Please try again later.</span></span>

### <a name="10015"></a><span data-ttu-id="a02ba-144">10015</span><span class="sxs-lookup"><span data-stu-id="a02ba-144">10015</span></span>
<span data-ttu-id="a02ba-145">SharePoint no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="a02ba-145">SharePoint is currently unavailable.</span></span> <span data-ttu-id="a02ba-146">Inténtelo de nuevo más tarde.</span><span class="sxs-lookup"><span data-stu-id="a02ba-146">Please try again later.</span></span>

### <a name="10016"></a><span data-ttu-id="a02ba-147">10016</span><span class="sxs-lookup"><span data-stu-id="a02ba-147">10016</span></span>
<span data-ttu-id="a02ba-148">La biblioteca de documentos en OneDrive del usuario o del grupo superó el límite de umbral de ámbitos de seguridad único.</span><span class="sxs-lookup"><span data-stu-id="a02ba-148">Document library on the user or group’s OneDrive exceeded unique security scopes threshold limit.</span></span> <span data-ttu-id="a02ba-149">El número máximo de ámbitos de seguridad únicos establecidos para una biblioteca no debe exceder de 50 000.</span><span class="sxs-lookup"><span data-stu-id="a02ba-149">The maximum number of unique security scopes set for a library cannot exceed 50,000.</span></span>

### <a name="10017"></a><span data-ttu-id="a02ba-150">10017</span><span class="sxs-lookup"><span data-stu-id="a02ba-150">10017</span></span>
<span data-ttu-id="a02ba-151">Solicitud incorrecta (Bad Request)</span><span class="sxs-lookup"><span data-stu-id="a02ba-151">Bad Request.</span></span>

### <a name="19999"></a><span data-ttu-id="a02ba-152">19999</span><span class="sxs-lookup"><span data-stu-id="a02ba-152">19999</span></span>
<span data-ttu-id="a02ba-153">Ha habido un error en la solicitud porque se produjo un error sin determinar.</span><span class="sxs-lookup"><span data-stu-id="a02ba-153">The request failed because an undetermined error occurred.</span></span>

## <a name="codes-from-20001-to-29999"></a><span data-ttu-id="a02ba-154">Códigos de 20001 a 29999</span><span class="sxs-lookup"><span data-stu-id="a02ba-154">Codes from 20001 to 29999</span></span>

<span data-ttu-id="a02ba-155">El código de la aplicación ha hecho algo mal.</span><span class="sxs-lookup"><span data-stu-id="a02ba-155">The application code has done something wrong.</span></span>

### <a name="20001"></a><span data-ttu-id="a02ba-156">20001</span><span class="sxs-lookup"><span data-stu-id="a02ba-156">20001</span></span>

<span data-ttu-id="a02ba-157">Falta la parte "Presentación", necesaria en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-157">The request is missing the required "Presentation" part.</span></span> <span data-ttu-id="a02ba-158">Se necesita exactamente una.</span><span class="sxs-lookup"><span data-stu-id="a02ba-158">Exactly one is required.</span></span> 

### <a name="20002"></a><span data-ttu-id="a02ba-159">20002</span><span class="sxs-lookup"><span data-stu-id="a02ba-159">20002</span></span>
<span data-ttu-id="a02ba-160">La solicitud contiene dos o más partes "Presentación".</span><span class="sxs-lookup"><span data-stu-id="a02ba-160">The request contains two or more "Presentation" parts.</span></span> <span data-ttu-id="a02ba-161">Se necesita exactamente una.</span><span class="sxs-lookup"><span data-stu-id="a02ba-161">Exactly one is required.</span></span>

### <a name="20003"></a><span data-ttu-id="a02ba-162">20003</span><span class="sxs-lookup"><span data-stu-id="a02ba-162">20003</span></span>
<span data-ttu-id="a02ba-163">El tipo de contenido de la parte "Presentación" puede ser solo texto/HTML o aplicación/XHTML+XML.</span><span class="sxs-lookup"><span data-stu-id="a02ba-163">The content type of the "Presentation" part can be only text/HTML or application/XHTML+XML.</span></span> 

### <a name="20004"></a><span data-ttu-id="a02ba-164">20004</span><span class="sxs-lookup"><span data-stu-id="a02ba-164">20004</span></span>
<span data-ttu-id="a02ba-p113">EL HTML de la parte "Presentation" contiene una etiqueta de imagen con el conjunto de propiedades **src** y el **data-render-src**. La API ignorará la propiedad **src** y usará la propiedad **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="a02ba-p113">The "Presentation" part HTML contains an image tag with both the **src** and the **data-render-src** properties set. The API will ignore the **src** property and use the **data-render-src** property.</span></span> 

### <a name="20005"></a><span data-ttu-id="a02ba-167">20005</span><span class="sxs-lookup"><span data-stu-id="a02ba-167">20005</span></span>
<span data-ttu-id="a02ba-168">El URI de la solicitud es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="a02ba-168">The request URI is too long.</span></span> <span data-ttu-id="a02ba-169">El tamaño máximo del URI (incluyendo todos los parámetros y datos) es de 16 KB o 16 384 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a02ba-169">The maximum size of the URI (including all parameters and data) is 16 KB or 16,384 characters.</span></span>

### <a name="20006"></a><span data-ttu-id="a02ba-170">20006</span><span class="sxs-lookup"><span data-stu-id="a02ba-170">20006</span></span>
<span data-ttu-id="a02ba-171">El HTML de la parte "Presentación" contiene una etiqueta de imagen sin los conjuntos de propiedades src o **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="a02ba-171">The "Presentation" part HTML contains an image tag with neither the src nor the **data-render-src** properties set.</span></span> <span data-ttu-id="a02ba-172">La API omitirá la etiqueta **imagen**.</span><span class="sxs-lookup"><span data-stu-id="a02ba-172">The API will ignore the **image** tag.</span></span> 

### <a name="20007"></a><span data-ttu-id="a02ba-173">20007</span><span class="sxs-lookup"><span data-stu-id="a02ba-173">20007</span></span>
<span data-ttu-id="a02ba-174">El código HTML de la parte "Presentation" contiene una cadena de fecha y hora de creación que no coincide con ninguno de los formatos permitidos.</span><span class="sxs-lookup"><span data-stu-id="a02ba-174">The "Presentation" part HTML contains a created date/time string that does not match any of the allowed formats.</span></span> 

### <a name="20008"></a><span data-ttu-id="a02ba-175">20008</span><span class="sxs-lookup"><span data-stu-id="a02ba-175">20008</span></span>
<span data-ttu-id="a02ba-176">El tamaño de la solicitud es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="a02ba-176">The size of the request is too large.</span></span> 

### <a name="20009"></a><span data-ttu-id="a02ba-177">20009</span><span class="sxs-lookup"><span data-stu-id="a02ba-177">20009</span></span>
<span data-ttu-id="a02ba-178">La solicitud contiene partes con nombres duplicados.</span><span class="sxs-lookup"><span data-stu-id="a02ba-178">The request contains parts with duplicate names.</span></span> <span data-ttu-id="a02ba-179">Los nombres de las partes deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="a02ba-179">Part names must be unique.</span></span> 

### <a name="20010"></a><span data-ttu-id="a02ba-180">20010</span><span class="sxs-lookup"><span data-stu-id="a02ba-180">20010</span></span>
<span data-ttu-id="a02ba-181">No se proporcionó el encabezado Content-Disposition para el tipo de contenido especificado.</span><span class="sxs-lookup"><span data-stu-id="a02ba-181">The Content-Disposition header was not supplied for the specified content type.</span></span> 

### <a name="20011"></a><span data-ttu-id="a02ba-182">20011</span><span class="sxs-lookup"><span data-stu-id="a02ba-182">20011</span></span>
<span data-ttu-id="a02ba-183">La solicitud contiene una carga de varias partes con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="a02ba-183">The request contains a malformed multipart payload.</span></span> <span data-ttu-id="a02ba-184">Entre los problemas se incluyen la falta de líneas en blanco, falta de la última línea, separadores de partes con formato incorrecto, etc.</span><span class="sxs-lookup"><span data-stu-id="a02ba-184">Problems could include missing blank lines, a missing last line, incorrectly formatted part separators, and so on.</span></span> <span data-ttu-id="a02ba-185">Si va a crear el mensaje de varias partes a mano, revise cuidadosamente la lógica o considere el uso de una biblioteca de terceros.</span><span class="sxs-lookup"><span data-stu-id="a02ba-185">If you're building the multipart message by hand, carefully check the logic, or consider using a third-party library.</span></span> 

### <a name="20012"></a><span data-ttu-id="a02ba-186">20012</span><span class="sxs-lookup"><span data-stu-id="a02ba-186">20012</span></span>
<span data-ttu-id="a02ba-187">La solicitud no proporciona un tipo de contenido para la parte especificada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-187">The request doesn't supply a content type for the specified part.</span></span> 

### <a name="20013"></a><span data-ttu-id="a02ba-188">20013</span><span class="sxs-lookup"><span data-stu-id="a02ba-188">20013</span></span>
<span data-ttu-id="a02ba-189">La solicitud no proporciona los encabezados Content-Type y Content-Disposition para la parte especificada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-189">The request doesn't supply Content-Type and Content-Disposition headers for the specified part.</span></span> 

### <a name="20014"></a><span data-ttu-id="a02ba-190">20014</span><span class="sxs-lookup"><span data-stu-id="a02ba-190">20014</span></span>
<span data-ttu-id="a02ba-191">La longitud de una parte en el mensaje de varias partes supera el tamaño máximo de 25 MB.</span><span class="sxs-lookup"><span data-stu-id="a02ba-191">The length of a part in the multipart message exceeds the maximum size of 25 MB.</span></span> 

### <a name="20015"></a><span data-ttu-id="a02ba-192">20015</span><span class="sxs-lookup"><span data-stu-id="a02ba-192">20015</span></span>
<span data-ttu-id="a02ba-193">El recuento de partes en el mensaje de varias partes supera el límite de 500.</span><span class="sxs-lookup"><span data-stu-id="a02ba-193">The count of parts in the multipart message exceeds the limit of 500.</span></span> 

### <a name="20016"></a><span data-ttu-id="a02ba-194">20016</span><span class="sxs-lookup"><span data-stu-id="a02ba-194">20016</span></span>
<span data-ttu-id="a02ba-195">La longitud del mensaje de varias partes supera el límite de 75 MB.</span><span class="sxs-lookup"><span data-stu-id="a02ba-195">The length of the multipart message exceeds the limit of 75 MB.</span></span> 

### <a name="20017"></a><span data-ttu-id="a02ba-196">20017</span><span class="sxs-lookup"><span data-stu-id="a02ba-196">20017</span></span>
<span data-ttu-id="a02ba-197">El correo electrónico MIME está mal formado.</span><span class="sxs-lookup"><span data-stu-id="a02ba-197">The email MIME was malformed.</span></span> 

### <a name="20018"></a><span data-ttu-id="a02ba-198">20018</span><span class="sxs-lookup"><span data-stu-id="a02ba-198">20018</span></span>
<span data-ttu-id="a02ba-199">La reunión MIME o ICal está mal formada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-199">The meeting MIME or ICal was malformed.</span></span> 

### <a name="20019"></a><span data-ttu-id="a02ba-200">20019</span><span class="sxs-lookup"><span data-stu-id="a02ba-200">20019</span></span>
<span data-ttu-id="a02ba-201">No se ha encontrado ningún ICal.</span><span class="sxs-lookup"><span data-stu-id="a02ba-201">No ICal was found.</span></span> 

### <a name="20020"></a><span data-ttu-id="a02ba-202">20020</span><span class="sxs-lookup"><span data-stu-id="a02ba-202">20020</span></span>
<span data-ttu-id="a02ba-203">Se encontró JSON con formato incorrecto en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-203">Encountered malformed Json in request body.</span></span> 

### <a name="20100"></a><span data-ttu-id="a02ba-204">20100</span><span class="sxs-lookup"><span data-stu-id="a02ba-204">20100</span></span>
<span data-ttu-id="a02ba-205">Hay algún fallo en la sintaxis de su solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-205">Something is wrong with the syntax of your request.</span></span> 

### <a name="20101"></a><span data-ttu-id="a02ba-206">20101</span><span class="sxs-lookup"><span data-stu-id="a02ba-206">20101</span></span>
<span data-ttu-id="a02ba-207">La propiedad que ha solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="a02ba-207">The property that you requested doesn't exist.</span></span>

### <a name="20102"></a><span data-ttu-id="a02ba-208">20102</span><span class="sxs-lookup"><span data-stu-id="a02ba-208">20102</span></span>
<span data-ttu-id="a02ba-209">Ha solicitado un recurso que no existe.</span><span class="sxs-lookup"><span data-stu-id="a02ba-209">You requested a resource that doesn't exist.</span></span>

### <a name="20103"></a><span data-ttu-id="a02ba-210">20103</span><span class="sxs-lookup"><span data-stu-id="a02ba-210">20103</span></span>
<span data-ttu-id="a02ba-211">La consulta **expand** no se admite para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-211">The **expand** query is not supported for this request.</span></span> <span data-ttu-id="a02ba-212">Vea [Opciones de cadena de consultas OData admitidas](onenote-get-content.md#supported-odata-query-string-options).</span><span class="sxs-lookup"><span data-stu-id="a02ba-212">See [Supported OData query string options](onenote-get-content.md#supported-odata-query-string-options).</span></span>

### <a name="20104"></a><span data-ttu-id="a02ba-213">20104</span><span class="sxs-lookup"><span data-stu-id="a02ba-213">20104</span></span>
<span data-ttu-id="a02ba-p119">La opción de consulta **pagelevel** solo se admite al realizar consultas para la colección de páginas de una sección o de una página específica. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a02ba-p119">The **pagelevel** query option is supported only when querying for the pages collection in a section or for a specific page. For example:</span></span>  

```http
GET ../sections/{id}/pages?pagelevel=true
GET ../pages/{id}?pagelevel=true
```

### <a name="20106"></a><span data-ttu-id="a02ba-216">20106</span><span class="sxs-lookup"><span data-stu-id="a02ba-216">20106</span></span>
<span data-ttu-id="a02ba-217">La solicitud contiene un operador de consulta que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a02ba-217">Your request contains a query operator that is not supported.</span></span> 

### <a name="20108"></a><span data-ttu-id="a02ba-218">20108</span><span class="sxs-lookup"><span data-stu-id="a02ba-218">20108</span></span>
<span data-ttu-id="a02ba-219">La solicitud contiene parámetros de consulta de OData no compatibles.</span><span class="sxs-lookup"><span data-stu-id="a02ba-219">Your request contains unsupported OData query parameters.</span></span>

### <a name="20109"></a><span data-ttu-id="a02ba-220">20109</span><span class="sxs-lookup"><span data-stu-id="a02ba-220">20109</span></span>
<span data-ttu-id="a02ba-221">La carga útil de la solicitud PATCH no se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a02ba-221">The payload in the PATCH request is not constructed correctly.</span></span>

### <a name="20110"></a><span data-ttu-id="a02ba-222">20110</span><span class="sxs-lookup"><span data-stu-id="a02ba-222">20110</span></span>
<span data-ttu-id="a02ba-223">Las solicitudes de creación de la página con partes de datos requieren que el contenido tenga varias partes, con una parte "Presentación".</span><span class="sxs-lookup"><span data-stu-id="a02ba-223">Page create requests with data parts require the content to be multipart, with a "Presentation" part.</span></span> 

### <a name="20111"></a><span data-ttu-id="a02ba-224">20111</span><span class="sxs-lookup"><span data-stu-id="a02ba-224">20111</span></span>
<span data-ttu-id="a02ba-225">La solicitud usa una característica de OData que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a02ba-225">Your request uses an OData feature that isn't supported.</span></span>

### <a name="20112"></a><span data-ttu-id="a02ba-226">20112</span><span class="sxs-lookup"><span data-stu-id="a02ba-226">20112</span></span>
<span data-ttu-id="a02ba-227">Su solicitud contiene un identificador no válido para el bloc de notas de destino, el grupo de sección, la sección o la entidad de la página.</span><span class="sxs-lookup"><span data-stu-id="a02ba-227">Your request contains an invalid ID for the target notebook, section group, section, or page entity.</span></span>

### <a name="20113"></a><span data-ttu-id="a02ba-228">20113</span><span class="sxs-lookup"><span data-stu-id="a02ba-228">20113</span></span>
<span data-ttu-id="a02ba-229">Se ha eliminado el recurso especificado en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-229">The resource specified in the request has been deleted.</span></span>

### <a name="20115"></a><span data-ttu-id="a02ba-230">20115</span><span class="sxs-lookup"><span data-stu-id="a02ba-230">20115</span></span>
<span data-ttu-id="a02ba-231">El nombre contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="a02ba-231">The name contains invalid characters.</span></span> <span data-ttu-id="a02ba-232">El nombre de un bloc de notas no puede contener ninguno de los siguientes caracteres: `? * \ / : < > | ' "`</span><span class="sxs-lookup"><span data-stu-id="a02ba-232">A notebook name cannot contain any of the following characters: `? * \ / : < > | ' "`</span></span>

### <a name="20117"></a><span data-ttu-id="a02ba-233">20117</span><span class="sxs-lookup"><span data-stu-id="a02ba-233">20117</span></span>
<span data-ttu-id="a02ba-234">Ya existe un elemento con el nombre especificado en la ubicación indicada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-234">An item with the name you specified already exists in the location that you specified.</span></span>

### <a name="20119"></a><span data-ttu-id="a02ba-235">20119</span><span class="sxs-lookup"><span data-stu-id="a02ba-235">20119</span></span>
<span data-ttu-id="a02ba-236">El código HTML de la parte "Presentation" contiene un atributo **data-attachment** que no tiene un formato válido o que incluye uno o varios de estos caracteres no válidos para un nombre de archivo: `\ / : * ? < > | "`.</span><span class="sxs-lookup"><span data-stu-id="a02ba-236">The HTML in the "Presentation" part contains a **data-attachment** attribute that either doesn't have a valid format or includes one or more of these invalid characters for a file name: `\ / : * ? < > | "`.</span></span> <span data-ttu-id="a02ba-237">La solicitud sustituye el valor indicado en el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="a02ba-237">The request substituted the value indicated in the error message.</span></span>

### <a name="20120"></a><span data-ttu-id="a02ba-238">20120</span><span class="sxs-lookup"><span data-stu-id="a02ba-238">20120</span></span>
<span data-ttu-id="a02ba-239">Su solicitud especifica un destino PATCH que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="a02ba-239">Your request specifies a PATCH target that can't be located.</span></span>

### <a name="20121"></a><span data-ttu-id="a02ba-240">20121</span><span class="sxs-lookup"><span data-stu-id="a02ba-240">20121</span></span>
<span data-ttu-id="a02ba-p122">La solicitud contiene un argumento PATCH no válido. Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-p122">Your request contains an invalid PATCH argument. See [Update page content](onenote-update-page.md).</span></span>

### <a name="20122"></a><span data-ttu-id="a02ba-243">20122</span><span class="sxs-lookup"><span data-stu-id="a02ba-243">20122</span></span>
<span data-ttu-id="a02ba-p123">La solicitud especifica una acción PATCH no compatible. Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-p123">Your request specifies an unsupported PATCH action. See [Update page content](onenote-update-page.md).</span></span>

### <a name="20123"></a><span data-ttu-id="a02ba-246">20123</span><span class="sxs-lookup"><span data-stu-id="a02ba-246">20123</span></span>
<span data-ttu-id="a02ba-247">La solicitud PATCH no puede modificar la página especificada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-247">The PATCH request is unable to alter the specified page.</span></span>

### <a name="20124"></a><span data-ttu-id="a02ba-248">20124</span><span class="sxs-lookup"><span data-stu-id="a02ba-248">20124</span></span>
<span data-ttu-id="a02ba-249">La solicitud PATCH de varias partes no incluye una parte "commands" con la estructura JSON de la acción PATCH.</span><span class="sxs-lookup"><span data-stu-id="a02ba-249">Your multipart PATCH request doesn't include a "commands" part with the PATCH action JSON structure.</span></span> <span data-ttu-id="a02ba-250">Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-250">See [Update page content](onenote-update-page.md).</span></span>

### <a name="20125"></a><span data-ttu-id="a02ba-251">20125</span><span class="sxs-lookup"><span data-stu-id="a02ba-251">20125</span></span>
<span data-ttu-id="a02ba-p125">La solicitud PATCH no contiene acciones. Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-p125">Your PATCH request contains no actions. See [Update page content](onenote-update-page.md).</span></span>

### <a name="20126"></a><span data-ttu-id="a02ba-254">20126</span><span class="sxs-lookup"><span data-stu-id="a02ba-254">20126</span></span>
<span data-ttu-id="a02ba-255">El cuerpo del mensaje contiene JSON con un formato incorrecto o campos que no son compatibles con esta operación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-255">The message body contains either incorrectly formatted JSON or fields that are not supported for this operation.</span></span>

### <a name="20127"></a><span data-ttu-id="a02ba-256">20127</span><span class="sxs-lookup"><span data-stu-id="a02ba-256">20127</span></span>
<span data-ttu-id="a02ba-257">La solicitud especifica el nombre de una propiedad desconocida.</span><span class="sxs-lookup"><span data-stu-id="a02ba-257">Your request specifies the name of an unknown property.</span></span>

### <a name="20128"></a><span data-ttu-id="a02ba-258">20128</span><span class="sxs-lookup"><span data-stu-id="a02ba-258">20128</span></span>
<span data-ttu-id="a02ba-259">La solicitud contiene un error de sintaxis de OData en la posición indicada en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a02ba-259">Your request contains an OData syntax error at the position indicated in the message.</span></span>

### <a name="20129"></a><span data-ttu-id="a02ba-260">20129</span><span class="sxs-lookup"><span data-stu-id="a02ba-260">20129</span></span>
<span data-ttu-id="a02ba-261">La solicitud contiene una opción de la cadena de consulta **top** cuyo valor es demasiado alto.</span><span class="sxs-lookup"><span data-stu-id="a02ba-261">Your request contains a **top** query string option whose value is too high.</span></span> <span data-ttu-id="a02ba-262">Para las consultas de páginas, el valor máximo es 100 y el valor predeterminado es 20.</span><span class="sxs-lookup"><span data-stu-id="a02ba-262">For page queries, the maximum value is 100, and the default value is 20.</span></span>

### <a name="20130"></a><span data-ttu-id="a02ba-263">20130</span><span class="sxs-lookup"><span data-stu-id="a02ba-263">20130</span></span>
<span data-ttu-id="a02ba-264">La solicitud contiene un URI que apunta a un recurso de HTTP que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="a02ba-264">Your request contains a URI that points to an HTTP resource that can't be found.</span></span>

### <a name="20131"></a><span data-ttu-id="a02ba-265">20131</span><span class="sxs-lookup"><span data-stu-id="a02ba-265">20131</span></span>
<span data-ttu-id="a02ba-266">La solicitud contiene un valor no válido para Content-Type.</span><span class="sxs-lookup"><span data-stu-id="a02ba-266">Your request contains an invalid value for Content-Type.</span></span> <span data-ttu-id="a02ba-267">Use el valor indicado en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a02ba-267">Use the value indicated in the message.</span></span> 

### <a name="20132"></a><span data-ttu-id="a02ba-268">20132</span><span class="sxs-lookup"><span data-stu-id="a02ba-268">20132</span></span>
<span data-ttu-id="a02ba-269">Su solicitud incluye contenido no válido.</span><span class="sxs-lookup"><span data-stu-id="a02ba-269">Your request contains invalid content.</span></span> <span data-ttu-id="a02ba-270">Las causas comunes son la falta de un encabezado Content-Type o un cuerpo de la solicitud sin contenido.</span><span class="sxs-lookup"><span data-stu-id="a02ba-270">Common causes for this are a missing Content-Type request header and/or no content in the body of the request.</span></span> 

### <a name="20133"></a><span data-ttu-id="a02ba-271">20133</span><span class="sxs-lookup"><span data-stu-id="a02ba-271">20133</span></span>
<span data-ttu-id="a02ba-272">Su solicitud especifica un destino PATCH que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a02ba-272">Your request specifies a PATCH target that is not supported.</span></span> <span data-ttu-id="a02ba-273">Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-273">See [Update page content](onenote-update-page.md).</span></span>

### <a name="20134"></a><span data-ttu-id="a02ba-274">20134</span><span class="sxs-lookup"><span data-stu-id="a02ba-274">20134</span></span>
<span data-ttu-id="a02ba-p130">La solicitud especifica un elemento no válido como destino de la acción PATCH. Si el destino usa el identificador **data-id**, asegúrese de que tenga el símbolo # como prefijo. Consulte [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-p130">Your request specifies an invalid element as the target of the PATCH action. If the target uses the **data-id** identifier, make sure it's prefixed with a # symbol. See [Update page content](onenote-update-page.md).</span></span>

### <a name="20135"></a><span data-ttu-id="a02ba-278">20135</span><span class="sxs-lookup"><span data-stu-id="a02ba-278">20135</span></span>
<span data-ttu-id="a02ba-279">Su solicitud especifica un tipo de entidad que no es compatible con la operación PATCH.</span><span class="sxs-lookup"><span data-stu-id="a02ba-279">Your request specifies an entity type that is not supported for the PATCH operation.</span></span> <span data-ttu-id="a02ba-280">Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-280">See [Update page content](onenote-update-page.md).</span></span>

### <a name="20136"></a><span data-ttu-id="a02ba-281">20136</span><span class="sxs-lookup"><span data-stu-id="a02ba-281">20136</span></span>
<span data-ttu-id="a02ba-282">La solicitud contiene un atributo **data-render-src** o **data-render-method** no válido o que falta.</span><span class="sxs-lookup"><span data-stu-id="a02ba-282">Your request contains an invalid or missing **data-render-src** or **data-render-method** attribute.</span></span> <span data-ttu-id="a02ba-283">Vea [Extraer los datos de las capturas](onenote-extract-data.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-283">See [Extract data from captures](onenote-extract-data.md).</span></span>

### <a name="20137"></a><span data-ttu-id="a02ba-284">20137</span><span class="sxs-lookup"><span data-stu-id="a02ba-284">20137</span></span>
<span data-ttu-id="a02ba-285">La página de destino no admite solicitudes PATCH.</span><span class="sxs-lookup"><span data-stu-id="a02ba-285">The target page does not support PATCH requests.</span></span>

### <a name="20138"></a><span data-ttu-id="a02ba-286">20138</span><span class="sxs-lookup"><span data-stu-id="a02ba-286">20138</span></span>
<span data-ttu-id="a02ba-p133">El tipo de elemento de destino de la solicitud PATCH no admite la acción **append** especificada. Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-p133">The target element type in your PATCH request doesn't support the **append** action. See [Update page content](onenote-update-page.md).</span></span>

### <a name="20139"></a><span data-ttu-id="a02ba-289">20139</span><span class="sxs-lookup"><span data-stu-id="a02ba-289">20139</span></span>
<span data-ttu-id="a02ba-p134">La solicitud contiene un valor de atributo **data-tag** no válido. Vea [Usar etiquetas de nota](onenote-note-tags.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-p134">Your request contains an invalid **data-tag** attribute value. See [Use note tags](onenote-note-tags.md).</span></span>

### <a name="20140"></a><span data-ttu-id="a02ba-292">20140</span><span class="sxs-lookup"><span data-stu-id="a02ba-292">20140</span></span>
<span data-ttu-id="a02ba-293">La solicitud contiene un valor de estado **data-tag** no válido.</span><span class="sxs-lookup"><span data-stu-id="a02ba-293">Your request contains an invalid **data-tag** status value.</span></span> <span data-ttu-id="a02ba-294">Las etiquetas de nota de casillas pueden tener un estado **completed**.</span><span class="sxs-lookup"><span data-stu-id="a02ba-294">Check box note tags can have a **completed** status.</span></span> 

<span data-ttu-id="a02ba-295">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a02ba-295">Example:</span></span>

```html
    <p data-tag="to-do:completed">To-do note tag in completed state (checked box in the UI)</p>
```
<span data-ttu-id="a02ba-296">Vea [Uso de etiquetas de nota](onenote-note-tags.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-296">See [Use note tags](onenote-note-tags.md).</span></span>

### <a name="20141"></a><span data-ttu-id="a02ba-297">20141</span><span class="sxs-lookup"><span data-stu-id="a02ba-297">20141</span></span>
<span data-ttu-id="a02ba-298">El destino de la solicitud PATCH no admite la acción especificada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-298">The target in your PATCH request doesn't support the specified action.</span></span> <span data-ttu-id="a02ba-299">Vea [Actualizar contenido de la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-299">See [Update page content](onenote-update-page.md).</span></span>

### <a name="20142"></a><span data-ttu-id="a02ba-300">20142</span><span class="sxs-lookup"><span data-stu-id="a02ba-300">20142</span></span>
<span data-ttu-id="a02ba-301">La solicitud contiene una expresión **expand** para un elemento primario de entidades secundarias o un elemento secundario de entidades primarias, lo cual no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a02ba-301">Your request contains an **expand** expression for a parent of child entities or a child of parent entities, which is not supported.</span></span> <span data-ttu-id="a02ba-302">Vea [Opciones de cadena de consultas OData admitidas](onenote-get-content.md#supported-odata-query-string-options).</span><span class="sxs-lookup"><span data-stu-id="a02ba-302">See [Supported OData query string options](onenote-get-content.md#supported-odata-query-string-options).</span></span>

### <a name="20143"></a><span data-ttu-id="a02ba-303">20143</span><span class="sxs-lookup"><span data-stu-id="a02ba-303">20143</span></span>
<span data-ttu-id="a02ba-304">La consulta OData no es válida.</span><span class="sxs-lookup"><span data-stu-id="a02ba-304">The OData query is invalid.</span></span>

### <a name="20144"></a><span data-ttu-id="a02ba-305">20144</span><span class="sxs-lookup"><span data-stu-id="a02ba-305">20144</span></span>
<span data-ttu-id="a02ba-306">La solicitud contiene una expresión **expand** para una propiedad de no navegación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-306">Your request contains an **expand** expression for a non-navigation property.</span></span> <span data-ttu-id="a02ba-307">Únicamente se pueden expandir las propiedades de navegación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-307">Only navigation properties can be expanded.</span></span>

### <a name="20145"></a><span data-ttu-id="a02ba-308">20145</span><span class="sxs-lookup"><span data-stu-id="a02ba-308">20145</span></span>
<span data-ttu-id="a02ba-309">La expresión **select** o **expand** de la solicitud contiene un término no válido.</span><span class="sxs-lookup"><span data-stu-id="a02ba-309">The **select** or **expand** expression in your request contains an invalid term.</span></span>

### <a name="20146"></a><span data-ttu-id="a02ba-310">20146</span><span class="sxs-lookup"><span data-stu-id="a02ba-310">20146</span></span>
<span data-ttu-id="a02ba-311">El atributo `style="position:absolute"` se especifica en un elemento, pero el elemento **body** no especifica `data-absolute-enabled="true"`, que es necesario para admitir el posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="a02ba-311">The `style="position:absolute"` attribute is specified on an element, but the **body** element does not specify `data-absolute-enabled="true"`, which is required to support positioning.</span></span> <span data-ttu-id="a02ba-312">Se omitirán todas las configuraciones de posición.</span><span class="sxs-lookup"><span data-stu-id="a02ba-312">All position settings will be ignored.</span></span> <span data-ttu-id="a02ba-313">Vea [Crear elementos con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-313">See [Create absolute positioned elements](onenote-abs-pos.md).</span></span>

### <a name="20147"></a><span data-ttu-id="a02ba-314">20147</span><span class="sxs-lookup"><span data-stu-id="a02ba-314">20147</span></span>
<span data-ttu-id="a02ba-315">El atributo `style="position:absolute"` se especifica en un elemento que no es un elemento secundario directo del elemento **body**, que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a02ba-315">The `style="position:absolute"` attribute is specified on an element that is not a direct child of the **body** element, which is not supported.</span></span> <span data-ttu-id="a02ba-316">Si el elemento es un **div**, \*\*img \*\*u **object**, haga que sea un elemento secundario directo del cuerpo; en caso contrario, se pasarán por alto los valores de posición y representará su contenido dentro de un div de posición absoluta</span><span class="sxs-lookup"><span data-stu-id="a02ba-316">If the element is a **div**, **img**, or **object**, make it a direct child of the body; otherwise the position settings will be ignored and its content will render inside an absolute positioned div.</span></span> <span data-ttu-id="a02ba-317">Vea [Crear elementos con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-317">See [Create absolute positioned elements](onenote-abs-pos.md).</span></span>

### <a name="20148"></a><span data-ttu-id="a02ba-318">20148</span><span class="sxs-lookup"><span data-stu-id="a02ba-318">20148</span></span>
<span data-ttu-id="a02ba-319">El atributo `style="position:absolute"` se especifica en un tipo de elemento que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a02ba-319">The `style="position:absolute"` attribute is specified on an element type that does not support it.</span></span> <span data-ttu-id="a02ba-320">Solo **div**, **img** y **object** admiten la posición de los elementos que son elementos secundarios directos del cuerpo de la página.</span><span class="sxs-lookup"><span data-stu-id="a02ba-320">Only **div**, **img**, and **object** elements that are direct children of the page body support positioning.</span></span> <span data-ttu-id="a02ba-321">Vea [Crear elementos con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="a02ba-321">See [Create absolute positioned elements](onenote-abs-pos.md).</span></span>

### <a name="20149"></a><span data-ttu-id="a02ba-322">20149</span><span class="sxs-lookup"><span data-stu-id="a02ba-322">20149</span></span>
<span data-ttu-id="a02ba-323">Su solicitud especifica un elemento de destino que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="a02ba-323">Your request specifies a target element that cannot be found.</span></span>

### <a name="20150"></a><span data-ttu-id="a02ba-324">20150</span><span class="sxs-lookup"><span data-stu-id="a02ba-324">20150</span></span>
<span data-ttu-id="a02ba-325">La solicitud no es válida para este tipo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-325">The request is not valid for this authentication type.</span></span> <span data-ttu-id="a02ba-326">Use la ruta de acceso `../me/onenote/` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a02ba-326">Use the `../me/onenote/` path instead.</span></span>

### <a name="20151"></a><span data-ttu-id="a02ba-327">20151</span><span class="sxs-lookup"><span data-stu-id="a02ba-327">20151</span></span>
<span data-ttu-id="a02ba-328">La solicitud no es válida para este tipo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="a02ba-328">The request is not valid for this authentication type.</span></span> <span data-ttu-id="a02ba-329">Use el punto de conexión `../me/onenote/section/{id}/pages` para crear una página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="a02ba-329">Use the `../me/onenote/section/{id}/pages` endpoint to create a page in a specific section.</span></span>

### <a name="20152"></a><span data-ttu-id="a02ba-330">20152</span><span class="sxs-lookup"><span data-stu-id="a02ba-330">20152</span></span>
<span data-ttu-id="a02ba-p144">No hay ningún valor name especificado para la entidad. El nombre debe estar definido y no puede contener solo espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="a02ba-p144">There is no name value specified for the entity. The name must be defined, and it cannot contain whitespaces only.</span></span>

### <a name="20153"></a><span data-ttu-id="a02ba-333">20153</span><span class="sxs-lookup"><span data-stu-id="a02ba-333">20153</span></span>
<span data-ttu-id="a02ba-334">El nombre de la entidad contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="a02ba-334">The entity name contains invalid characters.</span></span> <span data-ttu-id="a02ba-335">El nombre de la organización no puede contener los siguientes caracteres: `? * \ / : < > | & # " % ~`</span><span class="sxs-lookup"><span data-stu-id="a02ba-335">The name cannot contain the following characters: `? * \ / : < > | & # " % ~`</span></span>

### <a name="20154"></a><span data-ttu-id="a02ba-336">20154</span><span class="sxs-lookup"><span data-stu-id="a02ba-336">20154</span></span>
<span data-ttu-id="a02ba-337">El nombre de la entidad no puede comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="a02ba-337">The entity name cannot start with a space.</span></span>

### <a name="20155"></a><span data-ttu-id="a02ba-338">20155</span><span class="sxs-lookup"><span data-stu-id="a02ba-338">20155</span></span>
<span data-ttu-id="a02ba-339">El nombre de entidad es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="a02ba-339">The entity name is too long.</span></span> <span data-ttu-id="a02ba-340">Los nombres de los blocs de notas tienen un límite de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a02ba-340">Notebook names have a 128-character limit.</span></span> <span data-ttu-id="a02ba-341">Los nombres de otras entidades tienen un límite de 50 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a02ba-341">Other entity names have a 50-character limit.</span></span>

### <a name="20156"></a><span data-ttu-id="a02ba-342">20156</span><span class="sxs-lookup"><span data-stu-id="a02ba-342">20156</span></span>
<span data-ttu-id="a02ba-343">El identificador especificado para el recurso de destino no existe.</span><span class="sxs-lookup"><span data-stu-id="a02ba-343">The specified ID for the destination resource does not exist.</span></span>

### <a name="20157"></a><span data-ttu-id="a02ba-344">20157</span><span class="sxs-lookup"><span data-stu-id="a02ba-344">20157</span></span>
<span data-ttu-id="a02ba-345">El identificador especificado para la entidad de destino no es válido.</span><span class="sxs-lookup"><span data-stu-id="a02ba-345">The specified ID for the destination entity is invalid.</span></span>

### <a name="20158"></a><span data-ttu-id="a02ba-346">20158</span><span class="sxs-lookup"><span data-stu-id="a02ba-346">20158</span></span>
<span data-ttu-id="a02ba-347">No se pueden obtener los metadatos de la dirección URL del sitio especificada en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-347">Unable to get metadata for the site URL specified in the request.</span></span> <span data-ttu-id="a02ba-348">Compruebe el formato de la dirección URL suministrada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-348">Check the format of the supplied URL.</span></span> <span data-ttu-id="a02ba-349">Los formatos admitidos son `https://domain.sharepoint.com/site-a` y `https://domain.com/sites/site-a`.</span><span class="sxs-lookup"><span data-stu-id="a02ba-349">Supported formats include `https://domain.sharepoint.com/site-a` and `https://domain.com/sites/site-a`.</span></span>

### <a name="20160"></a><span data-ttu-id="a02ba-350">20160</span><span class="sxs-lookup"><span data-stu-id="a02ba-350">20160</span></span>
<span data-ttu-id="a02ba-351">No se puede encontrar un grupo unificado de Office 365 con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="a02ba-351">Unable to find an Office 365 unified group that has the specified ID.</span></span>

### <a name="20161"></a><span data-ttu-id="a02ba-352">20161</span><span class="sxs-lookup"><span data-stu-id="a02ba-352">20161</span></span>
<span data-ttu-id="a02ba-353">El contexto no especifica ningún Id. de usuario válido.</span><span class="sxs-lookup"><span data-stu-id="a02ba-353">The context does not specify a valid user ID.</span></span> <span data-ttu-id="a02ba-354">Un error frecuente es que PUID/CID se ha pasado como un long en lugar de un hex.</span><span class="sxs-lookup"><span data-stu-id="a02ba-354">One common error is that PUID/CID was passed in as a long instead of a hex.</span></span>

### <a name="20166"></a><span data-ttu-id="a02ba-355">20166</span><span class="sxs-lookup"><span data-stu-id="a02ba-355">20166</span></span>
<span data-ttu-id="a02ba-356">La aplicación ha emitido demasiadas solicitudes en nombre de un usuario en un corto período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a02ba-356">The application has issued too many requests on behalf of a user in a short period of time.</span></span> <span data-ttu-id="a02ba-357">Para ayudar a garantizar que la API de OneNote permanece estable y con capacidad de respuesta, la API devuelve un código de estado 429 y este error cuando detecta que una aplicación está usando demasiados recursos.</span><span class="sxs-lookup"><span data-stu-id="a02ba-357">To help ensure that the OneNote API remains stable and responsive, the API returns a 429 status code and this error when it detects that an application is using too many resources.</span></span> 

<span data-ttu-id="a02ba-358">Para obtener más información, consulte [OneNote API throttling and how to avoid it](https://blogs.msdn.com/b/onenotedev/archive/2016/01/13/onenote-api-throttling-and-best-practices.aspx) (Limitación de la API de OneNote y cómo evitarla).</span><span class="sxs-lookup"><span data-stu-id="a02ba-358">For more information, see [OneNote API throttling and how to avoid it](https://blogs.msdn.com/b/onenotedev/archive/2016/01/13/onenote-api-throttling-and-best-practices.aspx).</span></span>

### <a name="20168"></a><span data-ttu-id="a02ba-359">20168</span><span class="sxs-lookup"><span data-stu-id="a02ba-359">20168</span></span>
<span data-ttu-id="a02ba-360">No se admite el origen de vídeo especificado en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-360">The video source specified in the request is not supported.</span></span> <span data-ttu-id="a02ba-361">Vea [Sitios de vídeo compatibles](onenote-images-files.md#adding-videos) para obtener la lista actual.</span><span class="sxs-lookup"><span data-stu-id="a02ba-361">See [Supported video sites](onenote-images-files.md#adding-videos) for the current list.</span></span>


## <a name="codes-from-30001-to-39999"></a><span data-ttu-id="a02ba-362">Códigos de 30001 a 39999</span><span class="sxs-lookup"><span data-stu-id="a02ba-362">Codes from 30001 to 39999</span></span>
<span data-ttu-id="a02ba-363">Hay algún fallo en la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-363">Something is wrong with the user's account.</span></span>

### <a name="30101"></a><span data-ttu-id="a02ba-364">30101</span><span class="sxs-lookup"><span data-stu-id="a02ba-364">30101</span></span>
<span data-ttu-id="a02ba-365">La cuenta de usuario ha excedido su cuota de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="a02ba-365">The user account has exceeded its OneDrive quota.</span></span> <span data-ttu-id="a02ba-366">Vea [OneDrive](https://onedrive.live.com/about/es-ES/).</span><span class="sxs-lookup"><span data-stu-id="a02ba-366">See [OneDrive](https://onedrive.live.com/about/es-ES/).</span></span>

### <a name="30102"></a><span data-ttu-id="a02ba-367">30102</span><span class="sxs-lookup"><span data-stu-id="a02ba-367">30102</span></span>
<span data-ttu-id="a02ba-368">No se puede agregar nada más a la sección solicitada porque ha alcanzado su tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="a02ba-368">Nothing more can be added to the requested section because it has reached its maximum size.</span></span>

### <a name="30103"></a><span data-ttu-id="a02ba-369">30103</span><span class="sxs-lookup"><span data-stu-id="a02ba-369">30103</span></span>
<span data-ttu-id="a02ba-370">El consumo de recursos es demasiado alto para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-370">Resource consumption is too high for the request.</span></span> <span data-ttu-id="a02ba-371">La cuenta de usuario de destino tiene un gran conjunto de datos o el servicio está recibiendo un gran número de solicitudes simultáneas para el mismo sitio (por ejemplo, el sitio personal del usuario o un sitio de grupo).</span><span class="sxs-lookup"><span data-stu-id="a02ba-371">Either the target user account has a large dataset, or the service is receiving a high number of concurrent requests to the same site (for example, the user's personal site or a team site).</span></span>

### <a name="30104"></a><span data-ttu-id="a02ba-372">30104</span><span class="sxs-lookup"><span data-stu-id="a02ba-372">30104</span></span>
<span data-ttu-id="a02ba-373">Se ha suspendido la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-373">The user account has been suspended.</span></span>

### <a name="30105"></a><span data-ttu-id="a02ba-374">30105</span><span class="sxs-lookup"><span data-stu-id="a02ba-374">30105</span></span>
<span data-ttu-id="a02ba-375">No se ha aprovisionado el OneDrive for Business del usuario, que es necesario para los portátiles de acceso.</span><span class="sxs-lookup"><span data-stu-id="a02ba-375">The user's personal OneDrive for Business site is not provisioned, which is required to access notebooks.</span></span> <span data-ttu-id="a02ba-376">El servicio de OneNote aprovisionará el sitio ahora.</span><span class="sxs-lookup"><span data-stu-id="a02ba-376">The OneNote service will provision the site now.</span></span> <span data-ttu-id="a02ba-377">Este proceso puede tardar varios minutos.</span><span class="sxs-lookup"><span data-stu-id="a02ba-377">This process may take several minutes.</span></span>

### <a name="30106"></a><span data-ttu-id="a02ba-378">30106</span><span class="sxs-lookup"><span data-stu-id="a02ba-378">30106</span></span>
<span data-ttu-id="a02ba-379">OneDrive for Business se está aprovisionando para el usuario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-379">OneDrive for Business is being provisioned for the user.</span></span>

### <a name="30108"></a><span data-ttu-id="a02ba-380">30108</span><span class="sxs-lookup"><span data-stu-id="a02ba-380">30108</span></span>
<span data-ttu-id="a02ba-381">No se pudo recuperar el OneDrive for Business personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-381">The user's personal OneDrive for Business could not be retrieved.</span></span> <span data-ttu-id="a02ba-382">En la tabla siguiente se enumeran algunas causas posibles.</span><span class="sxs-lookup"><span data-stu-id="a02ba-382">The following table lists some possible causes.</span></span>

| <span data-ttu-id="a02ba-383">Motivo</span><span class="sxs-lookup"><span data-stu-id="a02ba-383">Cause</span></span> | <span data-ttu-id="a02ba-384">Solución</span><span class="sxs-lookup"><span data-stu-id="a02ba-384">Resolution</span></span> |
|:------|:------|
| <span data-ttu-id="a02ba-385">No se ha aprovisionado el sitio personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-385">The user's personal site has not been provisioned.</span></span> | <span data-ttu-id="a02ba-386">El usuario debe abrir OneDrive for Business y seguir las instrucciones para crear el sitio.</span><span class="sxs-lookup"><span data-stu-id="a02ba-386">The user should open OneDrive for Business and follow any instructions to provision the site.</span></span> <span data-ttu-id="a02ba-387">Si esto no funciona, deben ponerse en contacto con su administrador de inquilinos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="a02ba-387">If this fails, they should contact their Office 365 tenant administrator.</span></span> |
| <span data-ttu-id="a02ba-388">Actualmente se está aprovisionando el sitio personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-388">The user's personal site is currently being provisioned.</span></span> | <span data-ttu-id="a02ba-389">Intente de nuevo la solicitud más tarde.</span><span class="sxs-lookup"><span data-stu-id="a02ba-389">Try the request later.</span></span> |
| <span data-ttu-id="a02ba-390">El usuario no tiene un OneDrive válido para la licencia de la empresa.</span><span class="sxs-lookup"><span data-stu-id="a02ba-390">The user does not have a valid OneDrive for Business license.</span></span> | <span data-ttu-id="a02ba-391">El usuario debe ponerse en contacto con su administrador de inquilinos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="a02ba-391">The user should contact their Office 365 tenant administrator.</span></span> |
| <span data-ttu-id="a02ba-392">Un problema de red ha impedido que la solicitud se enviase correctamente.</span><span class="sxs-lookup"><span data-stu-id="a02ba-392">A network issue prevented the request from being successfully sent.</span></span> | <span data-ttu-id="a02ba-393">Intente de nuevo la solicitud más tarde.</span><span class="sxs-lookup"><span data-stu-id="a02ba-393">Try the request later.</span></span> |

### <a name="30109"></a><span data-ttu-id="a02ba-394">30109</span><span class="sxs-lookup"><span data-stu-id="a02ba-394">30109</span></span>
<span data-ttu-id="a02ba-395">No existen algunos usuarios de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a02ba-395">Some users in the request do not exist.</span></span>

### <a name="30110"></a><span data-ttu-id="a02ba-396">30110</span><span class="sxs-lookup"><span data-stu-id="a02ba-396">30110</span></span>
<span data-ttu-id="a02ba-397">Los servicios de información de alumno no se han registrado para este arrendatario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-397">Student Information Services has not been registered for this tenant.</span></span>

### <a name="30111"></a><span data-ttu-id="a02ba-398">30111</span><span class="sxs-lookup"><span data-stu-id="a02ba-398">30111</span></span>
<span data-ttu-id="a02ba-399">Hay un error genérico con los servicios de información del alumno.</span><span class="sxs-lookup"><span data-stu-id="a02ba-399">There is a generic error with Student Information Services.</span></span>

### <a name="30112"></a><span data-ttu-id="a02ba-400">30112</span><span class="sxs-lookup"><span data-stu-id="a02ba-400">30112</span></span>
<span data-ttu-id="a02ba-401">Varios usuarios afectados por la solicitud tenían el mismo nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-401">Multiple users affected by the request had the same username.</span></span>

### <a name="30113"></a><span data-ttu-id="a02ba-402">30113</span><span class="sxs-lookup"><span data-stu-id="a02ba-402">30113</span></span>
<span data-ttu-id="a02ba-403">El bloc de notas no está configurado para permitir invitaciones.</span><span class="sxs-lookup"><span data-stu-id="a02ba-403">The notebook is not configured to allow invites.</span></span>

### <a name="30114"></a><span data-ttu-id="a02ba-404">30114</span><span class="sxs-lookup"><span data-stu-id="a02ba-404">30114</span></span>
<span data-ttu-id="a02ba-405">Falta un parámetro necesario.</span><span class="sxs-lookup"><span data-stu-id="a02ba-405">There is a required parameter missing.</span></span>

## <a name="codes-from-40001-to-49999"></a><span data-ttu-id="a02ba-406">Códigos de 40001 a 49999</span><span class="sxs-lookup"><span data-stu-id="a02ba-406">Codes from 40001 to 49999</span></span>
<span data-ttu-id="a02ba-407">El usuario o la aplicación no tienen los permisos correctos.</span><span class="sxs-lookup"><span data-stu-id="a02ba-407">The user or application does not have the correct permissions.</span></span>

### <a name="40001"></a><span data-ttu-id="a02ba-408">40001</span><span class="sxs-lookup"><span data-stu-id="a02ba-408">40001</span></span>
<span data-ttu-id="a02ba-409">La solicitud no contiene un token válido de OAuth.</span><span class="sxs-lookup"><span data-stu-id="a02ba-409">The request doesn't contain a valid OAuth token.</span></span> <span data-ttu-id="a02ba-410">Vea [Permisos de notas](permissions-reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="a02ba-410">See [Notes permissions](permissions-reference.md#notes-permissions).</span></span>

### <a name="40002"></a><span data-ttu-id="a02ba-411">40002</span><span class="sxs-lookup"><span data-stu-id="a02ba-411">40002</span></span>
<span data-ttu-id="a02ba-412">El usuario no tiene permiso para escribir en la ubicación solicitada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-412">The user doesn't have permission to write to the requested location.</span></span>

### <a name="40003"></a><span data-ttu-id="a02ba-413">40003</span><span class="sxs-lookup"><span data-stu-id="a02ba-413">40003</span></span>
<span data-ttu-id="a02ba-414">El usuario no tiene permiso para acceder al recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="a02ba-414">The user doesn't have permission to access the requested resource.</span></span>

### <a name="40004"></a><span data-ttu-id="a02ba-415">40004</span><span class="sxs-lookup"><span data-stu-id="a02ba-415">40004</span></span>
<span data-ttu-id="a02ba-416">El token de OAuth no tiene los ámbitos necesarios para realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-416">The OAuth token doesn't have the required scopes to perform the requested action.</span></span> <span data-ttu-id="a02ba-417">Vea [Permisos de notas](permissions-reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="a02ba-417">See [Notes permissions](permissions-reference.md#notes-permissions).</span></span>

### <a name="40006"></a><span data-ttu-id="a02ba-418">40006</span><span class="sxs-lookup"><span data-stu-id="a02ba-418">40006</span></span> 
<span data-ttu-id="a02ba-419">El token de OAuth no tiene los ámbitos necesarios para realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="a02ba-419">The OAuth token doesn't have the required scopes to perform the requested action.</span></span> <span data-ttu-id="a02ba-420">Específicamente, el permiso de edición.</span><span class="sxs-lookup"><span data-stu-id="a02ba-420">Specifically the edit permission.</span></span> <span data-ttu-id="a02ba-421">Vea [Permisos de notas](permissions-reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="a02ba-421">See [Notes permissions](permissions-reference.md#notes-permissions).</span></span>

### <a name="40007"></a><span data-ttu-id="a02ba-422">40007</span><span class="sxs-lookup"><span data-stu-id="a02ba-422">40007</span></span>
<span data-ttu-id="a02ba-423">El usuario no tiene permisos para acceder a este recurso.</span><span class="sxs-lookup"><span data-stu-id="a02ba-423">The user does not have permissions to access this resource.</span></span>

### <a name="40008"></a><span data-ttu-id="a02ba-424">40008</span><span class="sxs-lookup"><span data-stu-id="a02ba-424">40008</span></span>
<span data-ttu-id="a02ba-425">El acceso está prohibido para este recurso.</span><span class="sxs-lookup"><span data-stu-id="a02ba-425">Access is Forbidden for this resource.</span></span>

### <a name="40009"></a><span data-ttu-id="a02ba-426">40009</span><span class="sxs-lookup"><span data-stu-id="a02ba-426">40009</span></span>
<span data-ttu-id="a02ba-427">El contenedor ya está en uso por otro recurso.</span><span class="sxs-lookup"><span data-stu-id="a02ba-427">The container is already in use by another resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="a02ba-428">Ver también</span><span class="sxs-lookup"><span data-stu-id="a02ba-428">See also</span></span>

- [<span data-ttu-id="a02ba-429">Respuestas de error de Microsoft Graph y tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="a02ba-429">Microsoft Graph error responses and resource types</span></span>](errors.md)
- [<span data-ttu-id="a02ba-430">Referencia de OneNote</span><span class="sxs-lookup"><span data-stu-id="a02ba-430">OneNote reference</span></span>](/graph/api/resources/onenote?view=graph-rest-1.0)

