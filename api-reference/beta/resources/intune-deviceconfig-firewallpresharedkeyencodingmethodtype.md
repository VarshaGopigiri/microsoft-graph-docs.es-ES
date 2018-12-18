---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
author: tfitzmac
ms.openlocfilehash: 3ed2456f54bd27a3efa04d959edba48f7c100692
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324937"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a>tipo de enumeración firewallPreSharedKeyEncodingMethodType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallPreSharedKeyEncodingMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|ninguno|1|No se ha codificado clave previamente compartida. En su lugar, se guarda en su formato de caracteres anchos|
|utF8|2|Codificar la clave previamente compartida con UTF-8|





