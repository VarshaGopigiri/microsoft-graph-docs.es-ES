---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
ms.openlocfilehash: 9f9ee23d385ce4a7fca73e2d296c3f34063fc218
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028977"
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



