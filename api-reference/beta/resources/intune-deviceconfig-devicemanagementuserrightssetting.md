---
title: tipo de recurso deviceManagementUserRightsSetting
description: Representa una configuración de permisos de usuario.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 889ce941037013cb66134f9c78aa18fb90aed29a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931751"
---
# <a name="devicemanagementuserrightssetting-resource-type"></a>tipo de recurso deviceManagementUserRightsSetting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa una configuración de permisos de usuario.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|state|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Configuración de los derechos que representa el estado actual de este usuario. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|localUsersOrGroups|colección de [deviceManagementUserRightsLocalUserOrGroup](../resources/intune-deviceconfig-devicemanagementuserrightslocaluserorgroup.md)|Que representa una colección de usuarios locales o grupos que se establecerá en el dispositivo si se permite el estado de esta configuración. Esta colección puede contener un máximo de 500 elementos.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementUserRightsSetting",
  "state": "String",
  "localUsersOrGroups": [
    {
      "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
      "name": "String",
      "description": "String",
      "securityIdentifier": "String"
    }
  ]
}
```





