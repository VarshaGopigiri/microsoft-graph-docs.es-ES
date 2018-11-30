---
title: Obtener informe de actividades de Yammer
description: Para comprender el nivel de compromiso de la organización con Yammer, puede que se genere cuánta actividad a través de la organización y el número de usuarios únicos que registrar, like y leer los mensajes en Yammer.
ms.openlocfilehash: 3d70af700a55359044b4c24896a0118de5280fee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086287"
---
# <a name="yammer-activity-reports"></a>Obtener informe de actividades de Yammer

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción. Estas API no se admiten en China de Microsoft Graph operado por 21Vianet.

Para comprender el nivel de compromiso de la organización con Yammer, puede que se genere cuánta actividad a través de la organización y el número de usuarios únicos que registrar, like y leer los mensajes en Yammer.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Yammer](https://support.office.com/client/Yammer-activity-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getyammeractivityuserdetail.md) | Secuencia          | [yammerActivityUserDetail](../resources/yammeractivityuserdetail.md) | Obtiene información sobre las actividades de Yammer por usuario. |
| [Obtener recuentos de actividad](../api/reportroot-getyammeractivitycounts.md) | Secuencia          | [yammerActivitySummary](../resources/yammeractivitysummary.md) | Obtiene las tendencias sobre el número de actividades de Yammer en la organización y el número de mensajes que se publicaron, leyeron y etiquetaron como “Me gusta”. |
| [Obtener número de usuarios](../api/reportroot-getyammeractivityusercounts.md) | Secuencia          | [yammerActivitySummary](../resources/yammeractivitysummary.md) | Obtiene las tendencias sobre el número de usuarios únicos que publicaron, leyeron y etiquetaron como “Me gusta” mensajes de Yammer. |
