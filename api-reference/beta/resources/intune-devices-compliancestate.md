---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
ms.openlocfilehash: c49c0ecc2511f612e743fb5d86a53d150d3fbf45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089427"
---
# <a name="compliancestate-enum-type"></a>tipo de enumeración complianceState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





