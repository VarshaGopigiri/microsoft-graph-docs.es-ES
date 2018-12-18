---
title: tipo de enumeración folderProtectionType
description: Valores posibles de protección de carpeta
author: tfitzmac
ms.openlocfilehash: 93df62da9bb5d849cba86b52384f45bfe7bd760f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350606"
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





