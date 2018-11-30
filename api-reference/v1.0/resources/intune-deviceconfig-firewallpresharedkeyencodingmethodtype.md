---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
ms.openlocfilehash: 238d2b0845b0d79ea109cea5b326914815d600de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030798"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a>tipo de enumeración firewallPreSharedKeyEncodingMethodType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallPreSharedKeyEncodingMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|ninguno|1|No se ha codificado clave previamente compartida. En su lugar, se guarda en su formato de caracteres anchos|
|utF8|2|Codificar la clave previamente compartida con UTF-8|



