---
title: tipo de enumeración localSecurityOptionsMinimumSessionSecurity
description: Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 822c996d788fd5edb5c92f876c725b771b051c15
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952485"
---
# <a name="localsecurityoptionsminimumsessionsecurity-enum-type"></a>tipo de enumeración localSecurityOptionsMinimumSessionSecurity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|none|0|Enviar respuestas de LM y NTLM|
|requireNtmlV2SessionSecurity|1|Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar|
|require128BitEncryption|2|Enviar respuestas de LM y NTLM|
|ntlmV2And128BitEncryption|3|Enviar respuestas de LM & NTLMv2|





