# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a>Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios

La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios. Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](../../../concepts/webhooks.md).

Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:

- Mensajes
- Eventos
- Contacts
- Usuarios
- Grupos
- Conversaciones de grupo
- Contenido compartido en OneDrive, incluidas las unidades asociadas con los sitios de SharePoint
- Carpetas OneDrive personales de los usuarios
- Alertas de seguridad

## <a name="permissions"></a>Permisos

En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription_post_subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.

| Tipo de permiso                        | Tipos de recursos admitidos en v1.0                                 |
| :------------------------------------- | :--------------------------------------------------------------- |
| Delegado: cuenta profesional o educativa     | [póngase en contacto con][], [conversación][], [unidad][], [evento][], [mensaje][], [alerta][] |
| Delegado: cuenta personal de Microsoft | Ninguno                                                             |
| Aplicación                            | [póngase en contacto con][], [conversación][], [evento][], [mensaje][], [alerta][]           |

## <a name="see-also"></a>Recursos adicionales

- [Tipo de recurso de suscripción](./subscription.md)
- [Obtener suscripción](../api/subscription_get.md)
- [Crear suscripción](../api/subscription_post_subscriptions.md)
- [Actualizar suscripción](../api/subscription_update.md)
- [Eliminar suscripción](../api/subscription_delete.md)

[contact]: ./contact.md
[conversation]: ./conversation.md
[drive]: ./drive.md
[event]: ./event.md
[message]: ./message.md
[alerta]: ./alert.md