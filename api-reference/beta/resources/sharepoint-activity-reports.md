---
title: Obtener informe de actividades de SharePoint
description: Puede obtener la actividad de todos los usuarios con licencia para usar SharePoint observando su interacción con los archivos. También puede conocer el nivel de colaboración basándose en el número de archivos compartidos.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: d95c6920e4086c8f319f091802f00a3d24d81064
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935517"
---
# <a name="sharepoint-activity-reports"></a>Obtener informe de actividades de SharePoint

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener la actividad de todos los usuarios con licencia para usar SharePoint observando su interacción con los archivos. También puede conocer el nivel de colaboración basándose en el número de archivos compartidos.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de SharePoint](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getsharepointactivityuserdetail.md) | Secuencia          | [sharePointActivityUserDetail](../resources/sharepointactivityuserdetail.md) | Obtiene información sobre la actividad de SharePoint por usuario. |
| [Obtener número de archivos](../api/reportroot-getsharepointactivityfilecounts.md) | Secuencia          | [siteActivitySummary](../resources/siteactivitysummary.md) | Obtiene el número de usuarios con licencia únicos que interactuaron con archivos almacenados en sitios de SharePoint. |
| [Obtener número de usuarios](../api/reportroot-getsharepointactivityusercounts.md) | Secuencia          | [sharePointActivityUserCounts](../resources/sharepointactivityusercounts.md) | Obtiene la tendencia del número de usuarios activos. Un usuario se considera activo si ejecutó una actividad de archivos (guardar, sincronizar, modificar o compartir), o bien si visitó una página dentro del período de tiempo especificado. |
| [Obtener páginas](../api/reportroot-getsharepointactivitypages.md) | Secuencia          | [sharePointActivityPages](../resources/sharepointactivitypages.md) | Obtiene el número de páginas únicas visitadas por los usuarios. |
