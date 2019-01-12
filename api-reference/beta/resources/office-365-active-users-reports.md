---
title: Obtener informe de usuarios activos de Office 365
description: Puede usar el informe de usuarios activos de Office 365 para averiguar cuántas licencias de producto están siendo utilizadas por las personas de su organización y explorar en profundidad para obtener información sobre qué usuarios están utilizando qué productos. Este informe puede ayudar a los administradores a identificar infrautilizados productos o los usuarios que podrían necesitar información o recursos de aprendizaje adicionales.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 958cf769a2b54f1d22cdc315ee250cb1e677c301
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970510"
---
# <a name="office-365-active-users-reports"></a>Obtener informe de usuarios activos de Office 365

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede usar el informe de usuarios activos de Office 365 para averiguar cuántas licencias de producto están siendo utilizadas por las personas de su organización y explorar en profundidad para obtener información sobre qué usuarios están utilizando qué productos. Este informe puede ayudar a los administradores a identificar infrautilizados productos o los usuarios que podrían necesitar información o recursos de aprendizaje adicionales.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).

## <a name="reports"></a>Informes
| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getoffice365activeuserdetail.md) | Secuencia          | [office365ActiveUserDetail](../resources/office365activeuserdetail.md) | Obtiene información sobre los usuarios activos de Office 365. |
| [Obtener número de usuarios](../api/reportroot-getoffice365activeusercounts.md) | Secuencia          | [office365ActiveUserCounts](../resources/office365activeusercounts.md) | Obtiene el número de usuarios activos diarios en el período de informe por producto. |
| [Obtener número de usuarios de servicios](../api/reportroot-getoffice365servicesusercounts.md) | Secuencia          | [office365ServicesUserCounts](../resources/office365servicesusercounts.md) | Obtiene el número de usuarios por tipo de actividad y servicio. |
