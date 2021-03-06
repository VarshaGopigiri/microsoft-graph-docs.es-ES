---
title: Tipo de recurso sharedPCAccountManagerPolicy
description: Directiva de administrador de cuentas de PC compartido. Solo se aplica cuando el administrador de cuentas está activado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 42b8824f3f9b18722f69db4f3d0d116b2f46dfd2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914888"
---
# <a name="sharedpcaccountmanagerpolicy-resource-type"></a>Tipo de recurso sharedPCAccountManagerPolicy

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva de administrador de cuentas de PC compartido. Solo se aplica cuando el administrador de cuentas está activado.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|accountDeletionPolicy|[sharedPCAccountDeletionPolicyType](../resources/intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)|Configura cuándo se eliminan las cuentas. Los valores posibles son: `immediate`, `diskSpaceThreshold` y `diskSpaceThresholdOrInactiveThreshold`.|
|cacheAccountsAboveDiskFreePercentage|Int32|Establece el porcentaje de espacio en disco disponible que debería tener un equipo antes de detener la eliminación de cuentas de equipo compartido en caché. Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold. Valores válidos de 0 a 100|
|inactiveThresholdDays|Int32|Especifica si se empezarán a eliminar las cuentas cuando no se haya iniciado sesión durante el período especificado, expresado como número de días. Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.|
|removeAccountsBelowDiskFreePercentage|Int32|Establece el porcentaje de espacio en disco restante en un equipo antes de que se eliminen las cuentas en caché para liberar espacio en disco. Las cuentas que hayan estado inactivas más tiempo se eliminarán en primer lugar. Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThresholdOrInactiveThreshold. Valores válidos de 0 a 100|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.sharedPCAccountManagerPolicy",
  "accountDeletionPolicy": "String",
  "cacheAccountsAboveDiskFreePercentage": 1024,
  "inactiveThresholdDays": 1024,
  "removeAccountsBelowDiskFreePercentage": 1024
}
```





