---
title: tipo de enumeración managedAppDataEncryptionType
description: Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
author: tfitzmac
ms.openlocfilehash: 3cbb733eb578ca839e32851d8a6d217f69d6799d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330327"
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



