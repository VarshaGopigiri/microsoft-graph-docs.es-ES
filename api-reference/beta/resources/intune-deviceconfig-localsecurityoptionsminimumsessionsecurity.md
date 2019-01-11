---
title: tipo de enumeración localSecurityOptionsMinimumSessionSecurity
description: Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: fb6912e7d3bba42364849165cceb28050ddacfae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833239"
---
# <a name="localsecurityoptionsminimumsessionsecurity-enum-type"></a>tipo de enumeración localSecurityOptionsMinimumSessionSecurity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|none|0|Enviar respuestas de LM y NTLM|
|requireNtmlV2SessionSecurity|1|Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar|
|require128BitEncryption|2|Enviar respuestas de LM y NTLM|
|ntlmV2And128BitEncryption|3|Enviar respuestas de LM & NTLMv2|





