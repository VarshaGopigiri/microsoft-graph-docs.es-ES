---
title: tipo de recurso educationSynchronizationCustomization
description: 'Proporciona opciones de configuración para personalizar la sincronización de perfiles de datos de school de las entidades de recurso. La personalización puede aplicarse a todas las entidades que se están sincronizadas. '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: c4e8810202dbae5fdc3d978bd27e0463f0424d2e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962873"
---
# <a name="educationsynchronizationcustomization-resource-type"></a>tipo de recurso educationSynchronizationCustomization

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Proporciona opciones de configuración para personalizar la sincronización de perfiles de datos de school de las entidades de recurso. La personalización puede aplicarse a todas las entidades que se están sincronizadas. 

>**Nota:** La propiedad **synchronizationStartDate** sólo se aplica a la entidad **StudentEnrollment** .

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **optionalPropertiesToSync** | colección de cadena |  La colección de nombres de propiedad para la sincronización. Si establece en null, todas las propiedades será sincronizado.       |
| **synchronizationStartDate** | DateTime |  La fecha en la que debe comenzar la sincronización. Este valor debe establecerse en una fecha futura. Si se establece en null, el recurso se sincronizará cuando se complete la configuración del perfil. **Nota:** Esto sólo se aplica a la propiedad **StudentEnrollment** .      |
|**isSyncDeferred** |Booleano | Indica si la sincronización de la entidad principal se aplaza hasta una fecha posterior. |
| **allowDisplayNameUpdate** | Booleano |  Indica si el nombre para mostrar del recurso se puede sobrescribir con la sincronización.         |


## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationCustomization"
}-->

```json
{  
    "optionalPropertiesToSync":["String"],
    "synchronizationStartDate": "DateTimeOffset",
    "isSyncDeferred": "Boolean",
    "allowDisplayNameUpdate": "Boolean"
}
```
