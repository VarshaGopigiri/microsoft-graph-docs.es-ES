---
title: tipo de enumeración teamSpecialization
description: Describe el caso de uso especial para un equipo.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 18e1993272a94df989066cf95d01b6a4f66fd8d1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826043"
---
# <a name="teamspecialization-enum-type"></a>tipo de enumeración teamSpecialization

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Indica si el [equipo](../resources/team.md) está destinado a un caso de uso concreto. Cada especialización del [equipo](../resources/team.md) tiene acceso a comportamientos únicos y experiencias dirigidas a su caso de uso. Valor predeterminado es 'none'.

## <a name="members"></a>Miembros

| Miembro	             | Valor | Description                                                                |
| :----------------- | :---- | :------------------------------------------------------------------------- |
| none               | 0     | Tipo de un equipo que proporciona la experiencia de grupo estándar de forma predeterminada.          |
| unknownFutureValue | 7     | Sentinel valor reservado como un marcador de posición para una futura ampliación de la enumeración. |
