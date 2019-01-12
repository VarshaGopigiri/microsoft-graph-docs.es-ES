---
title: tipo de recurso loggedOnUser
description: Ha iniciado la sesión de usuario
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 056fae8051b70f2146930c8a2a1ae9505c0ec679
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962096"
---
# <a name="loggedonuser-resource-type"></a>tipo de recurso loggedOnUser

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Ha iniciado la sesión de usuario
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|userId|Cadena|Identificador de usuario|
|lastLogOnDateTime|DateTimeOffset|Fecha hora cuando el usuario inicia sesión|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.loggedOnUser"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.loggedOnUser",
  "userId": "String",
  "lastLogOnDateTime": "String (timestamp)"
}
```





