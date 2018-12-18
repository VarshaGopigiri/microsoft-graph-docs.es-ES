---
title: tipo de enumeración deviceManagementExchangeAccessStateReason
description: Razón del estado del dispositivo Exchange acceso.
author: tfitzmac
ms.openlocfilehash: 03e89b2405aac185f8b937828ade07479ced4cc3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318357"
---
# <a name="devicemanagementexchangeaccessstatereason-enum-type"></a>tipo de enumeración deviceManagementExchangeAccessStateReason

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Razón del estado del dispositivo Exchange acceso.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|ninguno|0|Ninguna razón de estado de access detectada desde Exchange|
|desconocido|1|Motivo del estado de acceso desconocido|
|exchangeGlobalRule|2|Estado de acceso determinado por regla Global de Exchange|
|exchangeIndividualRule|3|Estado de acceso determinado por regla Individual de Exchange|
|exchangeDeviceRule|4|Estado de acceso determinado por la regla de dispositivo de Exchange|
|exchangeUpgrade|5|Estado de acceso debido a la actualización de Exchange|
|exchangeMailboxPolicy|6|Estado de acceso determinado mediante una directiva de buzón de correo de Exchange|
|otros|7|Estado de acceso determinado por Exchange|
|compatible con|8|Estado de acceso concedido por el desafío de cumplimiento de normas|
|notCompliant|9|Estado de acceso revocado por desafío de cumplimiento de normas|
|notEnrolled|10|Revocado por el desafío de la administración de estado de Access|
|unknownLocation|12|Estado de acceso debido a la ubicación desconocida|
|mfaRequired|13|Estado de acceso debido a desafío MFA|
|azureADBlockDueToAccessPolicy|14|Estado de acceso revocado mediante una directiva de acceso de AAD|
|compromisedPassword|15|Estado de acceso revocado por contraseña en peligro|
|deviceNotKnownWithManagedApp|16|Estado de acceso revocado por desafío de aplicación administrada|





