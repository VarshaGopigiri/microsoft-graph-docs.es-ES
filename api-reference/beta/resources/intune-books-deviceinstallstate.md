---
title: Tipo de recurso deviceInstallState
description: Contiene las propiedades del estado de la instalación para un dispositivo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1b495bc41590ada44a9986dd9cc9cb262bcc68b6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959891"
---
# <a name="deviceinstallstate-resource-type"></a>Tipo de recurso deviceInstallState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del estado de la instalación para un dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceInstallStates](../api/intune-books-deviceinstallstate-list.md)|Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)|Enumere las propiedades y las relaciones de los objetos [deviceInstallState](../resources/intune-books-deviceinstallstate.md).|
|[Obtener deviceInstallState](../api/intune-books-deviceinstallstate-get.md)|[deviceInstallState](../resources/intune-books-deviceinstallstate.md)|Lea las propiedades y las relaciones del objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).|
|[Crear deviceInstallState](../api/intune-books-deviceinstallstate-create.md)|[deviceInstallState](../resources/intune-books-deviceinstallstate.md)|Cree un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).|
|[Eliminar deviceInstallState](../api/intune-books-deviceinstallstate-delete.md)|Ninguna|Elimina un [deviceInstallState](../resources/intune-books-deviceinstallstate.md).|
|[Actualizar deviceInstallState](../api/intune-books-deviceinstallstate-update.md)|[deviceInstallState](../resources/intune-books-deviceinstallstate.md)|Actualice las propiedades de un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|deviceName|String|Nombre del dispositivo.|
|deviceId|String|Id. del dispositivo|
|lastSyncDateTime|DateTimeOffset|Fecha y hora de la última sincronización.|
|installState|[installState](../resources/intune-books-installstate.md)|El estado de instalación del libro electrónico. Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.|
|errorCode|String|El código de error si hay errores de instalación.|
|osVersion|Cadena|Versión del sistema operativo.|
|osDescription|String|Descripción del sistema operativo.|
|userName|String|Nombre de usuario del dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceInstallState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "id": "String (identifier)",
  "deviceName": "String",
  "deviceId": "String",
  "lastSyncDateTime": "String (timestamp)",
  "installState": "String",
  "errorCode": "String",
  "osVersion": "String",
  "osDescription": "String",
  "userName": "String"
}
```





