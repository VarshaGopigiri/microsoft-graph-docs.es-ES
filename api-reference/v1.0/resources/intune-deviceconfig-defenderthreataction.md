---
title: tipo de enumeración defenderThreatAction
description: Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 51aa26483ac6b79d48567f7e5950733def31f01e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976649"
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



