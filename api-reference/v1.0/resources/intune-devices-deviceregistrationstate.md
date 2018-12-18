---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
author: tfitzmac
ms.openlocfilehash: 9fdd5cd3a63472e841f0d97f8cbee3a0f548380d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320094"
---
# <a name="deviceregistrationstate-enum-type"></a>tipo de enumeración deviceRegistrationState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de registro de dispositivo.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|no registradas|0|El dispositivo no está registrado.|
|registrado|2|El dispositivo está registrado.|
|revocado|3|El dispositivo se ha bloqueado, borre o retirado.|
|keyConflict|4|El dispositivo tiene un conflicto de clave.|
|approvalPending|5|El dispositivo está pendiente de aprobación.|
|certificateReset|6|Se ha restablecido el certificado del dispositivo.|
|notRegisteredPendingEnrollment|7|El dispositivo no está registrado y las pendientes de inscripción.|
|desconocido|8|El estado de registro de dispositivo es desconocido.|



