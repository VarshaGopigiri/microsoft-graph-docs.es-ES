---
title: tipo de recurso certificateConnectorSetting
description: Configuración de conector de certificados.
author: tfitzmac
ms.openlocfilehash: 8c993634eb4f41e16643ae3f40be74ecc3eb392f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326309"
---
# <a name="certificateconnectorsetting-resource-type"></a>tipo de recurso certificateConnectorSetting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de conector de certificados.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|status|Int32|Estado del conector de certificado|
|certExpiryTime|DateTimeOffset|Certificado caduque tiempo|
|enrollmentError|String|Error de inscripción de conector de certificado|
|lastConnectorConnectionTime|DateTimeOffset|Última vez certificado conector conectado|
|connectorVersion|String|Versión del conector de certificado|
|lastUploadVersion|Int64|Versión del conector de certificado que se cargan última|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.certificateConnectorSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.certificateConnectorSetting",
  "status": 1024,
  "certExpiryTime": "String (timestamp)",
  "enrollmentError": "String",
  "lastConnectorConnectionTime": "String (timestamp)",
  "connectorVersion": "String",
  "lastUploadVersion": 1024
}
```





