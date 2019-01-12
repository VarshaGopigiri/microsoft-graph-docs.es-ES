---
title: tipo de enumeración safeSearchFilterType
description: Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 49252525b3c6bcab6fd79a1ed7c27b3004665fe8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944799"
---
# <a name="safesearchfiltertype-enum-type"></a>tipo de enumeración safeSearchFilterType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Definido por el usuario, valor predeterminado, sin intención.|
|estricto|1|Estricto, mayor filtrado contra el contenido para adultos.|
|moderado|2|Moderar filtrado contra el contenido para adultos (no se filtrarán los resultados de búsqueda válido).|





