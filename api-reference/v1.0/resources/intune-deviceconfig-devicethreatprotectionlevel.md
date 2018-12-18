---
title: tipo de enumeración deviceThreatProtectionLevel
description: Niveles de protección de amenaza de dispositivo para la API de protección de amenaza de dispositivo.
author: tfitzmac
ms.openlocfilehash: 755fd861196839ec261dd18f458b88aa97cf0191
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356010"
---
# <a name="devicethreatprotectionlevel-enum-type"></a>tipo de enumeración deviceThreatProtectionLevel

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Niveles de protección de amenaza de dispositivo para la API de protección de amenaza de dispositivo.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|no está disponible|0|Valor predeterminado. No la use.|
|protegido|1|Requisitos de dispositivos de nivel de amenaza: protegido. Esto es el nivel más seguro y representa que no hay amenazas se han encontrado en el dispositivo.|
|baja|2|Requisito de nivel de protección contra amenazas de dispositivo: baja. Baja representa una gravedad de amenaza que representa un riesgo mínimo en el dispositivo o los datos del dispositivo.|
|medium|3|Requisito de nivel de protección contra amenazas de dispositivo: medio. Medio representa una gravedad de amenaza que plantea moderado riesgo para el dispositivo o los datos del dispositivo.|
|alta|4|Requisito de nivel de protección contra amenazas de dispositivo: alta. Alta representa una gravedad de amenaza que supone un riesgo grave para el dispositivo o los datos del dispositivo.|
|notSet|10|Requisito de nivel de protección contra amenazas de dispositivo: no establecido. No conjunto representa que no hay ningún requisito para el dispositivo cumplir con un nivel de protección contra amenazas.|



