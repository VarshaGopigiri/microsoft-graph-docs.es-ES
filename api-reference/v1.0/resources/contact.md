# <a name="contact-resource-type"></a>Tipo de recurso contact

Un contacto es un elemento de Outlook donde puede organizar y guardar información sobre las personas y organizaciones con las que se comunica. Los contactos se contienen en carpetas de contactos.

Este recurso admite:

- que agregue sus propios datos a las propiedades personalizadas mediante [extensiones](../../../concepts/extensibility_overview.md);
- que use una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/contact_delta.md).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener contacto](../api/contact_get.md) | [contact](contact.md) |Lea las propiedades y las relaciones del objeto de contacto.|
|[Crear](../api/user_post_contacts.md) | [contact](contact.md) |Agregue un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.|
|[Actualizar](../api/contact_update.md) | [contact](contact.md) |Actualice el objeto de contacto. |
|[Eliminar](../api/contact_delete.md) | Ninguno |Elimine el objeto contact. |
|[delta](../api/contact_delta.md)|Colección [contact](contact.md)| Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension_post_opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.|
|[Obtener extensión abierta](../api/opentypeextension_get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtenga un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](../../../concepts/extensibility_schema_groups.md) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[contact](contact.md)  |Cree una o varias propiedades extendidas de valor único en un contacto nuevo o existente.   |
|[Obtener contacto con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_get.md)  | [contact](contact.md) | Obtenga contactos que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [contact](contact.md) | Cree una o varias propiedades extendidas de varios valores en un contacto nuevo o existente.  |
|[Obtener contacto con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_get.md)  | [contact](contact.md) | Obtenga un contacto que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assistantName|String|El nombre del ayudante del contacto.|
|birthday|DateTimeOffset|El cumpleaños del contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|businessAddress|[PhysicalAddress](physicaladdress.md)|La dirección del trabajo del contacto.|
|businessHomePage|String|La página principal de la empresa del contacto.|
|businessPhones|Colección String|Los números de teléfono del trabajo del contacto.|
|categories|Colección String|Las categorías asociadas con el contacto.|
|changeKey|String|Identifica la versión del contacto. Cada vez que cambia el contacto, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto.|
|children|Colección String|Los nombres de los hijos del contacto.|
|companyName|String|El nombre de la empresa del contacto.|
|createdDateTime|DateTimeOffset|La hora en que se ha creado el contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|departamento|String|El departamento del contacto.|
|displayName|String|El nombre para mostrar del contacto.|
|emailAddresses|Colección [EmailAddress](emailaddress.md)|Las direcciones de correo electrónico del contacto.|
|flag|[followUpFlag](followupflag.md)|Valor de marca que indica el estado, la fecha de inicio, la fecha de vencimiento o la fecha de finalización del mensaje.|
|fileAs|String|El nombre con el que se ha archivado el contacto.|
|generation|String|La generación del contacto.|
|givenName|String|El nombre del contacto.|
|homeAddress|[PhysicalAddress](physicaladdress.md)|La dirección particular del contacto.|
|homePhones|Colección String|Los números de teléfono particular del contacto.|
|id|String|El identificador único del contacto. Solo lectura.|
|imAddresses|Colección String|Las direcciones de mensajería instantánea (MI) del contacto.|
|initials|String|Las iniciales del contacto.|
|jobTitle|String|El puesto del contacto.|
|lastModifiedDateTime|DateTimeOffset|La hora en que se ha modificado el contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|manager|String|El nombre del administrador del contacto.
|middleName|String|El segundo nombre del contacto.|
|mobilePhone|String|El número de teléfono móvil del contacto.|
|nickName|String|El sobrenombre del contacto.|
|officeLocation|String|La ubicación de la oficina del contacto.|
|otherAddress|[PhysicalAddress](physicaladdress.md)|Otras direcciones del contacto.|
|parentFolderId|String|El identificador de la carpeta principal del contacto.|
|personalNotes|String|Las notas del usuario sobre el contacto.|
|profession|String|La profesión del contacto.|
|spouseName|String|El nombre del cónyuge del contacto.|
|surname|String|Los apellidos del contacto.|
|title|String|El título del contacto.|
|yomiCompanyName|String|El nombre fonético japonés de la empresa del contacto.|
|yomiGivenName|String|El nombre (nombre de pila) fonético japonés del contacto.|
|yomiSurname|String|El apellido fonético japonés del contacto.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el contacto. Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el contacto. Solo lectura. Admite valores NULL.|
|Foto|[profilePhoto](profilephoto.md)| Imagen de contacto opcional. Puede obtener o establecer una foto para un contacto.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el contacto. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "extensions",
    "multiValueExtendedProperties",
    "photo",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.contact"
}-->

```json
{
  "assistantName": "string",
  "birthday": "String (timestamp)",
  "businessAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "businessHomePage": "string",
  "businessPhones": ["string"],
  "categories": ["string"],
  "changeKey": "string",
  "children": ["string"],
  "companyName": "string",
  "createdDateTime": "String (timestamp)",
  "department": "string",
  "displayName": "string",
  "emailAddresses": [{"@odata.type": "microsoft.graph.emailAddress"}],
  "flag": {"@odata.type": "microsoft.graph.followupFlag"},
  "fileAs": "string",
  "generation": "string",
  "givenName": "string",
  "homeAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "homePhones": ["string"],
  "id": "string (identifier)",
  "imAddresses": ["string"],
  "initials": "string",
  "jobTitle": "string",
  "lastModifiedDateTime": "String (timestamp)",
  "manager": "string",
  "middleName": "string",
  "mobilePhone": "string",
  "nickName": "string",
  "officeLocation": "string",
  "otherAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "parentFolderId": "string",
  "personalNotes": "string",
  "profession": "string",
  "spouseName": "string",
  "surname": "string",
  "title": "string",
  "yomiCompanyName": "string",
  "yomiGivenName": "string",
  "yomiSurname": "string",

  "photo": { "@odata.type": "microsoft.graph.profilePhoto" }
}

```

## <a name="see-also"></a>Consulte también

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md)
- [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md)
- [Agregar datos personalizados a los recursos mediante extensiones](../../../concepts/extensibility_overview.md)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](../../../concepts/extensibility_open_users.md)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
