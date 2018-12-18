---
title: recursos de educationPowerSchoolDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando PowerSchool se utiliza como el origen de entrada.
author: mmast-msft
ms.openlocfilehash: 714866d03c70aae8ea03a27b63fb3efbb4fa5ba4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312806"
---
# <a name="educationpowerschooldataprovider-resource"></a>recursos de educationPowerSchoolDataProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Se usa para configurar el perfil de sincronización de datos de school cuando [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) se utiliza como el origen de entrada.

Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **connectionUrl** | String | La dirección URL de conexión a la instancia de PowerSchool. |
| **clientId** | String |  El identificador de cliente que se usa para conectarse a PowerSchool. |
| **clientSecret** | String |  El secreto de cliente para autenticar la conexión a la instancia de PowerSchool. |
| **schoolsIds** | Colección String |  La lista de escuelas para sincronizar. |
| **schoolYear** | String |  El año escolar para sincronizar. |
| **allowTeachersInMultipleSchools** | Boolean |  Indica si el origen tiene varios identificadores para un solo alumno o profesor. |
| **personalizaciones** | [educationSynchronizationCustomizations](educationsynchronizationcustomizations.md) | Personalización opcional que se aplicará a los perfiles de sincronización.|

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationPowerSchoolDataProvider"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationPowerSchoolDataProvider",
    "connectionUrl": "String",
    "clientId": "String",
    "clientSecret": "String",
    "schoolsids": ["String"],
    "schoolYear": "String",
    "allowTeachersInMultipleSchools": "Boolean",
    "customizations": { "@odata.type": "microsoft.graph.educationSynchronizationCustomizations" }
}
```
