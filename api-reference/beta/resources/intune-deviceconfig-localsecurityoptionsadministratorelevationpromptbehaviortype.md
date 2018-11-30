---
title: tipo de enumeración localSecurityOptionsAdministratorElevationPromptBehaviorType
description: Valores posibles para LocalSecurityOptionsAdministratorElevationPromptBehavior
ms.openlocfilehash: 2959aebbb12bc567427c8a9b06a5ce2380933241
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086599"
---
# <a name="localsecurityoptionsadministratorelevationpromptbehaviortype-enum-type"></a>tipo de enumeración localSecurityOptionsAdministratorElevationPromptBehaviorType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para LocalSecurityOptionsAdministratorElevationPromptBehavior
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|No configurado|
|elevateWithoutPrompting|1|Elevar sin preguntar.|
|promptForCredentialsOnTheSecureDesktop|2|Símbolo del sistema para las credenciales en el escritorio seguro|
|promptForConsentOnTheSecureDesktop|3|Pedir consentimiento en el escritorio seguro|
|promptForCredentials|4|Solicitud de credenciales|
|promptForConsent|5|Solicitud de consentimiento|
|promptForConsentForNonWindowsBinaries|6|Pedir consentimiento para archivos binarios que no son de Windows|





