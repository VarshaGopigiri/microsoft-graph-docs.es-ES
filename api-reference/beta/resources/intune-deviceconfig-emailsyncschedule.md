---
title: tipo de enumeración emailSyncSchedule
description: Valores posibles para la programación de sincronización de correo electrónico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 178cba9e226b7f20e3fd917145e7bbd06f6c3a1a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838398"
---
# <a name="emailsyncschedule-enum-type"></a>tipo de enumeración emailSyncSchedule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para la programación de sincronización de correo electrónico.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|userDefined|0|Definido por el usuario, valor predeterminado, sin intención.|
|asMessagesArrive|1|Sincronizar que llegan mensajes.|
|Manual|2|Sincronizar manualmente.|
|fifteenMinutes|3|Sincronización de cada 15 minutos.|
|thirtyMinutes|4|Sincronización de cada 30 minutos.|
|sixtyMinutes|5|Sincronización de cada 60 minutos.|
|basedOnMyUsage|6|Según mi uso de sincronización.|





