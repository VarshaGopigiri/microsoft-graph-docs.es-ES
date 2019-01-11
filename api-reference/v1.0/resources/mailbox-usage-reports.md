---
title: Informes de uso de buzones
description: Use los informes de uso de buzones para obtener información sobre los usuarios con un buzón y su nivel de actividad, que se basa principalmente en los correos electrónicos enviados y recibidos. También puede ver cuánto almacenamiento usa cada buzón y cuantos buzones están próximos a sus cuotas de almacenamiento.
localization_priority: Priority
ms.openlocfilehash: a802b392d6dda1e7a56fecbee9cc489f1833caba
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826295"
---
# <a name="mailbox-usage-reports"></a>Informes de uso de buzones

Use los informes de uso de buzones para obtener información sobre los usuarios con un buzón y su nivel de actividad, que se basa principalmente en los correos electrónicos enviados y recibidos. También puede ver cuánto almacenamiento usa cada buzón y cuantos buzones están próximos a sus cuotas de almacenamiento.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto | Descripción                              |
| :--------------------------------------- | :---------- | :--------------------------------------- |
| [Obtener detalles del buzón](../api/reportroot-getmailboxusagedetail.md) | Secuencia      | Obtiene información sobre el uso de buzones.         |
| [Obtener recuentos de buzón](../api/reportroot-getmailboxusagemailboxcounts.md) | Secuencia      | Obtiene el número total de buzones de usuario en la organización y cuantos están activos cada día del período del informe. Un buzón se considera activo si el usuario envió o leyó cualquier correo electrónico. |
| [Obtener cuentas de buzón de estado de cuota](../api/reportroot-getmailboxusagequotastatusmailboxcounts.md) | Secuencia      | Obtiene el número de buzones de usuario en cada categoría de cuota. |
| [Obtener almacenamiento](../api/reportroot-getmailboxusagestorage.md) | Secuencia      | Obtiene la cantidad de almacenamiento usado en la organización. |
