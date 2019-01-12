---
title: Informes de uso de sitio de SharePoint
description: Puede obtener una vista de alto nivel del valor que va a obtener de SharePoint en cuanto al número total de archivos que los usuarios se almacenan en el almacenamiento de información consumido en todos estos sitios, cuántos archivos se usan activamente y sitios SharePoint. A continuación, puede ver detalles en el informe de uso del sitio de SharePoint para comprender las tendencias y por detalles a nivel de sitio para todos los sitios.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 964ec64a2cbb15d639a619cf8debd5fb5875245e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950532"
---
# <a name="sharepoint-site-usage-reports"></a>Informes de uso de sitio de SharePoint

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener una vista de alto nivel del valor que va a obtener de SharePoint en cuanto al número total de archivos que los usuarios se almacenan en el almacenamiento de información consumido en todos estos sitios, cuántos archivos se usan activamente y sitios SharePoint. A continuación, puede ver detalles en el informe de uso del sitio de SharePoint para comprender las tendencias y por detalles a nivel de sitio para todos los sitios.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de sitio de SharePoint](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles de sitio](../api/reportroot-getsharepointsiteusagedetail.md) | Secuencia          | [sharePointSiteUsageDetail](../resources/sharepointsiteusagedetail.md) | Obtiene información sobre el uso del sitio de SharePoint. |
| [Obtener número de archivos](../api/reportroot-getsharepointsiteusagefilecounts.md) | Secuencia          | [sharePointSiteUsageFileCounts](../resources/sharepointsiteusagefilecounts.md) | Obtiene el número total de archivos en todos los sitios y el número de archivos activos. Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado. |
| [Obtener número de sitios](../api/reportroot-getsharepointsiteusagesitecounts.md) | Secuencia          | [sharePointSiteUsageSiteCounts](../resources/sharepointsiteusagesitecounts.md) | Obtiene el número total de archivos en todos los sitios y el número de archivos activos. Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado. |
| [Obtener almacenamiento](../api/reportroot-getsharepointsiteusagestorage.md) | Secuencia          | [siteUsageStorage](../resources/siteusagestorage.md) | Obtiene la tendencia del almacenamiento asignado y usado durante el período del informe. |
| [Obtener páginas](../api/reportroot-getsharepointsiteusagepages.md) | Secuencia          | [sharePointSiteUsagePages](../resources/sharepointsiteusagepages.md) | Obtiene el número de páginas vistas en todos los sitios. |
