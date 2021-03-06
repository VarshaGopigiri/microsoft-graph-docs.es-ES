---
title: tipo de recurso bitLockerSystemDrivePolicy
description: Directivas de Base de cifrado BitLocker.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 28c3b597f25e7ea83577c18620280885f4149dcf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924660"
---
# <a name="bitlockersystemdrivepolicy-resource-type"></a>tipo de recurso bitLockerSystemDrivePolicy

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directivas de Base de cifrado BitLocker.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|encryptionMethod|[bitLockerEncryptionMethod](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|Seleccione el método de cifrado para unidades de sistema operativo. Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.|
|startupAuthenticationRequired|Booleano|Requerir autenticación adicional al inicio.|
|startupAuthenticationBlockWithoutTpmChip|Booleano|Indica si se debe permitir BitLocker sin un TPM compatible (se requiere una contraseña o una clave de inicio en una unidad flash USB).|
|startupAuthenticationTpmUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Indica si el inicio TPM es permitido o necesario o desactivarse. Los valores posibles son: `blocked`, `required` y `allowed`.|
|startupAuthenticationTpmPinUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Indica si el pin de inicio TPM es permitido o necesario o desactivarse. Los valores posibles son: `blocked`, `required` y `allowed`.|
|startupAuthenticationTpmKeyUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Indica si la clave de inicio TPM es permitido o necesario o desactivarse. Los valores posibles son: `blocked`, `required` y `allowed`.|
|startupAuthenticationTpmPinAndKeyUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Indica si el inicio TPM fijar claves y son permitidos o necesario o desactivarse. Los valores posibles son: `blocked`, `required` y `allowed`.|
|minimumPinLength|Int32|Indica la longitud mínima de pin de inicio. Valores válidos de 4 a 20|
|recoveryOptions|[bitLockerRecoveryOptions](../resources/intune-deviceconfig-bitlockerrecoveryoptions.md)|Permite recuperar unidades de sistema operativo de BitLocker cifrada en ausencia de la información de clave de inicio requerido. Esta configuración de directiva se aplica al activar BitLocker.|
|prebootRecoveryEnableMessageAndUrl|Booleano|Habilitar el mensaje de arranque previo a la recuperación y la dirección Url. Si requireStartupAuthentication es false, no afecta este valor.|
|prebootRecoveryMessage|Cadena|Define un mensaje de recuperación personalizada.|
|prebootRecoveryUrl|Cadena|Define una dirección URL de recuperación personalizada.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerSystemDrivePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerSystemDrivePolicy",
  "encryptionMethod": "String",
  "startupAuthenticationRequired": true,
  "startupAuthenticationBlockWithoutTpmChip": true,
  "startupAuthenticationTpmUsage": "String",
  "startupAuthenticationTpmPinUsage": "String",
  "startupAuthenticationTpmKeyUsage": "String",
  "startupAuthenticationTpmPinAndKeyUsage": "String",
  "minimumPinLength": 1024,
  "recoveryOptions": {
    "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
    "blockDataRecoveryAgent": true,
    "recoveryPasswordUsage": "String",
    "recoveryKeyUsage": "String",
    "hideRecoveryOptions": true,
    "enableRecoveryInformationSaveToStore": true,
    "recoveryInformationToStore": "String",
    "enableBitLockerAfterRecoveryInformationToStore": true
  },
  "prebootRecoveryEnableMessageAndUrl": true,
  "prebootRecoveryMessage": "String",
  "prebootRecoveryUrl": "String"
}
```





