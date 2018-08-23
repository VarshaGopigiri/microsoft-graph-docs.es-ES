# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a>Usar la API de Microsoft Graph para obtener notificaciones de cambios

La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su dirección URL para recibir notificaciones. Las aplicaciones cliente usan notificaciones para actualizar su estado cuando se producen cambios. Para obtener más detalles, incluido cómo suscribirse y gestionar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](../../../concepts/webhooks.md).

Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:

- Mensajes
- Eventos
- Contactos
- Usuarios
- Grupos
- Conversaciones de grupo
- Contenido compartido en OneDrive, incluidas las unidades de disco asociadas a sitios de SharePoint
- Carpetas de OneDrive personales de los usuarios

## <a name="permissions"></a>Permisos

En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription_post_subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.

| Tipo de permiso                        | Tipos de recursos admitidos en v1.0                                 |
| :------------------------------------- | :--------------------------------------------------------------- |
| Delegado: cuenta profesional o educativa     | [contacto][], [conversación][], [unidad de disco][], [evento][], [mensaje][] |
| Delegado: cuenta personal de Microsoft | Ninguno                                                             |
| Aplicación                            | [contacto][], [conversación][], [evento][], [mensaje][]            |

## <a name="see-also"></a>Consulte también

- [Tipo de recurso de suscripción](./subscription.md)
- [Obtener suscripción](../api/subscription_get.md)
- [Crear suscripción](../api/subscription_post_subscriptions.md)
- [Actualizar suscripción](../api/subscription_update.md)
- [Eliminar suscripción](../api/subscription_delete.md)

[contacto]: ./contact.md
[conversación]: ./conversation.md
[unidad de disco]: ./drive.md
[evento]: ./event.md
[mensaje]: ./message.md
