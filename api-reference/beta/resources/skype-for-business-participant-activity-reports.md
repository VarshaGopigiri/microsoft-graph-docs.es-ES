---
title: Obtener informe de actividades de participantes de Skype Empresarial
description: Puede obtener detalles sobre la actividad de conferencia en toda la organización. Estos detalles son muy útiles para investigar, planear y tomar otras decisiones empresariales en la organización.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: e826f5d0f07b3f4c87fb00772e30b726e81eead0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973576"
---
# <a name="skype-for-business-participant-activity-reports"></a>Obtener informe de actividades de participantes de Skype Empresarial

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener detalles sobre la actividad de conferencia en toda la organización. Estos detalles son muy útiles para investigar, planear y tomar otras decisiones empresariales en la organización.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de participantes de conferencias de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener recuentos de actividad](../api/reportroot-getskypeforbusinessparticipantactivitycounts.md) | Secuencia          | [skypeForBusinessParticipantActivityCounts](../resources/skypeforbusinessparticipantactivitycounts.md) | Obtiene tendencias de uso sobre el número y el tipo de sesiones de conferencia en las que participaron usuarios de la organización. Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web y acceso telefónico local o aceptación de llamada de terceros. |
| [Obtener número de usuarios](../api/reportroot-getskypeforbusinessparticipantactivityusercounts.md) | Secuencia          | [skypeForBusinessParticipantActivityUserCounts](../resources/skypeforbusinessparticipantactivityusercounts.md) | Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de conferencia en que participaron usuarios de la organización. Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web y acceso telefónico local o aceptación de llamada de terceros. |
| [Obtener número de minutos](../api/reportroot-getskypeforbusinessparticipantactivityminutecounts.md) | Secuencia          | [skypeForBusinessParticipantActivityMinuteCounts](../resources/skypeforbusinessparticipantactivityminutecounts.md) | Obtiene tendencias de uso sobre la duración en minutos y el tipo de las sesiones de conferencia en las que participaron los usuarios de la organización. En los tipos de sesiones de conferencia, se incluyen sesiones de audio o vídeo. |
