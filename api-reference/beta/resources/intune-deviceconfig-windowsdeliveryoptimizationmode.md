---
title: tipo de enumeración windowsDeliveryOptimizationMode
description: Modo de optimización de entrega para la distribución del mismo nivel
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 004bb3d3984d8d304f89dc339899035d218546a8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972659"
---
# <a name="windowsdeliveryoptimizationmode-enum-type"></a>tipo de enumeración windowsDeliveryOptimizationMode

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Modo de optimización de entrega para la distribución del mismo nivel
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Permitir al usuario que establezca.|
|httpOnly|1|HTTP sólo, sin interconexión|
|httpWithPeeringNat|2|Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red|
|httpWithPeeringPrivateGroup|3|Mezcla de HTTP con interconexión a través de un grupo privado|
|httpWithInternetPeering|4|HTTP mezclado con interconexión de Internet|
|simpleDownload|99|Modo de descarga simple con ningún interconexión|
|bypassMode|100|Modo de derivación. No use la optimización de entrega y usar BITS en su lugar|





