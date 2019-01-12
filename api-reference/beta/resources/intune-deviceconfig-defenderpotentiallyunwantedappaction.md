---
title: tipo de enumeración defenderPotentiallyUnwantedAppAction
description: Acción de Defender tomar detectado potencialmente no deseados aplicación (PUA).
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 96a3dd70ae0f56f2d0d5a9d6c4f87846e10bba45
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938562"
---
# <a name="defenderpotentiallyunwantedappaction-enum-type"></a>tipo de enumeración defenderPotentiallyUnwantedAppAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acción de Defender tomar detectado potencialmente no deseados aplicación (PUA).
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|Protección de PUA está desactivada. Defender no protegerá contra aplicaciones potencialmente no deseadas.|
|bloque|1|Protección de PUA está activada. Elementos detectados están bloqueados. Se muestran en el historial de junto con otras amenazas.|
|auditoría|2|Modo de auditoría. Defender se detecta aplicaciones potencialmente no deseadas, pero no tomar ninguna acción. Puede revisar información acerca de las aplicaciones Defender habría tomado acción contra buscando creados por Defender en el evento Visor de eventos.|





