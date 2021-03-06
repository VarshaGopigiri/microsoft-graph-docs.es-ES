---
title: Obtener informe de actividades de correo electrónico
description: Puede obtener una vista de alto nivel de tráfico de correo electrónico dentro de su organización desde la página informes. También puede navegar en el widget de actividad de correo electrónico para comprender las tendencias y los detalles de cada usuario de la actividad de correo electrónico de la organización.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: reports
ms.openlocfilehash: ccbe53a783da8f45294c3140f6cbf9405d1d1f04
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947683"
---
# <a name="email-activity-reports"></a>Obtener informe de actividades de correo electrónico

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener una vista de alto nivel de tráfico de correo electrónico dentro de su organización desde la página informes. También puede navegar en el widget de actividad de correo electrónico para comprender las tendencias y los detalles de cada usuario de la actividad de correo electrónico de la organización.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividades de correo electrónico](https://support.office.com/client/Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getemailactivityuserdetail.md) | Secuencia          | [emailActivityUserDetail](../resources/emailactivityuserdetail.md) | Obtiene información sobre las actividades de correo electrónico que realizaron los usuarios. |
| [Obtener recuentos de actividad](../api/reportroot-getemailactivitycounts.md) | Secuencia          | [emailActivitySummary](../resources/emailactivitysummary.md) | Le permite comprender las tendencias de las actividades de correo electrónico (por ejemplo, cuántos se enviaron, leyeron y recibieron) en la organización. |
| [Obtener número de usuarios](../api/reportroot-getemailactivityusercounts.md) | Secuencia          | [emailActivitySummary](../resources/emailactivitysummary.md) | Le permite comprender tendencias sobre el número de usuarios únicos que realizan actividades de correo electrónico, como enviar, leer y recibir. |
