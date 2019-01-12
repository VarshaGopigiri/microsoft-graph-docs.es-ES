---
title: tipo de enumeración eapFastConfiguration
description: Configuraciones disponibles para la configuración de EAP-FAST.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 65165929d388ed57f2651a0d277996e56d2f046e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954459"
---
# <a name="eapfastconfiguration-enum-type"></a>tipo de enumeración eapFastConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuraciones disponibles para la configuración de EAP-FAST.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|noProtectedAccessCredential|0|Usar EAP-FAST sin credenciales de acceso protegido (PAC).|
|useProtectedAccessCredential|1|Uso protegida credenciales de acceso (PAC).|
|useProtectedAccessCredentialAndProvision|2|Uso de acceso protegido (PAC) de credenciales y aprovisionamiento PAC.|
|useProtectedAccessCredentialAndProvisionAnonymously|3|Use acceso credencial protegido (PAC), PAC de aprovisionamiento y hacerlo de forma anónima.|





