---
title: Informes de uso de aplicaciones de correo electrónico
description: Puede ver cuántas aplicaciones de correo electrónico se utilizan para conectarse a Exchange Online. También puede ver qué versiones de aplicaciones de Outlook se usan, lo que le permitirá realizar un seguimiento de los usuarios que necesitan actualizar a versiones de Outlook compatibles.
ms.openlocfilehash: 0511bfb2832bac761ed1e56dfb18a41fc93beb01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088555"
---
# <a name="email-app-usage-reports"></a>Informes de uso de aplicaciones de correo electrónico

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede ver cuántas aplicaciones de correo electrónico se utilizan para conectarse a Exchange Online. También puede ver qué versiones de aplicaciones de Outlook se usan, lo que le permitirá realizar un seguimiento de los usuarios que necesitan actualizar a versiones de Outlook compatibles.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getemailappusageuserdetail.md) | Secuencia          | [emailAppUsageUserDetail](../resources/emailappusageuserdetail.md) | Obtiene información sobre las actividades que realizaron los usuarios en las diferentes aplicaciones de correo electrónico. |
| [Obtener número de usuarios de aplicaciones](../api/reportroot-getemailappusageappsusercounts.md) | Secuencia          | [emailAppUsageAppsUserCounts](../resources/emailappusageappsusercounts.md) | Obtiene el número de usuarios únicos por aplicación de correo electrónico. |
| [Obtener número de usuarios](../api/reportroot-getemailappusageusercounts.md) | Secuencia          | [emailAppUsageUserCounts](../resources/emailappusageusercounts.md) | Obtiene el número de usuarios únicos que se conectaron a Exchange Online con cualquier aplicación de correo electrónico. |
| [Obtener número de usuarios de versiones](../api/reportroot-getemailappusageversionsusercounts.md) | Secuencia          | [emailAppUsageVersionsUserCounts](../resources/emailappusageversionsusercounts.md) | Obtiene el número de usuarios únicos por versión de escritorio de Outlook. |
