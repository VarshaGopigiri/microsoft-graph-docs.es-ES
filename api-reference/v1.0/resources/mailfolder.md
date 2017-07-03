# <a name="mailfolder-resource-type"></a>Tipo de recurso mailFolder

Un recurso mailFolder en el buzón de un usuario, como Bandeja de entrada, Borradores y Elementos enviados. Los recursos mailFolder pueden contener mensajes y recursos mailFolder secundarios.

Este recurso es compatible con el uso de una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/mailfolder_delta.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener mailFolder](../api/mailfolder_get.md) | [mailFolder](mailfolder.md) |Lea las propiedades y las relaciones del objeto mailFolder.|
|[Crear MailFolder](../api/mailfolder_post_childfolders.md) |[MailFolder](mailfolder.md)| Cree un nuevo recurso mailFolder en el actual; para ello, publique en la colección childFolders.|
|[Enumerar childFolders](../api/mailfolder_list_childfolders.md) |Colección [MailFolder](mailfolder.md)| Obtenga la colección de carpetas en la carpeta especificada. Puede usar el acceso directo `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.|
|[Crear mensaje](../api/mailfolder_post_messages.md) |[Message](message.md)| Cree un nuevo mensaje en el recurso mailFolder actual; para ello, publique en la colección de mensajes.|
|[Enumerar mensajes](../api/mailfolder_list_messages.md) |Colección [Message](message.md)| Obtenga todos los mensajes del buzón del usuario que ha iniciado sesión o esos mensajes en una carpeta especificada del buzón.|
|[Actualizar](../api/mailfolder_update.md) | [mailFolder](mailfolder.md)|Actualice el objeto mailFolder especificado. |
|[Eliminar](../api/mailfolder_delete.md) | Ninguno |Elimine el objeto mailFolder especificado. |
|[copy](../api/mailfolder_copy.md)|[MailFolder](mailfolder.md)|Copie un objeto mailFolder y su contenido en otro objeto mailFolder.|
|[delta](../api/mailfolder_delta.md)|Colección [mailFolder](mailfolder.md)|Obtenga un conjunto de carpetas de correo que se hayan agregado, eliminado o quitado del buzón del usuario.|
|[move](../api/mailfolder_move.md)|[MailFolder](mailfolder.md)|Mueva un objeto mailFolder y su contenido a otro objeto mailFolder.|
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[mailFolder](mailFolder.md)  |Cree una o varias propiedades extendidas de valor único en un objeto mailFolder nuevo o existente.   |
|[Obtener mailFolder con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_get.md)  | [mailFolder](mailFolder.md) | Obtenga objetos mailFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [mailFolder](mailFolder.md) | Cree una o varias propiedades extendidas de varios valores en un objeto mailFolder nuevo o existente.  |
|[Obtener mailFolder con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_get.md)  | [mailFolder](mailFolder.md) | Obtenga un objeto mailFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|childFolderCount|Int32|El número de objetos mailFolder secundarios inmediatos en el objeto mailFolder actual.|
|displayName|String|El nombre para mostrar del objeto mailFolder.|
|id|String|El identificador único del objeto mailFolder. Puede usar los siguientes nombres conocidos para acceder a la carpeta correspondiente: Inbox, Drafts, SentItems, DeletedItems.|
|parentFolderId|String|El identificador único del objeto mailFolder principal del objeto mailFolder.|
|totalItemCount|Int32|El número de elementos en el objeto mailFolder.|
|unreadItemCount|Int32|El número de elementos en el objeto mailFolder marcados como no leídos.|

**Acceder a recuentos de elementos de forma eficaz**

Las propiedades TotalItemCount y UnreadItemCount de una carpeta le permiten calcular convenientemente el número de elementos leídos de la carpeta. Le permiten evitar consultas como la siguiente, que pueden ocasionar una latencia elevada:
```
https://outlook.office.com/api/v1.0/me/folders/inbox/messages?$count=true&$filter=isread%20eq%20false
```
Los objetos MailFolder en Outlook pueden contener más de un tipo de elementos; por ejemplo, la Bandeja de entrada puede contener elementos de convocatoria de reunión, que son distintos de los elementos de correo. Las propiedades TotalItemCount y UnreadItemCount incluyen elementos en un objeto MailFolder, independientemente de los tipos de elementos.


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|childFolders|Colección [MailFolder](mailfolder.md)|La colección de carpetas secundarias del objeto mailFolder.|
|messages|Colección [Message](message.md)|La colección de mensajes del objeto mailFolder.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "messages",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mailFolder"
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
  "messages": [ { "@odata.type": "microsoft.graph.message" } ],
  "multiValueExtendedProperties": [ { "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty" }],
  "singleValueExtendedProperties": [ { "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty" }]
}

```

## <a name="see-also"></a>Consulte también

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
