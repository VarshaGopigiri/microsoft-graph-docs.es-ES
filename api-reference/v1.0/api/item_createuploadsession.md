# <a name="upload-large-files-with-an-upload-session"></a><span data-ttu-id="0af8a-101">Cargar archivos de gran tamaño con una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="0af8a-101">Upload large files with an upload session</span></span>

<span data-ttu-id="0af8a-p101">Cree una sesión de carga para permitir que su aplicación cargue archivos de hasta el tamaño de archivo máximo. Una sesión de carga permite que su aplicación cargue intervalos del archivo en solicitudes API secuenciales, lo que permite que la transferencia se reanude si se interrumpe una conexión mientras la carga está en curso.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p101">Create an upload session to allow your app to upload files up to the maximum file size. An upload session allows your app to upload ranges of the file in sequental API requests, which allows the transfer to be resumed if a connection is dropped while the upload is in progress.</span></span>

<span data-ttu-id="0af8a-104">Para cargar un archivo mediante una sesión de carga hay que realizar dos pasos:</span><span class="sxs-lookup"><span data-stu-id="0af8a-104">To upload a file using an upload session, there are two steps:</span></span>

1. [<span data-ttu-id="0af8a-105">Crear una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="0af8a-105">Create an upload session</span></span>](#create-an-upload-session)
2. [<span data-ttu-id="0af8a-106">Cargar bytes a la sesión de carga</span><span class="sxs-lookup"><span data-stu-id="0af8a-106">Upload bytes to the upload session</span></span>](#upload-bytes-to-the-upload-session)

## <a name="prerequisites"></a><span data-ttu-id="0af8a-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0af8a-107">Prerequisites</span></span>
<span data-ttu-id="0af8a-108">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="0af8a-108">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="0af8a-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0af8a-109">Files.ReadWrite</span></span>
* <span data-ttu-id="0af8a-110">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0af8a-110">Files.ReadWrite.All</span></span>
* <span data-ttu-id="0af8a-111">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0af8a-111">Sites.ReadWrite.All</span></span>

> <span data-ttu-id="0af8a-p102">**Nota**: El permiso de aplicación Files.ReadWrite.All aún no se admite en esta API. Está prevista la compatibilidad completa próximamente.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p102">**Note**: The Files.ReadWrite.All application permission is not yet supported on this API. Full support is planned soon.</span></span> 

## <a name="create-an-upload-session"></a><span data-ttu-id="0af8a-114">Crear una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="0af8a-114">Create an upload session</span></span>

<span data-ttu-id="0af8a-p103">Para comenzar la carga de archivos de gran tamaño, su aplicación debe solicitar primero una nueva sesión de carga. Esto crea una ubicación de almacenamiento temporal donde se guardarán los bytes del archivo hasta que se cargue el archivo completo. Una vez que se haya cargado el último byte del archivo, termina la sesión de carga y el archivo final se muestra en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p103">To begin a large file upload, your app must first request a new upload session. This creates a temporary storage location where the bytes of the file will be saved until the complete file is uploaded. Once the last byte of the file has been uploaded the upload session is completed and the final file is shown in the destination folder.</span></span>

### <a name="http-request"></a><span data-ttu-id="0af8a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0af8a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root:/{path-to-item}:/createUploadSession
POST /me/drive/items/{parent-item-id}:/{filename}:/createUploadSession
```

### <a name="request-body"></a><span data-ttu-id="0af8a-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0af8a-119">Request body</span></span>
<span data-ttu-id="0af8a-p104">No es necesario ningún cuerpo de solicitud. Sin embargo, puede especificar un cuerpo de la solicitud para proporcionar datos adicionales sobre el archivo que se está cargando.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p104">No request body is required. However, you can specify a request body to provide additional data about the file being uploaded.</span></span>

<span data-ttu-id="0af8a-122">Por ejemplo, para controlar el comportamiento si ya existe el nombre de archivo, puede especificar la propiedad de comportamiento ante conflictos en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0af8a-122">For example, to control the behavior if the filename is already taken, you can specify the conflict behavior property in the body of the request.</span></span>

```json
{
    "item": {
        "@microsoft.graph.conflictBehavior": "rename"
    }
}
```

### <a name="optional-request-headers"></a><span data-ttu-id="0af8a-123">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="0af8a-123">Optional request headers</span></span>

| <span data-ttu-id="0af8a-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="0af8a-124">Name</span></span>       | <span data-ttu-id="0af8a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0af8a-125">Value</span></span> | <span data-ttu-id="0af8a-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="0af8a-126">Description</span></span>                                                                                                                                                            |
|:-----------|:------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af8a-127">*if-match*</span><span class="sxs-lookup"><span data-stu-id="0af8a-127">*if-match*</span></span> | <span data-ttu-id="0af8a-128">etag</span><span class="sxs-lookup"><span data-stu-id="0af8a-128">etag</span></span>  | <span data-ttu-id="0af8a-129">Si se incluye este encabezado de solicitud y la eTag (o cTag) proporcionada no coincide con la eTag actual en el elemento, se devuelve una respuesta de error `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="0af8a-129">If this request header is included and the eTag (or cTag) provided does not match the current etag on the item, a `412 Precondition Failed` errr response is returned.</span></span> |


### <a name="response"></a><span data-ttu-id="0af8a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0af8a-130">Response</span></span>
<span data-ttu-id="0af8a-131">La respuesta a esta solicitud ofrecerá los detalles de la [uploadSession](../resources/uploadsession.md) recién creada, que incluye la dirección URL utilizada para cargar las partes del archivo.</span><span class="sxs-lookup"><span data-stu-id="0af8a-131">The response to this request will provide the details of the newly created [uploadSession](../resources/uploadsession.md), which includes the URL used for uploading the parts of the file.</span></span> 

### <a name="example"></a><span data-ttu-id="0af8a-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0af8a-132">Example</span></span>

<!-- {
  "blockType": "request",
  "name": "driveItem_createUploadSession"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root:/{item-path}:/createUploadSession
```

##### <a name="response"></a><span data-ttu-id="0af8a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0af8a-133">Response</span></span> 

<span data-ttu-id="0af8a-134">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0af8a-134">The following example shows the formula bar</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.uploadSession"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "uploadUrl": "https://tenant-my.sharepoint.com/alkjl1kjklna",
  "expirationDateTime": "2020-08-24T10:58:00Z",
  "nextExpectedRanges": ["0-"]
}
```

## <a name="upload-bytes-to-the-upload-session"></a><span data-ttu-id="0af8a-135">Cargar bytes en la sesión de carga</span><span class="sxs-lookup"><span data-stu-id="0af8a-135">Upload bytes to the upload session</span></span>

<span data-ttu-id="0af8a-p105">Para cargar el archivo o una parte del archivo, la aplicación envía una solicitud PUT al valor **uploadUrl** recibido en la respuesta **createUploadSession**. Puede cargar el archivo completo o dividir el archivo en fragmentos, siempre y cuando el número máximo de bytes de cualquier solicitud dada sea inferior a 60 MiB. Los fragmentos del archivo se deben cargar secuencialmente en orden. La carga de fragmentos sin un orden producirá un error.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p105">To upload the file, or a portion of the file, your app makes a PUT request to the **uploadUrl** value received in the **createUploadSession** response. You can upload the entire file, or split the file into fragments, as long as the maximum bytes in any given request is less than 60 MiB. The fragments of the file must be uploaded sequentally in order. Uploading fragments out of order will result in an error.</span></span>

<span data-ttu-id="0af8a-p106">**Nota:** Si su aplicación divide un archivo en varios fragmentos, el tamaño de cada fragmento **DEBE** ser un múltiplo de 320 KiB. Usar un tamaño de fragmento que no puede dividirse uniformemente por 320 ocasionará errores a la hora de confirmar algunos archivos.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p106">**Note:** If your app splits a file into multiple fragments, the size of each fragment **MUST** be a multiple of 320 KiB. Using a fragment size that does not divide evenly by 320 will result in errors committing some files.</span></span>

### <a name="example"></a><span data-ttu-id="0af8a-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0af8a-142">Example</span></span>

<span data-ttu-id="0af8a-p107">Este ejemplo carga los primeros 26 bytes de un archivo de 128 bytes. El encabezado **Content-Length** especifica el tamaño de la solicitud actual. El encabezado **Content-Range** indica el intervalo de bytes en el archivo global que representa esta solicitud. Se debe conocer la longitud total del archivo antes de cargar el primer fragmento del archivo.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p107">This example is uploading the first 26 bytes of a 128 byte file. The **Content-Length** header specifies the size of the current request. The **Content-Range** header indicates the range of bytes in the overall file that this request represents. The total length of the file must be known before you can upload the first fragment of the file.</span></span>

<!-- { "blockType": "request", "name": "upload-fragment-piece", "scopes": "files.readwrite" } -->
```
PUT https://tenant-my.sharepoint.com/alkjl1kjklna
Content-Length: 26
Content-Range: bytes 0-25/128

<bytes 0-25 of the file>
```

<span data-ttu-id="0af8a-p108">**Importante:** Su aplicación debe asegurarse de que el tamaño total del archivo especificado en el encabezado **Content-Range** sea el mismo en todas las solicitudes. Si un fragmento indica un tamaño de archivo diferente, se producirá un error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p108">**Important:** Your app must ensure the total file size specified in the **Content-Range** header is the same for all requests. If a fragment declares a different file size, the request will fail.</span></span>

##### <a name="response"></a><span data-ttu-id="0af8a-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0af8a-149">Response</span></span>

<span data-ttu-id="0af8a-150">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0af8a-150">The following example shows the formula bar</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["26-"]
}
```

<span data-ttu-id="0af8a-p109">Su aplicación puede utilizar el valor **nextExpectedRanges** para determinar dónde comenzar el siguiente fragmento. Puede ver varios intervalos especificados, lo que indica las partes del archivo que aún no ha recibido el servidor. Esto resulta útil si necesita reanudar una transferencia que se ha interrumpido y su cliente no está seguro del estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p109">Your app can use the **nextExpectedRanges** value to determine where to start the next fragment. You may see multiple ranges specified, indicating parts of the file that the server has not yet received. This is useful if you need to resume a transfer that was interrupted and your client is unsure of the state on the service.</span></span>

<span data-ttu-id="0af8a-p110">Siempre debe determinar el tamaño del fragmento según las siguientes recomendaciones. No suponga que **nextExpectedRanges** devolverá intervalos del tamaño adecuado de un fragmento de carga. La propiedad **nextExpectedRanges** indica intervalos del archivo que no se han recibido y no un patrón de cómo debe cargar el archivo.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p110">You should always determine the fragment size according to the best practices below. Do not assume that **nextExpectedRanges** will return reanges of proper size for an upload fragment. The **nextExpectedRanges** property indicates ranges of the file that have not been received and not a pattern for how you should upload the file.</span></span>

<span data-ttu-id="0af8a-157">**Notas**:</span><span class="sxs-lookup"><span data-stu-id="0af8a-157">**Notes:**</span></span>

* <span data-ttu-id="0af8a-158">La propiedad `nextExpectedRanges` no siempre enumera todos los intervalos que faltan.</span><span class="sxs-lookup"><span data-stu-id="0af8a-158">The `nextExpectedRanges` property won't always list all of the missing ranges.</span></span>
* <span data-ttu-id="0af8a-p111">Cuando las escrituras de fragmento se ejecuten correctamente, devolverá el siguiente intervalo desde el que empezar (ej. "523-").</span><span class="sxs-lookup"><span data-stu-id="0af8a-p111">On successful fragment writes, it will return the next range to start from (eg. "523-").</span></span>
* <span data-ttu-id="0af8a-p112">Cuando se produzcan errores en los que el cliente envíe un fragmento que el servidor ya ha recibido, el servidor responderá `HTTP 416 Requested Range Not Satisfiable`. Puede [solicitar el estado de la carga](#resuming-an-in-progress-upload) para obtener una lista más detallada de los intervalos que faltan.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p112">On failures when the client sent a fragment the server had already received, the server will respond with `HTTP 416 Requested Range Not Satisfiable`. You can [request upload status](#resuming-an-in-progress-upload) to get a more detailed list of missing ranges.</span></span>
* <span data-ttu-id="0af8a-p113">Incluir el encabezado de autorización al emitir la llamada `PUT` puede resultar en la respuesta `HTTP 401 Unauthorized`. El encabezado de autorización y el token de portador deberían enviarse únicamente al emitir el `POST` durante el primer paso. No debería incluirse al emitir el `PUT`.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p113">Including the Authorization header when issuing the `PUT` call may result in a `HTTP 401 Unauthorized` response. The Authoization header and bearer token should only be sent when issueing the `POST` during the first step. It should be not be included when issueing the `PUT`.</span></span>   


## <a name="completing-a-file"></a><span data-ttu-id="0af8a-166">Finalización de un archivo</span><span class="sxs-lookup"><span data-stu-id="0af8a-166">Completing a file</span></span>

<span data-ttu-id="0af8a-p114">Cuando se reciba el último fragmento de un archivo, el servidor responderá `HTTP 201 Created` o `HTTP 200 OK`. El cuerpo de la respuesta incluirá también la propiedad predeterminada establecida del **driveItem** que representa el archivo completo.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p114">When the last fragment of a file is received the server will response with an `HTTP 201 Created` or `HTTP 200 OK`. The response body will also include the default property set for the **driveItem** representing the completed file.</span></span>

<!-- { "blockType": "request", "name": "upload-fragment-final", "scopes": "files.readwrite" } -->
```
PUT https://tenant-my.sharepoint.com/alkjl1kjklna
Content-Length: 21
Content-Range: bytes 101-127/128

<final bytes of the file>
```

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->
```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "912310013A123",
  "name": "largefile.vhd",
  "size": 128,
  "file": { }
}
```
<span data-ttu-id="0af8a-169">**Nota:** La respuesta del elemento está truncada para que la documentación sea más clara.</span><span class="sxs-lookup"><span data-stu-id="0af8a-169">**Note:** The item response is truncated for documentation clarity.</span></span>

## <a name="cancel-an-upload-session"></a><span data-ttu-id="0af8a-170">Cancelar una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="0af8a-170">Cancel an upload session</span></span>

<span data-ttu-id="0af8a-p115">Para cancelar una sesión de carga, envíe una solicitud DELETE a la dirección URL de carga. Esto limpia el archivo temporal que contiene los datos previamente cargados. Debe utilizarse en los casos en los que se anula la carga, por ejemplo, si el usuario cancela la transferencia.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p115">To cancel an upload session send a DELETE request to the upload URL. This cleans up the temporary file holding the data previously uploaded. This should be used in scenarios where the upload is aborted, for example, if the user cancels the transfer.</span></span>

<span data-ttu-id="0af8a-174">Los archivos temporales y la sesión de carga que los acompaña se limpian automáticamente cuando pasa la **expirationDateTime**.</span><span class="sxs-lookup"><span data-stu-id="0af8a-174">Temporary files and their accompanying upload session are automatically cleaned up after the **expirationDateTime** has passed.</span></span>

### <a name="example"></a><span data-ttu-id="0af8a-175">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0af8a-175">Example</span></span>

<span data-ttu-id="0af8a-176">La solicitud DELETE hará que la sesión de carga expire inmediatamente y eliminará los bytes cargados previamente.</span><span class="sxs-lookup"><span data-stu-id="0af8a-176">The DELETE request will immedately expire the upload session and remove any previously uploaded bytes.</span></span>

<!-- { "blockType": "request", "name": "upload-fragment-cancel", "scopes": "files.readwrite" } -->
```http
DELETE https://tenant-my.sharepoint.com/alkjl1kjklna
```

##### <a name="response"></a><span data-ttu-id="0af8a-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0af8a-177">Response</span></span> 

<span data-ttu-id="0af8a-178">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0af8a-178">The following example shows the formula bar</span></span>

<!-- { "blockType": "response" } -->
```http
HTTP/1.1 204 No Content
```

## <a name="resuming-an-in-progress-upload"></a><span data-ttu-id="0af8a-179">Reanudar una carga en curso</span><span class="sxs-lookup"><span data-stu-id="0af8a-179">Resuming an in-progress upload</span></span>

<span data-ttu-id="0af8a-p116">Si una solicitud de carga se desconecta o si falla antes de que se complete la solicitud, se pasan por alto todos los bytes de dicha solicitud. Esto puede ocurrir si se interrumpe la conexión entre la aplicación y el servicio. Si esto ocurre, la aplicación todavía puede reanudar la transferencia de archivos desde el fragmento completado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p116">If an upload request is disconnected or fails before the request is completed, all bytes in that request are ignored. This can occur if the connection between your app and the service is dropped. If this occurs, your app can still resume the file transfer from the previously completed fragment.</span></span>

<span data-ttu-id="0af8a-183">Para averiguar qué intervalos de bytes se han recibido anteriormente, su aplicación puede solicitar el estado de una sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="0af8a-183">To find out which byte ranges have been received previously, your app can request the status of an upload session.</span></span>

### <a name="example"></a><span data-ttu-id="0af8a-184">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0af8a-184">Example</span></span>
<span data-ttu-id="0af8a-185">Consulte el estado de la carga mediante el envío de una solicitud GET a `uploadUrl`.</span><span class="sxs-lookup"><span data-stu-id="0af8a-185">Query the status of the upload by sending a GET request to the `uploadUrl`.</span></span>

<!-- { "blockType": "request", "name": "upload-fragment-resume", "scopes": "files.readwrite" } -->
```
GET https://tenant-my.sharepoint.com/alkjl1kjklna
```

<span data-ttu-id="0af8a-186">El servidor responderá con una lista de los intervalos de bytes que faltan por cargar y la fecha de expiración de la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="0af8a-186">The server will respond with a list of missing byte ranges that need to be uploaded and the expiration time for the upload session.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->
```http
HTTP/1.1 200 OK

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["12345-"]
}
```

### <a name="upload-remaining-data"></a><span data-ttu-id="0af8a-187">Cargar los datos restantes</span><span class="sxs-lookup"><span data-stu-id="0af8a-187">Upload remaining data</span></span>
<span data-ttu-id="0af8a-188">Ahora que la aplicación sabe desde dónde iniciar la carga, reanude la carga siguiendo los pasos descritos en [cargar bytes a la sesión de carga](#upload-bytes-to-the-upload-session).</span><span class="sxs-lookup"><span data-stu-id="0af8a-188">Now that your app knows where to start the upload from, resume the upload by following the steps in [upload bytes to the upload session](#upload-bytes-to-the-upload-session).</span></span>


## <a name="best-practices"></a><span data-ttu-id="0af8a-189">Procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="0af8a-189">Best practices</span></span>

* <span data-ttu-id="0af8a-190">Reanude o vuelva a ejecutar las cargas que fallaron debido a las interrupciones de la conexión o a los errores 5xx, como:</span><span class="sxs-lookup"><span data-stu-id="0af8a-190">Resume or retry uploads that fail due to connection interruptions or any 5xx errors, including:</span></span>
  * `500 Internal Server Error`
  * `502 Bad Gateway`
  * `503 Service Unavailable`
  * `504 Gateway Timeout`
* <span data-ttu-id="0af8a-191">Utilice una estrategia de interrupción exponencial si se devuelve cualquier error 5xx del servidor al reanudar o volver a ejecutar solicitudes de carga.</span><span class="sxs-lookup"><span data-stu-id="0af8a-191">Use an exponential back off strategy if any 5xx server errors are returned when resuming or retrying upload requests.</span></span>
* <span data-ttu-id="0af8a-192">Si hay otros errores, no debe utilizar una estrategia de interrupción exponencial sino limitar el número de reintentos realizados.</span><span class="sxs-lookup"><span data-stu-id="0af8a-192">For other errors, you should not use an exponential back off strategy but limit the number of retry attempts made.</span></span>
* <span data-ttu-id="0af8a-193">Controle los errores `404 Not Found` al realizar cargas reanudables volviendo a iniciar la carga completa.</span><span class="sxs-lookup"><span data-stu-id="0af8a-193">Handle `404 Not Found` errors when doing resumable uploads by starting the entire upload over.</span></span>
* <span data-ttu-id="0af8a-194">Utilice transferencias de archivo reanudables para los archivos de más de 10 MiB (10 \* 1024 \* 1024 bytes).</span><span class="sxs-lookup"><span data-stu-id="0af8a-194">Use resumable file transfers for files larger than 10 MiB (10 \* 1024 \* 1024 bytes).</span></span>
* <span data-ttu-id="0af8a-p117">Un tamaño de fragmento de 10 MiB para conexiones estables de alta velocidad es óptimo. Para conexiones más lentas o menos fiables puede obtener mejores resultados con tamaños de fragmento más pequeños. El tamaño de fragmento recomendado es entre 5 y 10 MiB.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p117">A fragment size of 10 MiB for stable high speed connections is optimal. For slower or less reliable connections you may get better results from a smaller fragment size. The recommended fragment size is between 5-10 MiB.</span></span>
* <span data-ttu-id="0af8a-p118">Utilice un tamaño de fragmento que sea múltiplo de 320 KiB (320 \* 1024 bytes). Si no utiliza un tamaño de fragmento que sea múltiplo de 320 KiB, las transferencias de archivos de gran tamaño pueden fallar después de que se cargue el último fragmento.</span><span class="sxs-lookup"><span data-stu-id="0af8a-p118">Use a fragment size that is a multiple of 320 KiB (320 \* 1024 bytes). Failing to use a fragment size that is a multiple of 320 KiB can result in large file transfers failing after the last fragment is uploaded.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Upload item",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
