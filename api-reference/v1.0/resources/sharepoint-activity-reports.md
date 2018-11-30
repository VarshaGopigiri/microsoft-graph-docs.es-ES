---
title: Obtener informe de actividades de SharePoint
description: Puede usar los informes de actividades de SharePoint para obtener la actividad de todos los usuarios con licencia para usar SharePoint al analizar sus interacciones con los archivos. También puede conocer el nivel de colaboración basándose en el número de archivos compartidos.
ms.openlocfilehash: b180a098cdec6ef432ec2837c576192e7aa80b1c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029325"
---
# <a name="sharepoint-activity-reports"></a>Obtener informe de actividades de SharePoint

Puede usar los informes de actividades de SharePoint para obtener la actividad de todos los usuarios con licencia para usar SharePoint al analizar sus interacciones con los archivos. También puede conocer el nivel de colaboración basándose en el número de archivos compartidos.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de SharePoint](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto | Descripción                              |
| :--------------------------------------- | :---------- | :--------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getsharepointactivityuserdetail.md) | Secuencia      | Obtiene información sobre la actividad de SharePoint por usuario. |
| [Obtener número de archivos](../api/reportroot-getsharepointactivityfilecounts.md) | Secuencia      | Obtiene el número de usuarios con licencia únicos que interactuaron con archivos almacenados en sitios de SharePoint. |
| [Obtener número de usuarios](../api/reportroot-getsharepointactivityusercounts.md) | Secuencia      | Obtiene la tendencia del número de usuarios activos. Un usuario se considera activo si ejecutó una actividad de archivos (guardar, sincronizar, modificar o compartir), o bien si visitó una página dentro del período de tiempo especificado. |
| [Obtener páginas](../api/reportroot-getsharepointactivitypages.md) | Secuencia      | Obtiene el número de páginas únicas visitadas por los usuarios. |
