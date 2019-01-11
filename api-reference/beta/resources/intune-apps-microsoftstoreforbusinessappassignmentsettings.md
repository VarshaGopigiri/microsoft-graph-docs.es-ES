---
title: Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8ef23919912d8a91beceefeb034de7cc09cb941c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805029"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a>Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





