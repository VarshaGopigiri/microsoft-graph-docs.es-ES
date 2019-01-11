---
title: Obtener informes de uso de dispositivos de Yammer
description: Los informes de uso de dispositivos para Yammer le ofrecen información sobre los dispositivos que usan los usuarios para interactuar en Yammer. Puede ver el número de usuarios por tipo de dispositivo durante un período de tiempo seleccionado y ver detalles por usuario.
localization_priority: Normal
ms.openlocfilehash: f8effbe250b352d290e04c0e23c5454447ebf4d4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885686"
---
# <a name="yammer-device-usage-reports"></a>Obtener informes de uso de dispositivos de Yammer

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción. Estas API no se admiten en China de Microsoft Graph operado por 21Vianet.

Los informes de uso de dispositivos para Yammer le ofrecen información sobre los dispositivos que usan los usuarios para interactuar en Yammer. Puede ver el número de usuarios por tipo de dispositivo durante un período de tiempo seleccionado y ver detalles por usuario.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de dispositivos de Yammer](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getyammerdeviceusageuserdetail.md) | Secuencia          | [yammerDeviceUsageUserDetail](../resources/yammerdeviceusageuserdetail.md) | Obtiene información sobre el uso de dispositivos de Yammer por usuario. |
| [Obtener número de usuarios de distribución](../api/reportroot-getyammerdeviceusagedistributionusercounts.md) | Secuencia          | [yammerDeviceUsageDistributionUserCounts](../resources/yammerdeviceusagedistributionusercounts.md) | Obtiene el número de usuarios por tipo de dispositivo.  |
| [Obtener número de usuarios](../api/reportroot-getyammerdeviceusageusercounts.md) | Secuencia          | [yammerDeviceUsageUserCounts](../resources/yammerdeviceusageusercounts.md) | Obtiene el número de usuarios diario por tipo de dispositivo. |
