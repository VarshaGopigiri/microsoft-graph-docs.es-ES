---
title: Tipo de recurso onPremisesConditionalAccessSettings
description: Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.
author: tfitzmac
ms.openlocfilehash: 534d76b00246763c6dec49149920a1f296148596
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353931"
---
# <a name="onpremisesconditionalaccesssettings-resource-type"></a>Tipo de recurso onPremisesConditionalAccessSettings

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener onPremisesConditionalAccessSettings](../api/intune-onboarding-onpremisesconditionalaccesssettings-get.md)|[onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|Lea las propiedades y las relaciones del objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).|
|[Actualizar onPremisesConditionalAccessSettings](../api/intune-onboarding-onpremisesconditionalaccesssettings-update.md)|[onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Todavía no documentado|
|enabled|Booleano|Indica si está habilitado el acceso condicional local para esta organización|
|includedGroups|Colección Guid|Grupos de usuarios a los que se dirigirá el acceso condicional local. Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.|
|excludedGroups|Colección Guid|Grupos de usuarios que estarán exentos del acceso condicional local. Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.|
|overrideDefaultRule|Booleano|Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.onPremisesConditionalAccessSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.onPremisesConditionalAccessSettings",
  "id": "String (identifier)",
  "enabled": true,
  "includedGroups": [
    "Guid"
  ],
  "excludedGroups": [
    "Guid"
  ],
  "overrideDefaultRule": true
}
```



