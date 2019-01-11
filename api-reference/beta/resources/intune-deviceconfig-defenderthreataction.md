---
title: tipo de enumeración defenderThreatAction
description: Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
localization_priority: Normal
ms.openlocfilehash: 7e448e6fae0ebbb0f14a3b7932e6f306a70588b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837873"
---
# <a name="defenderthreataction-enum-type"></a>tipo de enumeración defenderThreatAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|deviceDefault|0|Aplicar la acción en función de la definición de actualización.|
|clean|1|Limpiar la amenaza detectada.|
|cuarentena|2|La amenaza detectada en cuarentena.|
|remove|3|Quitar la amenaza detectada.|
|Permitir|4|Permitir la amenaza detectada.|
|userDefined|5|Permitir que el usuario determinar la acción que se realizará con la amenaza detectada.|
|bloque|6|Bloquear la amenaza detectada.|





