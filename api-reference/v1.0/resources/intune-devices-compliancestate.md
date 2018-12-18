---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
author: tfitzmac
ms.openlocfilehash: 3045685518f1c7718f9a5f46cd10e0add6fe05b3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330278"
---
# <a name="compliancestate-enum-type"></a>tipo de enumeración complianceState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de cumplimiento.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|Unknown (desconocido).|
|compatible con|1|Compatible con.|
|no compatible|2|Dispositivo no cumple y se bloquea de recursos corporativos.|
|conflicto|3|Conflicto con otras reglas.|
|error|4|Error|
|inGracePeriod|254|Dispositivo no cumple pero todavía tiene acceso a recursos corporativos|
|configManager|255|Administrado por el Administrador de configuración|



