---
title: tipo de enumeración teamSpecialization
description: Describe el caso de uso especial para un equipo.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 02a2272ee085d0c265adc9ce2e3f1c598e45be21
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930288"
---
# <a name="teamspecialization-enum-type"></a>tipo de enumeración teamSpecialization

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Indica si el [equipo](../resources/team.md) está destinado a un caso de uso concreto. Cada especialización del [equipo](../resources/team.md) tiene acceso a comportamientos únicos y experiencias dirigidas a su caso de uso. Valor predeterminado es 'none'.

## <a name="members"></a>Miembros

| Miembro	             | Valor | Descripción                                                                |
| :----------------- | :---- | :------------------------------------------------------------------------- |
| none               | 0     | Tipo de un equipo que proporciona la experiencia de grupo estándar de forma predeterminada.          |
| unknownFutureValue | 7     | Sentinel valor reservado como un marcador de posición para una futura ampliación de la enumeración. |
