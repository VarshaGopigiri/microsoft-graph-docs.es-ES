---
title: Obtener informes de actividades de grupos de Yammer
description: Puede obtener entendimiento de la actividad de grupos de Yammer en la organización y ver cuántos grupos de Yammer que se crea y usa.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: e2726e55e089aa494eaf35d0948f0fa3948be781
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950819"
---
# <a name="yammer-groups-activity-reports"></a>Obtener informes de actividades de grupos de Yammer

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción. Estas API no se admiten en China de Microsoft Graph operado por 21Vianet.

Puede obtener entendimiento de la actividad de grupos de Yammer en la organización y ver cuántos grupos de Yammer que se crea y usa.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles de grupo](../api/reportroot-getyammergroupsactivitydetail.md) | Secuencia          | [yammerGroupsActivityDetail](../resources/yammergroupsactivitydetail.md) | Obtiene información sobre la actividad de grupos de Yammer por grupo. |
| [Obtener número de grupos](../api/reportroot-getyammergroupsactivitygroupcounts.md) | Secuencia          | [yammerGroupsActivityGroupCounts](../resources/yammergroupsactivitygroupcounts.md) | Obtiene el número total de grupos que existen y en cuántos se incluyeron actividades de conversaciones de grupo. |
| [Obtener recuentos de actividad](../api/reportroot-getyammergroupsactivitycounts.md) | Secuencia          | [yammerGroupsActivityCounts](../resources/yammergroupsactivitycounts.md) | Obtiene el número de mensajes de Yammer publicados, leídos y etiquetados como “Me gusta” en grupos. |
