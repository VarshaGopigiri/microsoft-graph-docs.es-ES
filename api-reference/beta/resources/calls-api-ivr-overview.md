---
title: Escenarios IVR en las llamadas
description: 'Los siguientes son los escenarios de respuesta de voz interactiva (IVR) que admiten las API de llamada en Microsoft Graph:'
author: VinodRavichandran
ms.openlocfilehash: cf7d6543c09b69050db9aedc270616cfea113c28
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380474"
---
# <a name="ivr-scenarios-in-calls"></a><span data-ttu-id="a3713-103">Escenarios IVR en las llamadas</span><span class="sxs-lookup"><span data-stu-id="a3713-103">IVR scenarios in calls</span></span>

> <span data-ttu-id="a3713-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a3713-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a3713-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a3713-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a3713-106">Los siguientes son los escenarios de respuesta de voz interactiva (IVR) que admiten las API de llamada en Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="a3713-106">The following are the Interactive Voice Response (IVR) scenarios that the calling APIs in Microsoft Graph support:</span></span>

- <span data-ttu-id="a3713-107">Reproducir un mensaje de audio - por ejemplo, cuando se realiza una llamada en la cola del agente de servicio de atención al cliente.</span><span class="sxs-lookup"><span data-stu-id="a3713-107">Playing an audio prompt - for example, when a call is placed in a customer service agent's queue.</span></span>
- <span data-ttu-id="a3713-108">Registro - por ejemplo, para registrar el audio del autor de la llamada, normalmente después de que escuche un símbolo del sistema con las opciones.</span><span class="sxs-lookup"><span data-stu-id="a3713-108">Record - for example, to record the caller's audio, usually after they heard a prompt with options.</span></span>
- <span data-ttu-id="a3713-109">Suscribirse a tono - por ejemplo, cuando desea saber qué DTMF tonos de llamada el autor de la llamada seleccionada, normalmente tras escuchar el mensaje de audio.</span><span class="sxs-lookup"><span data-stu-id="a3713-109">Subscribe to tone - for example, when you want to know what DTMF tones the caller selected, usually after hearing the audio prompt.</span></span>
- <span data-ttu-id="a3713-110">Cancelar el procesamiento de medios - por ejemplo, cuando desea cancelar cualquier operación de registro o PlayPrompt que podría estar en proceso.</span><span class="sxs-lookup"><span data-stu-id="a3713-110">Cancel Media Processing - for example, when you want to cancel any PlayPrompt or Record operations that might be in process.</span></span>
