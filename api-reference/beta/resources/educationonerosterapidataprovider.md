---
title: recursos de educationOneRosterApiDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando se usa la API OneRoster como el origen de entrada.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 681a3331aba7bc84ac80911c4be8076d104f8a58
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938149"
---
# <a name="educationonerosterapidataprovider-resource"></a>recursos de educationOneRosterApiDataProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Se usa para configurar el perfil de sincronización de datos de school cuando se usa la [API de OneRoster](https://www.imsglobal.org/activity/onerosterlis) como el origen de entrada.

Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **connectionUrl** | Cadena | La dirección URL de conexión a la instancia de OneRoster. |
| **schoolsIds** | Colección String |  La lista de sourcedIds school para sincronizar. |
| **providerName** | Cadena | El nombre del proveedor de servicio de OneRoster tal y como se define en la [especificación de OneRoster](https://www.imsglobal.org/oneroster-v11-final-best-practice-and-implementation-guide#AppA). |
| **connectionSettings** | [educationSynchronizationConnectionSettings](educationsynchronizationconnectionsettings.md) | Configuración de conexión para la instancia de OneRoster. Debe ser del tipo [educationSynchronizationOAuth1ConnectionSettings](educationsynchronizationoauth1connectionsettings.md) o [educationSynchronizationOAuth2ClientCredentialsConnectionSettings](educationsynchronizationoauth2clientcredentialsconnectionsettings.md). |
| **personalizaciones** | [educationSynchronizationCustomizations](educationsynchronizationcustomizations.md) | Personalización opcional que se aplicará a los perfiles de sincronización.|

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationoneRosterApiDataProvider"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationoneRosterApiDataProvider",
    "connectionUrl": "String",
    "providerName": "String",
    "schoolsIds": [
        "String"
    ],
    "connectionSettings": {
        "@odata.type": "#microsoft.graph.educationSynchronizationOAuth1ConnectionSettings",
        "clientId": "String",
        "clientSecret": "String",
    },
    "customizations": { "@odata.type": "microsoft.graph.educationSynchronizationCustomizations" }
}
```
