---
title: tipo de enumeración diagnosticDataSubmissionMode
description: Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
ms.openlocfilehash: b09a4bf334af5981c3ce6dabbab0ac64e2b24887
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031658"
---
# <a name="diagnosticdatasubmissionmode-enum-type"></a>tipo de enumeración diagnosticDataSubmissionMode

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Permitir al usuario que establezca.|
|ninguno|1|No hay datos de telemetría se envían desde los componentes del sistema operativo. Nota: Este valor solo es aplicable a dispositivos de servidor y de la empresa. El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.|
|básica|2|Envía los datos de telemetría básica.|
|mejorado|3|Envía mejoradas, incluidos los datos de uso y entendimiento de los datos de telemetría.|
|completa|4|Envía datos de telemetría completa, incluidos los datos de diagnósticos, como estado del sistema.|



