---
title: tipo de enumeración firewallCertificateRevocationListCheckMethodType
description: Valores posibles para firewallCertificateRevocationListCheckMethod
author: tfitzmac
ms.openlocfilehash: ab496b5deb8f096bdc48a2b50a1af994c8ec8d5b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353665"
---
# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a>tipo de enumeración firewallCertificateRevocationListCheckMethodType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallCertificateRevocationListCheckMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|ninguno|1|No comprobar la lista de revocación de certificados|
|intento de|2|Intente la comprobación de CRL y permitir que un certificado sólo si el certificado está confirmado por la comprobación de|
|requerir|3|Requerir una comprobación CRL correcta antes de permitir que un certificado|



