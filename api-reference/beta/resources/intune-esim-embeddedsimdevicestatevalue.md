---
title: tipo de enumeración embeddedSIMDeviceStateValue
description: Describe los diferentes Estados de un código de activación de SIM incrustado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 67dd3850db1e759ded578f551eb41636ec231084
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985966"
---
# <a name="embeddedsimdevicestatevalue-enum-type"></a>tipo de enumeración embeddedSIMDeviceStateValue

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Describe los diferentes Estados de un código de activación de SIM incrustado.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|notEvaluated|0|Designa que el código de activación de SIM incrustado es gratuito y está disponible para ser asignado a un dispositivo.|
|failed|1|Designa que Intune Service no se pudo entregar este perfil para un dispositivo.|
|instalar|2|Designa que el código de activación de SIM incrustado se ha asignado a un dispositivo y el dispositivo que instala el token.|
|instalado|3|Designa que el código de activación de SIM incrustado se ha instalado correctamente en el dispositivo de destino.|
|eliminar|4|Designa Intune Service está intentando eliminar el perfil desde el dispositivo.|
|error|5|Designa que hay error con este perfil.|
|deleted|6|Designa que se ha eliminado el perfil desde el dispositivo.|
|removedByUser|7|Designa que el usuario quite el perfil desde el dispositivo|





