---
title: tipo de recurso educationIdentityCreationConfiguration
description: Define la configuración de creación de identidades de perfil de datos de school. Estas identidades incluyen estudiantes y profesores. En función de esta configuración, los usuarios se crearán en el directorio.
ms.openlocfilehash: edbfa03bb574a1d8d9d4faaa2032ec82f6d20f66
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090163"
---
## <a name="educationidentitycreationconfiguration-resource-type"></a>tipo de recurso educationIdentityCreationConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define la configuración de creación de identidades de perfil de datos de school. Estas identidades incluyen estudiantes y profesores. En función de esta configuración, los usuarios se crearán en el directorio.

> **Nota:** Si ha activado para la sincronización entre local de Active Directory y Azure Active Directory (AD Azure) de sincronización de directorios, use el recurso [educationIdentityMatchingConfiguration](educationidentitymatchingconfiguration.md) en su lugar.

Deriva de [educationIdentitySynchronizationConfiguration](educationidentitysynchronizationconfiguration.md).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **userDomains** | colección de [educationIdentityDomain](educationidentitydomain.md) |  Establece la lista de dominios que se usará por tipo de usuario.  |


## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityCreationConfiguration"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationIdentityCreationConfiguration",
    "userDomains": [
        {
            "@odata.type": "#microsoft.graph.educationIdentityDomain",
        }
    ]
}
```