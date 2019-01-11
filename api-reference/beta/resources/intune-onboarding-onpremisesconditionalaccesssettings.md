---
title: Tipo de recurso onPremisesConditionalAccessSettings
description: Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d21a74ecffebde15a2a0a89a79e7b6c95e1f53be
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804546"
---
# <a name="onpremisesconditionalaccesssettings-resource-type"></a>Tipo de recurso onPremisesConditionalAccessSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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
|id|Cadena|Todavía no documentado|
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





