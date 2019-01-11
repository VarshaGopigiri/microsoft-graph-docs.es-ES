---
title: tipo de recurso adminConsent
description: Información de consentimiento de administración.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4b6b2d9a8c32c9a1ce7e8587ebe853f7646b703a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815594"
---
# <a name="adminconsent-resource-type"></a>tipo de recurso adminConsent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Información de consentimiento de administración.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|shareAPNSData|[adminConsentState](../resources/intune-devices-adminconsentstate.md)|El estado de consentimiento de administración de uso compartido de datos de usuarios y dispositivos para Apple. Los valores posibles son: `notConfigured`, `granted` y `notGranted`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.adminConsent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.adminConsent",
  "shareAPNSData": "String"
}
```





