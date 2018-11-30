---
title: tipo de recurso ndesConnector
description: Entidad que representa un conector OnPrem Ndes.
ms.openlocfilehash: d8cce2601f0f51703cccabe0690165e67b0af2bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083626"
---
# <a name="ndesconnector-resource-type"></a>tipo de recurso ndesConnector

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que representa un conector OnPrem Ndes.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista ndesConnectors](../api/intune-deviceconfig-ndesconnector-list.md)|colección de [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md)|Propiedades de la lista y relaciones de los objetos [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) .|
|[Obtener ndesConnector](../api/intune-deviceconfig-ndesconnector-get.md)|[ndesConnector](../resources/intune-deviceconfig-ndesconnector.md)|Leer las propiedades y las relaciones del objeto [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) .|
|[Crear ndesConnector](../api/intune-deviceconfig-ndesconnector-create.md)|[ndesConnector](../resources/intune-deviceconfig-ndesconnector.md)|Crear un nuevo objeto [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) .|
|[Eliminar ndesConnector](../api/intune-deviceconfig-ndesconnector-delete.md)|Ninguno|Elimina un [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md).|
|[Actualizar ndesConnector](../api/intune-deviceconfig-ndesconnector-update.md)|[ndesConnector](../resources/intune-deviceconfig-ndesconnector.md)|Actualizar las propiedades de un objeto [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave del conector NDES.|
|lastConnectionDateTime|DateTimeOffset|Última hora de conexión para el conector Ndes|
|estado|[ndesConnectorState](../resources/intune-deviceconfig-ndesconnectorstate.md)|Estado de conector NDES. Los valores posibles son: `none`, `active` y `inactive`.|
|displayName|String|El nombre descriptivo del conector Ndes.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.ndesConnector"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.ndesConnector",
  "id": "String (identifier)",
  "lastConnectionDateTime": "String (timestamp)",
  "state": "String",
  "displayName": "String"
}
```





