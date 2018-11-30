---
title: tipo de recurso educationSynchronizationCustomizations
description: Contiene la lista de entidades de sincronización y sus personalizaciones, si hay alguno.
ms.openlocfilehash: d694c5ea1136d38e11ff3f1aca0ad0fde34b9d02
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087409"
---
# <a name="educationsynchronizationcustomizations-resource-type"></a>tipo de recurso educationSynchronizationCustomizations

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene la lista de entidades de sincronización y sus [personalizaciones](educationsynchronizationcustomization.md), si hay alguno.

> **Nota:** Personalización de las propiedades para la sincronización no se aplica a las entidades **studentEnrollment** y **teacherRoster** .

Este recurso es miembro de los proveedores de datos siguientes:

* [educationCsvDataProvider](educationcsvdataprovider.md)
* [educationPowerSchoolDataProvider](educationpowerschooldataprovider.md)

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
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
