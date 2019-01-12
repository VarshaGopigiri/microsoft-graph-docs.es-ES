---
title: Obtener informe de actividades de Skype Empresarial
description: Puede obtener detalles sobre la actividad en toda la organización. Estos detalles pueden resultarle útiles para investigar, planear y tomar otras decisiones empresariales para la organización.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: fcc40f0cba1e8a5f2304554088562af15c592964
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941677"
---
# <a name="skype-for-business-activity-reports"></a>Obtener informe de actividades de Skype Empresarial

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener detalles sobre la actividad en toda la organización. Estos detalles pueden resultarle útiles para investigar, planear y tomar otras decisiones empresariales para la organización.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getskypeforbusinessactivityuserdetail.md) | Secuencia          | [skypeForBusinessActivityUserDetail](../resources/skypeforbusinessactivityuserdetail.md) | Obtiene información sobre la actividad de Skype Empresarial por usuario. |
| [Obtener recuentos de actividad](../api/reportroot-getskypeforbusinessactivitycounts.md) | Secuencia          | [skypeForBusinessActivityCounts](../resources/skypeforbusinessactivitycounts.md) | Obtiene las tendencias sobre el número de usuarios que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial. En el informe, también se incluye el número de sesiones de punto a punto. |
| [Obtener número de usuarios](../api/reportroot-getskypeforbusinessactivityusercounts.md) | Secuencia          | [skypeForBusinessActivityUserCounts](../resources/skypeforbusinessactivityusercounts.md) | Obtiene las tendencias sobre el número de usuarios únicos que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial. En el informe, también se incluye el número de sesiones de punto a punto. |
