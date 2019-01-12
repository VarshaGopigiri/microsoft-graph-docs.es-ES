---
title: Tipo de recurso managedAppConfiguration
description: Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5571a1c4b3f115280499ead992758a8ff46b2f26
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963671"
---
# <a name="managedappconfiguration-resource-type"></a>Tipo de recurso managedAppConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.

Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppConfigurations](../api/intune-mam-managedappconfiguration-list.md)|Colección [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).|
|[Obtener managedAppConfiguration](../api/intune-mam-managedappconfiguration-get.md)|[managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)|Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|descripción|String|Descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|id|String|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|version|String|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|customSettings|Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)|Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppConfiguration",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ]
}
```





