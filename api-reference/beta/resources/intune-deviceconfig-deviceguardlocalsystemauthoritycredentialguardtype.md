---
title: tipo de enumeración deviceGuardLocalSystemAuthorityCredentialGuardType
description: Posibles valores de configuración de protección de credenciales.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7f59fed69647ead4ccdda0523ae80571aebcb57c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871585"
---
# <a name="deviceguardlocalsystemauthoritycredentialguardtype-enum-type"></a>tipo de enumeración deviceGuardLocalSystemAuthorityCredentialGuardType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de configuración de protección de credenciales.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|No configurado|0|Desactiva el Guard credenciales de forma remota si ha configurado anteriormente sin bloqueo UEFI.|
|enableWithUEFILock|1|Activa Guard de credenciales con bloqueo UEFI.|
|enableWithoutUEFILock|2|Sin bloqueo UEFI activa Guard de credenciales.|





