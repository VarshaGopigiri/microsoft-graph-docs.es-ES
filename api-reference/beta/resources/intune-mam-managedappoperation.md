---
title: Tipo de recurso managedAppOperation
description: Representa una operación que se aplica a un registro de la aplicación.
ms.openlocfilehash: 267adafc5a74ad447dfb3468cf9238e1c4642e5f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083217"
---
# <a name="managedappoperation-resource-type"></a>Tipo de recurso managedAppOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa una operación que se aplica a un registro de la aplicación.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppOperations](../api/intune-mam-managedappoperation-list.md)|Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)|Enumere las propiedades y las relaciones de los objetos [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Obtener managedAppOperation](../api/intune-mam-managedappoperation-get.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|Lea las propiedades y las relaciones del objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Crear managedAppOperation](../api/intune-mam-managedappoperation-create.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|Cree un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Eliminar managedAppOperation](../api/intune-mam-managedappoperation-delete.md)|Ninguna|Elimina un [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Actualizar managedAppOperation](../api/intune-mam-managedappoperation-update.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|Actualice las propiedades de un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|El nombre de la operación.|
|lastModifiedDateTime|DateTimeOffset|La última vez que se modificó el funcionamiento de la aplicación.|
|estado|String|El estado actual de la operación|
|id|String|Clave de la entidad.|
|version|String|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppOperation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "state": "String",
  "id": "String (identifier)",
  "version": "String"
}
```





