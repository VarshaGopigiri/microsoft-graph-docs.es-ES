---
title: tipo de recurso windowsKioskActiveDirectoryGroup
description: La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dc9db9aa120411c423492efa162973e33cc4c303
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850529"
---
# <a name="windowskioskactivedirectorygroup-resource-type"></a>tipo de recurso windowsKioskActiveDirectoryGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco

Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|groupName|Cadena|El nombre del grupo de AD que se bloqueará a esta configuración de quiosco|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskActiveDirectoryGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskActiveDirectoryGroup",
  "groupName": "String"
}
```





