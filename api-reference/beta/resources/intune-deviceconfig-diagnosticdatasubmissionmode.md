---
title: tipo de enumeración diagnosticDataSubmissionMode
description: Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
localization_priority: Normal
ms.openlocfilehash: 3be69b4be25ece2ced611c028a855347e4dba66e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871536"
---
# <a name="diagnosticdatasubmissionmode-enum-type"></a>tipo de enumeración diagnosticDataSubmissionMode

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|userDefined|0|Permitir al usuario que establezca.|
|none|1|No hay datos de telemetría se envían desde los componentes del sistema operativo. Nota: Este valor solo es aplicable a dispositivos de servidor y de la empresa. El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.|
|básica|2|Envía los datos de telemetría básica.|
|mejorado|3|Envía mejoradas, incluidos los datos de uso y entendimiento de los datos de telemetría.|
|completa|4|Envía datos de telemetría completa, incluidos los datos de diagnósticos, como estado del sistema.|





