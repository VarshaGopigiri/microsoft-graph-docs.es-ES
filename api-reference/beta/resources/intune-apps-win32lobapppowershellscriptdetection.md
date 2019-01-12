---
title: tipo de recurso win32LobAppPowerShellScriptDetection
description: Contiene las propiedades de la secuencia de comandos de PowerShell para detectar una aplicación de Win32
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 38a3df87ca5492b89000fc1090395d94c64e1888
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926970"
---
# <a name="win32lobapppowershellscriptdetection-resource-type"></a>tipo de recurso win32LobAppPowerShellScriptDetection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de la secuencia de comandos de PowerShell para detectar una aplicación de Win32

Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|enforceSignatureCheck|Booleano|Un valor que indica si se exige la comprobación de firma|
|runAs32Bit|Booleano|Un valor que indica si este script se debe ejecutar como de 32 bits|
|scriptContent|Cadena|La base64 codificado contenido de la secuencia de comandos para detectar la aplicación de línea de negocio (LoB) de Win32|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppPowerShellScriptDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppPowerShellScriptDetection",
  "enforceSignatureCheck": true,
  "runAs32Bit": true,
  "scriptContent": "String"
}
```





