---
title: tipo de recurso windowsKioskActiveDirectoryGroup
description: La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco
ms.openlocfilehash: 18e876b50bdc8c8946bd511348d6ed3a6fc8fe5c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084927"
---
# <a name="windowskioskactivedirectorygroup-resource-type"></a>tipo de recurso windowsKioskActiveDirectoryGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco

Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|groupName|String|El nombre del grupo de AD que se bloqueará a esta configuración de quiosco|

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





