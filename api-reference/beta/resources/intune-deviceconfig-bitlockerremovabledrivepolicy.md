---
title: Tipo de recurso bitLockerRemovableDrivePolicy
description: Directivas de unidad extraíble de BitLocker
author: tfitzmac
ms.openlocfilehash: 15de11384195350b455cd4696a260aedf1de7a26
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354038"
---
# <a name="bitlockerremovabledrivepolicy-resource-type"></a>Tipo de recurso bitLockerRemovableDrivePolicy

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directivas de unidad extraíble de BitLocker
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|encryptionMethod|[bitLockerEncryptionMethod](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|Seleccione el método de cifrado para las unidades extraíbles. Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.|
|requireEncryptionForWriteAccess|Booleano|Indica si se bloquea el acceso de escritura a dispositivos configurados en otra organización.  Si requireEncryptionForWriteAccess es false, este valor no se aplica.|
|blockCrossOrganizationWriteAccess|Booleano|Esta configuración de directiva determina si es necesaria la protección BitLocker para que se pueda escribir en las unidades de datos extraíbles en un equipo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerRemovableDrivePolicy",
  "encryptionMethod": "String",
  "requireEncryptionForWriteAccess": true,
  "blockCrossOrganizationWriteAccess": true
}
```





