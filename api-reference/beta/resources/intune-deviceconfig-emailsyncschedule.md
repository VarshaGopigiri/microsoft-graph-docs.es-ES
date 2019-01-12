---
title: tipo de enumeración emailSyncSchedule
description: Valores posibles para la programación de sincronización de correo electrónico.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9dc93bce19262d0b1aad1d1cc8f28ea4db56ce9f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924044"
---
# <a name="emailsyncschedule-enum-type"></a>tipo de enumeración emailSyncSchedule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para la programación de sincronización de correo electrónico.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Definido por el usuario, valor predeterminado, sin intención.|
|asMessagesArrive|1|Sincronizar que llegan mensajes.|
|Manual|2|Sincronizar manualmente.|
|fifteenMinutes|3|Sincronización de cada 15 minutos.|
|thirtyMinutes|4|Sincronización de cada 30 minutos.|
|sixtyMinutes|5|Sincronización de cada 60 minutos.|
|basedOnMyUsage|6|Según mi uso de sincronización.|





