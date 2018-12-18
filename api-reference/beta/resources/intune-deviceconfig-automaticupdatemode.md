---
title: tipo de enumeración automaticUpdateMode
description: Valores posibles para el modo de actualización automática.
author: tfitzmac
ms.openlocfilehash: d1bf3903b71dbd06be9151d67a925f374eb1f803
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344047"
---
# <a name="automaticupdatemode-enum-type"></a>tipo de enumeración automaticUpdateMode

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





