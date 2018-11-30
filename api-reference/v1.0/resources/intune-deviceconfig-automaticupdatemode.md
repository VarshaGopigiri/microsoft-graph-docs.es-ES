---
title: tipo de enumeración automaticUpdateMode
description: Valores posibles para el modo de actualización automática.
ms.openlocfilehash: c98927e1c1f66e3bf10fa07496aa54ac91bad20b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029047"
---
# <a name="automaticupdatemode-enum-type"></a>tipo de enumeración automaticUpdateMode

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para el modo de actualización automática.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Definido por el usuario, valor predeterminado, sin intención.|
|notifyDownload|1|Notificar al descargarlos.|
|autoInstallAtMaintenanceTime|2|Instalación automática en tiempo de mantenimiento.|
|autoInstallAndRebootAtMaintenanceTime|3|La instalación automática y reinicie el equipo en el momento de mantenimiento.|
|autoInstallAndRebootAtScheduledTime|4|La instalación automática y reinicie el equipo en la hora programada.|
|autoInstallAndRebootWithoutEndUserControl|5|La instalación automática y reiniciar sin control de usuario final|



