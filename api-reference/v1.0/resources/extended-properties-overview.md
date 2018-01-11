# <a name="outlook-extended-properties-overview"></a>Información general sobre las propiedades extendidas de Outlook

Las propiedades extendidas permiten almacenar datos personalizados y sirven específicamente como un mecanismo de reserva para que las aplicaciones accedan a datos personalizados de propiedades MAPI de Outlook si estas propiedades _aún no están expuestas en los metadatos de la API de Microsoft Graph_. Puede utilizar la API de REST de propiedades extendidas para almacenar u obtener dichos datos personalizados en los siguientes recursos de usuario:

- [message](../resources/message.md)
- [mailFolder](../resources/mailfolder.md)
- [event](../resources/event.md)
- [calendar](../resources/calendar.md)
- [contact](../resources/contact.md)
- [contactFolder](../resources/contactfolder.md) 

O bien en los siguientes recursos de grupo de Office 365:

- [evento](../resources/event.md) de grupo
- [calendar](../resources/calendar.md) de grupo
- [post](../resources/post.md) de grupo 

## <a name="use-extended-properties-or-open-extensions"></a>¿Usa propiedades extendidas o extensiones abiertas?

En los casos más comunes, debería poder utilizar las extensiones abiertas (representadas por [openTypeExtension](../resources/opentypeextension.md), anteriormente conocidas como extensiones de datos de Office 365) para almacenar y acceder a datos personalizados de instancias de recurso en el buzón de un usuario. Utilice las propiedades extendidas solo si necesita acceder a datos personalizados de las propiedades MAPI de Outlook que aún no están expuestos en los [metadatos de la API de Microsoft Graph]((http://developer.microsoft.com/es-ES/graph/docs/overview/call_api)). 

## <a name="types-of-extended-properties"></a>Tipos de propiedades extendidas

Dependiendo de si desea almacenar un valor único o varios valores (del mismo tipo) en una propiedad extendida, puede crear una propiedad extendida como [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) o [multiValueLegacyExtendedProperty](../resources/multiValueLegacyExtendedProperty.md).

Cada uno de estos tipos identifica la propiedad por su **id** (identificador) y almacena datos en **value**. 

Puede utilizar **id** para obtener una instancia de un recurso específico junto con esa propiedad extendida o filtrar una propiedad extendida de valor único para obtener todas las instancias que tienen esa propiedad. 

**Nota** No puede utilizar la API de REST para obtener todas las propiedades extendidas de una instancia específica en una llamada.
  

### <a name="id-formats"></a>Formatos de identificadores

Cuando cree una propiedad extendida de valor único o de varios valores, podrá especificar la propiedad **id** en uno de los dos formatos, mediante un nombre de cadena (**Name**) o un identificador numérico (**Id**), y en el tipo real del valor o de los valores de la propiedad. En las siguientes dos tablas, se describen los formatos compatibles para especificar propiedades extendidas de valor único y de varios valores. {_type_} representa el tipo de valor o valores de la propiedad. Lo que se muestra en los ejemplos son la cadena, el número entero y las matrices de esos tipos.

Como las propiedades extendidas interoperan en la mayoría de los casos con propiedades MAPI definidas que no están expuestas en los metadatos de la API de Microsoft Graph, por simplicidad, el formato que elija debe reflejar si la propiedad MAPI correspondiente usa una cadena de caracteres o un valor numérico en su [identificador de propiedad MAPI]((https://msdn.microsoft.com/es-ES/library/office/cc815528.aspx)).
Encontrará información sobre la asignación de una propiedad extendida a una propiedad MAPI existente (como el identificador de la propiedad y el GUID) en \[MS-OXPROPS\] Microsoft Corporation, [“Exchange Server Protocols Master Property List” (Lista de propiedades Master de los protocolos de Exchange Server)](https://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx).

**Nota**: Después de elegir un formato para el **id.**, deberá obtener acceso a la propiedad extendida únicamente con ese formato.


**Formatos de identificador válidos para propiedades extendidas de valor único**

|**Formato**|**Ejemplo**|**Descripción**|
|:---------|:----------|:--------------|
| “{_type_} {_guid_} **Nombre** {_name_}” | ```"String {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Name TestProperty"``` | Identifica una propiedad mediante el espacio de nombres (GUID) al que pertenece y mediante un nombre.         |
| “{_type_} {_guid_} **Id.** {_id_}”     | ```"Integer {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Id 0x8012"```        | Identifica una propiedad mediante el espacio de nombres (GUID) al que pertenece y mediante un identificador.  |

**Formatos de identificador válidos para propiedades extendidas de varios valores**

|**Formato**|**Ejemplo**|**Descripción**|
|:---------|:----------|:--------------|
| “{_type_} {_guid_} **Nombre** {_name_}” | ```"StringArray {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Name TestProperty"``` | Identifica una propiedad mediante un espacio de nombres (GUID) y un nombre.         |
| “{_type_} {_guid_} **Id.** {_id_}”     | ```"IntegerArray {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Id 0x8013"```        | Identifica una propiedad mediante un espacio de nombres (GUID) y un identificador.   |

### <a name="rest-api-operations"></a>Operaciones de la API de REST
 
Operaciones de propiedades extendidas de valor único:

- [Crear una propiedad extendida en una instancia de recurso nueva o existente](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md)
- [Obtener una instancia de recurso o una colección de ellas con una propiedad extendida mediante el uso de `$expand` o `$filter`](../api/singlevaluelegacyextendedproperty_get.md)

Operaciones de propiedades extendidas de varios valores:

- [Crear una propiedad extendida en una instancia de recurso nueva o existente](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md)
- [Obtener una instancia de recurso con una propiedad extendida mediante el uso de `$expand`](../api/multivaluelegacyextendedproperty_get.md)

