---
title: tipo de enumeración deviceGuardLocalSystemAuthorityCredentialGuardType
description: Posibles valores de configuración de protección de credenciales.
author: tfitzmac
ms.openlocfilehash: 6f6c952d1c480d42db45de6345eba883ff5848a8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346966"
---
# <a name="deviceguardlocalsystemauthoritycredentialguardtype-enum-type"></a>tipo de enumeración deviceGuardLocalSystemAuthorityCredentialGuardType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de configuración de protección de credenciales.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|Desactiva el Guard credenciales de forma remota si ha configurado anteriormente sin bloqueo UEFI.|
|enableWithUEFILock|1|Activa Guard de credenciales con bloqueo UEFI.|
|enableWithoutUEFILock|2|Sin bloqueo UEFI activa Guard de credenciales.|





