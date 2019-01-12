---
title: Tipo de recurso managedAppPolicy
description: El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5054566f0ee80940165ba19f8f0da197b5e4f3c0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981108"
---
# <a name="managedapppolicy-resource-type"></a>Tipo de recurso managedAppPolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppPolicies](../api/intune-mam-managedapppolicy-list.md)|Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|[Obtener managedAppPolicy](../api/intune-mam-managedapppolicy-get.md)|[managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).|
|[Acción targetApps](../api/intune-mam-managedapppolicy-targetapps.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre para mostrar de la directiva.|
|descripción|Cadena|La descripción de la directiva.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la directiva.|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva.|
|id|Cadena|Clave de la entidad.|
|version|Cadena|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicy",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String"
}
```



