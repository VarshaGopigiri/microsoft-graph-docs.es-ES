---
title: tipo de enumeración firewallCertificateRevocationListCheckMethodType
description: Valores posibles para firewallCertificateRevocationListCheckMethod
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c300b1d3c73cc4ae19ef1282c00d00800243b4b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889281"
---
# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a>tipo de enumeración firewallCertificateRevocationListCheckMethodType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallCertificateRevocationListCheckMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|none|1|No comprobar la lista de revocación de certificados|
|intento de|2|Intente la comprobación de CRL y permitir que un certificado sólo si el certificado está confirmado por la comprobación de|
|requerir|3|Requerir una comprobación CRL correcta antes de permitir que un certificado|





