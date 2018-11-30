---
title: Informes de actividad de usuario de Microsoft Teams
description: Use los informes de actividad de usuario de Microsoft Teams para obtener información sobre la actividad de usuario de Microsoft Teams en su organización.
ms.openlocfilehash: 26af58ad88541fb4e9e0f64159505846bfe90bb5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084053"
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
