---
title: Informes de uso de OneDrive
description: Puede usar los informes de uso de OneDrive para obtener una vista general del valor que obtiene de OneDrive en términos del número total de archivos y la cantidad de almacenamiento usado en todas las cuentas de OneDrive de la organización. Después, puede explorar en profundidad para comprender las tendencias de las cuentas de OneDrive activas, el número de archivos con el que interactuaron los usuarios y la cantidad de almacenamiento usado. Estos informes también pueden ofrecerle detalles por cada cuenta de OneDrive.
ms.openlocfilehash: 33064678ba3d9217ed83ae59b10cb375f4f95231
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030140"
---
# <a name="onedrive-usage-reports"></a>Informes de uso de OneDrive

Puede usar los informes de uso de OneDrive para obtener una vista general del valor que obtiene de OneDrive en términos del número total de archivos y la cantidad de almacenamiento usado en todas las cuentas de OneDrive de la organización. Después, puede explorar en profundidad para comprender las tendencias de las cuentas de OneDrive activas, el número de archivos con el que interactuaron los usuarios y la cantidad de almacenamiento usado. Estos informes también pueden ofrecerle detalles por cada cuenta de OneDrive.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto | Descripción                              |
| :--------------------------------------- | :---------- | ---------------------------------------- |
| [Obtener detalle de cuenta](../api/reportroot-getonedriveusageaccountdetail.md) | Secuencia      | Obtiene información sobre el uso de OneDrive por cuenta. |
| [Obtener número de cuentas](../api/reportroot-getonedriveusageaccountcounts.md) | Secuencia      | Obtiene la tendencia sobre el número de sitios activos de OneDrive para la Empresa. Cualquier sitio en que los usuarios vieron, modificaron, cargaron, descargaron, compartieron o sincronizaron archivos se considera un sitio activo. |
| [Obtener número de archivos](../api/reportroot-getonedriveusagefilecounts.md) | Secuencia      | Obtiene el número total de archivos en todos los sitios y cuántos son archivos activos. Un archivo se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado. |
| [Obtener almacenamiento](../api/reportroot-getonedriveusagestorage.md) | Secuencia      | Obtiene las tendencias sobre la cantidad de almacenamiento que usa en OneDrive para la Empresa. |
