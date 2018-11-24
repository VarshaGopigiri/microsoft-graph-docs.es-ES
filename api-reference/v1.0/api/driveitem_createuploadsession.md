---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carga de archivos reanudable
ms.openlocfilehash: 14b9047f84b5390aea2f5285660e6c04a6bc3149
ms.sourcegitcommit: ebac77d2ca32438e552831de0258fe5e86fa225a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2018
ms.locfileid: "26564761"
---
# <a name="upload-large-files-with-an-upload-session"></a>Cargar archivos de gran tamaño con una sesión de carga

Cree una sesión de carga para permitir que la aplicación cargue archivos de hasta el tamaño de archivo máximo. Una sesión de carga permite que la aplicación cargue intervalos del archivo en solicitudes API secuenciales, lo que permite que la transferencia se reanude si se interrumpe una conexión mientras la carga está en curso.

Para cargar un archivo mediante una sesión de carga hay que realizar dos pasos:

1. [Crear una sesión de carga](#create-an-upload-session)
2. [Cargar bytes a la sesión de carga](#upload-bytes-to-the-upload-session)

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Sites.ReadWrite.All |

## <a name="create-an-upload-session"></a>Crear una sesión de carga

Para comenzar la carga de archivos de gran tamaño, su aplicación debe solicitar primero una nueva sesión de carga. Esto crea una ubicación de almacenamiento temporal donde se guardarán los bytes del archivo hasta que se cargue el archivo completo. Una vez que se haya cargado el último byte del archivo, termina la sesión de carga y el archivo final se muestra en la carpeta de destino.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/createUploadSession
POST /groups/{groupId}/drive/items/{itemId}/createUploadSession
POST /me/drive/items/{itemId}/createUploadSession
POST /sites/{siteId}/drive/items/{itemId}/createUploadSession
POST /users/{userId}/drive/items/{itemId}/createUploadSession
```

### <a name="request-body"></a>Cuerpo de la solicitud

No es necesario ningún cuerpo de solicitud.
Sin embargo, puede especificar un `item` (propiedad) en el cuerpo de la solicitud, que proporciona datos adicionales sobre el archivo que se está cargando.

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.driveItemUploadableProperties" } -->
```json
{
  "@microsoft.graph.conflictBehavior": "rename | fail | replace",
  "description": "description",
  "fileSystemInfo": { "@odata.type": "microsoft.graph.fileSystemInfo" },
  "name": "filename.txt"
}
```

Por ejemplo, para controlar el comportamiento si ya existe el nombre de archivo, puede especificar la propiedad de comportamiento ante conflictos en el cuerpo de la solicitud.

<!-- { "blockType": "ignored" } -->
```json
{
  "item": {
    "@microsoft.graph.conflictBehavior": "rename"
  }
}
```

### <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre       | Valor | Descripción                                                                                                                                                            |
|:-----------|:------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *if-match* | etag  | Si se incluye este encabezado de solicitud y la eTag (o cTag) proporcionada no coincide con la eTag actual en el elemento, se devuelve una respuesta de error `412 Precondition Failed`. |

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo               | Descripción
|:---------------------|:-------------------|:---------------------------------
| description          | String             | Proporciona una descripción del elemento visible para el usuario. Lectura y escritura. Solo en OneDrive Personal
| fileSystemInfo       | [fileSystemInfo][] | Información del sistema de archivos del cliente. Lectura y escritura.
| name                 | String             | El nombre del elemento (nombre de archivo y extensión). Lectura y escritura.

### <a name="request"></a>Solicitud

La respuesta a esta solicitud ofrecerá los detalles de la [uploadSession](../resources/uploadsession.md) recién creada, que incluye la dirección URL utilizada para cargar las partes del archivo. 

<!-- { "blockType": "request", "name": "upload-fragment-create-session", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /me/drive/root:/{item-path}:/createUploadSession
Content-Type: application/json

{
  "item": {
    "@odata.type": "microsoft.graph.driveItemUploadableProperties",
    "@microsoft.graph.conflictBehavior": "rename",
    "name": "largefile.dat"
  }
}
```

### <a name="response"></a>Respuesta

La respuesta a esta solicitud, si se realiza correctamente, proporcionará los detalles sobre dónde deben enviarse el resto de las solicitudes como un recurso [UploadSession](../resources/uploadSession.md).

Este recurso proporciona detalles sobre dónde debe cargarse el intervalo de bytes del archivo y cuándo expira la sesión de carga.

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

## <a name="upload-bytes-to-the-upload-session"></a>Cargar bytes en la sesión de carga

Para cargar el archivo o una parte del archivo, la aplicación envía una solicitud PUT al valor **uploadUrl** recibido en la respuesta **createUploadSession**.
Puede cargar el archivo completo o dividir el archivo en varios intervalos de bytes, siempre y cuando el número máximo de bytes de cualquier solicitud dada sea inferior a 60 MiB.

Los fragmentos del archivo se deben cargar secuencialmente en orden.
La carga de fragmentos sin un orden producirá un error.

**Nota:** Si su aplicación divide un archivo en varios intervalos de bits, el tamaño de cada uno **DEBE** ser un múltiplo de 320 KiB (327 680 bytes). Usar un tamaño de fragmento que no puede dividirse uniformemente por 320 KiB ocasionará errores a la hora de confirmar algunos archivos.

### <a name="example"></a>Ejemplo

En este ejemplo, la aplicación carga los primeros 26 bytes de un archivo de 128 bytes.

* El encabezado **Content-Length** especifica el tamaño de la solicitud actual.
* El encabezado **Content-Range** indica el intervalo de bytes en el archivo global que representa esta solicitud.
* La longitud total del archivo se conoce antes de cargar el primer fragmento del archivo.

<!-- { "blockType": "request", "opaqueUrl": true, "name": "upload-fragment-piece", "scopes": "files.readwrite" } -->

```http
PUT https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337
Content-Length: 26
Content-Range: bytes 0-25/128

<bytes 0-25 of the file>
```

**Importante:** Su aplicación debe asegurarse de que el tamaño total del archivo especificado en el encabezado **Content-Range** sea el mismo en todas las solicitudes.
Si un intervalo de bytes indica un tamaño de archivo diferente, se producirá un error en la solicitud.

### <a name="response"></a>Respuesta

Cuando se complete la solicitud, el servidor responderá con `202 Accepted` si existen más intervalos de bytes que necesitan cargarse.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->

```http
HTTP/1.1 202 Accepted
Content-Type: application/json

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["26-"]
}
```

Su aplicación puede usar el valor **nextExpectedRanges** para determinar dónde comenzar el siguiente intervalo de bytes.
Puede ver varios intervalos especificados, lo que indica las partes del archivo que aún no ha recibido el servidor. Esto resulta útil si necesita reanudar una transferencia que se ha interrumpido y su cliente no está seguro del estado del servicio.

Siempre debe determinar el tamaño de los intervalos de bytes según las siguientes recomendaciones. No suponga que **nextExpectedRanges** devolverá intervalos del tamaño adecuado de un intervalo de bytes de carga.
La propiedad **nextExpectedRanges** indica intervalos del archivo que no se han recibido y no un patrón de cómo debe cargar el archivo la aplicación.

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

## <a name="remarks"></a>Comentarios

* La propiedad `nextExpectedRanges` no siempre enumera todos los intervalos que faltan.
* Cuando las escrituras de fragmento se ejecuten correctamente, devolverá el siguiente intervalo desde el que empezar (ej. "523-").
* Cuando se produzcan errores en los que el cliente envíe un fragmento que el servidor ya ha recibido, el servidor responderá `HTTP 416 Requested Range Not Satisfiable`. Puede [solicitar el estado de la carga](#resuming-an-in-progress-upload) para obtener una lista más detallada de los intervalos que faltan.
* Incluir el encabezado de autorización al emitir la llamada `PUT` puede resultar en la respuesta `HTTP 401 Unauthorized`. El encabezado de autorización y el token de portador deberían enviarse únicamente al emitir el `POST` durante el primer paso. No debería incluirse al emitir el `PUT`.

## <a name="completing-a-file"></a>Finalización de un archivo

Cuando se reciba el último intervalo de bytes de un archivo, el servidor responderá `HTTP 201 Created` o `HTTP 200 OK`.
El cuerpo de la respuesta incluirá también la propiedad predeterminada establecida del **driveItem** que representa el archivo completo.

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

## <a name="handling-upload-conflicts"></a>Controlar conflictos de carga

Si se produce un conflicto después de que se cargue el archivo (por ejemplo, se ha creado un elemento con el mismo nombre durante la sesión de carga), se devuelve un error cuando se carga el último intervalo de bytes.

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

## <a name="cancel-the-upload-session"></a>Cancelar la sesión de carga

Para cancelar una sesión de carga, envíe una solicitud DELETE a la dirección URL de carga. Esto limpia el archivo temporal que contiene los datos previamente cargados. Debe utilizarse en los casos en los que se anula la carga, por ejemplo, si el usuario cancela la transferencia.

Los archivos temporales y la sesión de carga que los acompaña se limpian automáticamente cuando pasa la **expirationDateTime**.
Puede que los archivos temporales no se eliminen inmediatamente después de que haya transcurrido el tiempo de expiración.

### <a name="request"></a>Solicitud

<!-- { "blockType": "request", "opaqueUrl": true, "name": "upload-fragment-cancel", "scopes": "files.readwrite" } -->

```http
DELETE https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337
```

### <a name="response"></a>Respuesta

En el ejemplo siguiente se muestra la respuesta.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

## <a name="resuming-an-in-progress-upload"></a>Reanudar una carga en curso

Si una solicitud de carga se desconecta o si falla antes de que se complete la solicitud, se pasan por alto todos los bytes de dicha solicitud. Esto puede ocurrir si se interrumpe la conexión entre la aplicación y el servicio. Si esto ocurre, la aplicación todavía puede reanudar la transferencia de archivos desde el fragmento completado anteriormente.

Para averiguar qué intervalos de bytes se han recibido anteriormente, su aplicación puede solicitar el estado de una sesión de carga.

### <a name="example"></a>Ejemplo

Consulte el estado de la carga mediante el envío de una solicitud GET a `uploadUrl`.

<!-- { "blockType": "request", "opaqueUrl": true, "name": "upload-fragment-resume", "scopes": "files.readwrite" } -->

```
GET https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF86633784148bb98a1zjcUhf7b0mpUadahs
```

El servidor responderá con una lista de los intervalos de bytes que faltan por cargar y la fecha de expiración de la sesión de carga.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["12345-"]
}
```

### <a name="upload-remaining-data"></a>Cargar los datos restantes

Ahora que la aplicación sabe desde dónde iniciar la carga, reanude la carga siguiendo los pasos descritos en [cargar bytes a la sesión de carga](#upload-bytes-to-the-upload-session).

## <a name="handle-upload-errors"></a>Controlar errores de carga

Cuando se carga el último intervalo de bytes de un archivo, es posible que ocurra un error. Esto puede deberse a un conflicto de nombre o a que se ha excedido un límite de cuota.
La sesión de carga se conservará hasta el momento de la expiración, lo que permite que su aplicación recupere la carga al confirmar explícitamente la sesión de carga.

Para confirmar explícitamente la sesión de carga, la aplicación debe realizar una solicitud PUT con un nuevo recurso **driveItem** que se usará al confirmar la sesión de carga.
Esta nueva solicitud debería corregir el origen del error que ha generado el error de carga original.

Para indicar que su aplicación está confirmando una sesión de carga existente, la solicitud PUT debe incluir la propiedad `@microsoft.graph.sourceUrl` con el valor de la URL de la sesión de carga.

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

**Nota:** Puede usar los encabezados `@microsoft.graph.conflictBehavior` y `if-match` como se esperaba en esta llamada.

### <a name="http-response"></a>Respuesta HTTP

Si el archivo puede confirmarse con los nuevos metadatos, se devolverá una respuesta `HTTP 201 Created` o `HTTP 200 OK` con los metadatos Item para el archivo cargado.

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

## <a name="best-practices"></a>Procedimientos recomendados

* Reanude o vuelva a ejecutar las cargas que fallaron debido a las interrupciones de la conexión o a los errores 5xx, como:
  * `500 Internal Server Error`
  * `502 Bad Gateway`
  * `503 Service Unavailable`
  * `504 Gateway Timeout`
* Utilice una estrategia de interrupción exponencial si se devuelve cualquier error 5xx del servidor al reanudar o volver a ejecutar solicitudes de carga.
* Si hay otros errores, no debe utilizar una estrategia de interrupción exponencial sino limitar el número de reintentos realizados.
* Vuelva a iniciar la carga completa para controla los errores `404 Not Found` al realizar cargas reanudables. Esto indica que ya no existe la sesión de carga.
* Use transferencias de archivo reanudables para los archivos de más de 10 MiB (10.485.760 bytes).
* Un tamaño de intervalo de bytes de 10 MiB para conexiones estables de alta velocidad es óptimo. Para conexiones más lentas o menos fiables puede obtener mejores resultados con tamaños de fragmento más pequeños. El tamaño de fragmento recomendado es entre 5 y 10 MiB.
* Use un tamaño de intervalo de bytes que sea múltiplo de 320 KiB (327 680 bytes). Si no usa un tamaño de fragmento que sea múltiplo de 320 KiB, se puede producir un error en las transferencias de archivos de gran tamaño después de que se cargue el último intervalo de bytes.

## <a name="error-responses"></a>Respuestas de error

Vea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: ../../../concepts/errors.md
[item-resource]: ../resources/driveitem.md
[fileSystemInfo]: ../resources/filesysteminfo.md

<!-- {
  "type": "#page.annotation",
  "description": "Upload large files using an upload session.",
  "keywords": "upload,large file,fragment,BITS",
  "suppressions": [
    "Warning: /api-reference/v1.0/api/driveitem_createuploadsession.md:
      Found potential enums in resource example that weren't defined in a table:(rename,fail,replace) are in resource, but () are in table"
  ],
  "section": "documentation"
} -->
