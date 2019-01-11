---
title: Obtener informe de activaciones de Office 365
description: El informe de activación de Office 365 le ofrece una vista de los cuales los usuarios han activado sus suscripciones a Office 365 en al menos un dispositivo. Proporciona un desglose de la Office 365 ProPlus, Project y Visio Pro para las activaciones de suscripción de Office 365, así como el desglose de las activaciones de escritorio y dispositivos. Este informe puede ayudarlo a identificar a los usuarios que es posible que necesiten compatibilidad adicional para activar su suscripción de Office.
localization_priority: Normal
ms.openlocfilehash: 2576579879e60573a9ed70f805fe07532bab8ad8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822221"
---
# <a name="office-365-activations-reports"></a>Obtener informe de activaciones de Office 365

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El informe de activación de Office 365 le ofrece una vista de los cuales los usuarios han activado sus suscripciones a Office 365 en al menos un dispositivo. Proporciona un desglose de la Office 365 ProPlus, Project y Visio Pro para las activaciones de suscripción de Office 365, así como el desglose de las activaciones de escritorio y dispositivos. Este informe puede ayudarlo a identificar a los usuarios que es posible que necesiten compatibilidad adicional para activar su suscripción de Office.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).

## <a name="reports"></a>Informes
| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getoffice365activationsuserdetail.md) | Secuencia          | [office365ActivationsUserDetail](../resources/office365activationsuserdetail.md) | Obtiene información sobre qué usuarios activaron Office 365. |
| [Obtener recuentos de activación](../api/reportroot-getoffice365activationcounts.md) | Secuencia          | [office365ActivationCounts](../resources/office365activationcounts.md) | Obtiene el número de activaciones de Office 365 en dispositivos y equipos de escritorio. |
| [Obtener número de usuarios](../api/reportroot-getoffice365activationsusercounts.md) | Secuencia          | [office365ActivationsUserCounts](../resources/office365activationsusercounts.md) | Obtiene el número de usuarios habilitados y el número de usuarios que activaron la suscripción de Office en dispositivos o equipos de escritorio. |
