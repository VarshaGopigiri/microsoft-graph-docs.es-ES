# <a name="error-codes-for-onenote-apis-in-microsoft-graph"></a><span data-ttu-id="64068-101">Códigos de error de las API de OneNote en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="64068-101">Error codes for OneNote APIs in Microsoft Graph</span></span>

<span data-ttu-id="64068-102">Este artículo describe los códigos de error que devuelven las API de OneNote en Microsoft Graph cuando se produce un error en una solicitud enviada a través de la API.</span><span class="sxs-lookup"><span data-stu-id="64068-102">This article describes error codes that are returned by the OneNote APIs in Microsoft Graph whenever a request sent through the API fails.</span></span>

## <a name="error-response-example"></a><span data-ttu-id="64068-103">Ejemplo de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="64068-103">Error response example</span></span>
<span data-ttu-id="64068-104">Cuando la solicitud genera un error, la API de OneNote deja de realizar la solicitud y devuelve una respuesta de error como un objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="64068-104">When your request generates an error, the OneNote API stops performing the request and returns an error response as a JSON object.</span></span> <span data-ttu-id="64068-105">Una respuesta de error contiene el código de error asociado, un mensaje y un vínculo a la sección correspondiente en este artículo.</span><span class="sxs-lookup"><span data-stu-id="64068-105">An error response contains the associated error code, a message, and a link to the appropriate section of this article.</span></span> <span data-ttu-id="64068-106">El ejemplo siguiente muestra el aspecto de una respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="64068-106">The following example shows how an error response looks.</span></span>

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

<span data-ttu-id="64068-107">Para obtener más información sobre los errores de Microsoft Graph, consulte [Respuestas de error de Microsoft Graph y tipos de recursos](errors.md).</span><span class="sxs-lookup"><span data-stu-id="64068-107">For more information about Microsoft Graph errors, see [Microsoft Graph error responses and resource types](errors.md).</span></span>

## <a name="codes-from-10001-to-19999"></a><span data-ttu-id="64068-108">Códigos de 10001 a 19999</span><span class="sxs-lookup"><span data-stu-id="64068-108">Codes from 10001 to 19999</span></span>
<span data-ttu-id="64068-109">El servicio tiene problemas o está enviando información a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="64068-109">The service is having problems or is sending information to the application.</span></span>

### <a name="10001"></a><span data-ttu-id="64068-110">10001</span><span class="sxs-lookup"><span data-stu-id="64068-110">10001</span></span>
<span data-ttu-id="64068-111">Se produjo un error inesperado y la solicitud ha fallado.</span><span class="sxs-lookup"><span data-stu-id="64068-111">An unexpected error occurred and the request failed.</span></span>

### <a name="10002"></a><span data-ttu-id="64068-112">10002</span><span class="sxs-lookup"><span data-stu-id="64068-112">10002</span></span>
<span data-ttu-id="64068-113">El servicio no está disponible en este momento.</span><span class="sxs-lookup"><span data-stu-id="64068-113">The service is not currently available.</span></span>

### <a name="10003"></a><span data-ttu-id="64068-114">10003</span><span class="sxs-lookup"><span data-stu-id="64068-114">10003</span></span>
<span data-ttu-id="64068-115">La cuenta de usuario actual ha superado el número máximo de solicitudes activas.</span><span class="sxs-lookup"><span data-stu-id="64068-115">The current user's account has exceeded the maximum number of active requests.</span></span> <span data-ttu-id="64068-116">La aplicación tendrá que repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-116">Your app will have to repeat the request.</span></span>

### <a name="10004"></a><span data-ttu-id="64068-117">10004</span><span class="sxs-lookup"><span data-stu-id="64068-117">10004</span></span>
<span data-ttu-id="64068-118">El servicio no puede crear una página en la sección solicitada porque la sección está protegida por contraseña.</span><span class="sxs-lookup"><span data-stu-id="64068-118">The service can't create a page in the requested section because that section is protected by a password.</span></span>

### <a name="10005"></a><span data-ttu-id="64068-119">10005</span><span class="sxs-lookup"><span data-stu-id="64068-119">10005</span></span>
<span data-ttu-id="64068-120">La solicitud contiene más del número máximo de etiquetas de imagen en las que el atributo **data-render-src** contiene un PDF.</span><span class="sxs-lookup"><span data-stu-id="64068-120">The request contains more than the maximum number of image tags in which the **data-render-src** attribute contains a PDF.</span></span> <span data-ttu-id="64068-121">Vea [Agregar imágenes y archivos](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-images-files).</span><span class="sxs-lookup"><span data-stu-id="64068-121">See [Add images and files](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-images-files).</span></span>

### <a name="10006"></a><span data-ttu-id="64068-122">10006</span><span class="sxs-lookup"><span data-stu-id="64068-122">10006</span></span>
<span data-ttu-id="64068-123">La API de OneNote no pudo crear una página en la sección especificada porque esta sección está dañada.</span><span class="sxs-lookup"><span data-stu-id="64068-123">The OneNote API was unable to create a page in the specified section because that section is corrupt.</span></span>

### <a name="10007"></a><span data-ttu-id="64068-124">10007</span><span class="sxs-lookup"><span data-stu-id="64068-124">10007</span></span>
<span data-ttu-id="64068-p104">El servidor está demasiado ocupado para atender la solicitud entrante en este momento. Inténtelo de nuevo más tarde.</span><span class="sxs-lookup"><span data-stu-id="64068-p104">The server is too busy to handle the incoming request at this moment. Please try again later.</span></span>

### <a name="10008"></a><span data-ttu-id="64068-127">10008</span><span class="sxs-lookup"><span data-stu-id="64068-127">10008</span></span>
<span data-ttu-id="64068-128">Uno o más de las bibliotecas de documentos en OneDrive del usuario o del grupo contiene más de 5000 elementos de OneNote (blocs de notas, secciones, grupos de secciones) y no se puede consultar mediante la API.</span><span class="sxs-lookup"><span data-stu-id="64068-128">One or more of the document libraries on the user or group's OneDrive contains more than 5000 OneNote items (notebooks, sections, section groups), and cannot be queried using the API.</span></span> <span data-ttu-id="64068-129">Asegúrese de que ninguna de las bibliotecas de documentos del grupo o del usuario contiene más de 5000 elementos de OneNote.</span><span class="sxs-lookup"><span data-stu-id="64068-129">Please make sure that none of the user or group's document libraries contains more than 5000 OneNote items.</span></span> <span data-ttu-id="64068-130">Consulte el [blog de desarrollo de OneNote](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) para conocer los pasos de mitigación.</span><span class="sxs-lookup"><span data-stu-id="64068-130">See the [OneNote Dev blog](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) for mitigation steps.</span></span>

### <a name="10012"></a><span data-ttu-id="64068-131">10012</span><span class="sxs-lookup"><span data-stu-id="64068-131">10012</span></span>
<span data-ttu-id="64068-p106">No se puede crear ni actualizar la entidad porque la biblioteca que contiene el bloc de notas necesita extraer del repositorio los elementos antes de editarlos. Para obtener más información, vea https://support.office.com/en-us/article/Configure-a-site-library-to-require-check-out-of-files-f63fcbdc-1db6-4eb7-a3eb-dd815500c9e7.</span><span class="sxs-lookup"><span data-stu-id="64068-p106">Unable to create or update the entity because the library that contains the notebook requires items to be checked out before they can be edited.</span></span>

<span data-ttu-id="64068-134">Quite el requisito de desprotección de la biblioteca o mueva el bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="64068-134">Either remove the check-out requirement from the library, or move the notebook.</span></span>

### <a name="10013"></a><span data-ttu-id="64068-135">10013</span><span class="sxs-lookup"><span data-stu-id="64068-135">10013</span></span>
<span data-ttu-id="64068-136">Uno o más de las bibliotecas de documentos en OneDrive del usuario o del grupo contiene más de 20 000 elementos y no se puede indexar para realizar consultas mediante la API.</span><span class="sxs-lookup"><span data-stu-id="64068-136">One or more of the document libraries on the user or group's OneDrive contains more than 20,000 items and cannot be indexed for querying using the API.</span></span> <span data-ttu-id="64068-137">Asegúrese de que ninguna de las bibliotecas de documentos del grupo o del usuario contiene más de 20 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="64068-137">Please make sure that none of the user or group's document libraries contains more than 20,000 items.</span></span> <span data-ttu-id="64068-138">Consulte el [blog de desarrollo de OneNote](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) para conocer los pasos de mitigación.</span><span class="sxs-lookup"><span data-stu-id="64068-138">See the [OneNote Dev blog](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) for mitigation steps.</span></span>

### <a name="10014"></a><span data-ttu-id="64068-139">10014</span><span class="sxs-lookup"><span data-stu-id="64068-139">10014</span></span>
<span data-ttu-id="64068-140">Azure Key Vault está demasiado ocupado para atender la solicitud entrante en este momento.</span><span class="sxs-lookup"><span data-stu-id="64068-140">Azure Key Vault is too busy to handle the incoming request at this moment.</span></span> <span data-ttu-id="64068-141">Inténtelo de nuevo más tarde.</span><span class="sxs-lookup"><span data-stu-id="64068-141">Please try again later.</span></span>

### <a name="10015"></a><span data-ttu-id="64068-142">10015</span><span class="sxs-lookup"><span data-stu-id="64068-142">10015</span></span>
<span data-ttu-id="64068-143">SharePoint no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="64068-143">SharePoint is currently unavailable.</span></span> <span data-ttu-id="64068-144">Inténtelo de nuevo más tarde.</span><span class="sxs-lookup"><span data-stu-id="64068-144">Please try again later.</span></span>

### <a name="10016"></a><span data-ttu-id="64068-145">10016</span><span class="sxs-lookup"><span data-stu-id="64068-145">10016</span></span>
<span data-ttu-id="64068-146">La biblioteca de documentos en OneDrive del usuario o del grupo superó el límite de umbral de ámbitos de seguridad único.</span><span class="sxs-lookup"><span data-stu-id="64068-146">Document library on the user or group’s OneDrive exceeded unique security scopes threshold limit.</span></span> <span data-ttu-id="64068-147">El número máximo de ámbitos de seguridad únicos establecidos para una biblioteca no debe exceder de 50 000.</span><span class="sxs-lookup"><span data-stu-id="64068-147">The maximum number of unique security scopes set for a library cannot exceed 50,000.</span></span>

### <a name="10017"></a><span data-ttu-id="64068-148">10017</span><span class="sxs-lookup"><span data-stu-id="64068-148">10017</span></span>
<span data-ttu-id="64068-149">Solicitud incorrecta (Bad Request)</span><span class="sxs-lookup"><span data-stu-id="64068-149">Bad Request.</span></span>

### <a name="19999"></a><span data-ttu-id="64068-150">19999</span><span class="sxs-lookup"><span data-stu-id="64068-150">19999</span></span>
<span data-ttu-id="64068-151">Ha habido un error en la solicitud porque se produjo un error sin determinar.</span><span class="sxs-lookup"><span data-stu-id="64068-151">The request failed because an undetermined error occurred.</span></span>

## <a name="codes-from-20001-to-29999"></a><span data-ttu-id="64068-152">Códigos de 20001 a 29999</span><span class="sxs-lookup"><span data-stu-id="64068-152">Codes from 20001 to 29999</span></span>
<span data-ttu-id="64068-153">El código de la aplicación ha hecho algo mal.</span><span class="sxs-lookup"><span data-stu-id="64068-153">The application code has done something wrong.</span></span>

### <a name="20001"></a><span data-ttu-id="64068-154">20001</span><span class="sxs-lookup"><span data-stu-id="64068-154">20001</span></span>

<span data-ttu-id="64068-155">Falta la parte "Presentación", necesaria en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-155">The request is missing the required "Presentation" part.</span></span> <span data-ttu-id="64068-156">Se necesita exactamente una.</span><span class="sxs-lookup"><span data-stu-id="64068-156">Exactly one is required.</span></span> 

### <a name="20002"></a><span data-ttu-id="64068-157">20002</span><span class="sxs-lookup"><span data-stu-id="64068-157">20002</span></span>
<span data-ttu-id="64068-158">La solicitud contiene dos o más partes "Presentación".</span><span class="sxs-lookup"><span data-stu-id="64068-158">The request contains two or more "Presentation" parts.</span></span> <span data-ttu-id="64068-159">Se necesita exactamente una.</span><span class="sxs-lookup"><span data-stu-id="64068-159">Exactly one is required.</span></span>

### <a name="20003"></a><span data-ttu-id="64068-160">20003</span><span class="sxs-lookup"><span data-stu-id="64068-160">20003</span></span>
<span data-ttu-id="64068-161">El tipo de contenido de la parte "Presentación" puede ser solo texto/HTML o aplicación/XHTML+XML.</span><span class="sxs-lookup"><span data-stu-id="64068-161">The content type of the "Presentation" part can be only text/HTML or application/XHTML+XML.</span></span> 

### <a name="20004"></a><span data-ttu-id="64068-162">20004</span><span class="sxs-lookup"><span data-stu-id="64068-162">20004</span></span>
<span data-ttu-id="64068-163">El HTML de la parte "Presentación" contiene una etiqueta de imagen con ambos conjuntos de propiedades: **src** y **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="64068-163">The "Presentation" part HTML contains an image tag with both the **src** and the **data-render-src** properties set.</span></span> <span data-ttu-id="64068-164">La API omitirá la propiedad **src** y usará la propiedad **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="64068-164">The API will ignore the **src** property and use the **data-render-src** property.</span></span> 

### <a name="20005"></a><span data-ttu-id="64068-165">20005</span><span class="sxs-lookup"><span data-stu-id="64068-165">20005</span></span>
<span data-ttu-id="64068-166">El URI de la solicitud es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="64068-166">The request URI is too long.</span></span> <span data-ttu-id="64068-167">El tamaño máximo del URI (incluyendo todos los parámetros y datos) es de 16 KB o 16 384 caracteres.</span><span class="sxs-lookup"><span data-stu-id="64068-167">The maximum size of the URI (including all parameters and data) is 16 KB or 16,384 characters.</span></span>

### <a name="20006"></a><span data-ttu-id="64068-168">20006</span><span class="sxs-lookup"><span data-stu-id="64068-168">20006</span></span>
<span data-ttu-id="64068-169">El HTML de la parte "Presentación" contiene una etiqueta de imagen sin los conjuntos de propiedades src o **data-render-src**.</span><span class="sxs-lookup"><span data-stu-id="64068-169">The "Presentation" part HTML contains an image tag with neither the src nor the **data-render-src** properties set.</span></span> <span data-ttu-id="64068-170">La API omitirá la etiqueta **imagen**.</span><span class="sxs-lookup"><span data-stu-id="64068-170">The API will ignore the **image** tag.</span></span> 

### <a name="20007"></a><span data-ttu-id="64068-171">20007</span><span class="sxs-lookup"><span data-stu-id="64068-171">20007</span></span>
<span data-ttu-id="64068-172">El código HTML de la parte "Presentation" contiene una cadena de fecha y hora de creación que no coincide con ninguno de los formatos permitidos.</span><span class="sxs-lookup"><span data-stu-id="64068-172">The "Presentation" part HTML contains a created date/time string that does not match any of the allowed formats.</span></span> 

### <a name="20008"></a><span data-ttu-id="64068-173">20008</span><span class="sxs-lookup"><span data-stu-id="64068-173">20008</span></span>
<span data-ttu-id="64068-174">El tamaño de la solicitud es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="64068-174">The size of the request is too large.</span></span> 

### <a name="20009"></a><span data-ttu-id="64068-175">20009</span><span class="sxs-lookup"><span data-stu-id="64068-175">20009</span></span>
<span data-ttu-id="64068-176">La solicitud contiene partes con nombres duplicados.</span><span class="sxs-lookup"><span data-stu-id="64068-176">The request contains parts with duplicate names.</span></span> <span data-ttu-id="64068-177">Los nombres de las partes deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="64068-177">Part names must be unique.</span></span> 

### <a name="20010"></a><span data-ttu-id="64068-178">20010</span><span class="sxs-lookup"><span data-stu-id="64068-178">20010</span></span>
<span data-ttu-id="64068-179">No se proporcionó el encabezado Content-Disposition para el tipo de contenido especificado.</span><span class="sxs-lookup"><span data-stu-id="64068-179">The Content-Disposition header was not supplied for the specified content type.</span></span> 

### <a name="20011"></a><span data-ttu-id="64068-180">20011</span><span class="sxs-lookup"><span data-stu-id="64068-180">20011</span></span>
<span data-ttu-id="64068-181">La solicitud contiene una carga de varias partes con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="64068-181">The request contains a malformed multipart payload.</span></span> <span data-ttu-id="64068-182">Entre los problemas se incluyen la falta de líneas en blanco, falta de la última línea, separadores de partes con formato incorrecto, etc.</span><span class="sxs-lookup"><span data-stu-id="64068-182">Problems could include missing blank lines, a missing last line, incorrectly formatted part separators, and so on.</span></span> <span data-ttu-id="64068-183">Si va a crear el mensaje de varias partes a mano, revise cuidadosamente la lógica o considere el uso de una biblioteca de terceros.</span><span class="sxs-lookup"><span data-stu-id="64068-183">If you're building the multipart message by hand, carefully check the logic, or consider using a third-party library.</span></span> 

### <a name="20012"></a><span data-ttu-id="64068-184">20012</span><span class="sxs-lookup"><span data-stu-id="64068-184">20012</span></span>
<span data-ttu-id="64068-185">La solicitud no proporciona un tipo de contenido para la parte especificada.</span><span class="sxs-lookup"><span data-stu-id="64068-185">The request doesn't supply a content type for the specified part.</span></span> 
### <a name="20013"></a><span data-ttu-id="64068-186">20013</span><span class="sxs-lookup"><span data-stu-id="64068-186">20013</span></span>
<span data-ttu-id="64068-187">La solicitud no proporciona los encabezados Content-Type y Content-Disposition para la parte especificada.</span><span class="sxs-lookup"><span data-stu-id="64068-187">The request doesn't supply Content-Type and Content-Disposition headers for the specified part.</span></span> 

### <a name="20014"></a><span data-ttu-id="64068-188">20014</span><span class="sxs-lookup"><span data-stu-id="64068-188">20014</span></span>
<span data-ttu-id="64068-189">La longitud de una parte en el mensaje de varias partes supera el tamaño máximo de 25 MB.</span><span class="sxs-lookup"><span data-stu-id="64068-189">The length of a part in the multipart message exceeds the maximum size of 25 MB.</span></span> 

### <a name="20015"></a><span data-ttu-id="64068-190">20015</span><span class="sxs-lookup"><span data-stu-id="64068-190">20015</span></span>
<span data-ttu-id="64068-191">El recuento de partes en el mensaje de varias partes supera el límite de 500.</span><span class="sxs-lookup"><span data-stu-id="64068-191">The count of parts in the multipart message exceeds the limit of 500.</span></span> 

### <a name="20016"></a><span data-ttu-id="64068-192">20016</span><span class="sxs-lookup"><span data-stu-id="64068-192">20016</span></span>
<span data-ttu-id="64068-193">La longitud del mensaje de varias partes supera el límite de 75 MB.</span><span class="sxs-lookup"><span data-stu-id="64068-193">The length of the multipart message exceeds the limit of 75 MB.</span></span> 

### <a name="20017"></a><span data-ttu-id="64068-194">20017</span><span class="sxs-lookup"><span data-stu-id="64068-194">20017</span></span>
<span data-ttu-id="64068-195">El correo electrónico MIME está mal formado.</span><span class="sxs-lookup"><span data-stu-id="64068-195">The email MIME was malformed.</span></span> 

### <a name="20018"></a><span data-ttu-id="64068-196">20018</span><span class="sxs-lookup"><span data-stu-id="64068-196">20018</span></span>
<span data-ttu-id="64068-197">La reunión MIME o ICal está mal formada.</span><span class="sxs-lookup"><span data-stu-id="64068-197">The meeting MIME or ICal was malformed.</span></span> 

### <a name="20019"></a><span data-ttu-id="64068-198">20019</span><span class="sxs-lookup"><span data-stu-id="64068-198">20019</span></span>
<span data-ttu-id="64068-199">No se ha encontrado ningún ICal.</span><span class="sxs-lookup"><span data-stu-id="64068-199">No ICal was found.</span></span> 

### <a name="20020"></a><span data-ttu-id="64068-200">20020</span><span class="sxs-lookup"><span data-stu-id="64068-200">20020</span></span>
<span data-ttu-id="64068-201">Se encontró JSON con formato incorrecto en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-201">Encountered malformed Json in request body.</span></span> 

### <a name="20100"></a><span data-ttu-id="64068-202">20100</span><span class="sxs-lookup"><span data-stu-id="64068-202">20100</span></span>
<span data-ttu-id="64068-203">Hay algún fallo en la sintaxis de su solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-203">Something is wrong with the syntax of your request.</span></span> 
### <a name="20101"></a><span data-ttu-id="64068-204">20101</span><span class="sxs-lookup"><span data-stu-id="64068-204">20101</span></span>
<span data-ttu-id="64068-205">La propiedad que ha solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="64068-205">The property that you requested doesn't exist.</span></span>

### <a name="20102"></a><span data-ttu-id="64068-206">20102</span><span class="sxs-lookup"><span data-stu-id="64068-206">20102</span></span>
<span data-ttu-id="64068-207">Ha solicitado un recurso que no existe.</span><span class="sxs-lookup"><span data-stu-id="64068-207">You requested a resource that doesn't exist.</span></span>

### <a name="20103"></a><span data-ttu-id="64068-208">20103</span><span class="sxs-lookup"><span data-stu-id="64068-208">20103</span></span>
<span data-ttu-id="64068-209">La consulta **expand** no se admite para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-209">The **expand** query is not supported for this request.</span></span> <span data-ttu-id="64068-210">Vea [Opciones de cadena de consultas OData admitidas](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-get-content#query-options).</span><span class="sxs-lookup"><span data-stu-id="64068-210">See [Supported OData query string options](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-get-content#query-options).</span></span>

### <a name="20104"></a><span data-ttu-id="64068-211">20104</span><span class="sxs-lookup"><span data-stu-id="64068-211">20104</span></span>
<span data-ttu-id="64068-212">La opción de consulta **pagelevel** solo se admite al realizar consultas para la colección de páginas de una sección o de una página específica.</span><span class="sxs-lookup"><span data-stu-id="64068-212">The **pagelevel** query option is supported only when querying for the pages collection in a section or for a specific page.</span></span> <span data-ttu-id="64068-213">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="64068-213">For example:</span></span>  

```http
GET ../sections/{id}/pages?pagelevel=true
GET ../pages/{id}?pagelevel=true
```

### <a name="20106"></a><span data-ttu-id="64068-214">20106</span><span class="sxs-lookup"><span data-stu-id="64068-214">20106</span></span>
<span data-ttu-id="64068-215">La solicitud contiene un operador de consulta que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="64068-215">Your request contains a query operator that is not supported.</span></span> 

### <a name="20108"></a><span data-ttu-id="64068-216">20108</span><span class="sxs-lookup"><span data-stu-id="64068-216">20108</span></span>
<span data-ttu-id="64068-217">La solicitud contiene parámetros de consulta de OData no compatibles.</span><span class="sxs-lookup"><span data-stu-id="64068-217">Your request contains unsupported OData query parameters.</span></span>

### <a name="20109"></a><span data-ttu-id="64068-218">20109</span><span class="sxs-lookup"><span data-stu-id="64068-218">20109</span></span>
<span data-ttu-id="64068-219">La carga útil de la solicitud PATCH no se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="64068-219">The payload in the PATCH request is not constructed correctly.</span></span>

### <a name="20110"></a><span data-ttu-id="64068-220">20110</span><span class="sxs-lookup"><span data-stu-id="64068-220">20110</span></span>
<span data-ttu-id="64068-221">Las solicitudes de creación de la página con partes de datos requieren que el contenido tenga varias partes, con una parte "Presentación".</span><span class="sxs-lookup"><span data-stu-id="64068-221">Page create requests with data parts require the content to be multipart, with a "Presentation" part.</span></span> 

### <a name="20111"></a><span data-ttu-id="64068-222">20111</span><span class="sxs-lookup"><span data-stu-id="64068-222">20111</span></span>
<span data-ttu-id="64068-223">La solicitud usa una característica de OData que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="64068-223">Your request uses an OData feature that isn't supported.</span></span>

### <a name="20112"></a><span data-ttu-id="64068-224">20112</span><span class="sxs-lookup"><span data-stu-id="64068-224">20112</span></span>
<span data-ttu-id="64068-225">Su solicitud contiene un identificador no válido para el bloc de notas de destino, el grupo de sección, la sección o la entidad de la página.</span><span class="sxs-lookup"><span data-stu-id="64068-225">Your request contains an invalid ID for the target notebook, section group, section, or page entity.</span></span>

### <a name="20113"></a><span data-ttu-id="64068-226">20113</span><span class="sxs-lookup"><span data-stu-id="64068-226">20113</span></span>
<span data-ttu-id="64068-227">Se ha eliminado el recurso especificado en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-227">The resource specified in the request has been deleted.</span></span>

### <a name="20115"></a><span data-ttu-id="64068-228">20115</span><span class="sxs-lookup"><span data-stu-id="64068-228">20115</span></span>
<span data-ttu-id="64068-229">El nombre contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="64068-229">The name contains invalid characters.</span></span> <span data-ttu-id="64068-230">El nombre de un bloc de notas no puede contener ninguno de los siguientes caracteres: `? * \ / : < > | ' "`</span><span class="sxs-lookup"><span data-stu-id="64068-230">A notebook name cannot contain any of the following characters: `? * \ / : < > | ' "`</span></span>

### <a name="20117"></a><span data-ttu-id="64068-231">20117</span><span class="sxs-lookup"><span data-stu-id="64068-231">20117</span></span>
<span data-ttu-id="64068-232">Ya existe un elemento con el nombre especificado en la ubicación indicada.</span><span class="sxs-lookup"><span data-stu-id="64068-232">An item with the name you specified already exists in the location that you specified.</span></span>

### <a name="20119"></a><span data-ttu-id="64068-233">20119</span><span class="sxs-lookup"><span data-stu-id="64068-233">20119</span></span>
<span data-ttu-id="64068-234">El código HTML de la parte "Presentation" contiene un atributo **data-attachment** que no tiene un formato válido o que incluye uno o varios de estos caracteres no válidos para un nombre de archivo: `\ / : * ? < > | "`.</span><span class="sxs-lookup"><span data-stu-id="64068-234">The HTML in the "Presentation" part contains a **data-attachment** attribute that either doesn't have a valid format or includes one or more of these invalid characters for a file name: `\ / : * ? < > | "`.</span></span> <span data-ttu-id="64068-235">La solicitud sustituye el valor indicado en el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="64068-235">The request substituted the value indicated in the error message.</span></span>

### <a name="20120"></a><span data-ttu-id="64068-236">20120</span><span class="sxs-lookup"><span data-stu-id="64068-236">20120</span></span>
<span data-ttu-id="64068-237">Su solicitud especifica un destino PATCH que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="64068-237">Your request specifies a PATCH target that can't be located.</span></span>

### <a name="20121"></a><span data-ttu-id="64068-238">20121</span><span class="sxs-lookup"><span data-stu-id="64068-238">20121</span></span>
<span data-ttu-id="64068-239">La solicitud contiene un argumento PATCH no válido.</span><span class="sxs-lookup"><span data-stu-id="64068-239">Your request contains an invalid PATCH argument.</span></span> <span data-ttu-id="64068-240">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-240">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20122"></a><span data-ttu-id="64068-241">20122</span><span class="sxs-lookup"><span data-stu-id="64068-241">20122</span></span>
<span data-ttu-id="64068-242">La solicitud especifica una acción PATCH no compatible.</span><span class="sxs-lookup"><span data-stu-id="64068-242">Your request specifies an unsupported PATCH action.</span></span> <span data-ttu-id="64068-243">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-243">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20123"></a><span data-ttu-id="64068-244">20123</span><span class="sxs-lookup"><span data-stu-id="64068-244">20123</span></span>
<span data-ttu-id="64068-245">La solicitud PATCH no puede modificar la página especificada.</span><span class="sxs-lookup"><span data-stu-id="64068-245">The PATCH request is unable to alter the specified page.</span></span>

### <a name="20124"></a><span data-ttu-id="64068-246">20124</span><span class="sxs-lookup"><span data-stu-id="64068-246">20124</span></span>
<span data-ttu-id="64068-247">La solicitud PATCH de varias partes no incluye una parte "commands" con la estructura JSON de la acción PATCH.</span><span class="sxs-lookup"><span data-stu-id="64068-247">Your multipart PATCH request doesn't include a "commands" part with the PATCH action JSON structure.</span></span> <span data-ttu-id="64068-248">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-248">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20125"></a><span data-ttu-id="64068-249">20125</span><span class="sxs-lookup"><span data-stu-id="64068-249">20125</span></span>
<span data-ttu-id="64068-250">La solicitud PATCH no contiene acciones.</span><span class="sxs-lookup"><span data-stu-id="64068-250">Your PATCH request contains no actions.</span></span> <span data-ttu-id="64068-251">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-251">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20126"></a><span data-ttu-id="64068-252">20126</span><span class="sxs-lookup"><span data-stu-id="64068-252">20126</span></span>
<span data-ttu-id="64068-253">El cuerpo del mensaje contiene JSON con un formato incorrecto o campos que no son compatibles con esta operación.</span><span class="sxs-lookup"><span data-stu-id="64068-253">The message body contains either incorrectly formatted JSON or fields that are not supported for this operation.</span></span>

### <a name="20127"></a><span data-ttu-id="64068-254">20127</span><span class="sxs-lookup"><span data-stu-id="64068-254">20127</span></span>
<span data-ttu-id="64068-255">La solicitud especifica el nombre de una propiedad desconocida.</span><span class="sxs-lookup"><span data-stu-id="64068-255">Your request specifies the name of an unknown property.</span></span>

### <a name="20128"></a><span data-ttu-id="64068-256">20128</span><span class="sxs-lookup"><span data-stu-id="64068-256">20128</span></span>
<span data-ttu-id="64068-257">La solicitud contiene un error de sintaxis de OData en la posición indicada en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64068-257">Your request contains an OData syntax error at the position indicated in the message.</span></span>

### <a name="20129"></a><span data-ttu-id="64068-258">20129</span><span class="sxs-lookup"><span data-stu-id="64068-258">20129</span></span>
<span data-ttu-id="64068-259">La solicitud contiene una opción de la cadena de consulta **top** cuyo valor es demasiado alto.</span><span class="sxs-lookup"><span data-stu-id="64068-259">Your request contains a **top** query string option whose value is too high.</span></span> <span data-ttu-id="64068-260">Para las consultas de páginas, el valor máximo es 100 y el valor predeterminado es 20.</span><span class="sxs-lookup"><span data-stu-id="64068-260">For page queries, the maximum value is 100, and the default value is 20.</span></span>

### <a name="20130"></a><span data-ttu-id="64068-261">20130</span><span class="sxs-lookup"><span data-stu-id="64068-261">20130</span></span>
<span data-ttu-id="64068-262">La solicitud contiene un URI que apunta a un recurso de HTTP que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="64068-262">Your request contains a URI that points to an HTTP resource that can't be found.</span></span>

### <a name="20131"></a><span data-ttu-id="64068-263">20131</span><span class="sxs-lookup"><span data-stu-id="64068-263">20131</span></span>
<span data-ttu-id="64068-264">La solicitud contiene un valor no válido para Content-Type.</span><span class="sxs-lookup"><span data-stu-id="64068-264">Your request contains an invalid value for Content-Type.</span></span> <span data-ttu-id="64068-265">Use el valor indicado en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64068-265">Use the value indicated in the message.</span></span> 

### <a name="20132"></a><span data-ttu-id="64068-266">20132</span><span class="sxs-lookup"><span data-stu-id="64068-266">20132</span></span>
<span data-ttu-id="64068-267">Su solicitud incluye contenido no válido.</span><span class="sxs-lookup"><span data-stu-id="64068-267">Your request contains invalid content.</span></span> <span data-ttu-id="64068-268">Las causas comunes son la falta de un encabezado Content-Type o un cuerpo de la solicitud sin contenido.</span><span class="sxs-lookup"><span data-stu-id="64068-268">Common causes for this are a missing Content-Type request header and/or no content in the body of the request.</span></span> 

### <a name="20133"></a><span data-ttu-id="64068-269">20133</span><span class="sxs-lookup"><span data-stu-id="64068-269">20133</span></span>
<span data-ttu-id="64068-270">Su solicitud especifica un destino PATCH que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="64068-270">Your request specifies a PATCH target that is not supported.</span></span> <span data-ttu-id="64068-271">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-271">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20134"></a><span data-ttu-id="64068-272">20134</span><span class="sxs-lookup"><span data-stu-id="64068-272">20134</span></span>
<span data-ttu-id="64068-273">La solicitud especifica un elemento no válido como destino de la acción PATCH.</span><span class="sxs-lookup"><span data-stu-id="64068-273">Your request specifies an invalid element as the target of the PATCH action.</span></span> <span data-ttu-id="64068-274">Si el destino usa el identificador **data-id**, asegúrese de que tiene el prefijo con el símbolo #.</span><span class="sxs-lookup"><span data-stu-id="64068-274">If the target uses the **data-id** identifier, make sure it's prefixed with a # symbol.</span></span> <span data-ttu-id="64068-275">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-275">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20135"></a><span data-ttu-id="64068-276">20135</span><span class="sxs-lookup"><span data-stu-id="64068-276">20135</span></span>
<span data-ttu-id="64068-277">Su solicitud especifica un tipo de entidad que no es compatible con la operación PATCH.</span><span class="sxs-lookup"><span data-stu-id="64068-277">Your request specifies an entity type that is not supported for the PATCH operation.</span></span> <span data-ttu-id="64068-278">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-278">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20136"></a><span data-ttu-id="64068-279">20136</span><span class="sxs-lookup"><span data-stu-id="64068-279">20136</span></span>
<span data-ttu-id="64068-280">La solicitud contiene un atributo **data-render-src** o **data-render-method** no válido o que falta.</span><span class="sxs-lookup"><span data-stu-id="64068-280">Your request contains an invalid or missing **data-render-src** or **data-render-method** attribute.</span></span> <span data-ttu-id="64068-281">Vea [Extraer los datos de las capturas](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-extract-data).</span><span class="sxs-lookup"><span data-stu-id="64068-281">See [Extract data from captures](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-extract-data).</span></span>

### <a name="20137"></a><span data-ttu-id="64068-282">20137</span><span class="sxs-lookup"><span data-stu-id="64068-282">20137</span></span>
<span data-ttu-id="64068-283">La página de destino no admite solicitudes PATCH.</span><span class="sxs-lookup"><span data-stu-id="64068-283">The target page does not support PATCH requests.</span></span>

### <a name="20138"></a><span data-ttu-id="64068-284">20138</span><span class="sxs-lookup"><span data-stu-id="64068-284">20138</span></span>
<span data-ttu-id="64068-285">El tipo de elemento de destino de la solicitud PATCH no admite la acción **append** especificada.</span><span class="sxs-lookup"><span data-stu-id="64068-285">The target element type in your PATCH request doesn't support the **append** action.</span></span> <span data-ttu-id="64068-286">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-286">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20139"></a><span data-ttu-id="64068-287">20139</span><span class="sxs-lookup"><span data-stu-id="64068-287">20139</span></span>
<span data-ttu-id="64068-288">La solicitud contiene un valor de atributo **data-tag** no válido.</span><span class="sxs-lookup"><span data-stu-id="64068-288">Your request contains an invalid **data-tag** attribute value.</span></span> <span data-ttu-id="64068-289">Vea [Uso de etiquetas de nota](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-note-tags).</span><span class="sxs-lookup"><span data-stu-id="64068-289">See [Use note tags](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-note-tags).</span></span>

### <a name="20140"></a><span data-ttu-id="64068-290">20140</span><span class="sxs-lookup"><span data-stu-id="64068-290">20140</span></span>
<span data-ttu-id="64068-291">La solicitud contiene un valor de estado **data-tag** no válido.</span><span class="sxs-lookup"><span data-stu-id="64068-291">Your request contains an invalid **data-tag** status value.</span></span> <span data-ttu-id="64068-292">Las etiquetas de nota de casillas pueden tener un estado **completed**.</span><span class="sxs-lookup"><span data-stu-id="64068-292">Check box note tags can have a **completed** status.</span></span> <span data-ttu-id="64068-293">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="64068-293">Example:</span></span>
```html
    <p data-tag="to-do:completed">To-do note tag in completed state (checked box in the UI)</p>
```
<span data-ttu-id="64068-294">Vea [Uso de etiquetas de nota](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-note-tags).</span><span class="sxs-lookup"><span data-stu-id="64068-294">See [Use note tags](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-note-tags).</span></span>

### <a name="20141"></a><span data-ttu-id="64068-295">20141</span><span class="sxs-lookup"><span data-stu-id="64068-295">20141</span></span>
<span data-ttu-id="64068-296">El destino de la solicitud PATCH no admite la acción especificada.</span><span class="sxs-lookup"><span data-stu-id="64068-296">The target in your PATCH request doesn't support the specified action.</span></span> <span data-ttu-id="64068-297">Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="64068-297">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20142"></a><span data-ttu-id="64068-298">20142</span><span class="sxs-lookup"><span data-stu-id="64068-298">20142</span></span>
<span data-ttu-id="64068-299">La solicitud contiene una expresión **expand** para un elemento primario de entidades secundarias o un elemento secundario de entidades primarias, lo cual no es compatible.</span><span class="sxs-lookup"><span data-stu-id="64068-299">Your request contains an **expand** expression for a parent of child entities or a child of parent entities, which is not supported.</span></span> <span data-ttu-id="64068-300">Vea [Opciones de cadena de consultas OData admitidas](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-get-content#query-options).</span><span class="sxs-lookup"><span data-stu-id="64068-300">See [Supported OData query string options](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-get-content#query-options).</span></span>

### <a name="20143"></a><span data-ttu-id="64068-301">20143</span><span class="sxs-lookup"><span data-stu-id="64068-301">20143</span></span>
<span data-ttu-id="64068-302">La consulta OData no es válida.</span><span class="sxs-lookup"><span data-stu-id="64068-302">The OData query is invalid.</span></span>

### <a name="20144"></a><span data-ttu-id="64068-303">20144</span><span class="sxs-lookup"><span data-stu-id="64068-303">20144</span></span>
<span data-ttu-id="64068-304">La solicitud contiene una expresión **expand** para una propiedad de no navegación.</span><span class="sxs-lookup"><span data-stu-id="64068-304">Your request contains an **expand** expression for a non-navigation property.</span></span> <span data-ttu-id="64068-305">Únicamente se pueden expandir las propiedades de navegación.</span><span class="sxs-lookup"><span data-stu-id="64068-305">Only navigation properties can be expanded.</span></span>

### <a name="20145"></a><span data-ttu-id="64068-306">20145</span><span class="sxs-lookup"><span data-stu-id="64068-306">20145</span></span>
<span data-ttu-id="64068-307">La expresión **select** o **expand** de la solicitud contiene un término no válido.</span><span class="sxs-lookup"><span data-stu-id="64068-307">The **select** or **expand** expression in your request contains an invalid term.</span></span>

### <a name="20146"></a><span data-ttu-id="64068-308">20146</span><span class="sxs-lookup"><span data-stu-id="64068-308">20146</span></span>
<span data-ttu-id="64068-309">El atributo `style="position:absolute"` se especifica en un elemento, pero el elemento **body** no especifica `data-absolute-enabled="true"`, que es necesario para admitir el posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="64068-309">The `style="position:absolute"` attribute is specified on an element, but the **body** element does not specify `data-absolute-enabled="true"`, which is required to support positioning.</span></span> <span data-ttu-id="64068-310">Se omitirán todas las configuraciones de posición.</span><span class="sxs-lookup"><span data-stu-id="64068-310">All position settings will be ignored.</span></span> <span data-ttu-id="64068-311">Vea [Crear elementos con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="64068-311">See [Create absolute positioned elements](onenote-abs-pos.md).</span></span>

### <a name="20147"></a><span data-ttu-id="64068-312">20147</span><span class="sxs-lookup"><span data-stu-id="64068-312">20147</span></span>
<span data-ttu-id="64068-313">El atributo `style="position:absolute"` se especifica en un elemento que no es un elemento secundario directo del elemento **body**, que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="64068-313">The `style="position:absolute"` attribute is specified on an element that is not a direct child of the **body** element, which is not supported.</span></span> <span data-ttu-id="64068-314">Si el elemento es un **div**, **img **u **object**, haga que sea un elemento secundario directo del cuerpo; en caso contrario, se pasarán por alto los valores de posición y representará su contenido dentro de un div de posición absoluta</span><span class="sxs-lookup"><span data-stu-id="64068-314">If the element is a **div**, **img**, or **object**, make it a direct child of the body; otherwise the position settings will be ignored and its content will render inside an absolute positioned div.</span></span> <span data-ttu-id="64068-315">Vea [Crear elementos con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="64068-315">See [Create absolute positioned elements](onenote-abs-pos.md).</span></span>

### <a name="20148"></a><span data-ttu-id="64068-316">20148</span><span class="sxs-lookup"><span data-stu-id="64068-316">20148</span></span>
<span data-ttu-id="64068-317">El atributo `style="position:absolute"` se especifica en un tipo de elemento que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="64068-317">The `style="position:absolute"` attribute is specified on an element type that does not support it.</span></span> <span data-ttu-id="64068-318">Solo **div**, **img** y **object** admiten la posición de los elementos que son elementos secundarios directos del cuerpo de la página.</span><span class="sxs-lookup"><span data-stu-id="64068-318">Only **div**, **img**, and **object** elements that are direct children of the page body support positioning.</span></span> <span data-ttu-id="64068-319">Vea [Crear elementos con posición absoluta](onenote-abs-pos.md).</span><span class="sxs-lookup"><span data-stu-id="64068-319">See [Create absolute positioned elements](onenote-abs-pos.md).</span></span>

### <a name="20149"></a><span data-ttu-id="64068-320">20149</span><span class="sxs-lookup"><span data-stu-id="64068-320">20149</span></span>
<span data-ttu-id="64068-321">Su solicitud especifica un elemento de destino que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="64068-321">Your request specifies a target element that cannot be found.</span></span>

### <a name="20150"></a><span data-ttu-id="64068-322">20150</span><span class="sxs-lookup"><span data-stu-id="64068-322">20150</span></span>
<span data-ttu-id="64068-323">La solicitud no es válida para este tipo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="64068-323">The request is not valid for this authentication type.</span></span> <span data-ttu-id="64068-324">Use la ruta de acceso `../me/onenote/` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="64068-324">Use the `../me/onenote/` path instead.</span></span>

### <a name="20151"></a><span data-ttu-id="64068-325">20151</span><span class="sxs-lookup"><span data-stu-id="64068-325">20151</span></span>
<span data-ttu-id="64068-326">La solicitud no es válida para este tipo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="64068-326">The request is not valid for this authentication type.</span></span> <span data-ttu-id="64068-327">Use el punto de conexión `../me/onenote/section/{id}/pages` para crear una página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="64068-327">Use the `../me/onenote/section/{id}/pages` endpoint to create a page in a specific section.</span></span>

### <a name="20152"></a><span data-ttu-id="64068-328">20152</span><span class="sxs-lookup"><span data-stu-id="64068-328">20152</span></span>
<span data-ttu-id="64068-329">No hay ningún valor name especificado para la entidad.</span><span class="sxs-lookup"><span data-stu-id="64068-329">There is no name value specified for the entity.</span></span> <span data-ttu-id="64068-330">Debe definirse el nombre y no puede contener únicamente espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="64068-330">The name must be defined, and it cannot contain whitespaces only.</span></span>

### <a name="20153"></a><span data-ttu-id="64068-331">20153</span><span class="sxs-lookup"><span data-stu-id="64068-331">20153</span></span>
<span data-ttu-id="64068-332">El nombre de la entidad contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="64068-332">The entity name contains invalid characters.</span></span> <span data-ttu-id="64068-333">El nombre de la organización no puede contener los siguientes caracteres: `? * \ / : < > | & # " % ~`</span><span class="sxs-lookup"><span data-stu-id="64068-333">The name cannot contain the following characters: `? * \ / : < > | & # " % ~`</span></span>

### <a name="20154"></a><span data-ttu-id="64068-334">20154</span><span class="sxs-lookup"><span data-stu-id="64068-334">20154</span></span>
<span data-ttu-id="64068-335">El nombre de la entidad no puede comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="64068-335">The entity name cannot start with a space.</span></span>

### <a name="20155"></a><span data-ttu-id="64068-336">20155</span><span class="sxs-lookup"><span data-stu-id="64068-336">20155</span></span>
<span data-ttu-id="64068-337">El nombre de entidad es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="64068-337">The entity name is too long.</span></span> <span data-ttu-id="64068-338">Los nombres de los blocs de notas tienen un límite de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="64068-338">Notebook names have a 128-character limit.</span></span> <span data-ttu-id="64068-339">Los nombres de otras entidades tienen un límite de 50 caracteres.</span><span class="sxs-lookup"><span data-stu-id="64068-339">Other entity names have a 50-character limit.</span></span>

### <a name="20156"></a><span data-ttu-id="64068-340">20156</span><span class="sxs-lookup"><span data-stu-id="64068-340">20156</span></span>
<span data-ttu-id="64068-341">El identificador especificado para el recurso de destino no existe.</span><span class="sxs-lookup"><span data-stu-id="64068-341">The specified ID for the destination resource does not exist.</span></span>

### <a name="20157"></a><span data-ttu-id="64068-342">20157</span><span class="sxs-lookup"><span data-stu-id="64068-342">20157</span></span>
<span data-ttu-id="64068-343">El identificador especificado para la entidad de destino no es válido.</span><span class="sxs-lookup"><span data-stu-id="64068-343">The specified ID for the destination entity is invalid.</span></span>

### <a name="20158"></a><span data-ttu-id="64068-344">20158</span><span class="sxs-lookup"><span data-stu-id="64068-344">20158</span></span>
<span data-ttu-id="64068-345">No se pueden obtener los metadatos de la dirección URL del sitio especificada en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-345">Unable to get metadata for the site URL specified in the request.</span></span> <span data-ttu-id="64068-346">Compruebe el formato de la dirección URL suministrada.</span><span class="sxs-lookup"><span data-stu-id="64068-346">Check the format of the supplied URL.</span></span> <span data-ttu-id="64068-347">Los formatos admitidos son `https://domain.sharepoint.com/site-a` y `https://domain.com/sites/site-a`.</span><span class="sxs-lookup"><span data-stu-id="64068-347">Supported formats include `https://domain.sharepoint.com/site-a` and `https://domain.com/sites/site-a`.</span></span>

### <a name="20160"></a><span data-ttu-id="64068-348">20160</span><span class="sxs-lookup"><span data-stu-id="64068-348">20160</span></span>
<span data-ttu-id="64068-349">No se puede encontrar un grupo unificado de Office 365 con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="64068-349">Unable to find an Office 365 unified group that has the specified ID.</span></span>

### <a name="20161"></a><span data-ttu-id="64068-350">20161</span><span class="sxs-lookup"><span data-stu-id="64068-350">20161</span></span>
<span data-ttu-id="64068-351">El contexto no especifica ningún Id. de usuario válido.</span><span class="sxs-lookup"><span data-stu-id="64068-351">The context does not specify a valid user ID.</span></span> <span data-ttu-id="64068-352">Un error frecuente es que PUID/CID se ha pasado como un long en lugar de un hex.</span><span class="sxs-lookup"><span data-stu-id="64068-352">One common error is that PUID/CID was passed in as a long instead of a hex.</span></span>

### <a name="20166"></a><span data-ttu-id="64068-353">20166</span><span class="sxs-lookup"><span data-stu-id="64068-353">20166</span></span>
<span data-ttu-id="64068-354">La aplicación ha emitido demasiadas solicitudes en nombre de un usuario en un corto período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="64068-354">The application has issued too many requests on behalf of a user in a short period of time.</span></span> <span data-ttu-id="64068-355">Para ayudar a garantizar que la API de OneNote permanece estable y con capacidad de respuesta, la API devuelve un código de estado 429 y este error cuando detecta que una aplicación está usando demasiados recursos.</span><span class="sxs-lookup"><span data-stu-id="64068-355">To help ensure that the OneNote API remains stable and responsive, the API returns a 429 status code and this error when it detects that an application is using too many resources.</span></span> 

<span data-ttu-id="64068-356">Para obtener más información, consulte [OneNote API throttling and how to avoid it](http://blogs.msdn.com/b/onenotedev/archive/2016/01/13/onenote-api-throttling-and-best-practices.aspx) (Limitación de la API de OneNote y cómo evitarla).</span><span class="sxs-lookup"><span data-stu-id="64068-356">For more information, see [OneNote API throttling and how to avoid it](http://blogs.msdn.com/b/onenotedev/archive/2016/01/13/onenote-api-throttling-and-best-practices.aspx).</span></span>

### <a name="20168"></a><span data-ttu-id="64068-357">20168</span><span class="sxs-lookup"><span data-stu-id="64068-357">20168</span></span>
<span data-ttu-id="64068-358">No se admite el origen de vídeo especificado en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-358">The video source specified in the request is not supported.</span></span> <span data-ttu-id="64068-359">Vea [Sitios de vídeo compatibles](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-images-files#videos) para obtener la lista actual.</span><span class="sxs-lookup"><span data-stu-id="64068-359">See [Supported video sites](https://msdn.microsoft.com/es-ES/office/office365/howto/onenote-images-files#videos) for the current list.</span></span>


## <a name="codes-from-30001-to-39999"></a><span data-ttu-id="64068-360">Códigos de 30001 a 39999</span><span class="sxs-lookup"><span data-stu-id="64068-360">Codes from 30001 to 39999</span></span>
<span data-ttu-id="64068-361">Hay algún fallo en la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="64068-361">Something is wrong with the user's account.</span></span>

### <a name="30101"></a><span data-ttu-id="64068-362">30101</span><span class="sxs-lookup"><span data-stu-id="64068-362">30101</span></span>
<span data-ttu-id="64068-363">La cuenta de usuario ha excedido su cuota de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="64068-363">The user account has exceeded its OneDrive quota.</span></span> <span data-ttu-id="64068-364">Vea [OneDrive](https://onedrive.live.com/about/es-ES/).</span><span class="sxs-lookup"><span data-stu-id="64068-364">See [OneDrive](https://onedrive.live.com/about/es-ES/).</span></span>

### <a name="30102"></a><span data-ttu-id="64068-365">30102</span><span class="sxs-lookup"><span data-stu-id="64068-365">30102</span></span>
<span data-ttu-id="64068-366">No se puede agregar nada más a la sección solicitada porque ha alcanzado su tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="64068-366">Nothing more can be added to the requested section because it has reached its maximum size.</span></span>

### <a name="30103"></a><span data-ttu-id="64068-367">30103</span><span class="sxs-lookup"><span data-stu-id="64068-367">30103</span></span>
<span data-ttu-id="64068-368">El consumo de recursos es demasiado alto para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-368">Resource consumption is too high for the request.</span></span> <span data-ttu-id="64068-369">La cuenta de usuario de destino tiene un gran conjunto de datos o el servicio está recibiendo un gran número de solicitudes simultáneas para el mismo sitio (por ejemplo, el sitio personal del usuario o un sitio de grupo).</span><span class="sxs-lookup"><span data-stu-id="64068-369">Either the target user account has a large dataset, or the service is receiving a high number of concurrent requests to the same site (for example, the user's personal site or a team site).</span></span>

### <a name="30104"></a><span data-ttu-id="64068-370">30104</span><span class="sxs-lookup"><span data-stu-id="64068-370">30104</span></span>
<span data-ttu-id="64068-371">Se ha suspendido la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="64068-371">The user account has been suspended.</span></span>

### <a name="30105"></a><span data-ttu-id="64068-372">30105</span><span class="sxs-lookup"><span data-stu-id="64068-372">30105</span></span>
<span data-ttu-id="64068-373">No se ha aprovisionado el OneDrive for Business del usuario, que es necesario para los portátiles de acceso.</span><span class="sxs-lookup"><span data-stu-id="64068-373">The user's personal OneDrive for Business site is not provisioned, which is required to access notebooks.</span></span> <span data-ttu-id="64068-374">El servicio de OneNote aprovisionará el sitio ahora.</span><span class="sxs-lookup"><span data-stu-id="64068-374">The OneNote service will provision the site now.</span></span> <span data-ttu-id="64068-375">Este proceso puede tardar varios minutos.</span><span class="sxs-lookup"><span data-stu-id="64068-375">This process may take several minutes.</span></span>

### <a name="30106"></a><span data-ttu-id="64068-376">30106</span><span class="sxs-lookup"><span data-stu-id="64068-376">30106</span></span>
<span data-ttu-id="64068-377">OneDrive for Business se está aprovisionando para el usuario.</span><span class="sxs-lookup"><span data-stu-id="64068-377">OneDrive for Business is being provisioned for the user.</span></span>

### <a name="30108"></a><span data-ttu-id="64068-378">30108</span><span class="sxs-lookup"><span data-stu-id="64068-378">30108</span></span>
<span data-ttu-id="64068-379">No se pudo recuperar el OneDrive for Business personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="64068-379">The user's personal OneDrive for Business could not be retrieved.</span></span> <span data-ttu-id="64068-380">En la tabla siguiente se enumeran algunas causas posibles.</span><span class="sxs-lookup"><span data-stu-id="64068-380">The following table lists some possible causes.</span></span>

| <span data-ttu-id="64068-381">Motivo</span><span class="sxs-lookup"><span data-stu-id="64068-381">Cause</span></span> | <span data-ttu-id="64068-382">Solución</span><span class="sxs-lookup"><span data-stu-id="64068-382">Resolution</span></span> |
|:------|:------|
| <span data-ttu-id="64068-383">No se ha aprovisionado el sitio personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="64068-383">The user's personal site has not been provisioned.</span></span> | <span data-ttu-id="64068-384">El usuario debe abrir OneDrive for Business y seguir las instrucciones para crear el sitio.</span><span class="sxs-lookup"><span data-stu-id="64068-384">The user should open OneDrive for Business and follow any instructions to provision the site.</span></span> <span data-ttu-id="64068-385">Si esto no funciona, deben ponerse en contacto con su administrador de inquilinos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="64068-385">If this fails, they should contact their Office 365 tenant administrator.</span></span> |
| <span data-ttu-id="64068-386">Actualmente se está aprovisionando el sitio personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="64068-386">The user's personal site is currently being provisioned.</span></span> | <span data-ttu-id="64068-387">Intente de nuevo la solicitud más tarde.</span><span class="sxs-lookup"><span data-stu-id="64068-387">Try the request later.</span></span> |
| <span data-ttu-id="64068-388">El usuario no tiene un OneDrive válido para la licencia de la empresa.</span><span class="sxs-lookup"><span data-stu-id="64068-388">The user does not have a valid OneDrive for Business license.</span></span> | <span data-ttu-id="64068-389">El usuario debe ponerse en contacto con su administrador de inquilinos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="64068-389">The user should contact their Office 365 tenant administrator.</span></span> |
| <span data-ttu-id="64068-390">Un problema de red ha impedido que la solicitud se enviase correctamente.</span><span class="sxs-lookup"><span data-stu-id="64068-390">A network issue prevented the request from being successfully sent.</span></span> | <span data-ttu-id="64068-391">Intente de nuevo la solicitud más tarde.</span><span class="sxs-lookup"><span data-stu-id="64068-391">Try the request later.</span></span> |

### <a name="30109"></a><span data-ttu-id="64068-392">30109</span><span class="sxs-lookup"><span data-stu-id="64068-392">30109</span></span>
<span data-ttu-id="64068-393">No existen algunos usuarios de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64068-393">Some users in the request do not exist.</span></span>

### <a name="30110"></a><span data-ttu-id="64068-394">30110</span><span class="sxs-lookup"><span data-stu-id="64068-394">30110</span></span>
<span data-ttu-id="64068-395">Los servicios de información de alumno no se han registrado para este arrendatario.</span><span class="sxs-lookup"><span data-stu-id="64068-395">Student Information Services has not been registered for this tenant.</span></span>

### <a name="30111"></a><span data-ttu-id="64068-396">30111</span><span class="sxs-lookup"><span data-stu-id="64068-396">30111</span></span>
<span data-ttu-id="64068-397">Hay un error genérico con los servicios de información del alumno.</span><span class="sxs-lookup"><span data-stu-id="64068-397">There is a generic error with Student Information Services.</span></span>

### <a name="30112"></a><span data-ttu-id="64068-398">30112</span><span class="sxs-lookup"><span data-stu-id="64068-398">30112</span></span>
<span data-ttu-id="64068-399">Varios usuarios afectados por la solicitud tenían el mismo nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="64068-399">Multiple users affected by the request had the same username.</span></span>

### <a name="30113"></a><span data-ttu-id="64068-400">30113</span><span class="sxs-lookup"><span data-stu-id="64068-400">30113</span></span>
<span data-ttu-id="64068-401">El bloc de notas no está configurado para permitir invitaciones.</span><span class="sxs-lookup"><span data-stu-id="64068-401">The notebook is not configured to allow invites.</span></span>

### <a name="30114"></a><span data-ttu-id="64068-402">30114</span><span class="sxs-lookup"><span data-stu-id="64068-402">30114</span></span>
<span data-ttu-id="64068-403">Falta un parámetro necesario.</span><span class="sxs-lookup"><span data-stu-id="64068-403">There is a required parameter missing.</span></span>

## <a name="codes-from-40001-to-49999"></a><span data-ttu-id="64068-404">Códigos de 40001 a 49999</span><span class="sxs-lookup"><span data-stu-id="64068-404">Codes from 40001 to 49999</span></span>
<span data-ttu-id="64068-405">El usuario o la aplicación no tienen los permisos correctos.</span><span class="sxs-lookup"><span data-stu-id="64068-405">The user or application does not have the correct permissions.</span></span>

### <a name="40001"></a><span data-ttu-id="64068-406">40001</span><span class="sxs-lookup"><span data-stu-id="64068-406">40001</span></span>
<span data-ttu-id="64068-407">La solicitud no contiene un token válido de OAuth.</span><span class="sxs-lookup"><span data-stu-id="64068-407">The request doesn't contain a valid OAuth token.</span></span> <span data-ttu-id="64068-408">Vea [Permisos de notas](permissions_reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="64068-408">See [Notes permissions](permissions_reference.md#notes-permissions).</span></span>

### <a name="40002"></a><span data-ttu-id="64068-409">40002</span><span class="sxs-lookup"><span data-stu-id="64068-409">40002</span></span>
<span data-ttu-id="64068-410">El usuario no tiene permiso para escribir en la ubicación solicitada.</span><span class="sxs-lookup"><span data-stu-id="64068-410">The user doesn't have permission to write to the requested location.</span></span>

### <a name="40003"></a><span data-ttu-id="64068-411">40003</span><span class="sxs-lookup"><span data-stu-id="64068-411">40003</span></span>
<span data-ttu-id="64068-412">El usuario no tiene permiso para acceder al recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="64068-412">The user doesn't have permission to access the requested resource.</span></span>

### <a name="40004"></a><span data-ttu-id="64068-413">40004</span><span class="sxs-lookup"><span data-stu-id="64068-413">40004</span></span>
<span data-ttu-id="64068-414">El token de OAuth no tiene los ámbitos necesarios para realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="64068-414">The OAuth token doesn't have the required scopes to perform the requested action.</span></span> <span data-ttu-id="64068-415">Vea [Permisos de notas](permissions_reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="64068-415">See [Notes permissions](permissions_reference.md#notes-permissions).</span></span>

### <a name="40006"></a><span data-ttu-id="64068-416">40006</span><span class="sxs-lookup"><span data-stu-id="64068-416">40006</span></span> 
<span data-ttu-id="64068-417">El token de OAuth no tiene los ámbitos necesarios para realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="64068-417">The OAuth token doesn't have the required scopes to perform the requested action.</span></span> <span data-ttu-id="64068-418">Específicamente, el permiso de edición.</span><span class="sxs-lookup"><span data-stu-id="64068-418">Specifically the edit permission.</span></span> <span data-ttu-id="64068-419">Vea [Permisos de notas](permissions_reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="64068-419">See [Notes permissions](permissions_reference.md#notes-permissions).</span></span>

### <a name="40007"></a><span data-ttu-id="64068-420">40007</span><span class="sxs-lookup"><span data-stu-id="64068-420">40007</span></span>
<span data-ttu-id="64068-421">El usuario no tiene permisos para acceder a este recurso.</span><span class="sxs-lookup"><span data-stu-id="64068-421">The user does not have permissions to access this resource.</span></span>

### <a name="40008"></a><span data-ttu-id="64068-422">40008</span><span class="sxs-lookup"><span data-stu-id="64068-422">40008</span></span>
<span data-ttu-id="64068-423">El acceso está prohibido para este recurso.</span><span class="sxs-lookup"><span data-stu-id="64068-423">Access is Forbidden for this resource.</span></span>

### <a name="40009"></a><span data-ttu-id="64068-424">40009</span><span class="sxs-lookup"><span data-stu-id="64068-424">40009</span></span>
<span data-ttu-id="64068-425">El contenedor ya está en uso por otro recurso.</span><span class="sxs-lookup"><span data-stu-id="64068-425">The container is already in use by another resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="64068-426">Ver también</span><span class="sxs-lookup"><span data-stu-id="64068-426">See also</span></span>

- [<span data-ttu-id="64068-427">Respuestas de error de Microsoft Graph y tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="64068-427">Microsoft Graph error responses and resource types</span></span>](errors.md)
- [<span data-ttu-id="64068-428">Referencia de OneNote</span><span class="sxs-lookup"><span data-stu-id="64068-428">OneNote reference</span></span>](../api-reference/v1.0/resources/onenote.md)

