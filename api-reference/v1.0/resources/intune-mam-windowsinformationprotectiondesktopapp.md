---
title: Tipo de recurso windowsInformationProtectionDesktopApp
description: Aplicación de escritorio de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c381541379feacff7611e77882069c5fe2119e67
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822067"
---
# <a name="windowsinformationprotectiondesktopapp-resource-type"></a>Tipo de recurso windowsInformationProtectionDesktopApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Aplicación de escritorio de Windows Information Protection

Hereda de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar de la aplicación. Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)|
|descripción|cadena|La descripción de la aplicación. Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)|
|publisherName|cadena|Nombre del publicador. Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)|
|productName|cadena|El nombre del producto. Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)|
|denegado|Booleano|Si es true, se deniega la protección o la exención a la aplicación. Heredado de [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)|
|binaryName|cadena|El nombre del binario.|
|binaryVersionLow|cadena|La versión binaria inferior.|
|binaryVersionHigh|cadena|La versión binaria superior.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDesktopApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDesktopApp",
  "displayName": "String",
  "description": "String",
  "publisherName": "String",
  "productName": "String",
  "denied": true,
  "binaryName": "String",
  "binaryVersionLow": "String",
  "binaryVersionHigh": "String"
}
```



