---
title: Tipo de recurso windowsInformationProtectionDataRecoveryCertificate
description: Certificado de recuperación de datos de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: c45abb14669c3cf67571748a9da7d62bed037ff6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27325826"
---
# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a>Tipo de recurso windowsInformationProtectionDataRecoveryCertificate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Certificado de recuperación de datos de Windows Information Protection
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|subjectName|cadena|Nombre de asunto del certificado para la recuperación de datos|
|descripción|cadena|Descripción del certificado para la recuperación de datos|
|expirationDateTime|DateTimeOffset|Fecha y hora de expiración del certificado para la recuperación de datos|
|certificado|Binario|Certificado para la recuperación de datos|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
  "subjectName": "String",
  "description": "String",
  "expirationDateTime": "String (timestamp)",
  "certificate": "binary"
}
```





