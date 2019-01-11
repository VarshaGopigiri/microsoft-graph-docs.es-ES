---
title: tipo de recurso windowsKioskAzureADUser
description: La clase que se usa para identificar una cuenta de usuario de AzureAD para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 57b48bcdbac3f95da37704222cded29ba61cd32d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845888"
---
# <a name="windowskioskazureaduser-resource-type"></a>tipo de recurso windowsKioskAzureADUser

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La clase que se usa para identificar una cuenta de usuario de AzureAD para la configuración de quiosco

Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|userId|Cadena|El identificador del usuario AzureAD que se bloqueará a esta configuración de quiosco|
|userPrincipalName|Cadena|Las cuentas de usuario que se bloqueará a esta configuración de quiosco|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskAzureADUser"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskAzureADUser",
  "userId": "String",
  "userPrincipalName": "String"
}
```





