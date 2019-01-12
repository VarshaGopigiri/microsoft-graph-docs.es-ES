---
title: tipo de enumeración certificateRevocationStatus
description: Estado de revocación del certificado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8c1c77e267da5528088a7a8ef6400a872790aaf3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983124"
---
# <a name="certificaterevocationstatus-enum-type"></a>tipo de enumeración certificateRevocationStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de revocación del certificado.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|none|0|No se ha revocado.|
|pendiente|1|Revocación pendientes.|
|emitido|2|Comando de revocación emitido.|
|failed|3|No se pudo revocación.|
|revocado|4|Revocado.|





