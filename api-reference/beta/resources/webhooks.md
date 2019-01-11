---
title: Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios
description: La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios. Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea el conjunto de seguridad de las notificaciones de los cambios en los datos de usuario.
localization_priority: Normal
ms.openlocfilehash: 9b1907d37115e21b41a9e957de9b7ae0a32fd311
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816474"
---
# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a>Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios. Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](/graph/webhooks).

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

En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription-post-subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.

| Tipo de permiso                        | Tipos de recursos admitidos                                                      |
| :------------------------------------- | :------------------------------------------------------------------------------------ |
| Delegado: cuenta profesional o educativa     | [póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][] |
| Delegado: cuenta personal de Microsoft | [póngase en contacto con][], [unidad][], [evento][], [mensaje][]                                        |
| Aplicación                            | [póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][] |

## <a name="see-also"></a>Consulte también

- [Tipo de recurso de suscripción](subscription.md)
- [Suscripciones de lista](../api/subscription-list.md)
- [Obtener suscripción](../api/subscription-get.md)
- [Crear suscripción](../api/subscription-post-subscriptions.md)
- [Actualizar suscripción](../api/subscription-update.md)
- [Eliminar suscripción](../api/subscription-delete.md)

[contact]: ./contact.md
[conversation]: ./conversation.md
[drive]: ./drive.md
[event]: ./event.md
[group]: ./group.md
[message]: ./message.md
[user]: ./user.md
[alerta]: ./alert.md
