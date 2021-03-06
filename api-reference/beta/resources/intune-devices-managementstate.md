---
title: tipo de enumeración managementState
description: Estado de administración de dispositivos en Microsoft Intune.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7d9d083c56df366b9f896432328d51c295f62190
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961949"
---
# <a name="managementstate-enum-type"></a>tipo de enumeración managementState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de administración de dispositivos en Microsoft Intune.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|administrado|0|El dispositivo está bajo administración|
|retirePending|1|Un comando de retirada se está produciendo en el dispositivo y en el proceso de unenrolling de administración|
|retireFailed|2|Error en el dispositivo en el comando de retirada|
|wipePending|3|Un comando de barrido se está produciendo en el dispositivo y en el proceso de unenrolling de administración|
|wipeFailed|4|Error en el comando de barrido en el dispositivo|
|mal estado|5|El dispositivo tiene un estado incorrecto.|
|deletePending|6|Un comando de eliminación se está produciendo en el dispositivo |
|retireIssued|7|Un comando de retirada se ha emitido para el dispositivo|
|wipeIssued|8|Se emitió un comando de barrido del dispositivo|
|wipeCanceled|9|Se ha cancelado un comando de barrido para este dispositivo|
|retireCanceled|10|Se ha cancelado un comando de retirada para este dispositivo|
|detectado|11|El dispositivo es detectado pero suscrito no completamente.|





