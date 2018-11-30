---
title: tipo de enumeración appListType
description: Posibles valores de la lista de aplicaciones de cumplimiento.
ms.openlocfilehash: 2733723252f3b8f03cf08fda6d0b09f207ae5550
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032345"
---
# <a name="applisttype-enum-type"></a>tipo de enumeración appListType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de la lista de aplicaciones de cumplimiento.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|ninguno|0|Valor predeterminado, sin intención.|
|appsInListCompliant|1|La lista representa las aplicaciones que se considerarán compatibles con (solo son compatibles con las aplicaciones de la lista).|
|appsNotInListCompliant|2|La lista representa las aplicaciones que se considerarán no conformes (todas las aplicaciones son compatibles excepto en la lista de aplicaciones).|



