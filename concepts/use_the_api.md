# <a name="use-the-microsoft-graph-api"></a>Usar la API de Microsoft Graph

Microsoft Graph es una API para web REST que permite tener acceso a los recursos del servicio Microsoft Cloud. Después de [registrar su aplicación](auth_register_app_v2.md) y [obtener tokens de autenticación de un usuario](auth_v2_user.md) o [service](auth_v2_service.md), puede realizar solicitudes a la API de Microsoft Graph.

Para leer o escribir en un recurso como un usuario o un mensaje de correo electrónico, construya una solicitud similar a la siguiente.

```http
https://graph.microsoft.com/{version}/{resource}?query-parameters
```

Los componentes de una solicitud incluyen:

* [Método HTTP](#http-methods) - Método HTTP utilizado en la solicitud a Microsoft Graph.
* [`{version}`](#version) - La versión de la API de Microsoft Graph que utiliza la aplicación.
* [`{resource}`](#resource) - El recurso de Microsoft Graph al que se refiere.
* [query-parameters](#query-parameters-optional) - Un conjunto opcional de parámetros para modificar la solicitud o respuesta.

Después de realizar una solicitud, se devuelve una respuesta que incluye: 

* Código de estado - Un código de estado HTTP que indica éxito o error. Para obtener más información acerca de los códigos de error HTTP, consulte [Errores](errors.md).
* Mensaje de respuesta - Datos solicitados o resultado de la operación. El mensaje de respuesta puede estar vacío para algunas operaciones.
* Vínculo **Siguiente** - Si su solicitud devuelve una gran cantidad de datos, debe recorrer página a página mediante el vínculo **Siguiente**. Para más información, consulte [Paginación](paging.md).

## <a name="http-methods"></a>métodos HTTP

Microsoft Graph utiliza el método HTTP en la solicitud para determinar lo que está haciendo su solicitud. La API admite los siguientes métodos.


|**Método** |**Descripción**                             |
| :----- | :------------------------------------------- |
| OBTENER    | Lectura de datos de un recurso.                   |
| PUBLICAR   | Crear un nuevo recurso o realizar una acción. |
| REVISAR  | Actualizar un recurso con nuevos valores.           |
| PONER    | Reemplazar un recurso por otro nuevo.           |
| ELIMINAR | Eliminar un recurso.                           |

* Para los métodos **OBTENER** y **ELIMINAR**, no es necesario un cuerpo de solicitud.
* Los métodos **PUBLICAR**, **REVISAR**, y **PONER** requieren un cuerpo de la solicitud, generalmente especificado en formato JSON, que contiene información adicional, como los valores de las propiedades del recurso.

## <a name="version"></a>Versión

Microsoft Graph admite actualmente dos versiones: `v1.0` y `beta`.

* `v1.0` incluye las API que por lo general están disponibles. Utilice la versión v1.0 para todas las aplicaciones de producción.
* `beta` incluye las API que todavía están en vista previa. Debido a que podríamos introducir cambios importantes en nuestra API beta, recomendamos que utilice la versión beta solo para probar aplicaciones que están en desarrollo, no utilice la API beta en sus aplicaciones de producción.

Siempre estamos buscando comentarios sobre nuestras API beta. Para realizar comentarios o solicitar características, vea nuestra página [UserVoice](https://officespdev.uservoice.com/).

Para obtener más información acerca de las versiones de API, consulte [Control de versiones y soporte](versioning_and_support.md).

## <a name="resource"></a>Recurso

La dirección URL incluirá el recurso o los recursos con los que interactúa en la solicitud, como `me`, `users`, `groups`, `drives`, y `sites`. Cada uno de los recursos de nivel superior también incluye **relaciones**, que puede utilizar para tener acceso a recursos adicionales, como `me/messages` o `me/drive`. También puede interactuar con los recursos mediante **métodos**, por ejemplo, para enviar un correo electrónico, utilice `me/sendMail`.

Para obtener más información sobre cómo desplazarse por los métodos y relaciones de recursos, consulte el recorrido del gráfico. 

Cada recurso podría necesitar diferentes permisos de acceso. A menudo necesitará un mayor nivel de permisos para crear o actualizar un recurso que para leerlo. Para obtener más información acerca de los permisos necesarios, consulte el tema de referencia del método. 

Para obtener más información acerca de los permisos, consulte [Referencia de permisos](permissions_reference.md).

## <a name="query-parameters-optional"></a>Parámetros de consulta (opcional)

Puede utilizar parámetros de consulta opcionales para personalizar la respuesta de la aplicación Microsoft Graph. Use parámetros de consulta para incluir más o menos propiedades que la respuesta predeterminada, filtrar la respuesta para los elementos que coincidan con una consulta personalizada o proporcionar parámetros adicionales para un método.

Por ejemplo, agregar el siguiente parámetro de filtro restringe los mensajes devueltos solo a aquellos que tengan la propiedad `emailAddress` de `jon@contoso.com`.

```http
https://graph.microsoft.com/v1.0/me/messages?filter=emailAddress eq 'jon@contoso.com'
```

Para obtener más información acerca de los parámetros de consulta, consulte [Personalizar respuestas](query_parameters.md).

## <a name="next-steps"></a>Siguientes pasos

Está listo para poner en funcionamiento Microsoft Graph. Para obtener más información, vaya a [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) para probar algunas solicitudes, pruebe el [Inicio rápido](https://developer.microsoft.com/en-us/graph/quick-start), o comience con uno de nuestros [ejemplos de código y SDK](https://developer.microsoft.com/en-us/graph/code-samples-and-sdks).