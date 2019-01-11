---
title: tipo de recurso educationSynchronizationCustomizations
description: Contiene la lista de entidades de sincronización y sus personalizaciones, si hay alguno.
localization_priority: Normal
ms.openlocfilehash: 0c07b166c09b2bfa6bf88159533523dab869a325
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817041"
---
# <a name="educationsynchronizationcustomizations-resource-type"></a>tipo de recurso educationSynchronizationCustomizations

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene la lista de entidades de sincronización y sus [personalizaciones](educationsynchronizationcustomization.md), si hay alguno.

> **Nota:** Personalización de las propiedades para la sincronización no se aplica a las entidades **studentEnrollment** y **teacherRoster** .

Este recurso es miembro de los proveedores de datos siguientes:

* [educationCsvDataProvider](educationcsvdataprovider.md)
* [educationPowerSchoolDataProvider](educationpowerschooldataprovider.md)

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:-|:-|:-|
| **School** | [educationSynchronizationCustomization](educationsynchronizationcustomization.md) |  Personalización de una entidad de escuela.        |
| **section** | [educationSynchronizationCustomization](educationsynchronizationcustomization.md) |  Personalización de una entidad de sección.         |
| **student** | [educationSynchronizationCustomization](educationsynchronizationcustomization.md) |  Personalización de una entidad de estudiantes.         |
| **teacher** | [educationSynchronizationCustomization](educationsynchronizationcustomization.md) |  Personalización de una entidad de profesor.         |
| **studentEnrollment** | [educationSynchronizationCustomization](educationsynchronizationcustomization.md) |  Personalización de inscripción de estudiantes.           |
| **teacherRoster** | [educationSynchronizationCustomization](educationsynchronizationcustomization.md) |       Personalización de una lista de participantes profesor.    |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationCustomizations"
}-->

```json
{
  "school": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "section": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "student": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "teacher": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "studentEnrollment": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "teacherRoster": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"}
}
```
