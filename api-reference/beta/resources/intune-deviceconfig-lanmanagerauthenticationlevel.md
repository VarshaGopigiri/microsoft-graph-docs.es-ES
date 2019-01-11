---
title: tipo de enumeración lanManagerAuthenticationLevel
description: Valores posibles para LanManagerAuthenticationLevel
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 68af209a005dc1d7e8d25672f5e97e1d929ba25b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866916"
---
# <a name="lanmanagerauthenticationlevel-enum-type"></a>tipo de enumeración lanManagerAuthenticationLevel

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para LanManagerAuthenticationLevel
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|lmAndNltm|0|Enviar respuestas de LM y NTLM|
|lmNtlmAndNtlmV2|1|Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar|
|lmAndNtlmOnly|2|Enviar respuestas de LM y NTLM|
|lmAndNtlmV2|3|Enviar respuestas de LM & NTLMv2|
|lmNtlmV2AndNotLm|4|Enviar respuestas de LM y NTLMv2 únicamente. Rechazar LM|
|lmNtlmV2AndNotLmOrNtm|5|Enviar respuestas de LM y NTLMv2 únicamente. Rechazar LM y NTLM|





