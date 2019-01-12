---
title: Informes de actividad de usuario de Microsoft Teams
description: Use los informes de actividad de usuario de Microsoft Teams para obtener información sobre la actividad de usuario de Microsoft Teams en su organización.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 2dd3ed3cde8f1a00ae7a48336bfaef857721f046
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991436"
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
