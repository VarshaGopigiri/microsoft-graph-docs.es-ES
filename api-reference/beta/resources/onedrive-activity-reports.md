---
title: Obtener informe de actividades de OneDrive
description: Puede obtener la actividad de todos los usuarios con licencia para usar OneDrive observando su interacción con archivos en OneDrive. También ayuda a comprender el nivel de colaboración ocurriendo al mostrar el número de archivos compartidos.
localization_priority: Normal
ms.openlocfilehash: fc87eebeb7c0df1bd6d08a82fa67ccd6d9fa40a8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814493"
---
# <a name="onedrive-activity-reports"></a>Obtener informe de actividades de OneDrive

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener la actividad de todos los usuarios con licencia para usar OneDrive observando su interacción con archivos en OneDrive. También ayuda a comprender el nivel de colaboración ocurriendo al mostrar el número de archivos compartidos.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getonedriveactivityuserdetail.md) | Secuencia          | [oneDriveActivityUserDetail](../resources/onedriveactivityuserdetail.md) | Obtiene información sobre las actividades de OneDrive por usuario. |
| [Obtener número de usuarios](../api/reportroot-getonedriveactivityusercounts.md) | Secuencia          | [siteActivitySummary](../resources/siteactivitysummary.md) | Obtiene la tendencia en el número de usuarios de OneDrive activos. |
| [Obtener número de archivos](../api/reportroot-getonedriveactivityfilecounts.md) | Secuencia          | [siteActivitySummary](../resources/siteactivitysummary.md) | Obtiene el número de usuarios con licencia únicos que realizaron interacciones con archivos en una cuenta de OneDrive. |
