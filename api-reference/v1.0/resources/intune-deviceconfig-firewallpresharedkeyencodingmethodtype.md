---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bba6033985f2b960a272134614d98acc7203a9d8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871753"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a>tipo de enumeración firewallPreSharedKeyEncodingMethodType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallPreSharedKeyEncodingMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|none|1|No se ha codificado clave previamente compartida. En su lugar, se guarda en su formato de caracteres anchos|
|utF8|2|Codificar la clave previamente compartida con UTF-8|



