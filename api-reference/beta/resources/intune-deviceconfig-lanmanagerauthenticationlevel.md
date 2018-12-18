---
title: tipo de enumeración lanManagerAuthenticationLevel
description: Valores posibles para LanManagerAuthenticationLevel
author: tfitzmac
ms.openlocfilehash: fd5d63f262b9b6e9a27060725e721cb81c495a57
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308746"
---
# <a name="lanmanagerauthenticationlevel-enum-type"></a>tipo de enumeración lanManagerAuthenticationLevel

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para LanManagerAuthenticationLevel
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|lmAndNltm|0|Enviar respuestas de LM y NTLM|
|lmNtlmAndNtlmV2|1|Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar|
|lmAndNtlmOnly|2|Enviar respuestas de LM y NTLM|
|lmAndNtlmV2|3|Enviar respuestas de LM & NTLMv2|
|lmNtlmV2AndNotLm|4|Enviar respuestas de LM y NTLMv2 únicamente. Rechazar LM|
|lmNtlmV2AndNotLmOrNtm|5|Enviar respuestas de LM y NTLMv2 únicamente. Rechazar LM y NTLM|





