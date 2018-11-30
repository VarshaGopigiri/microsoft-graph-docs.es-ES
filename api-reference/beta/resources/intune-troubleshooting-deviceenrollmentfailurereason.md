---
title: tipo de enumeración deviceEnrollmentFailureReason
description: Categorías de errores de nivel superior para la inscripción.
ms.openlocfilehash: c0062a829811d9fb25453adb260d4d2be0295dd7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089469"
---
# <a name="deviceenrollmentfailurereason-enum-type"></a>tipo de enumeración deviceEnrollmentFailureReason

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Categorías de errores de nivel superior para la inscripción.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|Valor predeterminado, el motivo del error es desconocido.|
|autenticación|1|Error de autenticación|
|autorización|2|La llamada se ha autenticado pero no autorizado para inscribirse.|
|accountValidation|3|Error al validar la cuenta para la inscripción. (Cuenta bloqueada, no se ha habilitado la inscripción)|
|userValidation|4|No se pudo validar el usuario. (Usuario no existe, licencia que faltan)|
|deviceNotSupported|5|Dispositivo no es compatible para la administración de dispositivos móviles.|
|inMaintenance|6|Cuenta está en mantenimiento.|
|badRequest|7|Cliente envió una solicitud que no se entiende/admitidos por el servicio.|
|featureNotSupported|8|Utilizado por este inscripción las características no se admiten para esta cuenta.|
|enrollmentRestrictionsEnforced|9|Restricciones de inscripción configuradas por el administrador bloquean esta inscripción.|
|clientDisconnected|10|Cliente agotó el tiempo de espera o inscripción se anuló por para el usuario final.|
|userAbandonment|11|Se ha cancelado la inscripción por para el usuario final. (Para el usuario final inicia la incorporación de redes pero no se pudo completar en forma oportuna)|





