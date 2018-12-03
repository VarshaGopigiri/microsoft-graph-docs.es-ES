---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carga de archivos reanudable
ms.openlocfilehash: 09f76b4427df446b2f063827029473a11dba6341
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083748"
---
# <a name="upload-large-files-with-an-upload-session"></a><span data-ttu-id="fc966-102">Cargar archivos de gran tamaño con una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-102">Upload large files with an upload session</span></span>

> <span data-ttu-id="fc966-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc966-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc966-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc966-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fc966-p102">Cree una sesión de carga para permitir que la aplicación cargue archivos de hasta el tamaño de archivo máximo. Una sesión de carga permite que la aplicación cargue intervalos del archivo en solicitudes API secuenciales, lo que permite que la transferencia se reanude si se interrumpe una conexión mientras la carga está en curso.</span><span class="sxs-lookup"><span data-stu-id="fc966-p102">Create an upload session to allow your app to upload files up to the maximum file size. An upload session allows your app to upload ranges of the file in sequential API requests, which allows the transfer to be resumed if a connection is dropped while the upload is in progress.</span></span>

<span data-ttu-id="fc966-107">Para cargar un archivo mediante una sesión de carga hay que realizar dos pasos:</span><span class="sxs-lookup"><span data-stu-id="fc966-107">To upload a file using an upload session, there are two steps:</span></span>

1. [<span data-ttu-id="fc966-108">Crear una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-108">Create an upload session</span></span>](#create-an-upload-session)
2. [<span data-ttu-id="fc966-109">Cargar bytes a la sesión de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-109">Upload bytes to the upload session</span></span>](#upload-bytes-to-the-upload-session)

## <a name="permissions"></a><span data-ttu-id="fc966-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc966-110">Permissions</span></span>

<span data-ttu-id="fc966-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc966-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc966-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc966-113">Permission type</span></span>      | <span data-ttu-id="fc966-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc966-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fc966-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc966-115">Delegated (work or school account)</span></span> | <span data-ttu-id="fc966-116">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc966-116">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="fc966-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc966-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fc966-118">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc966-118">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="fc966-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc966-119">Application</span></span> | <span data-ttu-id="fc966-120">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc966-120">Sites.ReadWrite.All</span></span> |

## <a name="create-an-upload-session"></a><span data-ttu-id="fc966-121">Crear una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-121">Create an upload session</span></span>

<span data-ttu-id="fc966-122">Para empezar a una carga de archivos de gran tamaño, la aplicación deberá solicitar primero una nueva sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-122">To begin a large file upload, your app must first request a new upload session.</span></span>
<span data-ttu-id="fc966-123">Esto crea una ubicación de almacenamiento temporal donde se guardarán los bytes del archivo hasta que se carga el archivo completo.</span><span class="sxs-lookup"><span data-stu-id="fc966-123">This creates a temporary storage location where the bytes of the file will be saved until the complete file is uploaded.</span></span>
<span data-ttu-id="fc966-124">Una vez que se ha cargado el último byte del archivo se completa la sesión de carga y el final del archivo se muestra en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="fc966-124">Once the last byte of the file has been uploaded the upload session is completed and the final file is shown in the destination folder.</span></span>
<span data-ttu-id="fc966-125">Como alternativa, puede aplazar la creación del archivo en el destino final hasta que se establezca explícitamente una solicitud para llevar a cabo la carga mediante la configuración de la `deferCommit` (propiedad) en los argumentos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc966-125">Alternatively, you can defer final creation of the file in the destination until you explicitly make a request to complete the upload, by setting the `deferCommit` property in the request arguments.</span></span>

### <a name="http-request"></a><span data-ttu-id="fc966-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc966-126">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/createUploadSession
POST /groups/{groupId}/drive/items/{itemId}/createUploadSession
POST /me/drive/items/{itemId}/createUploadSession
POST /sites/{siteId}/drive/items/{itemId}/createUploadSession
POST /users/{userId}/drive/items/{itemId}/createUploadSession
```

### <a name="request-body"></a><span data-ttu-id="fc966-127">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc966-127">Request body</span></span>

<span data-ttu-id="fc966-128">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc966-128">No request body is required.</span></span>
<span data-ttu-id="fc966-129">Sin embargo, puede especificar las propiedades en el cuerpo de la solicitud que proporciona datos adicionales sobre el archivo que se está cargando y personalización de la semántica de la operación de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-129">However, you can specify properties in the request body providing additional data about the file being uploaded and customizing the semantics of the upload operation.</span></span>

<span data-ttu-id="fc966-130">Por ejemplo, el `item` (propiedad) permite configurar los siguientes parámetros:<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.driveItemUploadableProperties" } --></span><span class="sxs-lookup"><span data-stu-id="fc966-130">For example, the `item` property allows setting the following parameters: <!-- { "blockType": "resource", "@odata.type": "microsoft.graph.driveItemUploadableProperties" } --></span></span>
```json
{
  "@microsoft.graph.conflictBehavior": "rename | fail | overwrite",
  "description": "description",
  "name": "filename.txt"
}
```

<span data-ttu-id="fc966-131">En el ejemplo siguiente se controla el comportamiento si el nombre de archivo ya está asignado y también especifica que no se debe crear el archivo final hasta que se realiza una solicitud de finalización explícita:</span><span class="sxs-lookup"><span data-stu-id="fc966-131">The following example controls the behavior if the filename is already taken, and also specifies that the final file should not be created until an explicit completion request is made:</span></span>

<!-- { "blockType": "ignored" } -->
```json
{
  "item": {
    "@microsoft.graph.conflictBehavior": "rename"
  },
  "deferCommit": true
}
```

### <a name="optional-request-headers"></a><span data-ttu-id="fc966-132">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="fc966-132">Optional request headers</span></span>

| <span data-ttu-id="fc966-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc966-133">Name</span></span>       | <span data-ttu-id="fc966-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fc966-134">Value</span></span> | <span data-ttu-id="fc966-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc966-135">Description</span></span>                                                                                                                                                            |
|:-----------|:------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc966-136">*if-match*</span><span class="sxs-lookup"><span data-stu-id="fc966-136">*if-match*</span></span> | <span data-ttu-id="fc966-137">etag</span><span class="sxs-lookup"><span data-stu-id="fc966-137">etag</span></span>  | <span data-ttu-id="fc966-138">Si se incluye este encabezado de solicitud y la eTag (o cTag) proporcionada no coincide con la eTag actual en el elemento, se devuelve una respuesta de error `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="fc966-138">If this request header is included and the eTag (or cTag) provided does not match the current etag on the item, a `412 Precondition Failed` error response is returned.</span></span> |

## <a name="parameters"></a><span data-ttu-id="fc966-139">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc966-139">Parameters</span></span>

| <span data-ttu-id="fc966-140">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fc966-140">Parameter</span></span>            | <span data-ttu-id="fc966-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc966-141">Type</span></span>                          | <span data-ttu-id="fc966-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc966-142">Description</span></span>
|:---------------------|:------------------------------|:---------------------------------
| <span data-ttu-id="fc966-143">item</span><span class="sxs-lookup"><span data-stu-id="fc966-143">item</span></span>                 | <span data-ttu-id="fc966-144">driveItemUploadableProperties</span><span class="sxs-lookup"><span data-stu-id="fc966-144">driveItemUploadableProperties</span></span> | <span data-ttu-id="fc966-145">Datos sobre el archivo que se está cargando</span><span class="sxs-lookup"><span data-stu-id="fc966-145">Data about the file being uploaded</span></span>
| <span data-ttu-id="fc966-146">deferCommit</span><span class="sxs-lookup"><span data-stu-id="fc966-146">deferCommit</span></span>          | <span data-ttu-id="fc966-147">Booleano</span><span class="sxs-lookup"><span data-stu-id="fc966-147">Boolean</span></span>                       | <span data-ttu-id="fc966-148">Si se establece en true, final de creación del archivo en el destino requerirá una solicitud explícita.</span><span class="sxs-lookup"><span data-stu-id="fc966-148">If set to true, final creation of the file in the destination will require an explicit request.</span></span> <span data-ttu-id="fc966-149">Sólo en OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="fc966-149">Only on OneDrive for Business.</span></span>

## <a name="item-properties"></a><span data-ttu-id="fc966-150">Propiedades de elementos</span><span class="sxs-lookup"><span data-stu-id="fc966-150">Item properties</span></span>

| <span data-ttu-id="fc966-151">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc966-151">Property</span></span>             | <span data-ttu-id="fc966-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc966-152">Type</span></span>               | <span data-ttu-id="fc966-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc966-153">Description</span></span>
|:---------------------|:-------------------|:---------------------------------
| <span data-ttu-id="fc966-154">description</span><span class="sxs-lookup"><span data-stu-id="fc966-154">description</span></span>          | <span data-ttu-id="fc966-155">String</span><span class="sxs-lookup"><span data-stu-id="fc966-155">String</span></span>             | <span data-ttu-id="fc966-156">Proporciona una descripción del elemento visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fc966-156">Provides a user-visible description of the item.</span></span> <span data-ttu-id="fc966-157">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fc966-157">Read-write.</span></span> <span data-ttu-id="fc966-158">Sólo en OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="fc966-158">Only on OneDrive Personal.</span></span>
| <span data-ttu-id="fc966-159">name</span><span class="sxs-lookup"><span data-stu-id="fc966-159">name</span></span>                 | <span data-ttu-id="fc966-160">String</span><span class="sxs-lookup"><span data-stu-id="fc966-160">String</span></span>             | <span data-ttu-id="fc966-p108">El nombre del elemento (nombre de archivo y extensión). Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fc966-p108">The name of the item (filename and extension). Read-write.</span></span>

### <a name="request"></a><span data-ttu-id="fc966-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc966-163">Request</span></span>

<span data-ttu-id="fc966-164">La respuesta a esta solicitud ofrecerá los detalles de la [uploadSession](../resources/uploadsession.md) recién creada, que incluye la dirección URL utilizada para cargar las partes del archivo.</span><span class="sxs-lookup"><span data-stu-id="fc966-164">The response to this request will provide the details of the newly created [uploadSession](../resources/uploadsession.md), which includes the URL used for uploading the parts of the file.</span></span> 

<!-- { "blockType": "request", "name": "upload-fragment-create-session", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drive/root:/{item-path}:/createUploadSession
Content-Type: application/json

{
  "item": {
    "@odata.type": "microsoft.graph.driveItemUploadableProperties",
    "@microsoft.graph.conflictBehavior": "rename",
    "name": "largefile.dat"
  }
}
```

### <a name="response"></a><span data-ttu-id="fc966-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc966-165">Response</span></span>

<span data-ttu-id="fc966-166">La respuesta a esta solicitud, si se realiza correctamente, proporcionará los detalles sobre dónde deben enviarse el resto de las solicitudes como un recurso [UploadSession](../resources/uploadsession.md).</span><span class="sxs-lookup"><span data-stu-id="fc966-166">The response to this request, if successful, will provide the details for where the remainder of the requests should be sent as an [UploadSession](../resources/uploadsession.md) resource.</span></span>

<span data-ttu-id="fc966-167">Este recurso proporciona detalles sobre dónde debe cargarse el intervalo de bytes del archivo y cuándo expira la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-167">This resource provides details about where the byte range of the file should be uploaded and when the upload session expires.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession",
       "optionalProperties": [ "nextExpectedRanges" ]  } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "uploadUrl": "https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337",
  "expirationDateTime": "2015-01-29T09:21:55.523Z"
}
```

## <a name="upload-bytes-to-the-upload-session"></a><span data-ttu-id="fc966-168">Cargar bytes en la sesión de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-168">Upload bytes to the upload session</span></span>

<span data-ttu-id="fc966-169">Para cargar el archivo o una parte del archivo, la aplicación envía una solicitud PUT al valor **uploadUrl** recibido en la respuesta **createUploadSession**.</span><span class="sxs-lookup"><span data-stu-id="fc966-169">To upload the file, or a portion of the file, your app makes a PUT request to the **uploadUrl** value received in the **createUploadSession** response.</span></span>
<span data-ttu-id="fc966-170">Puede cargar el archivo completo o dividir el archivo en varios intervalos de bytes, siempre y cuando el número máximo de bytes de cualquier solicitud dada sea inferior a 60 MiB.</span><span class="sxs-lookup"><span data-stu-id="fc966-170">You can upload the entire file, or split the file into multiple byte ranges, as long as the maximum bytes in any given request is less than 60 MiB.</span></span>

<span data-ttu-id="fc966-171">Los fragmentos del archivo se deben cargar secuencialmente en orden.</span><span class="sxs-lookup"><span data-stu-id="fc966-171">The fragments of the file must be uploaded sequentially in order.</span></span>
<span data-ttu-id="fc966-172">La carga de fragmentos sin un orden producirá un error.</span><span class="sxs-lookup"><span data-stu-id="fc966-172">Uploading fragments out of order will result in an error.</span></span>

<span data-ttu-id="fc966-173">**Nota:** Si su aplicación divide un archivo en varios intervalos de bits, el tamaño de cada uno **DEBE** ser un múltiplo de 320 KiB (327 680 bytes).</span><span class="sxs-lookup"><span data-stu-id="fc966-173">**Note:** If your app splits a file into multiple byte ranges, the size of each byte range **MUST** be a multiple of 320 KiB (327,680 bytes).</span></span> <span data-ttu-id="fc966-174">Usar un tamaño de fragmento que no puede dividirse uniformemente por 320 KiB ocasionará errores a la hora de confirmar algunos archivos.</span><span class="sxs-lookup"><span data-stu-id="fc966-174">Using a fragment size that does not divide evenly by 320 KiB will result in errors committing some files.</span></span>

### <a name="example"></a><span data-ttu-id="fc966-175">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc966-175">Example</span></span>

<span data-ttu-id="fc966-176">En este ejemplo, la aplicación carga los primeros 26 bytes de un archivo de 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="fc966-176">In this example, the app is uploading the first 26 bytes of a 128 byte file.</span></span>

* <span data-ttu-id="fc966-177">El encabezado **Content-Length** especifica el tamaño de la solicitud actual.</span><span class="sxs-lookup"><span data-stu-id="fc966-177">The **Content-Length** header specifies the size of the current request.</span></span>
* <span data-ttu-id="fc966-178">El encabezado **Content-Range** indica el intervalo de bytes en el archivo global que representa esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc966-178">The **Content-Range** header indicates the range of bytes in the overall file that this request represents.</span></span>
* <span data-ttu-id="fc966-179">La longitud total del archivo se conoce antes de cargar el primer fragmento del archivo.</span><span class="sxs-lookup"><span data-stu-id="fc966-179">The total length of the file is known before you can upload the first fragment of the file.</span></span>

<!-- { "blockType": "request", "opaqueUrl": true, "name": "upload-fragment-piece", "scopes": "files.readwrite" } -->

```http
PUT https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337
Content-Length: 26
Content-Range: bytes 0-25/128

<bytes 0-25 of the file>
```

<span data-ttu-id="fc966-180">**Importante:** Su aplicación debe asegurarse de que el tamaño total del archivo especificado en el encabezado **Content-Range** sea el mismo en todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="fc966-180">**Important:** Your app must ensure the total file size specified in the **Content-Range** header is the same for all requests.</span></span>
<span data-ttu-id="fc966-181">Si un intervalo de bytes indica un tamaño de archivo diferente, se producirá un error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc966-181">If a byte range declares a different file size, the request will fail.</span></span>

### <a name="response"></a><span data-ttu-id="fc966-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc966-182">Response</span></span>

<span data-ttu-id="fc966-183">Cuando se complete la solicitud, el servidor responderá con `202 Accepted` si existen más intervalos de bytes que necesitan cargarse.</span><span class="sxs-lookup"><span data-stu-id="fc966-183">When the request is complete, the server will respond with `202 Accepted` if there are more byte ranges that need to be uploaded.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->

```http
HTTP/1.1 202 Accepted
Content-Type: application/json

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["26-"]
}
```

<span data-ttu-id="fc966-184">Su aplicación puede usar el valor **nextExpectedRanges** para determinar dónde comenzar el siguiente intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="fc966-184">Your app can use the **nextExpectedRanges** value to determine where to start the next byte range.</span></span>
<span data-ttu-id="fc966-185">Puede ver varios intervalos especificados, lo que indica las partes del archivo que aún no ha recibido el servidor.</span><span class="sxs-lookup"><span data-stu-id="fc966-185">You may see multiple ranges specified, indicating parts of the file that the server has not yet received.</span></span> <span data-ttu-id="fc966-186">Esto resulta útil si necesita reanudar una transferencia que se ha interrumpido y su cliente no está seguro del estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="fc966-186">This is useful if you need to resume a transfer that was interrupted and your client is unsure of the state on the service.</span></span>

<span data-ttu-id="fc966-187">Siempre debe determinar el tamaño de los intervalos de bytes según las siguientes recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="fc966-187">You should always determine the size of your byte ranges according to the best practices below.</span></span> <span data-ttu-id="fc966-188">No suponga que **nextExpectedRanges** devolverá intervalos del tamaño adecuado de un intervalo de bytes de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-188">Do not assume that **nextExpectedRanges** will return reanges of proper size for a byte range to upload.</span></span>
<span data-ttu-id="fc966-189">La propiedad **nextExpectedRanges** indica intervalos del archivo que no se han recibido y no un patrón de cómo debe cargar el archivo la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc966-189">The **nextExpectedRanges** property indicates ranges of the file that have not been received and not a pattern for how your app should upload the file.</span></span>

<!-- { "blockType": "ignored", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->

```http
HTTP/1.1 202 Accepted
Content-Type: application/json

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": [
  "12345-55232",
  "77829-99375"
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="fc966-190">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc966-190">Remarks</span></span>

* <span data-ttu-id="fc966-191">La propiedad `nextExpectedRanges` no siempre enumera todos los intervalos que faltan.</span><span class="sxs-lookup"><span data-stu-id="fc966-191">The `nextExpectedRanges` property won't always list all of the missing ranges.</span></span>
* <span data-ttu-id="fc966-p115">Cuando las escrituras de fragmento se ejecuten correctamente, devolverá el siguiente intervalo desde el que empezar (ej. "523-").</span><span class="sxs-lookup"><span data-stu-id="fc966-p115">On successful fragment writes, it will return the next range to start from (eg. "523-").</span></span>
* <span data-ttu-id="fc966-p116">Cuando se produzcan errores en los que el cliente envíe un fragmento que el servidor ya ha recibido, el servidor responderá `HTTP 416 Requested Range Not Satisfiable`. Puede [solicitar el estado de la carga](#resuming-an-in-progress-upload) para obtener una lista más detallada de los intervalos que faltan.</span><span class="sxs-lookup"><span data-stu-id="fc966-p116">On failures when the client sent a fragment the server had already received, the server will respond with `HTTP 416 Requested Range Not Satisfiable`. You can [request upload status](#resuming-an-in-progress-upload) to get a more detailed list of missing ranges.</span></span>
* <span data-ttu-id="fc966-p117">Incluir el encabezado de autorización al emitir la llamada `PUT` puede resultar en la respuesta `HTTP 401 Unauthorized`. El encabezado de autorización y el token de portador deberían enviarse únicamente al emitir el `POST` durante el primer paso. No debería incluirse al emitir el `PUT`.</span><span class="sxs-lookup"><span data-stu-id="fc966-p117">Including the Authorization header when issuing the `PUT` call may result in a `HTTP 401 Unauthorized` response. The Authorization header and bearer token should only be sent when issuing the `POST` during the first step. It should be not be included when issueing the `PUT`.</span></span>

## <a name="completing-a-file"></a><span data-ttu-id="fc966-199">Finalización de un archivo</span><span class="sxs-lookup"><span data-stu-id="fc966-199">Completing a file</span></span>

<span data-ttu-id="fc966-200">Si `deferCommit` es false o sin establecer, la carga se rellenará automáticamente cuando se coloca el intervalo de bytes final del archivo a la dirección URL de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-200">If `deferCommit` is false or unset, then the upload is automatically completed when the final byte range of the file is PUT to the upload URL.</span></span>
<span data-ttu-id="fc966-201">Si `deferCommit` es true, después de que el intervalo de bytes final del archivo se pone a la dirección URL de carga, la carga que se debe completar explícitamente por una solicitud POST final a la carga de dirección url con el contenido de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="fc966-201">If `deferCommit` is true, then after the final byte range of the file is PUT to the upload URL, the upload should be explicitly completed by a final POST request to the upload url with zero-length content.</span></span>

<span data-ttu-id="fc966-202">Una vez completada la carga, el servidor responderá a la solicitud final con un `HTTP 201 Created` o `HTTP 200 OK`.</span><span class="sxs-lookup"><span data-stu-id="fc966-202">When the upload is completed, the server will respond to the final request with an `HTTP 201 Created` or `HTTP 200 OK`.</span></span>
<span data-ttu-id="fc966-203">El cuerpo de la respuesta incluirá también la propiedad predeterminada establecida del **driveItem** que representa el archivo completo.</span><span class="sxs-lookup"><span data-stu-id="fc966-203">The response body will also include the default property set for the **driveItem** representing the completed file.</span></span>

<!-- { "blockType": "request", "opaqueUrl": true, "name": "upload-fragment-final", "scopes": "files.readwrite" } -->

```
PUT https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337
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


<!-- { "blockType": "request", "opaqueUrl": true, "name": "commit-upload", "scopes": "files.readwrite" } -->

```
POST https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337
Content-Length: 0
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

## <a name="handling-upload-conflicts"></a><span data-ttu-id="fc966-204">Controlar conflictos de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-204">Handling upload conflicts</span></span>

<span data-ttu-id="fc966-205">Si se produce un conflicto después de que se cargue el archivo (por ejemplo, se ha creado un elemento con el mismo nombre durante la sesión de carga), se devuelve un error cuando se carga el último intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="fc966-205">If a conflict occurs after the file is uploaded (for example, an item with the same name was created during the upload session), an error is returned when the last byte range is uploaded.</span></span>

```http
HTTP/1.1 409 Conflict
Content-Type: application/json

{
  "error":
  {
    "code": "upload_name_conflict",
    "message": "Another file exists with the same name as the uploaded session. You can redirect the upload session to use a new filename by calling PUT with the new metadata and @microsoft.graph.sourceUrl attribute.",
  }
}
```

## <a name="cancel-the-upload-session"></a><span data-ttu-id="fc966-206">Cancelar la sesión de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-206">Cancel the upload session</span></span>

<span data-ttu-id="fc966-p120">Para cancelar una sesión de carga, envíe una solicitud DELETE a la dirección URL de carga. Esto limpia el archivo temporal que contiene los datos previamente cargados. Debe utilizarse en los casos en los que se anula la carga, por ejemplo, si el usuario cancela la transferencia.</span><span class="sxs-lookup"><span data-stu-id="fc966-p120">To cancel an upload session send a DELETE request to the upload URL. This cleans up the temporary file holding the data previously uploaded. This should be used in scenarios where the upload is aborted, for example, if the user cancels the transfer.</span></span>

<span data-ttu-id="fc966-210">Los archivos temporales y la sesión de carga que los acompaña se limpian automáticamente cuando pasa la **expirationDateTime**.</span><span class="sxs-lookup"><span data-stu-id="fc966-210">Temporary files and their accompanying upload session are automatically cleaned up after the **expirationDateTime** has passed.</span></span>
<span data-ttu-id="fc966-211">Puede que los archivos temporales no se eliminen inmediatamente después de que haya transcurrido el tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="fc966-211">Temporary files may not be deleted immedately after the expiration time has elapsed.</span></span>

### <a name="request"></a><span data-ttu-id="fc966-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc966-212">Request</span></span>

<!-- { "blockType": "request", "opaqueUrl": true, "name": "upload-fragment-cancel", "scopes": "files.readwrite" } -->

```http
DELETE https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337
```

### <a name="response"></a><span data-ttu-id="fc966-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc966-213">Response</span></span>

<span data-ttu-id="fc966-214">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc966-214">The following example shows the response.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

## <a name="resuming-an-in-progress-upload"></a><span data-ttu-id="fc966-215">Reanudar una carga en curso</span><span class="sxs-lookup"><span data-stu-id="fc966-215">Resuming an in-progress upload</span></span>

<span data-ttu-id="fc966-p122">Si una solicitud de carga se desconecta o si falla antes de que se complete la solicitud, se pasan por alto todos los bytes de dicha solicitud. Esto puede ocurrir si se interrumpe la conexión entre la aplicación y el servicio. Si esto ocurre, la aplicación todavía puede reanudar la transferencia de archivos desde el fragmento completado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fc966-p122">If an upload request is disconnected or fails before the request is completed, all bytes in that request are ignored. This can occur if the connection between your app and the service is dropped. If this occurs, your app can still resume the file transfer from the previously completed fragment.</span></span>

<span data-ttu-id="fc966-219">Para averiguar qué intervalos de bytes se han recibido anteriormente, su aplicación puede solicitar el estado de una sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-219">To find out which byte ranges have been received previously, your app can request the status of an upload session.</span></span>

### <a name="example"></a><span data-ttu-id="fc966-220">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc966-220">Example</span></span>

<span data-ttu-id="fc966-221">Consulte el estado de la carga mediante el envío de una solicitud GET a `uploadUrl`.</span><span class="sxs-lookup"><span data-stu-id="fc966-221">Query the status of the upload by sending a GET request to the `uploadUrl`.</span></span>

<!-- { "blockType": "request", "opaqueUrl": true, "name": "upload-fragment-resume", "scopes": "files.readwrite" } -->

```
GET https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF86633784148bb98a1zjcUhf7b0mpUadahs
```

<span data-ttu-id="fc966-222">El servidor responderá con una lista de los intervalos de bytes que faltan por cargar y la fecha de expiración de la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-222">The server will respond with a list of missing byte ranges that need to be uploaded and the expiration time for the upload session.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["12345-"]
}
```

### <a name="upload-remaining-data"></a><span data-ttu-id="fc966-223">Cargar los datos restantes</span><span class="sxs-lookup"><span data-stu-id="fc966-223">Upload remaining data</span></span>

<span data-ttu-id="fc966-224">Ahora que la aplicación sabe desde dónde iniciar la carga, reanude la carga siguiendo los pasos descritos en [cargar bytes a la sesión de carga](#upload-bytes-to-the-upload-session).</span><span class="sxs-lookup"><span data-stu-id="fc966-224">Now that your app knows where to start the upload from, resume the upload by following the steps in [upload bytes to the upload session](#upload-bytes-to-the-upload-session).</span></span>

## <a name="handle-upload-errors"></a><span data-ttu-id="fc966-225">Controlar errores de carga</span><span class="sxs-lookup"><span data-stu-id="fc966-225">Handle upload errors</span></span>

<span data-ttu-id="fc966-226">Cuando se carga el último intervalo de bytes de un archivo, es posible que ocurra un error.</span><span class="sxs-lookup"><span data-stu-id="fc966-226">When the last byte range of a file is uploaded, it is possible for an error to occur.</span></span> <span data-ttu-id="fc966-227">Esto puede deberse a un conflicto de nombre o a que se ha excedido un límite de cuota.</span><span class="sxs-lookup"><span data-stu-id="fc966-227">This can be due to a name conflict or quota limitation being exceeded.</span></span>
<span data-ttu-id="fc966-228">La sesión de carga se conservará hasta el momento de la expiración, lo que permite que su aplicación recupere la carga al confirmar explícitamente la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-228">The upload session will be preserved until the expiration time, which allows your app to recover the upload by explicitly committing the upload session.</span></span>

<span data-ttu-id="fc966-229">Para confirmar explícitamente la sesión de carga, la aplicación debe realizar una solicitud PUT con un nuevo recurso **driveItem** que se usará al confirmar la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-229">To explicitly commit the upload session, your app must make a PUT request with a new **driveItem** resource that will be used when committing the upload session.</span></span>
<span data-ttu-id="fc966-230">Esta nueva solicitud debería corregir el origen del error que ha generado el error de carga original.</span><span class="sxs-lookup"><span data-stu-id="fc966-230">This new request should correct the source of error that generated the original upload error.</span></span>

<span data-ttu-id="fc966-231">Para indicar que su aplicación está confirmando una sesión de carga existente, la solicitud PUT debe incluir la propiedad `@microsoft.graph.sourceUrl` con el valor de la URL de la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-231">To indicate that your app is committing an existing upload session, the PUT request must include the `@microsoft.graph.sourceUrl` property with the value of your upload session URL.</span></span>

<!-- { "blockType": "ignored", "name": "explicit-upload-commit", "scopes": "files.readwrite", "tags": "service.graph" } -->

```http
PUT /me/drive/root:/{path_to_parent}
Content-Type: application/json
If-Match: {etag or ctag}

{
  "name": "largefile.vhd",
  "@microsoft.graph.conflictBehavior": "rename",
  "@microsoft.graph.sourceUrl": "{upload session URL}"
}
```

<span data-ttu-id="fc966-232">**Nota:** Puede usar los encabezados `@microsoft.graph.conflictBehavior` y `if-match` como se esperaba en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="fc966-232">**Note:** You can use the `@microsoft.graph.conflictBehavior` and `if-match` headers as expected in this call.</span></span>

### <a name="http-response"></a><span data-ttu-id="fc966-233">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="fc966-233">HTTP response</span></span>

<span data-ttu-id="fc966-234">Si el archivo puede confirmarse con los nuevos metadatos, se devolverá una respuesta `HTTP 201 Created` o `HTTP 200 OK` con los metadatos Item para el archivo cargado.</span><span class="sxs-lookup"><span data-stu-id="fc966-234">If the file can be committed using the new metadata, an `HTTP 201 Created` or `HTTP 200 OK` response will be returned with the Item metadata for the uploaded file.</span></span>

<!-- { "blockType": "ignored", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

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

## <a name="best-practices"></a><span data-ttu-id="fc966-235">Procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="fc966-235">Best practices</span></span>

* <span data-ttu-id="fc966-236">Reanude o vuelva a ejecutar las cargas que fallaron debido a las interrupciones de la conexión o a los errores 5xx, como:</span><span class="sxs-lookup"><span data-stu-id="fc966-236">Resume or retry uploads that fail due to connection interruptions or any 5xx errors, including:</span></span>
  * `500 Internal Server Error`
  * `502 Bad Gateway`
  * `503 Service Unavailable`
  * `504 Gateway Timeout`
* <span data-ttu-id="fc966-237">Utilice una estrategia de interrupción exponencial si se devuelve cualquier error 5xx del servidor al reanudar o volver a ejecutar solicitudes de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-237">Use an exponential back off strategy if any 5xx server errors are returned when resuming or retrying upload requests.</span></span>
* <span data-ttu-id="fc966-238">Si hay otros errores, no debe utilizar una estrategia de interrupción exponencial sino limitar el número de reintentos realizados.</span><span class="sxs-lookup"><span data-stu-id="fc966-238">For other errors, you should not use an exponential back off strategy but limit the number of retry attempts made.</span></span>
* <span data-ttu-id="fc966-239">Vuelva a iniciar la carga completa para controla los errores `404 Not Found` al realizar cargas reanudables.</span><span class="sxs-lookup"><span data-stu-id="fc966-239">Handle `404 Not Found` errors when doing resumable uploads by starting the entire upload over.</span></span> <span data-ttu-id="fc966-240">Esto indica que ya no existe la sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="fc966-240">This indicates the upload session no longer exists.</span></span>
* <span data-ttu-id="fc966-241">Use transferencias de archivo reanudables para los archivos de más de 10 MiB (10.485.760 bytes).</span><span class="sxs-lookup"><span data-stu-id="fc966-241">Use resumable file transfers for files larger than 10 MiB (10,485,760 bytes).</span></span>
* <span data-ttu-id="fc966-242">Un tamaño de intervalo de bytes de 10 MiB para conexiones estables de alta velocidad es óptimo.</span><span class="sxs-lookup"><span data-stu-id="fc966-242">A byte range size of 10 MiB for stable high speed connections is optimal.</span></span> <span data-ttu-id="fc966-243">Para conexiones más lentas o menos fiables puede obtener mejores resultados con tamaños de fragmento más pequeños.</span><span class="sxs-lookup"><span data-stu-id="fc966-243">For slower or less reliable connections you may get better results from a smaller fragment size.</span></span> <span data-ttu-id="fc966-244">El tamaño de fragmento recomendado es entre 5 y 10 MiB.</span><span class="sxs-lookup"><span data-stu-id="fc966-244">The recommended fragment size is between 5-10 MiB.</span></span>
* <span data-ttu-id="fc966-245">Use un tamaño de intervalo de bytes que sea múltiplo de 320 KiB (327 680 bytes).</span><span class="sxs-lookup"><span data-stu-id="fc966-245">Use a byte range size that is a multiple of 320 KiB (327,680 bytes).</span></span> <span data-ttu-id="fc966-246">Si no usa un tamaño de fragmento que sea múltiplo de 320 KiB, se puede producir un error en las transferencias de archivos de gran tamaño después de que se cargue el último intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="fc966-246">Failing to use a fragment size that is a multiple of 320 KiB can result in large file transfers failing after the last byte range is uploaded.</span></span>

## <a name="error-responses"></a><span data-ttu-id="fc966-247">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="fc966-247">Error responses</span></span>

<span data-ttu-id="fc966-248">Vea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="fc966-248">See the [Error Responses][error-response] topic for details about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Upload large files using an upload session.",
  "keywords": "upload,large file,fragment,BITS",
  "section": "documentation"
} -->
