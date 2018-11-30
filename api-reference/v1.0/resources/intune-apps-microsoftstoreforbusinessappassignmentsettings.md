---
title: Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.
ms.openlocfilehash: 62224841548c01ce84901251ab67204b82cbb4c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032562"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a>Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.

Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|useDeviceContext|Booleano|Si se debe usar o no el contexto de ejecución del dispositivo para la aplicación móvil de Microsoft Store para Empresas.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings",
  "useDeviceContext": true
}
```



