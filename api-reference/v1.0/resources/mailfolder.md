# <a name="mailfolder-resource-type"></a>Tipo de recurso mailFolder

Carpeta de recurso en el buzón de un usuario, como Bandeja de entrada y Borradores. Las carpetas de correo pueden contener mensajes, otros elementos de Outlook y carpetas de correo secundarias.

Este recurso es compatible con el uso de una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de las adiciones incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/mailfolder_delta.md).

**Nombres de carpeta conocidos**

Outlook crea determinadas carpetas para los usuarios de manera predeterminada. En lugar de usar el valor **id** de carpeta correspondiente, para su comodidad, puede usar los nombres de carpeta conocidas de la siguiente tabla al obtener acceso a estas carpetas. Por ejemplo, puede obtener la carpeta Borradores utilizando su nombre conocido con la siguiente consulta.

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/drafts
```

Los nombres conocidos funcionan independientemente de la configuración regional del buzón de correo del usuario, por lo que la consulta anterior devolverá siempre carpeta de borradores del usuario, independientemente de cómo se denomine.

| Nombre de carpeta conocidos | Descripción |
|:-----------------------|:------------|
| archive | Los mensajes de la carpeta de archivo se envían cuando se usa la característica de archivo en un clic en los clientes de Outlook que lo admitan. **Nota:** No es el mismo que la característica de buzón de archivo de Exchange Online. |
| clutter | Los mensajes con prioridad baja de la carpeta Otros correos se mueven cuando se usa la característica Otros Correos. |
| conflicts | La carpeta que contiene los elementos en conflicto en el buzón de correo. |
| conversationhistory | La carpeta donde Skype guarda las conversaciones de mensajería instantánea (si está configurado Skype para ello). |
| deleteditems | Los elementos de carpeta se mueven aquí cuando se eliminan. |
| drafts | La carpeta que contiene los mensajes no enviados. |
| inbox | Carpeta de bandeja de entrada. |
| junkemail | La carpeta de correo electrónico no deseado. |
| localfailures | La carpeta que contiene los elementos que existen en el cliente local pero que no se pudieron cargar en el servidor. |
| msgfolderroot | La carpeta "Raíz del almacén de información". Esta carpeta es la carpeta principal para las carpetas que se muestran en los clientes de correo normal, como la bandeja de entrada. |
| outbox | Carpeta de bandeja de salida. |
| recoverableitemsdeletions | La carpeta que contiene elementos eliminados temporalmente: eliminado desde la carpeta de elementos eliminados, o al presionar MAYÚS + SUPR en Outlook. Esta carpeta no está visible en todos los clientes de correo electrónico de Outlook, pero los usuarios finales pueden interaccionar con ella a través de la característica **Recuperar elementos eliminados del servidor** en Outlook o Outlook en la web. |
| scheduled | La carpeta que contiene los mensajes que están programados para volver a aparecer en la bandeja de entrada mediante la característica de programación de Outlook para iOS. |
| searchfolders | La carpeta principal para todas las carpetas de búsqueda definidas en el buzón del usuario. |
| sentitems | La carpeta de elementos enviados |
| serverfailures | La carpeta que contiene los elementos que existen en el servidor, pero que no se pudieron sincronizar con el cliente local. |
| syncissues | La carpeta que contiene los registros de sincronización creados por Outlook. |

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:-------|:------------|:------------|
|[Obtener mailFolder](../api/mailfolder_get.md) | [mailFolder](mailfolder.md) |Lea las propiedades y las relaciones del objeto mailFolder.|
|[Crear MailFolder](../api/mailfolder_post_childfolders.md) |[MailFolder](mailfolder.md)| Cree un nuevo recurso mailFolder en el actual; para ello, publique en la colección childFolders.|
|[Enumerar childFolders](../api/mailfolder_list_childfolders.md) |Colección [MailFolder](mailfolder.md)| Obtenga la colección de carpetas en la carpeta especificada. Puede usar el acceso directo `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.|
|[Crear mensaje](../api/mailfolder_post_messages.md) |[Mensaje](message.md)| Cree un nuevo mensaje en el recurso mailFolder actual; para ello, publique en la colección de mensajes.|
|[Enumerar mensajes](../api/mailfolder_list_messages.md) |Colección [Message](message.md)| Obtenga todos los mensajes del buzón del usuario que ha iniciado sesión o esos mensajes en una carpeta especificada del buzón.|
|[Actualizar](../api/mailfolder_update.md) | [mailFolder](mailfolder.md)|Actualice el objeto mailFolder especificado. |
|[Eliminar](../api/mailfolder_delete.md) | Ninguno |Elimine el objeto mailFolder especificado. |
|[copy](../api/mailfolder_copy.md)|[MailFolder](mailfolder.md)|Copie un objeto mailFolder y su contenido en otro objeto mailFolder.|
|[delta](../api/mailfolder_delta.md)|Colección [mailFolder](mailfolder.md)|Obtiene un conjunto de carpetas de correo que se hayan agregado, eliminado o quitado del buzón del usuario.|
|[move](../api/mailfolder_move.md)|[MailFolder](mailfolder.md)|Mueve un objeto mailFolder y su contenido a otro objeto mailFolder.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[mailFolder](mailFolder.md)  |Cree una o varias propiedades extendidas de valor único en un objeto mailFolder nuevo o existente.   |
|[Obtener mailFolder con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_get.md)  | [mailFolder](mailFolder.md) | Obtenga objetos mailFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [mailFolder](mailFolder.md) | Cree una o varias propiedades extendidas de varios valores en un objeto mailFolder nuevo o existente.  |
|[Obtener mailFolder con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_get.md)  | [mailFolder](mailFolder.md) | Obtenga un objeto mailFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------|:-----|:------------|
|childFolderCount|Int32|El número de objetos mailFolder secundarios inmediatos en el objeto mailFolder actual.|
|displayName|Cadena|El nombre para mostrar del objeto mailFolder.|
|id|Cadena|Identificador único del mailFolder.|
|parentFolderId|Cadena|El identificador único del objeto mailFolder principal del objeto mailFolder.|
|totalItemCount|Int32|El número de elementos en el objeto mailFolder.|
|unreadItemCount|Int32|El número de elementos en el objeto mailFolder marcados como no leídos.|

**Acceder a recuentos de elementos de forma eficaz**

Las propiedades `TotalItemCount`y `UnreadItemCount` de una carpeta le permiten calcular cómodamente el número de elementos leídos en la carpeta.
Le permiten evitar consultas como las siguientes que pueden incurrir en una latencia significativa:

```http
https://outlook.office.com/api/v1.0/me/folders/inbox/messages?$count=true&$filter=isread%20eq%20false
```

Las carpetas de correo en Outlook pueden contener más de un tipo de elementos, por ejemplo, la bandeja de entrada puede contener elementos de solicitud de reunión que son distintos de los elementos de correo. `TotalItemCount` y `UnreadItemCount` incluyen elementos en una carpeta independientemente de sus tipos de elementos.

## <a name="relationships"></a>Relaciones

| Relación | Tipo | Descripción |
|:-------------|:-----|:------------|
|childFolders|Colección [MailFolder](mailfolder.md)|La colección de carpetas secundarias del objeto mailFolder.|
|messageRules | Colección [messageRule](messagerule.md) | Conjunto de reglas que se aplican a la Bandeja de entrada del usuario. |
|messages|Colección [Message](message.md)|La colección de mensajes del objeto mailFolder.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "messageRules",
    "messages",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.mailFolder",
  "@odata.annotations": [
    {
      "property": "childFolders",
      "capabilities": {
        "changeTracking": false,
        "navigability": "single",
        "searchable": false
      }
    },
    {
      "property": "messageRules",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "messages",
      "capabilities": {
        "changeTracking": true,
        "navigability": "single"
      }
    }
  ]
}-->

```json
{
  "childFolderCount": 1024,
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string",
  "totalItemCount": 1024,
  "unreadItemCount": 1024,
  "childFolders": [ { "@odata.type": "microsoft.graph.mailFolder" } ],
  "messageRules": [ { "@odata.type": "microsoft.graph.messageRule" } ],
  "messages": [ { "@odata.type": "microsoft.graph.message" } ],
  "multiValueExtendedProperties": [ { "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty" }],
  "singleValueExtendedProperties": [ { "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty" }]
}
```

## <a name="see-also"></a>Recursos adicionales

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md)
- [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
