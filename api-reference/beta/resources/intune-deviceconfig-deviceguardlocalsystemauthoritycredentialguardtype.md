---
title: tipo de enumeración deviceGuardLocalSystemAuthorityCredentialGuardType
description: Posibles valores de configuración de protección de credenciales.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d284b81632c5ba48fa4c658719203a74fdf52837
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952744"
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





