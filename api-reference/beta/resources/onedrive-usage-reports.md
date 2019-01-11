---
title: Informes de uso de OneDrive
description: Puede obtener una vista de alto nivel del valor que se va a obtener de OneDrive en cuanto al número total de archivos y almacenamiento utilizado a través de todas las cuentas de OneDrive en la organización. Después, puede explorar en profundidad para comprender las tendencias de las cuentas de OneDrive activas, el número de archivos con el que interactuaron los usuarios y la cantidad de almacenamiento usado. También se ofrece la por OneDrive detalles de la cuenta.
localization_priority: Normal
ms.openlocfilehash: a3d75a7863a539c67ef4971193b108f0ba73a1fa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829739"
---
# <a name="onedrive-usage-reports"></a>Informes de uso de OneDrive

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener una vista de alto nivel del valor que se va a obtener de OneDrive en cuanto al número total de archivos y almacenamiento utilizado a través de todas las cuentas de OneDrive en la organización. Después, puede explorar en profundidad para comprender las tendencias de las cuentas de OneDrive activas, el número de archivos con el que interactuaron los usuarios y la cantidad de almacenamiento usado. También se ofrece la por OneDrive detalles de la cuenta.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | ---------------------------------------- | ---------------------------------------- |
| [Obtener detalle de cuenta](../api/reportroot-getonedriveusageaccountdetail.md) | Secuencia          | [oneDriveUsageAccountDetail](../resources/onedriveusageaccountdetail.md) | Obtiene información sobre el uso de OneDrive por cuenta. |
| [Obtener número de cuentas](../api/reportroot-getonedriveusageaccountcounts.md) | Secuencia          | [oneDriveUsageAccountCounts](../resources/onedriveusageaccountcounts.md) | Obtiene la tendencia sobre el número de sitios activos de OneDrive para la Empresa. Cualquier sitio en que los usuarios vieron, modificaron, cargaron, descargaron, compartieron o sincronizaron archivos se considera un sitio activo. |
| [Obtener número de archivos](../api/reportroot-getonedriveusagefilecounts.md) | Secuencia          | [oneDriveUsageFileCounts](../resources/onedriveusagefilecounts.md) | Obtiene el número total de archivos en todos los sitios y cuántos son archivos activos. Un archivo se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado. |
| [Obtener almacenamiento](../api/reportroot-getonedriveusagestorage.md) | Secuencia          | [siteUsageStorage](../resources/siteusagestorage.md) | Obtiene las tendencias sobre la cantidad de almacenamiento que usa en OneDrive para la Empresa. |
