# <a name="upload-large-files-with-an-upload-session"></a>Cargar archivos de gran tamaño con una sesión de carga

Cree una sesión de carga para permitir que su aplicación cargue archivos de hasta el tamaño de archivo máximo. Una sesión de carga permite que su aplicación cargue intervalos del archivo en solicitudes API secuenciales, lo que permite que la transferencia se reanude si se interrumpe una conexión mientras la carga está en curso.

Para cargar un archivo mediante una sesión de carga hay que realizar dos pasos:

1. [Crear una sesión de carga](#create-an-upload-session)
2. [Cargar bytes a la sesión de carga](#upload-bytes-to-the-upload-session)

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

* Files.ReadWrite
* Files.ReadWrite.All
* Sites.ReadWrite.All

> **Nota**: El permiso de aplicación Files.ReadWrite.All aún no se admite en esta API. Está prevista la compatibilidad completa próximamente. 

## <a name="create-an-upload-session"></a>Crear una sesión de carga

Para comenzar la carga de archivos de gran tamaño, su aplicación debe solicitar primero una nueva sesión de carga. Esto crea una ubicación de almacenamiento temporal donde se guardarán los bytes del archivo hasta que se cargue el archivo completo. Una vez que se haya cargado el último byte del archivo, termina la sesión de carga y el archivo final se muestra en la carpeta de destino.

### <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root:/{path-to-item}:/createUploadSession
POST /me/drive/items/{parent-item-id}:/{filename}:/createUploadSession
```

### <a name="request-body"></a>Cuerpo de la solicitud
No es necesario ningún cuerpo de solicitud. Sin embargo, puede especificar un cuerpo de la solicitud para proporcionar datos adicionales sobre el archivo que se está cargando.

Por ejemplo, para controlar el comportamiento si ya existe el nombre de archivo, puede especificar la propiedad de comportamiento ante conflictos en el cuerpo de la solicitud.

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


### <a name="response"></a>Respuesta
La respuesta a esta solicitud ofrecerá los detalles de la [uploadSession](../resources/uploadsession.md) recién creada, que incluye la dirección URL utilizada para cargar las partes del archivo. 

### <a name="example"></a>Ejemplo

<!-- {
  "blockType": "request",
  "name": "driveItem_createUploadSession"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root:/{item-path}:/createUploadSession
```

##### <a name="response"></a>Respuesta 

En el ejemplo siguiente se muestra la respuesta.

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

## <a name="upload-bytes-to-the-upload-session"></a>Cargar bytes en la sesión de carga

Para cargar el archivo o una parte del archivo, la aplicación envía una solicitud PUT al valor **uploadUrl** recibido en la respuesta **createUploadSession**. Puede cargar el archivo completo o dividir el archivo en fragmentos, siempre y cuando el número máximo de bytes de cualquier solicitud dada sea inferior a 60 MiB. Los fragmentos del archivo se deben cargar secuencialmente en orden. La carga de fragmentos sin un orden producirá un error.

**Nota:** Si su aplicación divide un archivo en varios fragmentos, el tamaño de cada fragmento **DEBE** ser un múltiplo de 320 KiB. Usar un tamaño de fragmento que no puede dividirse uniformemente por 320 ocasionará errores a la hora de confirmar algunos archivos.

### <a name="example"></a>Ejemplo

Este ejemplo carga los primeros 26 bytes de un archivo de 128 bytes. El encabezado **Content-Length** especifica el tamaño de la solicitud actual. El encabezado **Content-Range** indica el intervalo de bytes en el archivo global que representa esta solicitud. Se debe conocer la longitud total del archivo antes de cargar el primer fragmento del archivo.

<!-- { "blockType": "request", "name": "upload-fragment-piece", "scopes": "files.readwrite" } -->
```
PUT https://tenant-my.sharepoint.com/alkjl1kjklna
Content-Length: 26
Content-Range: bytes 0-25/128

<bytes 0-25 of the file>
```

**Importante:** Su aplicación debe asegurarse de que el tamaño total del archivo especificado en el encabezado **Content-Range** sea el mismo en todas las solicitudes. Si un fragmento indica un tamaño de archivo diferente, se producirá un error en la solicitud.

##### <a name="response"></a>Respuesta

En el ejemplo siguiente se muestra la respuesta.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["26-"]
}
```

Su aplicación puede utilizar el valor **nextExpectedRanges** para determinar dónde comenzar el siguiente fragmento. Puede ver varios intervalos especificados, lo que indica las partes del archivo que aún no ha recibido el servidor. Esto resulta útil si necesita reanudar una transferencia que se ha interrumpido y su cliente no está seguro del estado del servicio.

Siempre debe determinar el tamaño del fragmento según las siguientes recomendaciones. No suponga que **nextExpectedRanges** devolverá intervalos del tamaño adecuado de un fragmento de carga. La propiedad **nextExpectedRanges** indica intervalos del archivo que no se han recibido y no un patrón de cómo debe cargar el archivo.

**Notas**:

* La propiedad `nextExpectedRanges` no siempre enumera todos los intervalos que faltan.
* Cuando las escrituras de fragmento se ejecuten correctamente, devolverá el siguiente intervalo desde el que empezar (ej. "523-").
* Cuando se produzcan errores en los que el cliente envíe un fragmento que el servidor ya ha recibido, el servidor responderá `HTTP 416 Requested Range Not Satisfiable`. Puede [solicitar el estado de la carga](#resuming-an-in-progress-upload) para obtener una lista más detallada de los intervalos que faltan.
* Incluir el encabezado de autorización al emitir la llamada `PUT` puede resultar en la respuesta `HTTP 401 Unauthorized`. El encabezado de autorización y el token de portador deberían enviarse únicamente al emitir el `POST` durante el primer paso. No debería incluirse al emitir el `PUT`.   


## <a name="completing-a-file"></a>Finalización de un archivo

Cuando se reciba el último fragmento de un archivo, el servidor responderá `HTTP 201 Created` o `HTTP 200 OK`. El cuerpo de la respuesta incluirá también la propiedad predeterminada establecida del **driveItem** que representa el archivo completo.

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
**Nota:** La respuesta del elemento está truncada para que la documentación sea más clara.

## <a name="cancel-an-upload-session"></a>Cancelar una sesión de carga

Para cancelar una sesión de carga, envíe una solicitud DELETE a la dirección URL de carga. Esto limpia el archivo temporal que contiene los datos previamente cargados. Debe utilizarse en los casos en los que se anula la carga, por ejemplo, si el usuario cancela la transferencia.

Los archivos temporales y la sesión de carga que los acompaña se limpian automáticamente cuando pasa la **expirationDateTime**.

### <a name="example"></a>Ejemplo

La solicitud DELETE hará que la sesión de carga expire inmediatamente y eliminará los bytes cargados previamente.

<!-- { "blockType": "request", "name": "upload-fragment-cancel", "scopes": "files.readwrite" } -->
```http
DELETE https://tenant-my.sharepoint.com/alkjl1kjklna
```

##### <a name="response"></a>Respuesta 

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

<!-- { "blockType": "request", "name": "upload-fragment-resume", "scopes": "files.readwrite" } -->
```
GET https://tenant-my.sharepoint.com/alkjl1kjklna
```

El servidor responderá con una lista de los intervalos de bytes que faltan por cargar y la fecha de expiración de la sesión de carga.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.uploadSession", "truncated": true } -->
```http
HTTP/1.1 200 OK

{
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["12345-"]
}
```

### <a name="upload-remaining-data"></a>Cargar los datos restantes
Ahora que la aplicación sabe desde dónde iniciar la carga, reanude la carga siguiendo los pasos descritos en [cargar bytes a la sesión de carga](#upload-bytes-to-the-upload-session).


## <a name="best-practices"></a>Procedimientos recomendados

* Reanude o vuelva a ejecutar las cargas que fallaron debido a las interrupciones de la conexión o a los errores 5xx, como:
  * `500 Internal Server Error`
  * `502 Bad Gateway`
  * `503 Service Unavailable`
  * `504 Gateway Timeout`
* Utilice una estrategia de interrupción exponencial si se devuelve cualquier error 5xx del servidor al reanudar o volver a ejecutar solicitudes de carga.
* Si hay otros errores, no debe utilizar una estrategia de interrupción exponencial sino limitar el número de reintentos realizados.
* Controle los errores `404 Not Found` al realizar cargas reanudables volviendo a iniciar la carga completa.
* Utilice transferencias de archivo reanudables para los archivos de más de 10 MiB (10 \* 1024 \* 1024 bytes).
* Un tamaño de fragmento de 10 MiB para conexiones estables de alta velocidad es óptimo. Para conexiones más lentas o menos fiables puede obtener mejores resultados con tamaños de fragmento más pequeños. El tamaño de fragmento recomendado es entre 5 y 10 MiB.
* Utilice un tamaño de fragmento que sea múltiplo de 320 KiB (320 \* 1024 bytes). Si no utiliza un tamaño de fragmento que sea múltiplo de 320 KiB, las transferencias de archivos de gran tamaño pueden fallar después de que se cargue el último fragmento.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Upload item",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
