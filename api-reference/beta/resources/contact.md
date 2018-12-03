---
title: Tipo de recurso contact
description: Un contacto es un elemento de Outlook donde puede organizar y guardar información sobre las personas y organizaciones con las que se comunica. Los contactos se contienen en carpetas de contactos.
ms.openlocfilehash: 1f18118855417727a441b25c008cee9a0e826aff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085713"
---
# <a name="contact-resource-type"></a>Tipo de recurso contact

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un contacto es un elemento de Outlook donde puede organizar y guardar información sobre las personas y organizaciones con las que se comunica. Los contactos se contienen en carpetas de contactos.

Este recurso admite:

- Adición de sus propios datos a las propiedades personalizadas como [extensiones](/graph/extensibility-overview).
- Suscribirse a [las notificaciones de cambios](/graph/webhooks).
- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/contact-delta.md).

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
  "@odata.type": "microsoft.graph.contact"
}-->

```json
{
  "assistantName": "string",
  "birthday": "String (timestamp)",
  "categories": ["string"],
  "changeKey": "string",
  "children": ["string"],
  "companyName": "string",
  "createdDateTime": "String (timestamp)",
  "department": "string",
  "displayName": "string",
  "emailAddresses": [{"@odata.type": "microsoft.graph.typedEmailAddress"}],
  "fileAs": "string",
  "flag": {"@odata.type": "microsoft.graph.followupFlag"},
  "gender": "string",
  "generation": "string",
  "givenName": "string",
  "id": "string (identifier)",
  "imAddresses": ["string"],
  "initials": "string",
  "jobTitle": "string",
  "lastModifiedDateTime": "String (timestamp)",
  "manager": "string",
  "middleName": "string",
  "nickName": "string",
  "officeLocation": "string",
  "parentFolderId": "string",
  "personalNotes": "string",
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "postalAddresses": [{"@odata.type": "microsoft.graph.physicalAddress"}],
  "profession": "string",
  "spouseName": "string",
  "surname": "string",
  "title": "string",
  "websites": [{"@odata.type": "microsoft.graph.website"}],
  "weddingAnniversary": "date",
  "yomiCompanyName": "string",
  "yomiGivenName": "string",
  "yomiSurname": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assistantName|String|El nombre del ayudante del contacto.|
|birthday|DateTimeOffset|El cumpleaños del contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|categories|Colección String|Las categorías asociadas con el contacto. Cada categoría corresponde a la propiedad **displayName** de un [outlookCategory](outlookcategory.md) definidos para el usuario.|
|changeKey|String|Identifica la versión del contacto. Cada vez que cambia el contacto, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto.|
|children|Colección String|Los nombres de los hijos del contacto.|
|companyName|String|El nombre de la empresa del contacto.|
|createdDateTime|DateTimeOffset|La hora en que se ha creado el contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|departamento|String|El departamento del contacto.|
|displayName|String|El nombre para mostrar del contacto. Puede especificar el nombre para mostrar en una operación de [creación](../api/user-post-contacts.md) o [actualización](../api/contact-update.md) . Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado. Para conservar un valor existente, siempre incluirla como displayName en una operación [de actualización](../api/contact-update.md) .|
|emailAddresses|colección de [typedEmailAddress](typedemailaddress.md)|Las direcciones de correo electrónico del contacto.|
|fileAs|String|El nombre con el que se ha archivado el contacto.|
|flag|[followupFlag](followupflag.md)|El valor de marca que indica el estado, fecha de inicio, fecha de vencimiento o fecha de finalización para el contacto. |
|gender |String |Género del contacto. |
|generation|String|La generación del contacto.|
|givenName|String|El nombre del contacto.|
|id|String|El identificador único del contacto. Solo lectura.|
|imAddresses|Colección String|Las direcciones de mensajería instantánea (MI) del contacto.|
|initials|String|Las iniciales del contacto.|
|jobTitle|String|El puesto del contacto.|
|lastModifiedDateTime|DateTimeOffset|La hora en que se ha modificado el contacto. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|manager|String|El nombre del administrador del contacto.
|middleName|String|El segundo nombre del contacto.|
|nickName|String|El sobrenombre del contacto.|
|officeLocation|String|La ubicación de la oficina del contacto.|
|parentFolderId|String|El identificador de la carpeta principal del contacto.|
|personalNotes|String|Las notas del usuario sobre el contacto.|
|phones |Colección [phone](phone.md) |Números de teléfono asociados con el contacto, por ejemplo, teléfono particular, teléfono móvil y teléfono del trabajo. |
|postalAddresses |colección [physicalAddress](physicaladdress.md) |Direcciones asociadas con el contacto, por ejemplo, home dirección y dirección de la empresa. |
|profession|String|La profesión del contacto.|
|spouseName|String|El nombre del cónyuge del contacto.|
|surname|String|Los apellidos del contacto.|
|title|String|El título del contacto.|
|websites |Colección [website](website.md)|Sitios Web asociados con el contacto. |
|weddingAnniversary |Fecha |Aniversario de boda del contacto. |
|yomiCompanyName|String|El nombre fonético japonés de la empresa del contacto.|
|yomiGivenName|String|El nombre (nombre de pila) fonético japonés del contacto.|
|yomiSurname|String|El apellido fonético japonés del contacto.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensions|Colección de [extensiones](extension.md)|La colección de extensiones de open definidas para el contacto. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el contacto. Solo lectura. Admite valores NULL.|
|photo|[photo](profilephoto.md)| Imagen de contacto opcional. Puede obtener o establecer una foto para un contacto.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el contacto. Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener contacto](../api/contact-get.md) | [contact](contact.md) |Lea las propiedades y las relaciones del objeto de contacto.|
|[Crear](../api/user-post-contacts.md) | [contact](contact.md) |Agregue un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.|
|[Actualizar](../api/contact-update.md) | [contact](contact.md) |Actualice el objeto de contacto. |
|[Eliminar](../api/contact-delete.md) | Ninguno |Elimine el objeto contact. |
|[delta](../api/contact-delta.md)|Colección [contact](contact.md)| Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[contact](contact.md)  |Cree una o varias propiedades extendidas de valor único en un contacto nuevo o existente.   |
|[Obtener contacto con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [contact](contact.md) | Obtenga contactos que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [contact](contact.md) | Cree una o varias propiedades extendidas de varios valores en un contacto nuevo o existente.  |
|[Obtener contacto con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [contact](contact.md) | Obtenga un contacto que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="see-also"></a>Consulte también

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview)
- [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages)
- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
