---
title: tipo de enumeración defenderPotentiallyUnwantedAppAction
description: Acción de Defender tomar detectado potencialmente no deseados aplicación (PUA).
localization_priority: Normal
ms.openlocfilehash: 9b04cd6daeae303910519d0735165171575d8c44
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858649"
---
# <a name="defenderpotentiallyunwantedappaction-enum-type"></a>tipo de enumeración defenderPotentiallyUnwantedAppAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acción de Defender tomar detectado potencialmente no deseados aplicación (PUA).
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|deviceDefault|0|Protección de PUA está desactivada. Defender no protegerá contra aplicaciones potencialmente no deseadas.|
|bloque|1|Protección de PUA está activada. Elementos detectados están bloqueados. Se muestran en el historial de junto con otras amenazas.|
|auditoría|2|Modo de auditoría. Defender se detecta aplicaciones potencialmente no deseadas, pero no tomar ninguna acción. Puede revisar información acerca de las aplicaciones Defender habría tomado acción contra buscando creados por Defender en el evento Visor de eventos.|





