---
title: Obtener informes de uso de dispositivos de Skype Empresarial
description: Puede obtener detalles sobre los tipos de clientes y dispositivos que se usan en toda la organización. Estos detalles son muy útiles para investigar, planear y tomar otras decisiones empresariales en la organización.
ms.openlocfilehash: 7b77a78026475f8690f5ea47cc70db86b654450f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088544"
---
# <a name="skype-for-business-device-usage-reports"></a>Obtener informes de uso de dispositivos de Skype Empresarial

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede obtener detalles sobre los tipos de clientes y dispositivos que se usan en toda la organización. Estos detalles son muy útiles para investigar, planear y tomar otras decisiones empresariales en la organización.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto de CSV | Tipo de valor devuelto de JSON                         | Descripción                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot-getskypeforbusinessdeviceusageuserdetail.md) | Secuencia          | [skypeForBusinessDeviceUsageUserDetail](../resources/skypeforbusinessdeviceusageuserdetail.md) | Obtiene información sobre el uso de dispositivos de Skype Empresarial por usuario. |
| [Obtener número de usuarios de distribución](../api/reportroot-getskypeforbusinessdeviceusagedistributionusercounts.md) | Secuencia          | [skypeForBusinessDeviceUsageDistributionUserCounts](../resources/skypeforbusinessdeviceusagedistributionusercounts.md) | Obtiene el número de usuarios que usan dispositivos únicos en la organización. En el informe, se mostrará el número de usuarios por dispositivo, como Windows, teléfonos Windows, teléfonos Android, iPhone y iPad. |
| [Obtener número de usuarios](../api/reportroot-getskypeforbusinessdeviceusageusercounts.md) | Secuencia          | [skypeForBusinessDeviceUsageUserCounts](../resources/skypeforbusinessdeviceusageusercounts.md) | Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial. También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización. |
