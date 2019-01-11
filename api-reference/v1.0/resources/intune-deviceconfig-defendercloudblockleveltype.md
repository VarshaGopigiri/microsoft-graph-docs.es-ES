---
title: tipo de enumeración defenderCloudBlockLevelType
description: Posibles valores de nivel de bloque en la nube
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 283bb12c775b1215a1bcfecf4f248882a56573aa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839504"
---
# <a name="defendercloudblockleveltype-enum-type"></a>tipo de enumeración defenderCloudBlockLevelType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de nivel de bloque en la nube
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|No configurado|0|Valor predeterminado, se utiliza el bloqueo de Windows Defender Antivirus predeterminado de nivel y se proporciona una detección de segura sin aumentar el riesgo de detectar legítimos archivos|
|alta|1|Alta aplica a un alto nivel de detección.|
|highPlus|2|Alta + utiliza el nivel alto y se aplica a las medidas de protección de adición|
|zeroTolerance|3|Cero tolerancia bloquea todos los archivos ejecutables desconocidos|



