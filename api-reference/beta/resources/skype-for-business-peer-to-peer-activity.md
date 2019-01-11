---
title: Informe de actividades de punto a punto de Skype Empresarial
description: Puede obtener detalles sobre la actividad de punto a punto en toda la organización. Estos detalles son muy útiles para investigar, planear y tomar otras decisiones empresariales en la organización.
localization_priority: Normal
ms.openlocfilehash: 40ab1cc9f35de449ce5853b28c54606ceb089b22
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882743"
---
# <a name="skype-for-business-peer-to-peer-activity-reports"></a>Informe de actividades de punto a punto de Skype Empresarial

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener detalles sobre la actividad de punto a punto en toda la organización. Estos detalles son muy útiles para investigar, planear y tomar otras decisiones empresariales en la organización.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de punto a punto de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener recuentos de actividad](../api/reportroot-getskypeforbusinesspeertopeeractivitycounts.md) | Secuencia          | [skypeForBusinessPeerToPeerActivityCounts](../resources/skypeforbusinesspeertopeeractivitycounts.md) | Obtiene tendencias de uso sobre el número y el tipo de sesiones realizadas en la organización. Entre los tipos de sesiones, se incluyen la mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos. |
| [Obtener número de usuarios](../api/reportroot-getskypeforbusinesspeertopeeractivityusercounts.md) | Secuencia          | [skypeForBusinessPeerToPeerActivityUserCounts](../resources/skypeforbusinesspeertopeeractivityusercounts.md) | Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de punto a punto realizadas en la organización. Entre los diferentes tipos, se incluyen sesiones de mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos en sesiones de punto a punto. |
| [Obtener número de minutos](../api/reportroot-getskypeforbusinesspeertopeeractivityminutecounts.md) | Secuencia          | [skypeForBusinessPeerToPeerActivityMinuteCounts](../resources/skypeforbusinesspeertopeeractivityminutecounts.md) | Obtiene tendencias de uso sobre la duración en minutos y el tipo de sesiones de punto a punto realizadas en la organización. Entre los tipos de sesiones, se incluyen sesiones de audio y vídeo. |
