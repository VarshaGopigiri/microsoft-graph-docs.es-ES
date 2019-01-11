---
title: Informes de actividad de usuario de Microsoft Teams
description: Use los informes de actividad de usuario de Microsoft Teams para obtener información sobre la actividad de usuario de Microsoft Teams en su organización.
localization_priority: Normal
ms.openlocfilehash: 2fc2eee8243a338204687114d2f1de3d2e794a9f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845525"
---
# <a name="microsoft-teams-user-activity-reports"></a>Informes de actividad de usuario de Microsoft Teams

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción. Estas API no se admiten en China de Microsoft Graph operado por 21Vianet.

Use los informes de actividad de usuario de Microsoft Teams para obtener información sobre la actividad de usuario de Microsoft Teams en su organización.

## <a name="methods"></a>Métodos

| Método                                   | Tipo de valor devuelto                              | Descripción                              |
| :--------------------------------------- | :--------------------------------------- | :--------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getteamsuseractivityuserdetail.md) | [teamsUserActivityUserDetail](../resources/teamsuseractivityuserdetail.md) | Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario. |
| [Obtener recuentos de actividad](../api/reportroot-getteamsuseractivitycounts.md) | [teamsUserActivityCounts](../resources/teamsuseractivitycounts.md) | Obtener el número de actividades de Microsoft Teams por tipo de actividad. Los tipos de actividad son el número de mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipos. |
| [Obtener recuentos de usuario](../api/reportroot-getteamsuseractivityusercounts.md) | [teamsUserActivityUserCounts](../resources/teamsuseractivityusercounts.md) | Obtiene el número de usuarios por tipo de actividad. Los tipos de actividad son el número de mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipos. |
