# <a name="error-codes-for-onenote-apis-in-microsoft-graph"></a>Códigos de error de las API de OneNote en Microsoft Graph

Este artículo describe los códigos de error que devuelven las API de OneNote en Microsoft Graph cuando se produce un error en una solicitud enviada a través de la API.

## <a name="error-response-example"></a>Ejemplo de respuesta de error
Cuando la solicitud genera un error, la API de OneNote deja de realizar la solicitud y devuelve una respuesta de error como un objeto JSON. Una respuesta de error contiene el código de error asociado, un mensaje y un vínculo a la sección correspondiente en este artículo. El ejemplo siguiente muestra el aspecto de una respuesta de error.

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

Para obtener más información sobre los errores de Microsoft Graph, consulte [Respuestas de error de Microsoft Graph y tipos de recursos](errors.md).

## <a name="codes-from-10001-to-19999"></a>Códigos de 10001 a 19999
El servicio tiene problemas o está enviando información a la aplicación.

### <a name="10001"></a>10001
Se produjo un error inesperado y la solicitud ha fallado.

### <a name="10002"></a>10002
El servicio no está disponible en este momento.

### <a name="10003"></a>10003
La cuenta de usuario actual ha superado el número máximo de solicitudes activas. La aplicación tendrá que repetir la solicitud.

### <a name="10004"></a>10004
El servicio no puede crear una página en la sección solicitada porque la sección está protegida por contraseña.

### <a name="10005"></a>10005
La solicitud contiene más del número máximo de etiquetas de imagen en las que el atributo **data-render-src** contiene un PDF. Vea [Agregar imágenes y archivos](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-images-files).

### <a name="10006"></a>10006
La API de OneNote no pudo crear una página en la sección especificada porque esta sección está dañada.

### <a name="10007"></a>10007
El servidor está demasiado ocupado para atender la solicitud entrante en este momento. Inténtelo de nuevo más tarde.

### <a name="10008"></a>10008
Uno o más de las bibliotecas de documentos en OneDrive del usuario o del grupo contiene más de 5000 elementos de OneNote (blocs de notas, secciones, grupos de secciones) y no se puede consultar mediante la API. Asegúrese de que ninguna de las bibliotecas de documentos del grupo o del usuario contiene más de 5000 elementos de OneNote. Consulte el [blog de desarrollo de OneNote](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) para conocer los pasos de mitigación.

### <a name="10012"></a>10012
No se puede crear o actualizar la entidad porque la biblioteca que contiene el bloc de notas requiere que los elementos estén desprotegidos para poder modificarlos. Para obtener más información, consulte https://support.office.com/es-es/article/Configure-a-site-library-to-require-check-out-of-files-f63fcbdc-1db6-4eb7-a3eb-dd815500c9e7.

Quite el requisito de desprotección de la biblioteca o mueva el bloc de notas.

### <a name="10013"></a>10013
Uno o más de las bibliotecas de documentos en OneDrive del usuario o del grupo contiene más de 20 000 elementos y no se puede indexar para realizar consultas mediante la API. Asegúrese de que ninguna de las bibliotecas de documentos del grupo o del usuario contiene más de 20 000 elementos. Consulte el [blog de desarrollo de OneNote](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) para conocer los pasos de mitigación.

### <a name="10014"></a>10014
Azure Key Vault está demasiado ocupado para atender la solicitud entrante en este momento. Inténtelo de nuevo más tarde.

### <a name="10015"></a>10015
SharePoint no está disponible actualmente. Inténtelo de nuevo más tarde.

### <a name="10016"></a>10016
La biblioteca de documentos en OneDrive del usuario o del grupo superó el límite de umbral de ámbitos de seguridad único. El número máximo de ámbitos de seguridad únicos establecidos para una biblioteca no debe exceder de 50 000.

### <a name="10017"></a>10017
Solicitud incorrecta (Bad Request)

### <a name="19999"></a>19999
Ha habido un error en la solicitud porque se produjo un error sin determinar.

## <a name="codes-from-20001-to-29999"></a>Códigos de 20001 a 29999
El código de la aplicación ha hecho algo mal.

### <a name="20001"></a>20001

Falta la parte "Presentación", necesaria en la solicitud. Se necesita exactamente una. 

### <a name="20002"></a>20002
La solicitud contiene dos o más partes "Presentación". Se necesita exactamente una.

### <a name="20003"></a>20003
El tipo de contenido de la parte "Presentación" puede ser solo texto/HTML o aplicación/XHTML+XML. 

### <a name="20004"></a>20004
El HTML de la parte "Presentación" contiene una etiqueta de imagen con ambos conjuntos de propiedades: **src** y **data-render-src**. La API omitirá la propiedad **src** y usará la propiedad **data-render-src**. 

### <a name="20005"></a>20005
El URI de la solicitud es demasiado largo. El tamaño máximo del URI (incluyendo todos los parámetros y datos) es de 16 KB o 16 384 caracteres.

### <a name="20006"></a>20006
El HTML de la parte "Presentación" contiene una etiqueta de imagen sin los conjuntos de propiedades src o **data-render-src**. La API omitirá la etiqueta **imagen**. 

### <a name="20007"></a>20007
El código HTML de la parte "Presentation" contiene una cadena de fecha y hora de creación que no coincide con ninguno de los formatos permitidos. 

### <a name="20008"></a>20008
El tamaño de la solicitud es demasiado grande. 

### <a name="20009"></a>20009
La solicitud contiene partes con nombres duplicados. Los nombres de las partes deben ser únicos. 

### <a name="20010"></a>20010
No se proporcionó el encabezado Content-Disposition para el tipo de contenido especificado. 

### <a name="20011"></a>20011
La solicitud contiene una carga de varias partes con formato incorrecto. Entre los problemas se incluyen la falta de líneas en blanco, falta de la última línea, separadores de partes con formato incorrecto, etc. Si va a crear el mensaje de varias partes a mano, revise cuidadosamente la lógica o considere el uso de una biblioteca de terceros. 

### <a name="20012"></a>20012
La solicitud no proporciona un tipo de contenido para la parte especificada. 
### <a name="20013"></a>20013
La solicitud no proporciona los encabezados Content-Type y Content-Disposition para la parte especificada. 

### <a name="20014"></a>20014
La longitud de una parte en el mensaje de varias partes supera el tamaño máximo de 25 MB. 

### <a name="20015"></a>20015
El recuento de partes en el mensaje de varias partes supera el límite de 500. 

### <a name="20016"></a>20016
La longitud del mensaje de varias partes supera el límite de 75 MB. 

### <a name="20017"></a>20017
El correo electrónico MIME está mal formado. 

### <a name="20018"></a>20018
La reunión MIME o ICal está mal formada. 

### <a name="20019"></a>20019
No se ha encontrado ningún ICal. 

### <a name="20020"></a>20020
Se encontró JSON con formato incorrecto en el cuerpo de la solicitud. 

### <a name="20100"></a>20100
Hay algún fallo en la sintaxis de su solicitud. 
### <a name="20101"></a>20101
La propiedad que ha solicitado no existe.

### <a name="20102"></a>20102
Ha solicitado un recurso que no existe.

### <a name="20103"></a>20103
La consulta **expand** no se admite para esta solicitud. Vea [Opciones de cadena de consultas OData admitidas](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-get-content#query-options).

### <a name="20104"></a>20104
La opción de consulta **pagelevel** solo se admite al realizar consultas para la colección de páginas de una sección o de una página específica. Por ejemplo:  

```http
GET ../sections/{id}/pages?pagelevel=true
GET ../pages/{id}?pagelevel=true
```

### <a name="20106"></a>20106
La solicitud contiene un operador de consulta que no es compatible. 

### <a name="20108"></a>20108
La solicitud contiene parámetros de consulta de OData no compatibles.

### <a name="20109"></a>20109
La carga útil de la solicitud PATCH no se ha creado correctamente.

### <a name="20110"></a>20110
Las solicitudes de creación de la página con partes de datos requieren que el contenido tenga varias partes, con una parte "Presentación". 

### <a name="20111"></a>20111
La solicitud usa una característica de OData que no es compatible.

### <a name="20112"></a>20112
Su solicitud contiene un identificador no válido para el bloc de notas de destino, el grupo de sección, la sección o la entidad de la página.

### <a name="20113"></a>20113
Se ha eliminado el recurso especificado en la solicitud.

### <a name="20115"></a>20115
El nombre contiene caracteres no válidos. El nombre de un bloc de notas no puede contener ninguno de los siguientes caracteres: `? * \ / : < > | ' "`

### <a name="20117"></a>20117
Ya existe un elemento con el nombre especificado en la ubicación indicada.

### <a name="20119"></a>20119
El código HTML de la parte "Presentation" contiene un atributo **data-attachment** que no tiene un formato válido o que incluye uno o varios de estos caracteres no válidos para un nombre de archivo: `\ / : * ? < > | "`. La solicitud sustituye el valor indicado en el mensaje de error.

### <a name="20120"></a>20120
Su solicitud especifica un destino PATCH que no se encuentra.

### <a name="20121"></a>20121
La solicitud contiene un argumento PATCH no válido. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20122"></a>20122
La solicitud especifica una acción PATCH no compatible. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20123"></a>20123
La solicitud PATCH no puede modificar la página especificada.

### <a name="20124"></a>20124
La solicitud PATCH de varias partes no incluye una parte "commands" con la estructura JSON de la acción PATCH. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20125"></a>20125
La solicitud PATCH no contiene acciones. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20126"></a>20126
El cuerpo del mensaje contiene JSON con un formato incorrecto o campos que no son compatibles con esta operación.

### <a name="20127"></a>20127
La solicitud especifica el nombre de una propiedad desconocida.

### <a name="20128"></a>20128
La solicitud contiene un error de sintaxis de OData en la posición indicada en el mensaje.

### <a name="20129"></a>20129
La solicitud contiene una opción de la cadena de consulta **top** cuyo valor es demasiado alto. Para las consultas de páginas, el valor máximo es 100 y el valor predeterminado es 20.

### <a name="20130"></a>20130
La solicitud contiene un URI que apunta a un recurso de HTTP que no se encuentra.

### <a name="20131"></a>20131
La solicitud contiene un valor no válido para Content-Type. Use el valor indicado en el mensaje. 

### <a name="20132"></a>20132
Su solicitud incluye contenido no válido. Las causas comunes son la falta de un encabezado Content-Type o un cuerpo de la solicitud sin contenido. 

### <a name="20133"></a>20133
Su solicitud especifica un destino PATCH que no es compatible. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20134"></a>20134
La solicitud especifica un elemento no válido como destino de la acción PATCH. Si el destino usa el identificador **data-id**, asegúrese de que tiene el prefijo con el símbolo #. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20135"></a>20135
Su solicitud especifica un tipo de entidad que no es compatible con la operación PATCH. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20136"></a>20136
La solicitud contiene un atributo **data-render-src** o **data-render-method** no válido o que falta. Vea [Extraer los datos de las capturas](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-extract-data).

### <a name="20137"></a>20137
La página de destino no admite solicitudes PATCH.

### <a name="20138"></a>20138
El tipo de elemento de destino de la solicitud PATCH no admite la acción **append** especificada. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20139"></a>20139
La solicitud contiene un valor de atributo **data-tag** no válido. Vea [Uso de etiquetas de nota](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-note-tags).

### <a name="20140"></a>20140
La solicitud contiene un valor de estado **data-tag** no válido. Las etiquetas de nota de casillas pueden tener un estado **completed**. Ejemplo:
```html
    <p data-tag="to-do:completed">To-do note tag in completed state (checked box in the UI)</p>
```
Vea [Uso de etiquetas de nota](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-note-tags).

### <a name="20141"></a>20141
El destino de la solicitud PATCH no admite la acción especificada. Vea [Actualizar contenido de la página](../api-reference/v1.0/api/page_update.md).

### <a name="20142"></a>20142
La solicitud contiene una expresión **expand** para un elemento primario de entidades secundarias o un elemento secundario de entidades primarias, lo cual no es compatible. Vea [Opciones de cadena de consultas OData admitidas](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-get-content#query-options).

### <a name="20143"></a>20143
La consulta OData no es válida.

### <a name="20144"></a>20144
La solicitud contiene una expresión **expand** para una propiedad de no navegación. Únicamente se pueden expandir las propiedades de navegación.

### <a name="20145"></a>20145
La expresión **select** o **expand** de la solicitud contiene un término no válido.

### <a name="20146"></a>20146
El atributo `style="position:absolute"` se especifica en un elemento, pero el elemento **body** no especifica `data-absolute-enabled="true"`, que es necesario para admitir el posicionamiento. Se omitirán todas las configuraciones de posición. Vea [Crear elementos con posición absoluta](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos).

### <a name="20147"></a>20147
El atributo `style="position:absolute"` se especifica en un elemento que no es un elemento secundario directo del elemento **body**, que no es compatible. Si el elemento es un **div**, **img **u **object**, haga que sea un elemento secundario directo del cuerpo; en caso contrario, se pasarán por alto los valores de posición y representará su contenido dentro de un div de posición absoluta Vea [Crear elementos con posición absoluta](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos).

### <a name="20148"></a>20148
El atributo `style="position:absolute"` se especifica en un tipo de elemento que no es compatible. Solo **div**, **img** y **object** admiten la posición de los elementos que son elementos secundarios directos del cuerpo de la página. Vea [Crear elementos con posición absoluta](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos).

### <a name="20149"></a>20149
Su solicitud especifica un elemento de destino que no se encuentra.

### <a name="20150"></a>20150
La solicitud no es válida para este tipo de autenticación. Use la ruta de acceso `../me/onenote/` en su lugar.

### <a name="20151"></a>20151
La solicitud no es válida para este tipo de autenticación. Use el punto de conexión `../me/onenote/section/{id}/pages` para crear una página en una sección específica.

### <a name="20152"></a>20152
No hay ningún valor name especificado para la entidad. Debe definirse el nombre y no puede contener únicamente espacios en blanco.

### <a name="20153"></a>20153
El nombre de la entidad contiene caracteres no válidos. El nombre de la organización no puede contener los siguientes caracteres: `? * \ / : < > | & # " % ~`

### <a name="20154"></a>20154
El nombre de la entidad no puede comenzar con un espacio.

### <a name="20155"></a>20155
El nombre de entidad es demasiado largo. Los nombres de los blocs de notas tienen un límite de 128 caracteres. Los nombres de otras entidades tienen un límite de 50 caracteres.

### <a name="20156"></a>20156
El identificador especificado para el recurso de destino no existe.

### <a name="20157"></a>20157
El identificador especificado para la entidad de destino no es válido.

### <a name="20158"></a>20158
No se pueden obtener los metadatos de la dirección URL del sitio especificada en la solicitud. Compruebe el formato de la dirección URL suministrada. Los formatos admitidos son `https://domain.sharepoint.com/site-a` y `https://domain.com/sites/site-a`.

### <a name="20160"></a>20160
No se puede encontrar un grupo unificado de Office 365 con el identificador especificado.

### <a name="20161"></a>20161
El contexto no especifica ningún Id. de usuario válido. Un error frecuente es que PUID/CID se ha pasado como un long en lugar de un hex.

### <a name="20166"></a>20166
La aplicación ha emitido demasiadas solicitudes en nombre de un usuario en un corto período de tiempo. Para ayudar a garantizar que la API de OneNote permanece estable y con capacidad de respuesta, la API devuelve un código de estado 429 y este error cuando detecta que una aplicación está usando demasiados recursos. 

Para obtener más información, consulte [OneNote API throttling and how to avoid it](http://blogs.msdn.com/b/onenotedev/archive/2016/01/13/onenote-api-throttling-and-best-practices.aspx) (Limitación de la API de OneNote y cómo evitarla).

### <a name="20168"></a>20168
No se admite el origen de vídeo especificado en la solicitud. Vea [Sitios de vídeo compatibles](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-images-files#videos) para obtener la lista actual.


## <a name="codes-from-30001-to-39999"></a>Códigos de 30001 a 39999
Hay algún fallo en la cuenta del usuario.

### <a name="30101"></a>30101
La cuenta de usuario ha excedido su cuota de OneDrive. Vea [OneDrive](https://onedrive.live.com/about/en-us/).

### <a name="30102"></a>30102
No se puede agregar nada más a la sección solicitada porque ha alcanzado su tamaño máximo.

### <a name="30103"></a>30103
El consumo de recursos es demasiado alto para la solicitud. La cuenta de usuario de destino tiene un gran conjunto de datos o el servicio está recibiendo un gran número de solicitudes simultáneas para el mismo sitio (por ejemplo, el sitio personal del usuario o un sitio de grupo).

### <a name="30104"></a>30104
Se ha suspendido la cuenta de usuario.

### <a name="30105"></a>30105
No se ha aprovisionado el OneDrive for Business del usuario, que es necesario para los portátiles de acceso. El servicio de OneNote aprovisionará el sitio ahora. Este proceso puede tardar varios minutos.

### <a name="30106"></a>30106
OneDrive for Business se está aprovisionando para el usuario.

### <a name="30108"></a>30108
No se pudo recuperar el OneDrive for Business personal del usuario. En la tabla siguiente se enumeran algunas causas posibles.

| Motivo | Solución |
|:------|:------|
| No se ha aprovisionado el sitio personal del usuario. | El usuario debe abrir OneDrive for Business y seguir las instrucciones para crear el sitio. Si esto no funciona, deben ponerse en contacto con su administrador de inquilinos de Office 365. |
| Actualmente se está aprovisionando el sitio personal del usuario. | Intente de nuevo la solicitud más tarde. |
| El usuario no tiene un OneDrive válido para la licencia de la empresa. | El usuario debe ponerse en contacto con su administrador de inquilinos de Office 365. |
| Un problema de red ha impedido que la solicitud se enviase correctamente. | Intente de nuevo la solicitud más tarde. |

### <a name="30109"></a>30109
No existen algunos usuarios de la solicitud.

### <a name="30110"></a>30110
Los servicios de información de alumno no se han registrado para este arrendatario.

### <a name="30111"></a>30111
Hay un error genérico con los servicios de información del alumno.

### <a name="30112"></a>30112
Varios usuarios afectados por la solicitud tenían el mismo nombre de usuario.

### <a name="30113"></a>30113
El bloc de notas no está configurado para permitir invitaciones.

### <a name="30114"></a>30114
Falta un parámetro necesario.

## <a name="codes-from-40001-to-49999"></a>Códigos de 40001 a 49999
El usuario o la aplicación no tienen los permisos correctos.

### <a name="40001"></a>40001
La solicitud no contiene un token válido de OAuth. Vea [Permisos de notas](permissions_reference.md#notes-permissions).

### <a name="40002"></a>40002
El usuario no tiene permiso para escribir en la ubicación solicitada.

### <a name="40003"></a>40003
El usuario no tiene permiso para acceder al recurso solicitado.

### <a name="40004"></a>40004
El token de OAuth no tiene los ámbitos necesarios para realizar la acción solicitada. Vea [Permisos de notas](permissions_reference.md#notes-permissions).

### <a name="40006"></a>40006 
El token de OAuth no tiene los ámbitos necesarios para realizar la acción solicitada. Específicamente, el permiso de edición. Vea [Permisos de notas](permissions_reference.md#notes-permissions).

### <a name="40007"></a>40007
El usuario no tiene permisos para acceder a este recurso.

### <a name="40008"></a>40008
El acceso está prohibido para este recurso.

### <a name="40009"></a>40009
El contenedor ya está en uso por otro recurso.

## <a name="see-also"></a>Ver también

- [Respuestas de error de Microsoft Graph y tipos de recursos](errors.md)
- [Referencia de OneNote](../api-reference/v1.0/resources/onenote.md)

