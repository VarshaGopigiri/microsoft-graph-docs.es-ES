---
title: tipo de enumeración localSecurityOptionsMinimumSessionSecurity
description: Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
ms.openlocfilehash: 969c7d6576c613f5214bfc3b8a5a1ad36722f0df
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089000"
---
# <a name="localsecurityoptionsminimumsessionsecurity-enum-type"></a>tipo de enumeración localSecurityOptionsMinimumSessionSecurity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|ninguno|0|Enviar respuestas de LM y NTLM|
|requireNtmlV2SessionSecurity|1|Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar|
|require128BitEncryption|2|Enviar respuestas de LM y NTLM|
|ntlmV2And128BitEncryption|3|Enviar respuestas de LM & NTLMv2|





