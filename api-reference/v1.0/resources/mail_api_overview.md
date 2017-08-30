# <a name="use-the-microsoft-graph-api-to-integrate-with-outlook-mail"></a>Usar la API de Microsoft Graph para integrar con el correo de Outlook

Microsoft Graph permite que su aplicación obtenga acceso autorizado a los datos de correo de Outlook de un usuario en una cuenta personal o de organización. Con los [permisos apropiados delegados o de la aplicación](../../../concepts/permissions_reference.md), su aplicación puede tener acceso a los datos de correo del usuario que ha iniciado sesión o cualquier usuario en un espacio empresarial. Los datos de correo pueden estar en la nube en Exchange Online como parte de Office 365 o en Exchange local en una [implementación híbrida](../../../concepts/hybrid_rest_support.md).

## <a name="using-the-mail-rest-api"></a>Uso de la API de REST de correo
Se realizan solicitudes de API de correo en nombre de un [usuario](../resources/user.md) que puede identificarse por la propiedad de **id.** de un usuario (un GUID único), la dirección de correo electrónico o el alias de acceso directo `me` para el usuario que ha iniciado sesión.

Los mensajes de correo electrónico están representados por el recurso [message](../resources/message.md) y organizados en una carpeta [mailFolder](../resources/mailfolder.md). Los mensajes y las carpetas de correo se identifican por su propiedad de **id.**, que puede obtenerse de las operaciones `GET`. 

>**Nota:** En general, no se debe suponer que los id. **message** y **mailfolder** son únicos e inmutables dentro un buzón. Se podrían cambiar tras determinadas acciones como copiar, mover o enviar. 

Los cuerpos del mensaje se pueden mostrar en formato de texto o HTML.

Puede utilizar nombres de carpeta conocidos como `Inbox`, `Drafts`, `SentItems` o `DeletedItems` para identificar ciertas carpetas de correo que existen de forma predeterminada para todos los usuarios. Por ejemplo, puede obtener los mensajes en la carpeta **Elementos enviados** de Outlook del usuario que ha iniciado sesión, sin obtener primero el id. de la carpeta:
```
GET /me/mailFolders('SentItems')/messages?$select=sender,subject
```

## <a name="common-use-cases"></a>Casos de uso común 

El recurso **message** expone propiedades como **categories**, **conversationId**, **flag** e **importance** que corresponden a las funciones disponibles en la interfaz de usuario, lo que permite a las aplicaciones automatizarse o integrarse con la experiencia de usuario integrada de Outlook. 

La API de Microsoft Graph también proporciona métodos y acciones que admiten casos de uso común de mensajes.

| Casos de uso        | Recursos de REST | Consulte también |
|:---------------|:--------|:----------|
| **Acciones centradas en el usuario** | | |
| Borrador, leer, responder, reenviar, enviar, actualizar o eliminar los mensajes | [message](../resources/message.md) | [Métodos de message](../resources/message.md#methods) |
| Delegar a otro usuario para enviar mensajes en nombre del propietario del buzón | [message](../resources/message.md) | Configuración de las propiedades **de** y **remitente** en un [mensaje](../resources/message.md) |
| Permitir que el usuario vea primero los mensajes más importantes | [inferenceClassificationOverride](../resources/inferenceClassificationOverride.md) | [Bandeja de entrada Prioritarios](../resources/manage_focused_inbox.md) |
| Agregar, obtener o eliminar datos adjuntos de un mensaje | [attachment](../resources/attachment.md), <br> [fileAttachment](../resources/fileattachment.md), <br> [itemAttachment](../resources/itemattachment.md), <br> [referenceAttachment](../resources/referenceattachment.md), <br> [message](../resources/message.md) | [Métodos de attachment](../resources/attachment.md#methods) |
| Obtener o actualizar la configuración regional, la zona horaria o la respuesta automática de un usuario | [mailboxSettings](../resources/mailboxsettings.md), <br> [automaticRepliesSetting](../resources/automaticrepliessetting.md), <br> [localeInfo](../resources/localeinfo.md) | [Obtener la configuración del buzón del usuario](../api/user_get_mailboxsettings.md), <br> [Actualizar la configuración del buzón del usuario](../api/user_update_mailboxsettings.md), |
| **Administración de carpetas y correo** | | |
| Organizar los mensajes en una jerarquía de carpetas del correo | [mailFolder](../resources/mailfolder.md)  | [Métodos de mailFolder](../resources/mailfolder.md#methods) |
| Buscar y filtrar mensajes | [message](../resources/message.md) | [Parámetros de consulta](../../../concepts/query_parameters.md)  |
| Obtener notificaciones de los cambios en los mensajes de una carpeta | [subscription](../resources/subscription.md) | [Trabajar con webhooks en Microsoft Graph](../resources/webhooks.md) |
| Sincronizar la jerarquía de carpetas del correo o los mensajes | [message](../resources/message.md) | [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md) |
| **Desarrollo de aplicaciones** | | |
| Agregar datos personalizados de la aplicación a un mensaje utilizando extensiones | [openTypeExtension](../resources/opentypeextension.md), <br>[schemaExtension](../resources/schemaextension.md) | [Agregar datos personalizados a los recursos mediante extensiones](../../../concepts/extensibility_overview.md) |
| Datos personalizados de acceso para las propiedades de MAPI de Outlook subexpuestas | [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md), <br> [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) | [Información general sobre las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) |

## <a name="next-steps"></a>Siguientes pasos
La API de correo puede abrir nuevas formas de comunicarse con los usuarios: 

- Profundizar en los [métodos](../resources/message.md#methods), las [propiedades](../resources/message.md#properties) y las [relaciones](../resources/message.md#relationships) de los recursos [message](../resources/message.md) y [mailFolder](../resources/mailfolder.md).
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/en-us/graph/graph-explorer).

¿Necesita más ideas? Vea [cómo algunos de nuestros socios utilizan Microsoft Graph](https://developer.microsoft.com/en-us/graph/graph/examples#partners).


