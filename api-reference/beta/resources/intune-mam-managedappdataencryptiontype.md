---
title: tipo de enumeración managedAppDataEncryptionType
description: Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
ms.openlocfilehash: a642a3efc01f719ca72134f737fe2bdd2596d2b9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089084"
---
# <a name="managedappdataencryptiontype-enum-type"></a>tipo de enumeración managedAppDataEncryptionType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|useDeviceSettings|0|Datos de aplicación se cifran en función de la configuración predeterminada en el dispositivo.|
|afterDeviceRestart|1|Datos de aplicación se cifran cuando se reinicia el dispositivo.|
|whenDeviceLockedExceptOpenFiles|2|Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado, excepto los datos de los archivos que están abiertos|
|whenDeviceLocked|3|Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado|





