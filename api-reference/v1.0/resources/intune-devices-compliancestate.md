---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5a4f4c359665eb1a0087f64802b5e7c829002fd6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940200"
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



