---
title: API de retransmisión de dispositivo de Microsoft Graph (versión preliminar)
description: 'Hoy en día, las personas interactúan a diario con varios dispositivos. Los usuarios suelen iniciar actividades de entretenimiento y tareas de productividad en un dispositivo y continuarlas en otro. Para satisfacer las necesidades de sus clientes, sus aplicaciones deben poder cambiar entre dispositivos y plataforma sin problemas. '
ms.openlocfilehash: aa3bdd3401be9d26f55d5b3dcc792ed81e7dae87
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092853"
---
# <a name="device-relay-api-in-microsoft-graph-preview"></a>API de retransmisión de dispositivo de Microsoft Graph (versión preliminar)

Hoy en día, las personas interactúan a diario con varios dispositivos. Los usuarios suelen iniciar actividades de entretenimiento y tareas de productividad en un dispositivo y continuarlas en otro. Para satisfacer las necesidades de sus clientes, sus aplicaciones deben poder cambiar entre dispositivos y plataforma sin problemas. 

Puede usar la API de retransmisión de dispositivo para ofrecer una experiencia perfecta a los usuarios. Puede hacer posible que transfieran activamente una experiencia de un dispositivo a otro, o que la mejoren utilizando varios dispositivos a la vez. Esto se hace a través de acciones integradas en la aplicación (botón o selección en la aplicación) que llaman a la API de retransmisión de dispositivo para detectar dispositivos de los usuarios y permitirles iniciar la aplicación en esos otros dispositivos y enviarle mensajes.

## <a name="why-integrate-with-device-relay"></a>¿Por qué realizar la integración a través de la retransmisión de dispositivo?

La API de retransmisión de dispositivo permite a la aplicación registrarse y detectar la aplicación en los dispositivos del usuario, ejecutar comandos y enviarle mensajes. De este modo, puede convertir las tareas en las que sus clientes trabajan en el eje fundamental. Pueden trabajar en el dispositivo que les resulte más cómodo; solo tienen que detectarlo y transferirle tareas. También pueden mejorar una experiencia continua con la aplicación mediante otros dispositivos a su alrededor.

Puede usar la API de retransmisión de dispositivo en dispositivos complementarios o escenarios de control remoto. Use las funcionalidades de mensajería para crear un canal de aplicaciones entre dos dispositivos con el fin de enviar y recibir mensajes personalizados. Por ejemplo, puede permitir que los clientes utilicen el teléfono para controlar la reproducción en un televisor. También puede ofrecer una aplicación complementaria en un escenario de productividad mostrando acciones de uso común basadas en el contexto en un teléfono mientras sus usuarios trabajan en la vista principal de la aplicación en su PC.

Los clientes también pueden transferir activamente una experiencia de un dispositivo a otro realizando una acción en su aplicación. Por ejemplo, un usuario puede estar viendo una difusión en directo en su teléfono mientras está en el autobús, pero cuando llega a casa quiere transferir la reproducción a su PC de la sala de estar. También se admiten escenarios de productividad con la retransmisión de dispositivo. 

### <a name="extend-the-experience"></a>Extender la experiencia

Extienda el uso de la aplicación ofreciendo una experiencia de usuario para detectar dispositivos e iniciar la aplicación en ellos. Por ejemplo, puede que el usuario esté trabajando en un pedido de compra en su teléfono, detecte su PC de la oficina e inicie allí la aplicación para acabar de completar el pedido de compra.  

### <a name="augment-the-experience"></a>Aumentar la experiencia

Cree una experiencia complementaria de la aplicación en otro de los dispositivos del usuario. Por ejemplo, la aplicación puede incluir una experiencia de usuario que se inicie en otros dispositivos. En un juego, el usuario puede iniciar la aplicación en un dispositivo con una pantalla más grande (por ejemplo, de su PC a una Xbox). La Xbox podría presentar una vista completa del juego (una vista en primera persona), mientras que el dispositivo con la pantalla más pequeña podría presentar una vista diferente con contexto adicional (una vista de nivel superior del nivel de juego que muestra la ubicación del jugador y de los oponentes).  

### <a name="enrich-the-experience"></a>Enriquecer la experiencia

Agregue capacidades adicionales de control a la aplicación. Por ejemplo, especifique capacidades de control remoto para la aplicación principal desde un dispositivo complementario. Cuando el usuario inicia una aplicación de un dispositivo a otro, el dispositivo de destino podría mostrar toda la experiencia (por ejemplo, un modelo 3D en una aplicación de diseño), mientras que el dispositivo de origen podría mostrar una lista de las acciones más comunes según el estado de la aplicación en el dispositivo de destino (por ejemplo, girar, cambiar el tamaño o cambiar la paleta de colores).

## <a name="see-also"></a>Vea también

- [Cross-device experiences in Microsoft Graph](cross-device-concept-overview.md) (Experiencias entre dispositivos en Microsoft Graph)
- [Learn more about the device relay API](/graph/api/resources/project-rome-overview?view=graph-rest-beta) (Más información sobre la API de retransmisión de dispositivo)
- [Learn more about Project Rome](https://aka.ms/projectrome) (Más información sobre Project Rome)
