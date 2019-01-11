---
title: tipo de enumeración remoteAction
description: Acciones remotas Intune admite.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e12b3c52ebe40dd8bccad56bdbc9c291486177c3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847162"
---
# <a name="remoteaction-enum-type"></a>tipo de enumeración remoteAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acciones remotas Intune admite.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|desconocido|0|Usuario inicia una acción desconocida.|
|factoryReset|1|Usuario inicia una acción a la fábrica de restablece un dispositivo. |
|removeCompanyData|2|Usuario inicia una acción para quitar los datos de la compañía de un dispositivo. |
|resetPasscode|3|Usuario inicia una acción para quitar el código de acceso de un dispositivo de iOS o restablecer la contraseña de Android / dispositivo de Windows. |
|remoteLock|4|Usuario inicia una acción a bloqueo remoto de un dispositivo.|
|enableLostMode|5|Usuario inicia una acción para habilitar el modo pierden en un dispositivo iOS controlados.|
|disableLostMode|6|Usuario inicia una acción para deshabilitar el modo pierden en un dispositivo iOS controlados.|
|locateDevice|7|Usuario inicia una acción para buscar un dispositivo iOS controlados.|
|rebootNow|8|Usuario inicia una acción para reiniciar un dispositivo de Windows.|
|recoverPasscode|9|Usuario inicia una acción para restablecer el NIP de passport para trabajar en el dispositivo de windows phone.|
|cleanWindowsDevice|10|Usuario inicia una acción de limpieza de dispositivo de windows.|
|logoutSharedAppleDeviceActiveUser|11|Usuario inicia una acción para cerrar la sesión de usuario actual en el dispositivo de apple compartida.|
|quickScan|12|Usuario inicia una acción para ejecutar el examen rápido en el dispositivo.|
|fullScan|13|Usuario inicia una acción para ejecutar el examen completo en el dispositivo.|
|windowsDefenderUpdateSignatures|14|Usuario inicia una acción para actualizar las firmas de malware en el dispositivo.|
|factoryResetKeepEnrollmentData|15|Usuario inicia un dispositivo de borrado remoto de acción con mantenimiento de los datos de inscripción.|
|updateDeviceAccount|16|Usuario inicia una acción para actualizar la cuenta en el dispositivo.|
|automaticRedeployment|17|Usuario inicia una acción a los puentes reimplementar el dispositivo|
|Apagado|18|Usuario inicia una acción a apagar el dispositivo.|





