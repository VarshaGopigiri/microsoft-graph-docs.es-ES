---
title: tipo de enumeración managedAppDataEncryptionType
description: Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
ms.openlocfilehash: 7efda037bc2b4d5794c575823845c0955be46477
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031431"
---
# <a name="managedappdataencryptiontype-enum-type"></a>tipo de enumeración managedAppDataEncryptionType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|useDeviceSettings|0|Datos de aplicación se cifran en función de la configuración predeterminada en el dispositivo.|
|afterDeviceRestart|1|Datos de aplicación se cifran cuando se reinicia el dispositivo.|
|whenDeviceLockedExceptOpenFiles|2|Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado, excepto los datos de los archivos que están abiertos|
|whenDeviceLocked|3|Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado|



