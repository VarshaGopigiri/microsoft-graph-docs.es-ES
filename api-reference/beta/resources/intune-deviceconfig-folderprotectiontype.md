---
title: tipo de enumeración folderProtectionType
description: Valores posibles de protección de carpeta
ms.openlocfilehash: a02f1602f8b9a962124fb7bf2a9731662a6f3057
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086022"
---
# <a name="folderprotectiontype-enum-type"></a>tipo de enumeración folderProtectionType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles de protección de carpeta
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Valor predeterminado de dispositivo, sin intención.|
|habilitar|1|Funcionalidad de bloque.|
|auditMode|2|Permitir la funcionalidad pero los registros que se genere.|
|blockDiskModification|3|Bloquear las aplicaciones que no se confía escribir en sectores de disco.|
|auditDiskModification|4|Generar registros al escriben aplicaciones que no se confía a sectores de disco.|





