---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
author: tfitzmac
ms.openlocfilehash: b8ab119c58aec6e62c0a32ccf310f43eab029573
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343592"
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



