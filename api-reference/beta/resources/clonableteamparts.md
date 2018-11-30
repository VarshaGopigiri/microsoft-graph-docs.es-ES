---
title: tipo de enumeración clonableTeamParts
description: 'Describe qué parte de un equipo se debería clonar. '
ms.openlocfilehash: 123cdb5ff7fd4a4291df5d9352b0db466908cc3c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084481"
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
