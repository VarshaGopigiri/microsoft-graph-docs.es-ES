# <a name="featured-scenarios-for-microsoft-graph"></a>Escenarios destacados para Microsoft Graph

Consulte algunos escenarios comunes y destacados para trabajar con la API de Microsoft Graph. Explore los temas de esta sección y pruebe algunas de las solicitudes populares que aparecen en la tabla siguiente. Los vínculos le llevan a nuestro [Probador de Graph](https://developer.microsoft.com/en-us/graph/graph-explorer).


## <a name="popular-requests"></a>Solicitudes populares
| **Operación** | **URL** |
|:--------------------------|:----------------------------------------|
|   OBTENER mi perfil |    [`https://graph.microsoft.com/v1.0/me`](https://developer.microsoft.com/graph/graph-explorer/?request=me&version=v1.0) |
|   OBTENER mis archivos | [`https://graph.microsoft.com/v1.0/me/drive/root/children`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fdrive%2Froot%2Fchildren&version=v1.0) |
|   OBTENER mi foto | [`https://graph.microsoft.com/v1.0/me/photo/$value`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fphoto%2F%24value&version=v1.0) |
|   OBTENER mi correo |   [`https://graph.microsoft.com/v1.0/me/messages`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmessages&version=v1.0) |
|   OBTENER mi correo electrónico de importancia alta | [`https://graph.microsoft.com/v1.0/me/messages?$filter=importance%20eq%20'high'`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmessages%3F%24filter%3Dimportance%2520eq%2520'high'&version=v1.0) |
|   OBTENER mis eventos de calendario |    [`https://graph.microsoft.com/v1.0/me/events`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fevents&version=v1.0) |
|   OBTENER mi administrador  | [`https://graph.microsoft.com/v1.0/me/manager`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmanager&version=v1.0) |
|   OBTENER el último usuario que modificó el archivo foo.txt |  [`https://graph.microsoft.com/v1.0/me/drive/root/children/foo.txt/lastModifiedByUser`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fdrive%2Froot%2Fchildren%2Ffoo.txt%2FlastModifiedByUser&version=v1.0) |
|   OBTENER grupos de Office 365 de los que soy miembro| [`https://graph.microsoft.com/v1.0/me/memberOf/$/microsoft.graph.group?$filter=groupTypes/any(a:a%20eq%20'unified')`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2FmemberOf%2F%24%2Fmicrosoft.graph.group%3F%24filter%3DgroupTypes%2Fany(a%3Aa%2520eq%2520'unified')&version=v1.0) |
|   OBTENER usuarios de mi organización     | [`https://graph.microsoft.com/v1.0/users`](https://developer.microsoft.com/graph/graph-explorer/?request=users&version=v1.0) |
|   OBTENER grupos de mi organización | [`https://graph.microsoft.com/v1.0/groups`](https://developer.microsoft.com/graph/graph-explorer/?request=groups&version=v1.0) |
|   OBTENER usuarios relacionados conmigo    | [`https://graph.microsoft.com/v1.0/me/people`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fpeople&version=beta)  |
|   OBTENER elementos de tendencias a mi alrededor |  [`https://graph.microsoft.com/beta/me/insights/trending`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Finsights%2Ftrending&version=beta) |
|   OBTENER mis notas |  [`https://graph.microsoft.com/beta/me/onenote/notebooks`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fonenote%2Fnotebooks&version=beta) |

## <a name="next-steps"></a>Pasos siguientes

Pruebe algunas llamadas más en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer) y use nuestro [inicio rápido](https://developer.microsoft.com/graph/quick-start) para ponerlo todo en funcionamiento de manera rápida. Obtenga más información sobre cómo [usar la API](use_the_api.md) para compilar su primera aplicación.