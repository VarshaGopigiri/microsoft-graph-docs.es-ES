---
title: tipo de enumeración defenderPromptForSampleSubmission
description: Valores posibles para solicitar información de usuario para el envío de ejemplos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8dfc1a3aeb80a22041f799fb40ff9b2cc6e3870b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924828"
---
# <a name="defenderpromptforsamplesubmission-enum-type"></a>tipo de enumeración defenderPromptForSampleSubmission

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para solicitar información de usuario para el envío de ejemplos.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Definido por el usuario, valor predeterminado, sin intención.|
|alwaysPrompt|1|Preguntar siempre.|
|promptBeforeSendingPersonalData|2|Preguntar antes de enviar datos personales.|
|neverSendData|3|No enviar nunca datos.|
|sendAllDataWithoutPrompting|4|Enviar todos los datos sin preguntar.|





