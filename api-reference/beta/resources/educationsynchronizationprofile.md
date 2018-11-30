---
title: tipo de recurso educationSynchronizationProfile
description: Representa un conjunto de configuraciones que se usa para sincronizar la información de la lista de participantes desde un directorio de origen para Azure Active Directory (AD Azure) y entidades de educación. Este recurso proporciona una representación mediante programación utilizada en la sincronización de datos de School.
ms.openlocfilehash: 89b605a7044526975f8caa6d7a1b6a716f012921
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090459"
---
# <a name="educationsynchronizationprofile-resource-type"></a>tipo de recurso educationSynchronizationProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un conjunto de configuraciones que se usa para sincronizar la información de la lista de participantes desde un directorio de origen para Azure Active Directory (AD Azure) y entidades de educación. Este recurso proporciona una representación mediante programación utilizada en la [Sincronización de datos de School](https://sds.microsoft.com).

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:-|:-|:-|
| [Perfiles de sincronización de lista](../api/educationsynchronizationprofile-list.md) | colección de **educationSynchronizationProfile** | Obtener una lista de todos los perfiles de sincronización en el inquilino. |
| [Obtener el perfil de sincronización](../api/educationsynchronizationprofile-get.md) | **educationSynchronizationProfile** | Recuperar un perfil específico especifica el identificador de perfil. |
| [Crear perfil de sincronización](../api/educationsynchronizationprofile-post.md) | Ninguno | Crear un nuevo perfil de sincronización. |
| [Eliminar el perfil de sincronización](../api/educationsynchronizationprofile-delete.md) | **educationSynchronizationProfile** | Eliminar un perfil específico especifica el identificador de perfil. |
| [Detener una sincronización en curso](../api/educationsynchronizationprofile-pause.md) | Ninguno | Detener una sincronización en curso. |
| [Reanudar una sincronización en pausa](../api/educationsynchronizationprofile-resume.md) | Ninguno | Reanudar una sincronización en pausa. |
| [Restablecer una sincronización](../api/educationsynchronizationprofile-reset.md) | Ninguno | Restablecer el estado de los perfiles y reinicie la sincronización. |
| [Iniciar la sincronización para los archivos cargados](../api/educationsynchronizationprofile-start.md) | colección de [educationFileSynchronizationVerificationMessage](educationfilesynchronizationverificationmessage.md)| Compruebe los archivos de origen que se cargan e iniciar la sincronización. Sólo se aplica cuando el proveedor de datos es [educationCsvDataProvider](educationcsvdataprovider.md). |
| [Obtener una dirección URL de carga](../api/educationsynchronizationprofile-uploadurl.md) | string | Devolver la dirección URL de corta duración para cargar los archivos de datos CSV. Sólo se aplica cuando el proveedor de datos es [educationCsvDataProvider](educationcsvdataprovider.md). |
| [Obtener el estado de una sincronización](../api/educationsynchronizationprofilestatus-get.md) | [status](educationsynchronizationprofilestatus.md) | Devolver el estado de un perfil de sincronización específica. |
| [Obtener errores de sincronización](../api/educationsynchronizationerrors-get.md) | colección de [educationSynchronizationError](educationsynchronizationerror.md)| Obtener todos los errores generados durante la sincronización. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **displayName** | string |  Nombre del perfil de configuración para la sincronización de identidades.         |
| **dataProvider** | [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md) |  El proveedor de datos utilizado para el perfil.         |
| **identitysynchronizationconfiguration** | [educationIdentitySynchronizationConfiguration](educationidentitysynchronizationconfiguration.md) | Configuración de [creación](educationidentitycreationconfiguration.md) o [coincidentes](educationidentitymatchingconfiguration.md) de identidad.        |
| **licensesToAssign** | colección de [educationSynchronizationLicenseAssignment](educationsynchronizationlicenseassignment.md)|  Configuración de licencia del programa de instalación.        |
| **state** | string |  El estado de los perfiles. Los valores posibles son: `provisioning`, `provisioned`, `provisioningFailed`, `deleting` y `deletionFailed`.          |

## <a name="relationships"></a>Relaciones

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **errors** | colección de [educationSynchronizationError](educationsynchronizationerror.md)| Todos los errores asociados a este perfil de sincronización. |
| **profileStatus** | [educationSynchronizationProfileStatus](educationsynchronizationprofilestatus.md) | El estado de sincronización. |

## <a name="json-representation"></a>Representación JSON
La siguiente es una representación de JSON del recurso **educationSynchronizationProfile** .

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationProfile"
}-->

```json
{
    "displayName": "String",
    "state": { "@odata.type": "microsoft.graph.educationSynchronizationProfileState" },
    "profileStatus": {"@odata.type": "microsoft.graph.educationSynchronizationProfileStatus"},
    "errors": [{"@odata.type": "microsoft.graph.educationSynchronizationProfileStatus" }],
    "dataProvider": { "@odata.type": "#microsoft.graph.educationcsvdataprovider" },
    "identitySynchronizationConfiguration": { "@odata.type": "#microsoft.graph.educationIdentitySynchronizationConfiguration" },
    "licensesToAssign": [{"@odata.type":"microsoft.graph.educationSynchronizationLicenseAssignment"}],
    "handleSpecialCharacterConstraint": "Boolean"
}
```
