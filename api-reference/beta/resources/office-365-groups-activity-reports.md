---
title: Obtener informes de actividades de Grupos de Office 365
description: Puede obtener información sobre la actividad de los grupos de Office 365 en su organización y ver cuántos grupos de Office 365 se están crea y usa.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 8db142bcc7ae283df41dd6809ab97e81c996c10a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971189"
---
# <a name="office-365-groups-activity-reports"></a>Obtener informes de actividades de Grupos de Office 365

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener información sobre la actividad de los grupos de Office 365 en su organización y ver cuántos grupos de Office 365 se están crea y usa.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles de grupo](../api/reportroot-getoffice365groupsactivitydetail.md) | Secuencia          | [office365GroupsActivityDetail](../resources/office365groupsactivitydetail.md) | Obtiene información sobre la actividad de Grupos de Office 365 por grupo. |
| [Obtener recuentos de actividad](../api/reportroot-getoffice365groupsactivitycounts.md) | Secuencia          | [office365GroupsActivityCounts](../resources/office365groupsactivitycounts.md) | Obtiene el número de actividades de grupo en cargas de trabajo en grupo. |
| [Obtener número de grupos](../api/reportroot-getoffice365groupsactivitygroupcounts.md) | Secuencia          | [office365GroupsActivityGroupCounts](../resources/office365groupsactivitygroupcounts.md) | Obtiene el número total diario de grupos y cuántos de ellos estuvieron activos según las conversaciones de correo electrónico, las publicaciones de Yammer y las actividades en archivos de SharePoint. |
| [Obtener almacenamiento](../api/reportroot-getoffice365groupsactivitystorage.md) | Secuencia          | [office365GroupsActivityStorage](../resources/office365groupsactivitystorage.md) | Obtiene el total de almacenamiento usado en todos los buzones de grupo y sitios de grupo. |
| [Obtener número de archivos](../api/reportroot-getoffice365groupsactivityfilecounts.md) | Secuencia          | [office365GroupsActivityFileCounts](../resources/office365groupsactivityfilecounts.md) | Obtiene el número total de archivos y cuántos estaban activos en todos los sitios de grupo asociados con un grupo de Office 365. |
