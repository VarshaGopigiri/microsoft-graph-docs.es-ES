---
title: tipo de enumeración wiFiSecurityType
description: Tipos de seguridad de Wi-Fi.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6ddadaa31febaea08050ad49ffa540de53ff4819
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920222"
---
# <a name="wifisecuritytype-enum-type"></a>tipo de enumeración wiFiSecurityType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Tipos de seguridad de Wi-Fi.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|Abra|0|Abra (sin autenticación).|
|wpaPersonal|1|WPA-Personal.|
|wpaEnterprise|2|WPA-Enterprise. Debe usar el tipo de IOSEnterpriseWifiConfiguration para configurar las opciones de la empresa.|
|WEP|3|Cifrado WEP.|
|wpa2Personal|4|WPA2-Personal.|
|wpa2Enterprise|5|WPA2-empresa. Debe usar el tipo de WindowsWifiEnterpriseEAPConfiguration para configurar las opciones de la empresa.|





