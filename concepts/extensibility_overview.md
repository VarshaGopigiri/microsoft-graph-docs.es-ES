# <a name="add-custom-data-to-resources-using-extensions"></a>Agregar datos personalizados a los recursos mediante extensiones

Microsoft Graph proporciona un único punto de conexión de API que le da acceso a información y datos centrados en personas enriquecidos a través de varios recursos como [user](../api-reference/beta/resources/user.md) y [message](../api-reference/beta/resources/message.md). Ahora hay una forma de _**extender**_ Microsoft Graph con sus propios datos de aplicación. Puede agregar propiedades personalizadas a los recursos de Microsoft Graph sin necesidad de un almacén de datos externo. Por ejemplo, puede que no desee que su aplicación ocupe mucho espacio y almacenar datos específicos del usuario específico de la aplicación en Microsoft Graph extendiendo el recurso **user**. O puede que desee conservar el perfil de usuario existente en su aplicación y simplemente agregar un identificador de almacenamiento específico de aplicación al recurso **user**.

Microsoft Graph ofrece dos tipos de extensiones. Elija el tipo de extensión que mejor se adapte a sus necesidades de aplicación:

*  **Extensiones abiertas**: Una buena manera para que los desarrolladores empiecen a trabajar.
*  **Extensiones de esquema**: Un mecanismo más versátil para los desarrolladores que se preocupan por el almacenamiento de datos escritos, que hace su esquema reconocible y compartible, y les permitirá en el futuro realizar la autorización y validación de datos de entrada.

>**Importante:** No debe utilizar extensiones para almacenar información de identificación personal confidencial, como credenciales de cuenta, números de identificación gubernamentales, información de propietarios de tarjetas de crédito, datos de cuentas bancarias, información médica o antecedentes delicados.

## <a name="supported-resources"></a>Recursos admitidos

En la siguiente tabla, se muestra la compatibilidad actual para las extensiones de esquema y abiertas, tanto si están en disponibilidad general (GA /v1.0 y /beta) o solo en versión preliminar (/beta). 

| Recurso | Extensiones abiertas | Extensiones de esquema |
|---------------|-------|-------|
| [Unidad administrativa](../api-reference/beta/resources/administrativeunit.md) | Solo versión preliminar | Próximamente |
|  [evento de calendario](../api-reference/beta/resources/event.md) | GA | Solo versión preliminar |
|  [evento de calendario](../api-reference/beta/resources/event.md) de grupo | GA | Solo versión preliminar |
|  [Publicación](../api-reference/beta/resources/post.md) de subproceso de conversación de grupo | GA | Solo versión preliminar |
|  [dispositivo](../api-reference/beta/resources/device.md) | Solo versión preliminar | Solo versión preliminar |
|  [grupo](../api-reference/beta/resources/group.md) | Solo versión preliminar | Solo versión preliminar |
|  [mensaje](../api-reference/beta/resources/message.md) | GA | Solo versión preliminar |
|  [organización](../api-reference/beta/resources/organization.md) | Solo versión preliminar | Próximamente |
|  [Contacto personal](../api-reference/beta/resources/contact.md)| GA | Próximamente |
|  [usuario](../api-reference/beta/resources/user.md) | Solo versión preliminar | Solo versión preliminar |

## <a name="open-extensions"></a>Extensiones abiertas
Las [extensiones abiertas](../api-reference/beta/resources/opentypeextension.md) (anteriormente conocidas como extensiones de datos de Office 365) son [tipos abiertos](http://www.odata.org/getting-started/advanced-tutorial/#openType) que ofrecen una forma flexible de agregar datos de la aplicación sin tipo directamente a una instancia de recurso. 

Las extensiones abiertas, junto con sus datos personalizados, son accesibles a través de la propiedad de navegación **extensions** de la instancia del recurso. La propiedad **extensionName** es la única propiedad _predefinida_ y modificable una extensión abierta. Al crear una extensión abierta, debe asignar a la propiedad **NombreExtensión** un nombre que sea único dentro del inquilino. Una forma de hacerlo es usar un método inverso del formato de nombres de dominio (DNS) que dependa de _su propio dominio_, por ejemplo, `Com.Contoso.ContactInfo`. No use el dominio de Microsoft (`Com.Microsoft` o `Com.OnMicrosoft`) en un nombre de extensión.

Puede [crear una extensión abierta](../api-reference/beta/api/opentypeextension_post_opentypeextension.md) en una instancia de recurso y almacenar datos personalizados en ella en la misma operación (tenga en cuenta la [siguiente limitación conocida](#known-limitations-for-extensions) para algunos de los recursos admitidos). Posteriormente, puede [leer](../api-reference/beta/api/opentypeextension_get.md), [actualizar](../api-reference/beta/api/opentypeextension_update.md) o [eliminar](../api-reference/beta/api/opentypeextension_delete.md) la extensión y sus datos. 

>**Nota:** Las extensiones abiertas generalmente han estado disponibles (GA) para los eventos, los mensajes del grupo, los mensajes y los contactos personales. Ahora también están disponibles para unidades administrativas, dispositivos, grupos, organizaciones y usuarios en la versión preliminar.

Ejemplo de extensión abierta: [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](extensibility_open_users.md)

## <a name="schema-extensions-preview"></a>Extensiones de esquema (versión preliminar)
Las [extensiones de esquema](../api-reference/beta/resources/schemaextension.md) permiten definir un esquema que puede utilizar para extender un tipo de recurso. En primer lugar, se crea una definición de extensión de esquema. Después, se utiliza para ampliar las instancias de recurso con datos personalizados inflexibles. Además, es posible controlar el [estado](#schema-extensions-lifecycle) de la extensión de esquema y permitir que sea reconocible por otras aplicaciones. Estas aplicaciones, a su vez, pueden utilizar la extensión para sus datos y crear experiencias adicionales a partir de ella.

Al crear una definición de extensión de esquema, debe proporcionar un nombre único para su **id**. Existen dos opciones de nomenclaturas:

- Si ya tiene un dominio de cortesía `.com` que haya comprobado con su arrendatario, puede utilizar el nombre de dominio junto con el nombre de esquema para definir un nombre exclusivo, con este formato \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}. Por ejemplo, si su dominio de cortesía es contoso.com, puede definir un **id** de `contoso_mySchema`.  Esta es la opción preferida.
- Si no tiene un dominio de cortesía comprobado, solo puede establecer el **id** a un esquema de nombres (sin un prefijo de nombre de dominio), por ejemplo, `mySchema`. Microsoft Graph le asignará un identificador de cadena basado en el nombre proporcionado en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}.  Por ejemplo, `extkvbmkofy_mySchema`.

Verá que este nombre único en el **id** se utiliza como el nombre del tipo complejo que almacenará sus datos personalizados en la instancia de recurso extendido. 


A diferencia de las extensiones abiertas, la administración de las definiciones de extensión de esquema ([list](../api-reference/beta/api/schemaextension_list.md), [create](../api-reference/beta/api/schemaextension_post_schemaextensions.md), [get](../api-reference/beta/api/schemaextension_get.md), [update](../api-reference/beta/api/schemaextension_update.md) y [delete](../api-reference/beta/api/schemaextension_delete.md)) y sus datos (agregar, obtener, actualizar y eliminar datos) son conjuntos independientes de operaciones de API. 

Puesto que las extensiones de esquema son accesibles como tipos complejos en las instancias de los recursos de destino, puede realizar operaciones CRUD en los datos en una extensión de esquema de las siguientes maneras:

- Utilice el método de recurso `POST` para especificar datos personalizados al crear una nueva instancia del recurso.
- Utilice el método de recurso `GET` para leer los datos personalizados.
- Utilice el método de recurso `PATCH` para agregar o actualizar datos personalizados en una instancia de recurso existente.
- Utilice el método de recurso `PATCH` para establecer el tipo complejo en null, para eliminar los datos en la instancia de recurso personalizados. 

Ejemplo de extensión de esquema: [Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)](extensibility_schema_groups.md)


### <a name="schema-extensions-lifecycle"></a>Ciclo de vida de extensiones de esquema
Cuando la aplicación crea una definición de extensión de esquema, se marca como propietaria de esa extensión de esquema. 

La aplicación propietaria puede mover la extensión a través de diferentes estados de un ciclo de vida, mediante una operación PATCH en su propiedad **status**. Dependiendo del estado actual, el propietario de la aplicación puede actualizar o eliminar la extensión. Las actualizaciones de una extensión de esquema solo deberían ser aditivas y de no separación.


| Estado | Comportamiento de estado de ciclo de vida |
|-------------|------------|
| InDevelopment | - Estado inicial después de su creación. El propietario de la aplicación aún está desarrollando la extensión de esquema. <br> - En este estado, solo el propietario de la aplicación puede utilizar la extensión de esquema. La aplicación propietaria puede actualizar la definición de extensión con cambios que se incorporen o eliminarla. Solo la aplicación propietaria puede ampliar instancias de recursos con esta definición de esquema y solo en el mismo directorio donde está registrada la aplicación propietaria. <br> - La aplicación propietaria puede mover la extensión del estado `InDevelopment` a `Available`. |
| Available | - La extensión de esquema está disponible para su uso por todas las aplicaciones de los inquilinos. <br> - Una vez que la aplicación propietaria establezca la extensión en `Available`, cualquier aplicación puede simplemente agregar datos personalizados a instancias de esos tipos de recursos especificadas en la extensión (siempre que la aplicación tenga permisos para ese recurso). La aplicación puede asignar datos personalizados al crear una nueva instancia o al actualizar una instancia existente. Solo la aplicación propietaria puede actualizar la definición de extensión con cambios que se incorporen o eliminarla. <br> - La aplicación propietaria también puede mover la extensión de esquema del estado `Available` a `Deprecated`. |
| Deprecated | - La definición de la extensión de esquema ya no se puede leer o modificar. <br> - Ninguna aplicación puede ver, actualizar, agregar nuevas propiedades o eliminar la extensión. Sin embargo, las aplicaciones todavía pueden leer, actualizar o eliminar los _valores de la propiedad_ de la extensión. <br> - La aplicación propietaria puede devolver la extensión de esquema del estado `Deprecated` a `Available`. |

>**Nota:** Puede continuar accediendo a los datos personalizados o eliminándolos en una extensión de esquema en el estado `Deprecated`. Sin embargo, actualmente, hay un [problema conocido](#known-limitations-for-extensions) que hace que se pierda el acceso a sus datos personalizados una vez que se elimina la extensión de esquema.

### <a name="supported-property-data-types"></a>Tipos de datos de propiedad admitidos 
Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:

| Tipo de propiedad | Observaciones |
|-------------|------------|
| Binario | Máximo de 256 bytes. |
| Booleano | No se admite para los mensajes, eventos y publicaciones. |
| DateTime | Debe especificarse en el formato ISO 8601. Se almacenarán en UTC. |
| Entero | Valor de 32 bits. No se admite para los mensajes, eventos y publicaciones. |
| String | Máximo de 256 caracteres. |

>**Nota:** Actualmente no se admiten propiedades de varios valores.

### <a name="azure-ad-directory-schema-extensions"></a>Extensiones de esquema de directorio de Azure AD
Azure AD es compatible con un tipo similar de extensiones, conocido como las [extensiones de esquema de directorio](https://msdn.microsoft.com/en-us/library/azure/ad/graph/howto/azure-ad-graph-api-directory-schema-extensions), en unos pocos recursos [directoryObject](../api-reference/beta/resources/directoryObject.md). Aunque debe utilizar la API Graph de Azure AD para crear y administrar las definiciones de las extensiones de esquema de directorio, puede utilizar la API Graph de Microsoft para agregar, obtener, actualizar y eliminar _datos_ en las propiedades de estas extensiones.

## <a name="permissions"></a>Permisos
Los mismos [permisos](../authorization/permission_scopes.md) necesarios para leer de o escribir en un recurso específico, también son necesarios para hacerlo en cualquier extensión de datos de dicho recurso.  Por ejemplo, para que una aplicación pueda actualizar el perfil del usuario que ha iniciado sesión con datos personalizados de la misma, esta debe tener el permiso *User.ReadWrite.all*.

Además, para crear y administrar definiciones de extensión de esquema, una aplicación debe contar con el permiso *Directory.AccessAsUser.All*.
 
## <a name="known-limitations-for-extensions"></a>Limitaciones conocidas para extensiones
-   No se puede especificar una extensión abierta a la vez que se crea una instancia de **administrativeUnit**, **device**, **group**, **organization** o **user**. Debe crear primero la instancia y después especificar los datos de extensión abierta en una solicitud ``POST`` posterior en esa instancia.  
-   El seguimiento de cambios (consulta de delta) aún no se admite para las propiedades de extensiones abiertas o de esquema.
-   Aún no se admite el filtrado de los valores de propiedad de una extensión del sistema (pero pronto será posible).
-   Eliminar una definición de extensión de esquema quitará el acceso a los datos personalizados agregados en función del esquema eliminado. Es una limitación temporal.
-   Actualmente, es posible eliminar una extensión de esquema en todos los estados. En el futuro, solo se podrán eliminar las extensiones de esquema en el estado `InDevelopment`.
-   Para quitar un tipo complejo de extensión de esquema de una instancia de recurso, debe establecer todos los valores de propiedad de tipo complejo en `null`.  En el futuro, esto será posible estableciendo el tipo complejo de extensión de esquema en `null`.
-   Los recursos de directorio, como usuarios, grupos y dispositivos, limitan en la actualidad a 100 el número total de valores de propiedad de extensión de esquema que pueden establecerse en un recurso.

## <a name="extension-examples"></a>Ejemplos de extensión
[Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](extensibility_open_users.md)

[Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)](extensibility_schema_groups.md)

## <a name="see-also"></a>Recursos adicionales

[Dominios de Office 365](https://technet.microsoft.com/en-us/library/office-365-domains.aspx)

[Agregar y comprobar un dominio para un inquilino de Office 365](http://office365support.ca/adding-and-verifying-a-domain-for-the-new-office-365/)
