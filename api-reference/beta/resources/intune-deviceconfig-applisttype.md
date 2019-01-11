---
title: tipo de enumeración appListType
description: Posibles valores de la lista de aplicaciones de cumplimiento.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 17452d09976d84f19ed56bbaeb4e558a727b1c7c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841023"
---
# <a name="applisttype-enum-type"></a>tipo de enumeración appListType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de la lista de aplicaciones de cumplimiento.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|none|0|Valor predeterminado, sin intención.|
|appsInListCompliant|1|La lista representa las aplicaciones que se considerarán compatibles con (solo son compatibles con las aplicaciones de la lista).|
|appsNotInListCompliant|2|La lista representa las aplicaciones que se considerarán no conformes (todas las aplicaciones son compatibles excepto en la lista de aplicaciones).|





