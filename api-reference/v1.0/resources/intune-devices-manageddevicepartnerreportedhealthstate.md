---
title: tipo de enumeración managedDevicePartnerReportedHealthState
description: Estados de mantenimiento disponible para la API de estado de dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 85d6731fc34bb3133fa7aed631d3d687a45a7dce
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919053"
---
# <a name="manageddevicepartnerreportedhealthstate-enum-type"></a>tipo de enumeración managedDevicePartnerReportedHealthState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estados de mantenimiento disponible para la API de estado de dispositivo
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|Estado de mantenimiento del dispositivo no se ha notificado|
|activado|1|Dispositivo se ha activado por un socio de defensa de amenaza móvil, pero aún no ha notificado mantenimiento.|
|desactivado|2|Se ha desactivado el dispositivo por un socio de defensa de amenaza móvil. No se conoce el estado del dispositivo.|
|protegido|3|Dispositivo se considera protegidos por el socio de defensa de amenaza móvil.|
|lowSeverity|4|Dispositivo se considera una amenaza baja por el socio de defensa de amenaza móvil.|
|mediumSeverity|5|Dispositivo se considera como amenaza mediana por el socio de defensa de amenaza móvil.|
|highSeverity|6|Dispositivo se considera como amenaza alto por el socio de defensa de amenaza móvil.|
|no responde|7|Dispositivo se considera que no responden por el socio de defensa de amenaza móvil. No se conoce el estado del dispositivo.|
|en riesgo|8|Dispositivo se considera en riesgo por el socio de defensa contra las amenazas. Esto significa que el dispositivo tiene una amenaza activo o el riesgo que no se corrigió fácilmente por el usuario final y el usuario debe ponerse en contacto con su administrador de TI.|
|configuración errónea|9|Dispositivo se considera mal configurado con el socio de defensa contra las amenazas. Esto significa que el dispositivo falta un perfil requerido o configuración del socio de defensa de amenaza funcione correctamente y, por lo tanto, amenaza o no es capaz de completar el análisis de riesgos.|



