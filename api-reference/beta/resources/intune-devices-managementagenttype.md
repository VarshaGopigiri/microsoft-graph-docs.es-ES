---
title: tipo de enumeración managementAgentType
description: Tipo de agente de administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1711ad647afabc2b8877bd2f99b049bd1c1dd4e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914286"
---
# <a name="managementagenttype-enum-type"></a>tipo de enumeración managementAgentType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Tipo de agente de administración.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
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
|microsoft365ManagedMdm|258|Este dispositivo está administrado por Microsoft 365 a través de Intune.|





