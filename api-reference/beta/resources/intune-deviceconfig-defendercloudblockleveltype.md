---
title: tipo de enumeración defenderCloudBlockLevelType
description: Posibles valores de nivel de bloque en la nube
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 13f8828478eb063eaa25d8561d5a254c86f4b856
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924723"
---
# <a name="defendercloudblockleveltype-enum-type"></a>tipo de enumeración defenderCloudBlockLevelType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de nivel de bloque en la nube
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|Valor predeterminado, se utiliza el bloqueo de Windows Defender Antivirus predeterminado de nivel y se proporciona una detección de segura sin aumentar el riesgo de detectar legítimos archivos|
|alta|1|Alta aplica a un alto nivel de detección.|
|highPlus|2|Alta + utiliza el nivel alto y se aplica a las medidas de protección de adición|
|zeroTolerance|3|Cero tolerancia bloquea todos los archivos ejecutables desconocidos|





