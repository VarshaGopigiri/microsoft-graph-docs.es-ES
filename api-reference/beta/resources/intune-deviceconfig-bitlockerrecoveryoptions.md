---
title: tipo de recurso bitLockerRecoveryOptions
description: Opciones de recuperación de BitLocker.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: eae2052f71d1b1d048072c70dc76437811c1cd8f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806457"
---
# <a name="bitlockerrecoveryoptions-resource-type"></a>tipo de recurso bitLockerRecoveryOptions

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Opciones de recuperación de BitLocker.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|blockDataRecoveryAgent|Booleano|Indica si se debe bloquear el agente de recuperación de datos basada en certificados.|
|recoveryPasswordUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Indica si los usuarios están permitidos o necesarios para generar una contraseña de recuperación de 48 dígitos para fijo o disco de sistema. Los valores posibles son: `blocked`, `required` y `allowed`.|
|recoveryKeyUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Indica si los usuarios están permitidos o necesarios para generar una clave de recuperación de 256 bits para fijo o disco de sistema. Los valores posibles son: `blocked`, `required` y `allowed`.|
|hideRecoveryOptions|Booleano|Indica si se debe o no permitir que muestra las opciones de recuperación en el Asistente para la instalación de BitLocker para fijo o disco de sistema.|
|enableRecoveryInformationSaveToStore|Booleano|Indica si se debe o no permitir la información de recuperación de BitLocker almacenar en AD DS.|
|recoveryInformationToStore|[bitLockerRecoveryInformationType](../resources/intune-deviceconfig-bitlockerrecoveryinformationtype.md)|Configurar qué elementos de información de recuperación de BitLocker se almacenan en AD DS. Los valores posibles son: `passwordAndKey` y `passwordOnly`.|
|enableBitLockerAfterRecoveryInformationToStore|Booleano|Indica si se va a habilitar BitLocker hasta que se almacena información de recuperación en AD DS o no.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerRecoveryOptions"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerRecoveryOptions",
  "blockDataRecoveryAgent": true,
  "recoveryPasswordUsage": "String",
  "recoveryKeyUsage": "String",
  "hideRecoveryOptions": true,
  "enableRecoveryInformationSaveToStore": true,
  "recoveryInformationToStore": "String",
  "enableBitLockerAfterRecoveryInformationToStore": true
}
```





