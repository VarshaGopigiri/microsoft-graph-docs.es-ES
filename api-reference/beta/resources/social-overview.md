---
title: Usar la API de gráfico de Microsoft para integrar inteligencia sociales en una aplicación
description: Microsoft Graph admite gestos sociales en contexto social de un usuario y proporciona acceso a personas útiles y datos de contenido social.
ms.openlocfilehash: b83c5ea08c6d66dc800f736717f50324f0e2b4b8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088970"
---
# <a name="use-the-microsoft-graph-api-to-integrate-social-intelligence-in-an-app"></a>Usar la API de gráfico de Microsoft para integrar inteligencia sociales en una aplicación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Microsoft Graph admite gestos sociales en contexto social de un usuario y proporciona acceso a personas útiles y datos de contenido social.

## <a name="aggregate-and-extract-specific-information-about-people"></a>Agregar y extraer información específica acerca de las personas

Utilice el recurso de [persona](../resources/person.md) y agregar información acerca de una persona de la API de personas a través de correo, contactos y las redes sociales. Los resultados se ordenan por su importancia en función de varias relaciones empresariales, colaboración y comunicación. La API permite a examinar, ordenar, seleccionar, filtrar o búsqueda de personas en función de los criterios.

- [List people](../api/user-list-people.md)

## <a name="manage--mentions"></a>Administrar @ menciones

Realizar llamadas a un destinatario notificar y obtener atención del destinatario de un mensaje es un gesto social comunes.
El recurso [mencione](../resources/mention.md) y la API de menciones proporcionan un mecanismo ligero para llamar a un destinatario de un [mensaje](../resources/message.md), obtener todos los mensajes en el que un usuario recibe una notificación mediante una mención @, u obtener cada mención en un mensaje.

<!--
Include the next sentence when supporting events.

**Mention** is also supported by [Event](../resources/event.md).

-->

- Crear menciones en un mensaje nuevo

  - [Crear y enviar menciones como parte de un nuevo mensaje](../api/user-sendmail.md#request-2)
  - [Crear menciones como parte de un borrador de mensaje](../api/user-post-messages.md#request-2)

- Obtener información acerca de menciones en un mensaje

  - [Obtener todos los mensajes en el buzón del usuario que ha iniciado sesión que indiquen el usuario](../api/user-list-messages.md#request-2)
  - [Obtener detalles de cada mención en un mensaje](../api/message-get.md#request-2)

- [Eliminar una mención](../api/message-delete.md#request-2) en un mensaje

## <a name="access-social-data-around-and-about-a-user"></a>Datos de contenido social acceso alrededor y acerca de un usuario

Gráfico de Office encapsula las relaciones entre las distintas entidades en Office 365. Utilice el gráfico de Office para obtener perspectivas sociales a usuarios individuales a través de Office 365.

- Lista de los elementos [tendencias alrededor de](../api/insights-list-trending.md) un usuario
- Los usuarios que han sido [trabajar con](../api/user-list-people.md) la lista de un usuario
