---
title: tipo de enumeración appListType
description: Posibles valores de la lista de aplicaciones de cumplimiento.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 76c13c26812fd8ab7c8e1224b55e616502b514ff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839273"
---
# <a name="applisttype-enum-type"></a>tipo de enumeración appListType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de la lista de aplicaciones de cumplimiento.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|none|0|Valor predeterminado, sin intención.|
|appsInListCompliant|1|La lista representa las aplicaciones que se considerarán compatibles con (solo son compatibles con las aplicaciones de la lista).|
|appsNotInListCompliant|2|La lista representa las aplicaciones que se considerarán no conformes (todas las aplicaciones son compatibles excepto en la lista de aplicaciones).|



