---
title: tipo de enumeración windowsUpdateType
description: Qué dispositivos de sucursal recibirá sus actualizaciones desde
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 90d1f946dd497e650df5eb07004560dda028e14f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930344"
---
# <a name="windowsupdatetype-enum-type"></a>tipo de enumeración windowsUpdateType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Qué dispositivos de sucursal recibirá sus actualizaciones desde
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Permitir al usuario que establezca.|
|all|1|Punto y anuales del canal (destino). Dispositivo Obtiene todas las actualizaciones aplicables característica de punto y anuales del canal (destino).|
|businessReadyOnly|2|Punto y anuales del canal. Dispositivo Obtiene las actualizaciones de la característica de punto y anuales del canal.|
|windowsInsiderBuildFast|3|Compilación de información confidencial de Windows - Fast|
|windowsInsiderBuildSlow|4|Compilación de información confidencial de Windows - lento|
|windowsInsiderBuildRelease|5|Versión de lanzamiento de información confidencial de Windows|



