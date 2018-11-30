---
title: Escenarios IVR en las llamadas
description: 'Los siguientes son los escenarios de respuesta de voz interactiva (IVR) que admiten las API de llamada en Microsoft Graph:'
ms.openlocfilehash: 22318b2bc755b161a55fc42fd924017545d38e3b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083227"
---
# <a name="ivr-scenarios-in-calls"></a>Escenarios IVR en las llamadas

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Los siguientes son los escenarios de respuesta de voz interactiva (IVR) que admiten las API de llamada en Microsoft Graph:

- Reproducir un mensaje de audio - por ejemplo, cuando se realiza una llamada en la cola del agente de servicio de atención al cliente.
- Registro - por ejemplo, para registrar el audio del autor de la llamada, normalmente después de que escuche un símbolo del sistema con las opciones.
- Suscribirse a tono - por ejemplo, cuando desea saber qué DTMF tonos de llamada el autor de la llamada seleccionada, normalmente tras escuchar el mensaje de audio.
- Cancelar el procesamiento de medios - por ejemplo, cuando desea cancelar cualquier operación de registro o PlayPrompt que podría estar en proceso.
