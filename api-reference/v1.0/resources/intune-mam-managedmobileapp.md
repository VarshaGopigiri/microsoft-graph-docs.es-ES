---
title: Tipo de recurso managedMobileApp
description: El identificador de la implementación de una aplicación.
ms.openlocfilehash: 7915ef27dccfeef681475161261f36b64b79ff23
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032625"
---
# <a name="managedmobileapp-resource-type"></a>Tipo de recurso managedMobileApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El identificador de la implementación de una aplicación.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedMobileApps](../api/intune-mam-managedmobileapp-list.md)|Colección [managedMobileApp](../resources/intune-mam-managedmobileapp.md)|Enumere las propiedades y las relaciones de los objetos [managedMobileApp](../resources/intune-mam-managedmobileapp.md).|
|[Obtener managedMobileApp](../api/intune-mam-managedmobileapp-get.md)|[managedMobileApp](../resources/intune-mam-managedmobileapp.md)|Lea las propiedades y las relaciones del objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).|
|[Crear managedMobileApp](../api/intune-mam-managedmobileapp-create.md)|[managedMobileApp](../resources/intune-mam-managedmobileapp.md)|Cree un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).|
|[Eliminar managedMobileApp](../api/intune-mam-managedmobileapp-delete.md)|Ninguna|Elimina un [managedMobileApp](../resources/intune-mam-managedmobileapp.md).|
|[Actualizar managedMobileApp](../api/intune-mam-managedmobileapp-update.md)|[managedMobileApp](../resources/intune-mam-managedmobileapp.md)|Actualice las propiedades de un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|mobileAppIdentifier|[mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)|El identificador de una aplicación con el tipo de sistema operativo.|
|id|String|Clave de la entidad.|
|version|String|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedMobileApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "String (identifier)",
  "version": "String"
}
```



