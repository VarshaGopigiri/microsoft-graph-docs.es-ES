---
title: tipo de enumeración defenderThreatAction
description: Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
ms.openlocfilehash: a5eb108a3ab26596eec9abe838e3bbfe853d96d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031483"
---
# <a name="defenderthreataction-enum-type"></a>tipo de enumeración defenderThreatAction

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|Aplicar la acción en función de la definición de actualización.|
|clean|1|Limpiar la amenaza detectada.|
|cuarentena|2|La amenaza detectada en cuarentena.|
|remove|3|Quitar la amenaza detectada.|
|Permitir|4|Permitir la amenaza detectada.|
|userDefined|5|Permitir que el usuario determinar la acción que se realizará con la amenaza detectada.|
|bloque|6|Bloquear la amenaza detectada.|



