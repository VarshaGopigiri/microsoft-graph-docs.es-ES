---
title: Informes de uso de buzones
description: Puede obtener información acerca de los usuarios con un buzón de correo y su nivel de actividad que se basa principalmente en los correos electrónicos enviados y recibidos. También puede ver cuánto almacenamiento usa cada buzón y cuantos buzones están próximos a sus cuotas de almacenamiento.
ms.openlocfilehash: 77814784d75bb7056336c873ad7f2eb0fddc04f4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087207"
---
# <a name="mailbox-usage-reports"></a>Informes de uso de buzones

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener información acerca de los usuarios con un buzón de correo y su nivel de actividad que se basa principalmente en los correos electrónicos enviados y recibidos. También puede ver cuánto almacenamiento usa cada buzón y cuantos buzones están próximos a sus cuotas de almacenamiento.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del buzón](../api/reportroot-getmailboxusagedetail.md) | Secuencia          | [mailboxUsageDetail](../resources/mailboxusagedetail.md) | Obtiene información sobre el uso de buzones.         |
| [Obtener recuentos de buzón](../api/reportroot-getmailboxusagemailboxcounts.md) | Secuencia          | [mailboxUsageMailboxCounts](../resources/mailboxusagemailboxcounts.md) | Obtiene el número total de buzones de usuario en la organización y cuantos están activos cada día del período del informe. Un buzón se considera activo si el usuario envió o leyó cualquier correo electrónico. |
| [Obtener cuentas de buzón de estado de cuota](../api/reportroot-getmailboxusagequotastatusmailboxcounts.md) | Secuencia          | [mailboxUsageQuotaStatusMailboxCounts](../resources/mailboxusagequotastatusmailboxcounts.md) | Obtiene el número de buzones de usuario en cada categoría de cuota. |
| [Obtener almacenamiento](../api/reportroot-getmailboxusagestorage.md) | Secuencia          | [mailboxUsageStorage](../resources/mailboxusagestorage.md) | Obtiene la cantidad de almacenamiento usado en la organización. |
