---
title: tipo de recurso deviceManagementUserRightsLocalUserOrGroup
description: Representa información de un usuario local o el grupo que se utiliza para establecer los derechos de usuario.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 63e2dc3d16d17b76c4437e76eae642976711071c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972897"
---
# <a name="devicemanagementuserrightslocaluserorgroup-resource-type"></a>tipo de recurso deviceManagementUserRightsLocalUserOrGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa información de un usuario local o el grupo que se utiliza para establecer los derechos de usuario.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|name|Cadena|El nombre de este usuario o grupo local.|
|descripción|Cadena|Descripción del Administrador de este usuario o grupo local.|
|securityIdentifier|Cadena|El identificador de seguridad de este usuario o grupo local (por ejemplo, * S-1-5-32-544).|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
  "name": "String",
  "description": "String",
  "securityIdentifier": "String"
}
```





