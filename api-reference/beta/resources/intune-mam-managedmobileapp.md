---
title: Tipo de recurso managedMobileApp
description: El identificador de la implementación de una aplicación.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: eedb5c565a25007db7e8a4a98f54e7363cf6187f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964595"
---
# <a name="managedmobileapp-resource-type"></a>Tipo de recurso managedMobileApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





