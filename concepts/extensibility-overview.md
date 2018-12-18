---
title: Agregar datos personalizados a los recursos mediante extensiones
description: Microsoft Graph proporciona un único punto de conexión de API que le da acceso a información y datos centrados en personas enriquecidos a través de varios recursos como user y message. También puede extender Microsoft Graph con sus propios datos de aplicación. Puede agregar propiedades personalizadas a los recursos de Microsoft Graph sin necesidad de un almacén de datos externo.
author: dkershaw10
ms.openlocfilehash: ccbd86fda648bf30d46c9ad3c92afa92bed1f6a4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334961"
---
# <a name="add-custom-data-to-resources-using-extensions"></a>Agregar datos personalizados a los recursos mediante extensiones

Microsoft Graph proporciona un único punto de conexión de API que le da acceso a información y datos centrados en personas enriquecidos a través de varios recursos como [user](/graph/api/resources/user?view=graph-rest-1.0) y [message](/graph/api/resources/message?view=graph-rest-1.0). También puede extender Microsoft Graph con sus propios datos de aplicación. Puede agregar propiedades personalizadas a los recursos de Microsoft Graph sin necesidad de un almacén de datos externo.

Por ejemplo, puede que no desee que su aplicación ocupe mucho espacio y almacenar datos específicos del usuario específico de la aplicación en Microsoft Graph extendiendo el recurso **user**. O puede que desee conservar el perfil de usuario existente en su aplicación y simplemente agregar un identificador de almacenamiento específico de aplicación al recurso **user**.

Microsoft Graph ofrece dos tipos de extensiones. Elija el tipo de extensión que mejor se adapte a sus necesidades de aplicación:

- **Extensiones abiertas**: Una buena manera para que los desarrolladores empiecen a trabajar.
- **Extensiones de esquema**: Un mecanismo más versátil para los desarrolladores que se preocupan por el almacenamiento de datos escritos, que hace su esquema reconocible y compartible, y les permitirá en el futuro realizar la autorización y validación de datos de entrada.

> **Importante:** No debe utilizar extensiones para almacenar información de identificación personal confidencial, como credenciales de cuenta, números de identificación gubernamentales, información de propietarios de tarjetas de crédito, datos de cuentas bancarias, información médica o antecedentes delicados.

## <a name="supported-resources"></a>Recursos admitidos

En la tabla siguiente, se enumeran los recursos que admiten extensiones abiertas y de esquema, y se indica si tienen un estado de disponibilidad general (GA) (disponibles en los puntos de conexión beta y v1.0) o si están en versión preliminar (disponibles solo en el punto de conexión beta).

|Recurso |Extensiones abiertas |Extensiones de esquema |
|:------- |:------ |:------ |
| [Unidad administrativa](/graph/api/resources/administrativeunit?view=graph-rest-beta) | Solo versión preliminar | Solo versión preliminar |
| [Evento de calendario](/graph/api/resources/event?view=graph-rest-1.0) | GA | GA |
| [Dispositivo](/graph/api/resources/device?view=graph-rest-1.0) | GA | GA |
| [Grupo](/graph/api/resources/group?view=graph-rest-1.0) | GA | GA |
| [Evento de calendario de grupo](/graph/api/resources/event?view=graph-rest-1.0) | GA | GA |
| [Publicación de conversación de grupo](/graph/api/resources/post?view=graph-rest-1.0) | GA | GA |
| [Mensaje](/graph/api/resources/message?view=graph-rest-1.0) | GA | GA |
| [Organización](/graph/api/resources/organization?view=graph-rest-1.0) | GA | GA |
| [Contacto personal](/graph/api/resources/contact?view=graph-rest-1.0)| GA | GA |
| [Usuario](/graph/api/resources/user?view=graph-rest-1.0) | GA | GA |

Puede usar las extensiones de todos estos recursos al iniciar sesión con una cuenta profesional o educativa. Además, puede usar las extensiones en los recursos **event**, **post**, **group**, **message**, **contact** y **user** al iniciar sesión con una cuenta personal.

## <a name="open-extensions"></a>Extensiones abiertas

Las [extensiones abiertas](/graph/api/resources/opentypeextension?view=graph-rest-1.0) (anteriormente conocidas como extensiones de datos de Office 365) son [tipos abiertos](https://www.odata.org/getting-started/advanced-tutorial/#openType) que ofrecen una forma flexible de agregar datos de la aplicación sin tipo directamente a una instancia de recurso.

Las extensiones abiertas, junto con sus datos personalizados, son accesibles a través de la propiedad de navegación **extensions** de la instancia del recurso.
La propiedad **extensionName** es la única propiedad _predefinida_ y modificable una extensión abierta. Al crear una extensión abierta, debe asignar a la propiedad **NombreExtensión** un nombre que sea único dentro del inquilino.

Una forma de hacerlo es usar un método inverso del formato de nombres de dominio (DNS) que dependa de _su propio dominio_, por ejemplo, `Com.Contoso.ContactInfo`.

No use el dominio de Microsoft (`Com.Microsoft` o `Com.OnMicrosoft`) en un nombre de extensión.

Puede [crear una extensión abierta](/graph/api/opentypeextension-post-opentypeextension?view=graph-rest-1.0) en una instancia de recurso y almacenar datos personalizados en ella en la misma operación (tenga en cuenta la [limitación conocida](known-issues.md#extensions) para algunos de los recursos admitidos).

Posteriormente, puede [leer](/graph/api/opentypeextension-get?view=graph-rest-1.0), [actualizar](/graph/api/opentypeextension-update?view=graph-rest-1.0) o [eliminar](/graph/api/opentypeextension-delete?view=graph-rest-1.0) la extensión y sus datos.

Ejemplo de extensión abierta: [Agregar datos personalizados a los usuarios mediante extensiones abiertas](extensibility-open-users.md)

## <a name="schema-extensions"></a>Extensiones de esquema

Las [extensiones de esquema](/graph/api/resources/schemaextension?view=graph-rest-1.0) permiten definir un esquema que puede usar para extender un tipo de recurso. En primer lugar, se crea una definición de extensión de esquema. Después, se utiliza para ampliar las instancias de recurso con datos personalizados inflexibles. Además, es posible controlar el [estado](#schema-extensions-lifecycle) de la extensión de esquema y permitir que sea reconocible por otras aplicaciones. Estas aplicaciones, a su vez, pueden utilizar la extensión para sus datos y crear experiencias adicionales a partir de ella.

Al crear una definición de extensión de esquema, debe proporcionar un nombre único para su **id**. Existen dos opciones de nomenclaturas:

- Si ya tiene un dominio de cortesía `.com`, `.net`, `.gov`, `.edu` o `.org` que haya comprobado con su arrendatario, puede usar el nombre de dominio junto con el nombre de esquema para definir un nombre exclusivo, con este formato \{_&#65279;nombreDominio_\}\_\{_&#65279;nombreEsquema_\}. Por ejemplo, si su dominio de cortesía es contoso.com, puede definir un **id.** de `contoso_mySchema`. Esta es la opción preferida.
- Si no tiene un dominio de cortesía comprobado, solo puede establecer el **id** a un esquema de nombres (sin un prefijo de nombre de dominio), por ejemplo, `mySchema`. Microsoft Graph le asignará un identificador de cadena basado en el nombre proporcionado en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}.  Por ejemplo, `extkvbmkofy_mySchema`.

Verá que este nombre único en el **id.** se usa como el nombre del tipo complejo que almacenará sus datos personalizados en la instancia de recurso extendido.

A diferencia de las extensiones abiertas, la administración de las definiciones de extensión de esquema ([list](/graph/api/schemaextension-list?view=graph-rest-1.0), [create](/graph/api/schemaextension-post-schemaextensions?view=graph-rest-1.0), [get](/graph/api/schemaextension-get?view=graph-rest-1.0), [update](/graph/api/schemaextension-update?view=graph-rest-1.0) y [delete](/graph/api/schemaextension-delete?view=graph-rest-1.0)) y de sus datos (agregar, obtener, actualizar y eliminar datos) son conjuntos independientes de operaciones de API.

Como las extensiones de esquema son accesibles como tipos complejos en las instancias de los recursos de destino, puede realizar operaciones CRUD en los datos personalizados en una extensión de esquema de las siguientes maneras:

- Utilice el método de recurso `POST` para especificar datos personalizados al crear una nueva instancia del recurso. Tenga en cuenta que hay un [problema conocido](known-issues.md#creating-a-resource-instance-and-adding-schema-extension-data-at-the-same-time) con los recursos de **contacto**, **evento**, **mensaje** y **publicación** que requiere la creación de una extensión de esquema con una operación `PATCH`.
- Utilice el método de recurso `GET` para leer los datos personalizados.
- Utilice el método de recurso `PATCH` para agregar o actualizar datos personalizados en una instancia de recurso existente.
- Utilice el método de recurso `PATCH` para establecer el tipo complejo en null, para eliminar los datos en la instancia de recurso personalizados.

Ejemplo de extensión de esquema: [Agregar datos personalizados a los grupos mediante extensiones de esquema](extensibility-schema-groups.md)

### <a name="schema-extensions-lifecycle"></a>Ciclo de vida de extensiones de esquema

Cuando la aplicación crea una definición de extensión de esquema, se marca como propietaria de esa extensión de esquema.

La aplicación propietaria puede mover la extensión a través de diferentes estados de un ciclo de vida, mediante una operación PATCH en su propiedad **status**. Dependiendo del estado actual, el propietario de la aplicación puede actualizar o eliminar la extensión. Las actualizaciones de una extensión de esquema solo deberían ser aditivas y de no separación.

|Estado |Comportamiento de estado de ciclo de vida |
|:-------------|:------------|
| InDevelopment | <ul><li>Estado inicial después de su creación. El propietario de la aplicación aún está desarrollando la extensión de esquema. </li><li>En este estado, cualquier aplicación que esté en el mismo directorio donde se ha registrado la aplicación propietaria puede ampliar las instancias de recursos con esta definición de esquema (siempre y cuando la aplicación tenga los permisos de ese recurso). </li><li>Solamente la aplicación propietaria puede actualizar la definición de extensión con cambios que se incorporen o eliminarla. </li><li>La aplicación del propietario puede mover la extensión de **InDevelopment** al estado **Disponible**.</li></ul> |
| Disponible | <ul><li>La extensión de esquema está disponible para su uso por todas las aplicaciones de los inquilinos. </li><li>Después de que la aplicación propietaria establezca la extensión en **Disponible**, cualquier aplicación puede simplemente agregar datos personalizados a instancias de esos tipos de recursos especificadas en la extensión (siempre que la aplicación tenga permisos para ese recurso). La aplicación puede asignar datos personalizados al crear una nueva instancia o al actualizar una instancia existente. </li><li>Solamente la aplicación propietaria puede actualizar la definición de extensión con cambios que se incorporen. Ninguna aplicación puede eliminar la definición de la extensión en este estado. </li><li>La aplicación del propietario puede mover la extensión de esquema de **Disponible** al estado **En desuso**.</li></ul> |
| En desuso | <ul><li>La definición de la extensión de esquema ya no se puede leer o modificar. </li><li>Ninguna aplicación puede ver, actualizar, agregar nuevas propiedades o eliminar la extensión. </li><li>Sin embargo, las aplicaciones todavía pueden leer, actualizar o eliminar los _valores de la propiedad_ de la extensión existente. </li></ul> |

### <a name="supported-property-data-types"></a>Tipos de datos de propiedad admitidos

Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:

| Tipo de propiedad | Observaciones |
|:-------------|:------------|
| Binario | Máximo de 256 bytes. |
| Booleano | No se admite para los mensajes, eventos y publicaciones. |
| DateTime | Debe especificarse en el formato ISO 8601. Se almacenarán en UTC. |
| Entero | Valor de 32 bits. No se admite para los mensajes, eventos y publicaciones. |
| String | Máximo de 256 caracteres. |

> **Nota:** No se admiten propiedades de varios valores.

### <a name="azure-ad-directory-schema-extensions"></a>Extensiones de esquema de directorio de Azure AD

Azure AD es compatible con un tipo similar de extensiones, conocido como las [extensiones de esquema de directorio](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-directory-schema-extensions), en unos pocos recursos [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0). Aunque debe utilizar la [API Graph de Azure AD](https://msdn.microsoft.com/library/azure/ad/graph/api/api-catalog) para crear y administrar las definiciones de las extensiones de esquema de directorio, puede utilizar la API de Microsoft Graph para agregar, obtener, actualizar y eliminar _datos_ en las propiedades de estas extensiones.

## <a name="permissions"></a>Permisos

Los mismos [permisos](./permissions-reference.md) necesarios para leer de o escribir en un recurso específico, también son necesarios para hacerlo en cualquier extensión de datos de dicho recurso. Por ejemplo, para que una aplicación pueda actualizar el perfil del usuario que ha iniciado sesión con datos personalizados de la misma, esta debe tener el permiso *User.ReadWrite.all*.

Además, para crear y administrar definiciones de extensión de esquema, una aplicación debe contar con el permiso *Directory.AccessAsUser.All*.

## <a name="data-limits"></a>Límites de datos

### <a name="open-extension-limits"></a>Límites de extensión abiertos

Los límites siguientes se aplican a los recursos de directorio (como **user**, **group**, **device**):

- Cada extensión abierta puede tener hasta 2 KB de datos (incluida la propia definición de extensión).
- Una aplicación puede agregar hasta dos extensiones abiertas por cada instancia del recurso.

Los siguientes límites se aplican a los recursos de Outlook (como **message**, **event** y **contact**):

- Cada extensión abierta se almacena en una [propiedad con nombre MAPI](https://msdn.microsoft.com/library/cc765864(v=office.15).aspx), que es un recurso limitado en el buzón de correo de un usuario. Para obtener más información, consulte [Tipo de recurso openTypeExtension](/graph/api/resources/opentypeextension?view=graph-rest-1.0).

### <a name="schema-extension-limits"></a>Límites de extensión del esquema

Una aplicación no puede crear más de cinco definiciones de **extensión del esquema**.

## <a name="known-limitations"></a>Limitaciones conocidas

Para ver las limitaciones conocidas al usar las extensiones, consulte la [sección de extensiones](known-issues.md#extensions) del artículo de problemas conocidos.

## <a name="extension-examples"></a>Ejemplos de extensión

- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](extensibility-open-users.md)

- [Agregar datos personalizados a los grupos mediante extensiones de esquema](extensibility-schema-groups.md)

## <a name="see-also"></a>Consulte también

- [Dominios de Office 365](https://technet.microsoft.com/es-ES/library/office-365-domains.aspx)

- [Agregar y comprobar un dominio para un inquilino de Office 365](https://office365support.ca/adding-and-verifying-a-domain-for-the-new-office-365/)
