---
title: tipo de enumeración clonableTeamParts
description: 'Describe qué parte de un equipo se debería clonar. '
localization_priority: Normal
ms.openlocfilehash: 7eb71de266ea4f0ed9f94900dd03a47da1a24cc1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860560"
---
# <a name="clonableteamparts-enum-type"></a>tipo de enumeración clonableTeamParts

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Describe qué parte de un [equipo](../resources/team.md) se debería clonar. 

## <a name="members"></a>Miembros

| Miembro	 | Valor| Descripción |
|:---------------|:--------|:----------|
|aplicaciones|1|Copie la lista de aplicaciones instaladas.|
|fichas|2|copia las fichas dentro de los canales.|
|settings|4|Copia todas las opciones de dentro del equipo, junto con la configuración de grupo de claves.|
|canales|8|copia la estructura de canal (pero no los mensajes en el canal).|
|members|16|copia los miembros y propietarios del equipo.|
