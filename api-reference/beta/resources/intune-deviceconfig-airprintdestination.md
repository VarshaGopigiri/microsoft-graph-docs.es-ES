---
title: tipo de recurso airPrintDestination
description: Representa un destino de AirPrint.
author: tfitzmac
ms.openlocfilehash: 046f85c65d382b34e6920f30f6b2718f817371a9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361057"
---
# <a name="airprintdestination-resource-type"></a>tipo de recurso airPrintDestination

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa un destino de AirPrint.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|ipAddress|cadena|La dirección IP de destino AirPrint.|
|resourcePath|String|La ruta de acceso de recursos asociados con la impresora. Esto corresponde al parámetro de la _ipps.tcp Bonjour registro rp. Por ejemplo: Canon_MG5300_series/impresoras, impresoras/Xerox_Phaser_7600, ipp, print y Epson_IPP_Printer.|
|port|Int32|El puerto de escucha del destino AirPrint. Si no se especifica esta clave AirPrint va a usar el puerto predeterminado. Disponible en iOS 11.0 y versiones posteriores.|
|forceTls|Boolean|Si es true conexiones AirPrint están protegidas por la seguridad de capa de transporte (TLS). Valor predeterminado es false. Disponible en iOS 11.0 y versiones posteriores.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.airPrintDestination"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.airPrintDestination",
  "ipAddress": "String",
  "resourcePath": "String",
  "port": 1024,
  "forceTls": true
}
```





