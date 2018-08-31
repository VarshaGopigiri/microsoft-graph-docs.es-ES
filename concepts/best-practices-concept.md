# <a name="best-practices-for-working-with-microsoft-graph"></a>Procedimientos recomendados para trabajar con Microsoft Graph.

En este artículo se describen los procedimientos recomendados que puede usar para que sus aplicaciones saquen el máximo provecho de Microsoft Graph, ya sea que se trate de aprender sobre Microsoft Graph, mejorar el rendimiento de las aplicaciones o aumentar la confiabilidad de la aplicación para los usuarios finales.

## <a name="use-graph-explorer-to-get-to-know-the-api"></a>Usar la herramienta Probador de Graph para familiarizarse con la API

La mejor manera de empezar a explorar los datos disponibles en Microsoft Graph es usar [Probador de Graph](https://aka.ms/ge). Probador de Graph le permite crear solicitudes REST (con soporte completo de CRUD), adaptar los encabezados de solicitud HTTP y ver las respuestas de datos. Para ayudarle a empezar, Probador de Graph ofrece también un conjunto de consultas de ejemplo.

Experimente con nuevas API antes de integrarlas en la aplicación.

## <a name="authentication"></a>Autenticación

Para tener acceso a los datos de Microsoft Graph, la aplicación debe adquirir un token de acceso OAuth 2.0 y presentarlo a Microsoft Graph mediante:

- El encabezado de solicitud *Authorization* HTTP, como token de *portador*
- El constructor cliente de Graph, cuando use una biblioteca cliente de Microsoft Graph

Use la API Biblioteca de autenticación de Microsoft ([MSAL](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-libraries)) para adquirir el token de acceso a Microsoft Graph.

## <a name="consent-and-authorization"></a>Consentimiento y autorización

Siga estos procedimientos recomendados para otorgar consentimiento y autorización en la aplicación:

- **Utilizar privilegios mínimos**. Solicite únicamente permisos absolutamente necesarios y solo cuando los necesite. Para las API a las que llama la aplicación, consulte la sección de permisos en los temas de método (por ejemplo, vea [Crear usuario](../api-reference/v1.0/api/user_post_users.md) y elija los permisos con privilegios mínimos. Para obtener la lista completa de permisos, vea [Referencia de permisos](permissions_reference.md).

- **Utilizar el tipo de permiso basado en escenarios adecuado**. Si crea una aplicación interactiva en la que está presente un usuario que ha iniciado sesión, la aplicación debe utilizar los permisos *delegados*, en donde se delega en la aplicación el permiso para actuar como usuario que ha iniciado sesión al realizar llamadas a Microsoft Graph. En cambio, si la aplicación se ejecuta sin que haya un usuario que ha iniciado sesión, como un demonio o servicio en segundo plano, la aplicación debe usar permisos de aplicación.

    >**Nota:** El uso de permisos de aplicación en escenarios interactivos puede exponer la aplicación a riesgos de seguridad y cumplimiento normativo. Se pueden elevar involuntariamente los privilegios de acceso a datos de un usuario, lo que elude las directivas configuradas por un administrador.
<!-- LG: Use a more clear lead-in here, like "Consider the end user and admin experience"? -->
- **Tener cuidado al configurar la aplicación**. Esto afectará directamente a las experiencias de usuario final y de administrador, así como a la seguridad y la adopción de la aplicación. Por ejemplo:

    - La declaración de privacidad, los términos de uso, el nombre, el logotipo y el dominio de la aplicación aparecerán en las experiencias de consentimiento y de otro tipo, por lo que debe asegurarse de configurarlos atentamente para que los usuarios finales las entiendan.
    - Tenga en cuenta quiénes darán consentimiento en la aplicación (administradores o usuarios finales) y configure la aplicación para [solicitar permisos adecuadamente](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-scopes).
    - Asegúrese de que comprende la diferencia entre [consentimiento estático, dinámico e incremental](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-compare#incremental-and-dynamic-consent).

- **Considerar el uso de aplicaciones multiempresa**. Cuente con la posibilidad de que los clientes tengan varios controles de aplicación y consentimiento en diferentes estados. Por ejemplo:

    - Los administradores de inquilinos pueden deshabilitar la posibilidad de que los usuarios finales den su consentimiento a las aplicaciones. En este caso, un administrador tendrá que dar el consentimiento en nombre de los usuarios.
    - Los administradores de inquilinos pueden establecer directivas de autorización personalizadas tales como impedir que los usuarios lean los perfiles de otros usuarios o restringir la creación de grupos de autoservicio a un conjunto limitado de usuarios. En este caso, es de esperar que la aplicación tenga que controlar la respuesta de error 403 cuando actúe en nombre de un usuario.

## <a name="handle-responses-effectively"></a>Controlar las respuestas con eficacia

Las aplicaciones han de estar preparadas para controlar distintos tipos de respuestas en función de las solicitudes que se realicen en Microsoft Graph. Estos son algunos de los procedimientos más importantes que hay que seguir para garantizar que la aplicación tenga un comportamiento confiable y predecible para los usuarios finales.

### <a name="pagination"></a>Paginación

Al consultar una colección de recursos, es muy probable que Microsoft Graph establezca el conjunto de resultados obtenido en varias páginas, debido a límites de tamaño de página en el servidor. Cuando un conjunto de resultados abarca varias páginas, Microsoft Graph devuelve una propiedad `@odata.nextLink` en la respuesta que contiene una dirección URL a la siguiente página de resultados.

Por ejemplo, al mostrar los mensajes de usuarios que han iniciado sesión:

```http
GET https://graph.microsoft.com/v1.0/me/messages
```

Se devolverá una respuesta que contiene una propiedad `@odata.nextLink` si el conjunto de resultados supera el límite de tamaño de página del servidor.

```json
"@odata.nextLink": "https://graph.microsoft.com/v1.0/me/messages?$skip=23"
```

>**Nota:** La aplicación **siempre** debe controlar la posibilidad de que las respuestas se paginen por naturaleza y usen la propiedad `@odata.nextLink` para obtener el próximo conjunto de resultados paginado, hasta que se hayan leído todas las páginas del conjunto de resultados. La última página no contendrá ninguna propiedad `@odata.nextLink`. Debe incluir la dirección URL completa en la propiedad `@odata:nextLink` de la solicitud de la siguiente página de resultados, que trata la URL completa como opaca.

Para más información, vea [paginación](paging.md).

### <a name="handling-expected-errors"></a>Control de errores esperados

Aunque la aplicación debe controlar todas las respuestas de error (en los rangos de 400 y 500), preste especial atención a determinados errores esperados y respuestas, que aparecen en la tabla siguiente.

| Tema   | Código de error HTTP    | Procedimiento recomendado|
|:-----------|:--------|:----------|
| User does not have access (El usuario no tiene acceso) | 403 | Si la aplicación está funcionando, podría encontrarse este error aunque se le hayan concedido los permisos necesarios mediante una experiencia de consentimiento.  En este caso, es muy probable que el usuario que ha iniciado sesión no tenga privilegios de acceso al recurso solicitado. La aplicación debe presentar un error genérico "Acceso denegado" al usuario que ha iniciado sesión. |
|No encontrado| 404 | En algunos casos, es posible que no se encuentre el recurso solicitado. Por ejemplo, puede que un recurso no exista, porque no se ha aprovisionado todavía (como la foto de un usuario) o se ha eliminado. Algunos recursos eliminados *podrían* restaurarse completamente en los 30 días siguientes a la eliminación, como los recursos de usuario, de grupo y de aplicación, por lo que la aplicación también debe tener esto en cuenta.|
|Limitación|429|Puede que las API limiten las solicitudes en cualquier momento por diversos motivos, por lo que la aplicación debe estar **siempre** preparada para controlar respuestas 429. Esta respuesta de error incluye el campo *Retry-After* (volver a intentar más adelante) en el encabezado de la respuesta HTTP. La interrupción de solicitudes con el retraso *Retry-After* (volver a intentar más adelante) es la mejor forma de recuperarse de la limitación de solicitudes. Para más información, vea [limitación](throttling.md).|
|Servicio no disponible| 503 | Probablemente se deba a que el servicio está ocupado. Debe emplear una estrategia de interrupción similar a la respuesta 429. Además, debe realizar **siempre** nuevas solicitudes de reintento a través de una nueva conexión HTTP.|

### <a name="evolvable-enums"></a>Enumeraciones desarrollables

Las aplicaciones cliente pueden dividirse mediante la adición de miembros a una enumeración existente. Con algunas de las enumeraciones más recientes de Microsoft Graph, hay un mecanismo disponible que permite agregar nuevos miembros sin provocar un cambio importante. En estas enumeraciones más recientes, verá un miembro *centinela* común denominado `unknownFutureValue` que delimita los miembros de enumeración conocidos y desconocidos. Los miembros conocidos tendrán un número menor que el miembro centinela, mientras que los miembros desconocidos tendrán un valor mayor.
De forma predeterminada, Microsoft Graph no devuelve miembros desconocidos. Aunque, si la aplicación está escrita para controlar la aparición de miembros desconocidos, se puede optar por recibir miembros de enumeración desconocidos, mediante un encabezado de solicitud HTTP *Prefer*.

>**Nota:** Si la aplicación está preparada para controlar los miembros de enumeración desconocidos, debe optar por recibirlos mediante un encabezado de solicitud HTTP *Prefer*: `Prefer: include-unknown-enum-members`.


## <a name="storing-data-locally"></a>Almacenamiento de datos local

Lo ideal es que la aplicación realice llamadas a Microsoft Graph para recuperar datos en tiempo real cuando sea necesario. Solo deben almacenarse datos en caché o localmente si es necesario en un escenario específico y si ese caso de uso está cubierto por las condiciones de uso y la directiva de privacidad del usuario y no infringe los [Términos de uso Microsoft Graph](https://developer.microsoft.com/es-ES/graph/docs/misc/terms-of-use). La aplicación también debe implementar políticas de retención y eliminación adecuadas.

## <a name="optimizations"></a>Optimizaciones

En general, por motivos de rendimiento e incluso de seguridad o privacidad, solo deben obtenerse los datos que la aplicación realmente necesita y nada más.

### <a name="use-projections"></a>Proyecciones de uso

Elija solo las propiedades que la aplicación realmente necesita y nada más, porque así ahorra tráfico de red y procesamiento de datos innecesarios en su aplicación (y en el servicio).

>**Nota:** Utilice el parámetro de consulta `$select` para limitar las propiedades devueltas por una consulta a las necesarias para la aplicación.

Por ejemplo, al recuperar los mensajes del usuario que ha iniciado sesión, puede especificar que solo se devuelvan las propiedades **from** y **subject**:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

### <a name="getting-minimal-responses"></a>Obtener respuestas mínimas

Con algunas operaciones, como PUT y PATCH (y, en algunos casos, POST), si la aplicación no tiene que usar una carga útil de respuesta, puede pedir a la API que devuelva datos mínimos. Tenga en cuenta que algunos servicios ya devuelven una respuesta 204 No Content (No hay contenido) en operaciones PUT y PATCH.

>**Nota:** Solicite respuestas de representación mínima mediante un encabezado de solicitud HTTP cuando corresponda: *Prefer: return=minimal*. Tenga en cuenta que, para las operaciones de creación, esto tal vez no sea adecuado porque puede que la aplicación espere obtener el `id` del servicio generado para el objeto recién creado en la respuesta.

### <a name="track-changes-delta-query-and-webhook-notifications"></a>Control de cambios: consulta delta y notificaciones de webhook

Si la aplicación tiene que estar informada de los cambios en los datos, se puede obtener una notificación de webhook siempre que los datos de interés hayan cambiado. Esto resulta más eficaz que simplemente realizar sondeos periódicamente.

Utilice [notificaciones de webhook](../api-reference/v1.0/resources/webhooks.md) para recibir notificaciones push cuando cambien los datos.

Si se requiere que la aplicación almacene en caché o localmente los datos de Microsoft Graph y los mantenga actualizados o que, por otros motivos, siga los cambios en los datos, debe utilizarse la consulta delta. Esto evita que la aplicación realice cálculos excesivos para recuperar datos que ya tiene, minimiza el tráfico de red y reduce la probabilidad de alcanzar un umbral de limitación.

Use la [consulta delta](delta_query_overview.md) para mantener los datos actualizados con eficacia.

### <a name="using-webhooks-and-delta-query-together"></a>Uso conjunto de webhooks y consulta delta

Suele ser preferible utilizar los webhooks y la consulta delta juntos, porque si se utiliza solo la consulta delta, es necesario averiguar el intervalo de sondeo correcto: si es demasiado corto podría traducirse en respuestas vacías que desperdician recursos y, si es demasiado largo, es posible que se acabe con datos obsoletos. Si utiliza notificaciones de webhook como desencadenador de llamadas de consulta delta, obtendrá lo mejor de ambos mundos.

Utilice [notificaciones de webhook](../api-reference/v1.0/resources/webhooks.md) como desencadenador de llamadas de consulta delta. También debe asegurarse de que la aplicación tenga un umbral de sondeo de seguridad en caso de que no se active ninguna notificación.

### <a name="batching"></a>Procesamiento por lotes

El procesamiento por lotes de JSON le permite optimizar la aplicación combinando varias solicitudes en un solo objeto JSON. La combinación de solicitudes individuales en una sola solicitud por lotes puede ahorrarle a la aplicación una cantidad significativa de latencia de red y conservar los recursos de conexión.

Use [procesamiento por lotes](json_batching.md) cuando una de latencia de red significativa pueda tener un gran impacto en el rendimiento.

## <a name="reliability-and-support"></a>Confiabilidad y compatibilidad
Para garantizar la confiabilidad y facilitar la compatibilidad con la aplicación:

- Respete el TTL de DNS y establezca el TTL de la conexión para que coincidan. Esto garantiza la disponibilidad en caso de conmutaciones por error.
- Abra las conexiones a todas las respuestas DNS anunciadas.
- Genere un GUID único y envíelo en cada solicitud del resto de Microsoft Graph REST. Esto le ayudará a Microsoft a investigar los errores más fácilmente si necesita informar de un problema con Microsoft Graph.
  - En cada solicitud de Microsoft Graph, genere un GUID único, envíelo por el `client-request-id` encabezado de la solicitud HTTP y también iniciar sesión en los registros de la aplicación.
  - Inicie siempre la `request-id`, `timestamp` y `x-ms-ags-diagnostic` de los encabezados de respuesta HTTP. Estos, junto con `client-request-id`, son necesarios para informar de problemas en [Desbordamiento de pila](https://stackoverflow.com/questions/tagged/microsoft-graph) o Microsoft Support.
