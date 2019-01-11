---
title: recursos de educationPowerSchoolDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando PowerSchool se utiliza como el origen de entrada.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 48a23a2e2a50e2e235b5722466c67094275236a1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868785"
---
# <a name="educationpowerschooldataprovider-resource"></a>recursos de educationPowerSchoolDataProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Se usa para configurar el perfil de sincronización de datos de school cuando [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) se utiliza como el origen de entrada.

Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:-|:-|:-|
| **connectionUrl** | Cadena | La dirección URL de conexión a la instancia de PowerSchool. |
| **clientId** | Cadena |  El identificador de cliente que se usa para conectarse a PowerSchool. |
| **clientSecret** | Cadena |  El secreto de cliente para autenticar la conexión a la instancia de PowerSchool. |
| **schoolsIds** | Colección String |  La lista de escuelas para sincronizar. |
| **schoolYear** | Cadena |  El año escolar para sincronizar. |
| **allowTeachersInMultipleSchools** | Booleano |  Indica si el origen tiene varios identificadores para un solo alumno o profesor. |
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
