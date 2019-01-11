---
title: tipo de enumeración managementAgentType
description: Tipo de agente de administración.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 66441a37b417cef13cbb09219a26a98250cbf610
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888490"
---
# <a name="managementagenttype-enum-type"></a>tipo de enumeración managementAgentType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Tipo de agente de administración.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|EAS|1|El dispositivo se administra mediante Exchange server.|
|MDM|2|El dispositivo se administra mediante la Intune MDM.|
|easMdm|3|El dispositivo se administra mediante Exchange server y MDM. Intune|
|intuneClient|4|Intune administrados de cliente.|
|easIntuneClient|5|El dispositivo está EAS y Intune administrados de cliente dual.|
|configurationManagerClient|8|El dispositivo se administra mediante el Administrador de configuración.|
|configurationManagerClientMdm|10|El dispositivo está administrado por el Administrador de configuración y MDM.|
|configurationManagerClientMdmEas|11|El dispositivo está administrado por el Administrador de configuración, MDM y Eas.|
|desconocido|16|Tipo de agente de administración desconocido.|
|jamf|32|Los atributos del dispositivo se obtienen de Jamf.|
|googleCloudDevicePolicyController|64|El dispositivo se administra mediante CloudDPC de Google.|



