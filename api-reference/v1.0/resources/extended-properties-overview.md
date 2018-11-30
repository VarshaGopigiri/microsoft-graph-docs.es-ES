---
title: Información general sobre las propiedades extendidas de Outlook
description: 'Las propiedades extendidas permiten almacenar datos personalizados y específicamente actuar como un mecanismo de reserva para aplicaciones para obtener acceso a '
ms.openlocfilehash: 062c39eca7a32f52f88334b43a79ad413b986ad7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029479"
---
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

En los casos más comunes, debería poder utilizar las extensiones abiertas (representadas por [openTypeExtension](../resources/opentypeextension.md), anteriormente conocidas como extensiones de datos de Office 365) para almacenar y acceder a datos personalizados de instancias de recurso en el buzón de un usuario. Utilice las propiedades extendidas solo si necesita acceder a datos personalizados de las propiedades MAPI de Outlook que aún no están expuestos en los [metadatos de la API de Microsoft Graph](https://developer.microsoft.com/graph/docs/overview/call_api). 

## <a name="types-of-extended-properties"></a>Tipos de propiedades extendidas

Dependiendo de si desea almacenar un valor único o varios valores (del mismo tipo) en una propiedad extendida, puede crear una propiedad extendida como [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) o [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md).

Cada uno de estos tipos identifica la propiedad por su **id** (identificador) y almacena datos en **value**. 

Puede utilizar **id** para obtener una instancia de un recurso específico junto con esa propiedad extendida o filtrar una propiedad extendida de valor único para obtener todas las instancias que tienen esa propiedad. 

**Nota** No puede utilizar la API de REST para obtener todas las propiedades extendidas de una instancia específica en una llamada.
  

### <a name="id-formats"></a>formatos de identificador

Puede especificar el **identificador** de una propiedad extendida en uno de estos tres formatos:

- Como una propiedad con nombre, identificada por el tipo de propiedad extendida, espacio de nombres y un nombre de cadena.
- Como una propiedad con nombre, identificada por un identificador numérico, espacio de nombres y el tipo de propiedad extendida.
- En un formato proptag, identificado por el tipo de propiedad extendida y una [etiqueta de propiedad MAPI](https://docs.microsoft.com/en-us/office/client-developer/outlook/mapi/mapi-property-tags).

Las 2 a continuación tablas describen estos formatos como propiedades extendidas aplicadas al único y de varios valores. {_tipo_} representa el tipo del valor o valores de la propiedad extendida. Lo que se muestra en los ejemplos son la cadena, el número entero y las matrices de esos tipos.

**Formatos de identificador válidos para propiedades extendidas de valor único**

|**Formato**|**Ejemplo**|**Descripción**|
|:---------|:----------|:--------------|
| “{_type_} {_guid_} **Nombre** {_name_}” | ```"String {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Name TestProperty"``` | Identifica una propiedad por el espacio de nombres (GUID) al que pertenece y un nombre de cadena.         |
| “{_type_} {_guid_} **Id.** {_id_}”     | ```"Integer {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Id 0x8012"```        | Identifica una propiedad por el espacio de nombres (GUID) al que pertenece y un identificador numérico.  |
| "{_tipo_} {_proptag_}"                    | ```"String 0x4001001E"```                                           | Identifica una propiedad definida previamente por su etiqueta de propiedad. |

**Formatos de identificador válidos para propiedades extendidas de varios valores**

|**Formato**|**Ejemplo**|**Descripción**|
|:---------|:----------|:--------------|
| “{_type_} {_guid_} **Nombre** {_name_}” | ```"StringArray {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Name TestProperty"``` | Identifica una propiedad por el espacio de nombres (GUID) y un nombre de cadena.         |
| “{_type_} {_guid_} **Id.** {_id_}”     | ```"IntegerArray {8ECCC264-6880-4EBE-992F-8888D2EEAA1D} Id 0x8013"```        | Identifica una propiedad por el espacio de nombres (GUID) y un identificador numérico.   |
| "{_tipo_} {_proptag_}"                    | ```"StringArray 0x4002101E"```                                           | Identifica una propiedad definida previamente por su etiqueta de propiedad. |


Use uno de los formatos de propiedad con nombre para definir una propiedad extendida de valor único o varios valor como una propiedad personalizada. Entre los dos formatos, el primero de ellos que toma un nombre de cadena (**nombre**) es el formato preferido para facilitar la referencia. Propiedades con nombre tienen sus [identificadores de propiedades](https://docs.microsoft.com/en-us/office/client-developer/outlook/mapi/mapi-property-identifier-overview) en el 0 x 8000-0xfffe intervalo.

Utilice el formato proptag para tener acceso a las propiedades predeterminadas de MAPI, o por un cliente o servidor, y que no han ya se ha expuesto en Microsoft Graph. Estas propiedades tienen identificadores de propiedades en el 0 x 0001-0x7fff intervalo. No intente definir una propiedad personalizada con el formato proptag. 

Encontrará información sobre la asignación de una propiedad extendida a una propiedad MAPI existente (como el identificador de la propiedad y el GUID) en \[MS-OXPROPS\] Microsoft Corporation, [“Exchange Server Protocols Master Property List” (Lista de propiedades Master de los protocolos de Exchange Server)](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx).

**Nota**: Después de elegir un formato para el **id.**, deberá obtener acceso a la propiedad extendida únicamente con ese formato.

### <a name="rest-api-operations"></a>Operaciones de la API de REST
 
Operaciones de propiedades extendidas de valor único:

- [Crear una propiedad extendida en una instancia de recurso nueva o existente](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md)
- [Obtener una instancia de recurso o una colección de ellas con una propiedad extendida mediante el uso de `$expand` o `$filter`](../api/singlevaluelegacyextendedproperty-get.md)

Operaciones de propiedades extendidas de varios valores:

- [Crear una propiedad extendida en una instancia de recurso nueva o existente](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md)
- [Obtener una instancia de recurso con una propiedad extendida mediante el uso de `$expand`](../api/multivaluelegacyextendedproperty-get.md)

