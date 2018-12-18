---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
author: tfitzmac
ms.openlocfilehash: a622613bd4ca5e065c3d9eb0331c05c360c1837c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360546"
---
# <a name="deviceregistrationstate-enum-type"></a>tipo de enumeración deviceRegistrationState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





