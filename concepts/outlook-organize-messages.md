---
title: Organizar mensajes de Outlook
description: 'Outlook permite a los clientes organizar sus mensajes como prefieran, tanto si quieren dejar todos sus mensajes en la carpeta Bandeja de entrada como si prefieren organizar sus mensajes en una estructura de carpetas tipo árbol dentro de la Bandeja de entrada para adaptarse a sus necesidades específicas. Puede filtrar, buscar u organizar los mensajes según le convenga en '
author: angelgolfer-ms
ms.openlocfilehash: cb75da8e800fccf13c639188b04b07b62c3c6431
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307542"
---
# <a name="organize-outlook-messages"></a>Organizar mensajes de Outlook

Outlook permite a los clientes organizar sus mensajes como prefieran, tanto si quieren dejar todos sus mensajes en la carpeta Bandeja de entrada como si prefieren organizar sus mensajes en una estructura de carpetas tipo árbol dentro de la Bandeja de entrada para adaptarse a sus necesidades específicas. Puede [filtrar, buscar u ordenar](query-parameters.md) fácilmente los mensajes de todo el buzón del usuario o de carpetas específicas.

## <a name="accessing-mail-folders"></a>Obtener acceso a carpetas de correo

Con programación, las carpetas de mensajes se representan con el recurso [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0), y la bandeja de entrada es una de las carpetas en el directorio raíz de la estructura de carpetas.

Cada **mailFolder** se identifica por su id. de carpeta y tiene una propiedad que permite la escritura **displayName**. Outlook crea otras carpetas para los clientes de forma predeterminada. Puede hacer referencia a estas carpetas predeterminadas por los id. de carpeta, o bien por los nombres conocidos. Para obtener una lista de los nombres de carpetas conocidos disponibles, vea [Tipo de recurso mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0).

Para una carpeta personalizada que no sea predeterminada, si conoce la ruta de la carpeta, puede obtener acceso a la carpeta si primero usa el acceso directo `/users/{id}/mailfolders` para obtener acceso al nivel raíz y obtener todas las carpetas de nivel superior:

```http
GET https://graph.microsoft.com/v1.0/users/{id}/mailFolders
```

Después, especifique el id. de carpeta (`{folder_id}`) al navegar a cada nivel del árbol de carpetas:

```http
GET https://graph.microsoft.com/v1.0/users/{id}/mailFolders/{folder_id}/childfolders
```

Repita este procedimiento hasta que llegue a la carpeta personalizada en el árbol.

## <a name="creating-and-organizing-the-folder-tree"></a>Crear y organizar el árbol de carpetas

Puede [crear carpetas de correo dentro de la bandeja de entrada](/graph/api/user-post-mailfolders?view=graph-rest-1.0), o bien como [carpetas secundarias dentro de otras carpetas](/graph/api/mailfolder-post-childfolders?view=graph-rest-1.0). Al crear, [copiar](/graph/api/mailfolder-copy?view=graph-rest-1.0) o [mover](/graph/api/mailfolder-move?view=graph-rest-1.0) una carpeta y su contenido, Outlook actualiza las propiedades **parentFolderId** y **childFolderCount** de solo lectura de las carpetas correspondientes. Cuando se copia o mueve el contenido de una carpeta a otra carpeta, de forma predeterminada, los id. de entrada individuales de los contenidos también cambiarán.

En el nivel de los contenidos, **totalItemCount** y **unreadItemCount** indican respectivamente el número de elementos y el número de elementos no leídos de una carpeta de correo.
En el nivel de las carpetas secundarias, puede [mostrar una lista de las carpetas secundarias](/graph/api/user-list-mailfolders?view=graph-rest-1.0) dentro de la bandeja de entrada o de cualquier otra carpeta.
La propiedad **childFolderCount** representa el número de carpetas secundarias inmediatas.

Tenga en cuenta que las carpetas de correo de Outlook pueden contener mensajes y elementos que no sean mensajes, como eventos y contactos. En general, las carpetas de Outlook pueden contener elementos heterogéneos.

## <a name="using-rules-to-automate-copying-or-moving-messages"></a>Usar reglas para automatizar la copia o movimiento de mensajes

Outlook permite a los clientes configurar reglas para automatizar acciones específicas en mensajes entrantes cuando se cumplan condiciones predeterminadas. Puede [crear una regla](/graph/api/mailfolder-post-messagerules?view=graph-rest-1.0) para la bandeja de entrada, como [messageRule](/graph/api/resources/messagerule?view=graph-rest-1.0) para copiar o mover un mensaje en una carpeta específica cuando se cumplan condiciones específicas.
Las condiciones son [messageRulePredicates](/graph/api/resources/messagerulepredicates?view=graph-rest-1.0). Algunos ejemplos pueden ser texto que aparezca en el cuerpo o el asunto del mensaje, que el mensaje se envíe desde direcciones de correo electrónico específicas, que el mensaje esté marcado como importante, etc.

## <a name="directing-only-the-messages-you-care-for-to-the-focused-inbox"></a>Dirigir solo los mensajes importantes a la Bandeja de entrada Prioritarios

La Bandeja de entrada Prioritarios permite a los clientes entrenar Outlook para mostrar solo los mensajes entrantes de remitentes que consideren importantes en la pestaña **Prioritarios**, y el resto de los mensajes en la pestaña **Otros correos**. Inicialmente, el sistema de clasificación de Outlook organiza los mensajes de la bandeja de entrada de una forma predeterminada. Puede corregir y entrenar el sistema con el tiempo a través de la interfaz de usuario o con programación. Cuanto más use la Bandeja de entrada Prioritarios, mejor podrá el sistema de clasificación deducir qué mensajes entrantes quiere ver en la pestaña **Prioritarios**.

Con programación, puede actualizar la propiedad **inferenceClassification** de un [mensaje](/graph/api/resources/message?view=graph-rest-1.0) para indicar si quiere ver el mensaje en la pestaña **Prioritarios** o en la pestaña **Otros correos**. Esta es una designación de un solo uso para un mensaje específico. Si, por otra parte, quiere ver mensajes de un remitente específico siempre en la pestaña **Prioritarios** o en la pestaña **Otros correos**, puede [configurar una instrucción](/graph/api/inferenceclassification-post-overrides?view=graph-rest-1.0) para Outlook. Cada instrucción es una instancia de [inferenceClassificationOverride](/graph/api/resources/inferenceclassificationoverride?view=graph-rest-1.0) donde se especifica que el nombre del remitente y la designación de mensajes de ese remitente siempre sea `focused` o `other`. Las instrucciones de cada usuario para la Bandeja de entrada Prioritarios del usuario se almacenan como una colección de instancias de [inferenceClassificationOverride](/graph/api/resources/inferenceclassificationoverride?view=graph-rest-1.0) en el objeto [user](/graph/api/resources/user?view=graph-rest-1.0).

## <a name="keeping-messages-and-mail-folders-up-to-date-in-apps"></a>Mantener actualizados los mensajes y las carpetas de correo en las aplicaciones

Con frecuencia, las aplicaciones tienen que sincronizarse y mantener actualizados los datos de correo de un usuario en el almacén local de la aplicación. Microsoft Graph le permite suscribirse a notificaciones de cambios para recibir notificaciones cuando se produzcan cambios en los datos, y consultar los cambios actuales en cuanto se produzcan.

Las notificaciones se entregan con [webhooks](/graph/api/resources/webhooks?view=graph-rest-1.0) de forma asincrónica cuando se producen los cambios, lo que evita que las aplicaciones se sobrecarguen al tener que sondear frecuentemente. Puede [suscribirse a notificaciones de cambios](/graph/api/subscription-post-subscriptions?view=graph-rest-1.0) de adiciones, actualizaciones o eliminaciones en los datos de correo de un usuario. Por ejemplo, puede crear una suscripción a mensajes en una carpeta específica (por ejemplo, `/me/mailFolders('{folderId'}')`) o en el nivel raíz (por ejemplo, `/me/messages`). La suscripción especifica un elemento **notificationUrl**, donde Microsoft Graph notificará a la aplicación cuando se produzcan los tipos de cambios solicitados.

Para sincronizar inicialmente un buzón de usuario, primero [realice una consulta delta en las carpetas de correo, empezando en el nivel raíz](/graph/api/mailfolder-delta?view=graph-rest-1.0), para sincronizar todas las carpetas de correo, seguido de una [consulta delta de los mensajes en cada carpeta](/graph/api/message-delta?view=graph-rest-1.0) para sincronizar los mensajes individuales.

Para encontrar las entidades exactas que se cambiaron sin tener que leer todo el recurso con cada notificación, puede usar una [consulta delta](delta-query-overview.md) para realizar un seguimiento de los cambios que más le interesen y sincronizar el almacén local con esos cambios. Puede [realizar un seguimiento de los cambios en los mensajes de una carpeta específica](delta-query-messages.md). También puede realizar un seguimiento de los cambios en las carpetas de correo en el nivel raíz (por ejemplo, `/me/mailfolders`).

## <a name="next-steps"></a>Pasos siguientes

Obtenga más información sobre:

- [¿Por qué integrar con el correo de Outlook?](outlook-mail-concept-overview.md)
- [Usar la API de correo](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) y sus [casos de uso](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) en Microsoft Graph v1.0.
