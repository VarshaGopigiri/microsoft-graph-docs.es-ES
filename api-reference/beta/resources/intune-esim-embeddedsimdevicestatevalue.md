---
title: tipo de enumeración embeddedSIMDeviceStateValue
description: Describe los diferentes Estados de un código de activación de SIM incrustado.
author: tfitzmac
ms.openlocfilehash: 51e550669d9cd29d7d5bb246fe2cba017b02187c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320597"
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





