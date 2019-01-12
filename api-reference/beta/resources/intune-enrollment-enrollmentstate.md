---
title: tipo de enumeración enrollmentState
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9394755c5b6e6de8ed039b226d03074f1ef16cc3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933592"
---
# <a name="enrollmentstate-enum-type"></a>tipo de enumeración enrollmentState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|Se desconoce el estado de inscripción de dispositivo|
|inscrito|1|Dispositivo está inscrito.|
|pendingReset|2|Inscritos pero lo está inscrito a través de perfil de inscripción y el perfil inscrito es diferente del perfil asignado.|
|failed|3|No se inscriben y no hay registro de errores de inscripción.|
|notContacted|4|Dispositivo se importa, pero no se inscriben.|
|bloqueado|5|Dispositivo está inscrito como userless, pero se bloquea de mover a inscripción de usuario porque no se pudo instalar la aplicación.|





