# <a name="activity-resource-type"></a>tipo de recurso de actividad

Representa una única actividad dentro de una app, por ejemplo, un programa de TV, un documento o una campaña actual de un videojuego. Cuando un usuario interactúa con dicha actividad, la interacción se captura como un [elemento de historial](projectrome_historyitem.md) que indica la hora de inicio y final de esa actividad. Cuando el usuario vuelve a interactuar con esa actividad con el paso del tiempo, se registran múltiples elementos de historial para una única actividad de usuario.

Puede usar las actividades de Microsoft Graph para permitir que los usuarios vuelvan a lo que estaba haciendo en su app en múltiples dispositivos. Las actividades que crea la aplicación aparecen en los dispositivos de todos los usuarios, y se muestran a estos como enlaces profundos a contenidos específicos dentro de la aplicación. Puede expresar un contenido específico dentro de la aplicación como un destino que se mostrará en Windows, el cual será accesible en dispositivos iOS y Android mediante notificaciones de Cortana.

Debido a que cada aplicación es diferente, le corresponde a usted conocer la mejor forma de asignar acciones dentro de la aplicación a las actividades del usuario que aparecerán en Cortana y Timeline. Por ejemplo, los juegos pueden crear una actividad para cada campaña, las aplicaciones de creación de documentos pueden crear una actividad para cada documento único y las aplicaciones de línea de negocio pueden crear una actividad para cada flujo de trabajo.

Las actividades del usuario se mostrarán en la experiencias de usuario de Cortana y Windows Timeline, que se centran en aumentar la productividad y eficacia de los usuarios al ayudarles a ponerse en contacto con los contenidos que han funcionado en el pasado.

## <a name="methods"></a>Métodos

|Método | Tipo de valor devuelto | Descripción|
|:------|:------------|:-----------|
|[Crear o reemplazar una actividad](../api/projectrome_put_activity.md) | [activity](projectrome_activity.md) |Crea o reemplaza una actividad existente (upsert). El appActivityId debe ser seguro en términos de URL (todos los caracteres excepto los no reservados para RFC 2396 deben convertirse a su representación hexadecimal), aunque el appActivityId original no tiene que ser seguro en lo que respecta a la URL. |
|[Eliminar una actividad](../api/projectrome_delete_activity.md) | Sin contenido | Elimina la actividad especificada para ese usuario desde la aplicación.|
|[Obtener actividades](../api/projectrome_get_activities.md) | Colección de [actividades](projectrome_activity.md) | Obtiene las actividades de la aplicación para un usuario determinado.|
|[Obtener actividades recientes](../api/projectrome_get_recent_activities.md) | Colección de [actividades](projectrome_activity.md) | Obtiene las actividades más recientes de la app para un usuario determinado, ordenadas según los [historyItems](projectrome_historyitem.md) creados o actualizados más recientemente.|

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|userTimezone | Cadena | Opcional. La zona horaria en la que se encontraba el dispositivo del usuario utilizado para generar la actividad en el momento de creación de la actividad; valores proporcionados como identificadores Olson con el fin de admitir la representación multiplataforma.|
|createdDateTime | DateTimeOffset | Establecida por el servidor. DateTime en UTC en la que se creó el objeto en el servidor. |
|lastModifiedDateTime | DateTimeOffset | Establecida por el servidor. DateTime en UTC en la que se modificó el objeto en el servidor. |
|id | Cadena | Identificador generado por el servidor usado para el direccionamiento URL.|
|appActivityId | Cadena | Obligatorio. El identificador de actividad único en el contexto de la app - suministrado por el autor de la llamada e inmutable a partir de ese momento.|
|activitySourceHost | Cadena | Obligatorio. URL para el dominio que representa la asignación de identidad de multiplataforma para la app. La asignación se almacena o bien como archivo JSON hospedado en el dominio o bien como configurable a través de Windows Dev Center. El archivo JSON se nombra según los identificadores de app multiplataforma y se hospeda en la raíz de su dominio HTTPS, ya sea en el dominio de nivel superior o incluido en un subdominio. Por ejemplo: https://contoso.com o https://myapp.contoso.com, pero NO https://myapp.contoso.com/somepath. Debe tener un archivo único y un dominio (o subdominio) por cada identidad de app multiplataforma. Por ejemplo, se necesitan un archivo y un dominio independientes para Word y PowerPoint.|
|appDisplayName | Cadena | Opcional. Descripción con un breve texto de la aplicación que se ha usado para generar la actividad, para su uso en los casos en los que la aplicación no esté instalada en el dispositivo del usuario local.|
|activationUrl | Cadena | Obligatorio. URL utilizada para iniciar la actividad en la mejor experiencia nativa representada por el appId. Es posible que se inicie una aplicación basada en la web si no existe ninguna aplicación nativa.|
|fallbackUrl | Cadena | Opcional. URL utilizada para iniciar la actividad en una aplicación basada en la web, si está disponible.|
|contentUrl | Cadena | Opcional. Se usa en el caso de que el contenido se pueda representar fuera de una experiencia de app nativa o basada en la web (por ejemplo, un puntero hacia un elemento en una fuente RSS).|
|visualElements| [visualInfo](../resources/projectrome_visualinfo.md) | Obligatorio. El objeto que contiene la información para representar a la actividad en la UX.|
|contentInfo | Objeto JSON sin tipo | Opcional. Un fragmento personalizado de datos - descripción extensible JSON-LD del contenido de acuerdo con la sintaxis de [schema.org](http://schema.org).|
|expirationDateTime | DateTimeOffset | Establecida por el servidor. DateTime en UTC en la que expiró el objeto en el servidor.|
|status | status | Establecida por el servidor. Un código de estado que se usa para identificar objetos válidos. Valores: activo, actualizado, eliminado, ignorado.|

## <a name="relationships"></a>Relaciones

|Relación | Tipo | Descripción|
|:------------|:-----|:-----------|
|historyItems| colección de [activityHistoryItem](../resources/projectrome_historyitem.md) | Opcional. NavigationProperty/Containment; propiedad de navegación para los historyItems de la actividad.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "userTimezone",
    "appDisplayName",
    "fallbackUrl",
    "contentUrl",
    "contentInfo",
    "visualElements",
    "historyItems"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.userActivity",
  "@odata.annotations": [
    {
      "capabilities": {
        "countable": false,
        "selectable": false,
        "skippable": false
      }
    }
  ]
}-->

```json
{
    "appActivityId": "String",
    "activitySourceHost": "String (host name/domain/URL)",
    "userTimezone": "String",
    "appDisplayName": "String",
    "activationUrl": "String (URL)",
    "contentUrl": "String (URL)",
    "fallbackUrl": "String (URL)",
    "createdDateTime": "DateTimeOffset",
    "lastModifiedDateTime": "DateTimeOffset",
    "expirationDateTime": "DateTimeOffset",
    "id": "String",
    "status": "active | updated | deleted | ignored",
    "contentInfo": { "@odata.type": "microsoft.graph.Json" },
    "visualElements": { "@odata.type": "microsoft.graph.visualInfo" },
    "historyItems": [{ "@odata.type": "microsoft.graph.activityHistoryItem" }]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "activity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
