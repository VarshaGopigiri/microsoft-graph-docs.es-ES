---
title: tipo de enumeración firewallPacketQueueingMethodType
description: Valores posibles para firewallPacketQueueingMethod
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9538db02afc108573338556c8899495ca9c1f26c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957798"
---
# <a name="firewallpacketqueueingmethodtype-enum-type"></a>tipo de enumeración firewallPacketQueueingMethodType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallPacketQueueingMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|deshabilitado|1|Deshabilitar la puesta en cola de paquetes|
|queueInbound|2|Poner en cola los paquetes cifrados entrantes|
|queueOutbound|3|Cola descifra los paquetes salientes para desvío de llamadas|
|queueBoth|4|Paquetes entrantes y salientes en cola|





