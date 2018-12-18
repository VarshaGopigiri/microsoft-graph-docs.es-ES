---
title: tipo de recurso windowsKioskAzureADGroup
description: La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco
author: tfitzmac
ms.openlocfilehash: 3c4cdd8388c71b5f051ea8338e82123c241ec429
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339525"
---
# <a name="windowskioskazureadgroup-resource-type"></a>tipo de recurso windowsKioskAzureADGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco

Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|El nombre para mostrar del grupo AzureAD que se bloqueará a esta configuración de quiosco|
|groupId|String|El identificador del grupo AzureAD que se bloqueará a esta configuración de quiosco|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskAzureADGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskAzureADGroup",
  "displayName": "String",
  "groupId": "String"
}
```





