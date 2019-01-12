---
title: tipo de recurso enrollmentProfile
description: El recurso enrollmentProfile representa una colección de configuraciones que debe proporcionarse previo a la inscripción para habilitar la inscripción de ciertos dispositivos cuyas identidades han sido previamente por fases. Las identidades del dispositivo previamente por fases se asignan a este tipo de perfil para aplicar las configuraciones del perfil en inscripción del dispositivo correspondiente.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: b88745c060e71e32199a96b23f94fa0d3229d451
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935594"
---
# <a name="enrollmentprofile-resource-type"></a>tipo de recurso enrollmentProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso enrollmentProfile representa una colección de configuraciones que debe proporcionarse previo a la inscripción para habilitar la inscripción de ciertos dispositivos cuyas identidades han sido previamente por fases. Las identidades del dispositivo previamente por fases se asignan a este tipo de perfil para aplicar las configuraciones del perfil en inscripción del dispositivo correspondiente.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista enrollmentProfiles](../api/intune-enrollment-enrollmentprofile-list.md)|colección de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|Propiedades de la lista y relaciones de los objetos [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .|
|[Obtener enrollmentProfile](../api/intune-enrollment-enrollmentprofile-get.md)|[enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|Leer las propiedades y las relaciones del objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .|
|[Crear enrollmentProfile](../api/intune-enrollment-enrollmentprofile-create.md)|[enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|Crear un nuevo objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .|
|[Eliminar enrollmentProfile](../api/intune-enrollment-enrollmentprofile-delete.md)|Ninguno|Elimina un [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).|
|[Actualizar enrollmentProfile](../api/intune-enrollment-enrollmentprofile-update.md)|[enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)|Actualizar las propiedades de un objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .|
|[acción setDefaultProfile](../api/intune-enrollment-enrollmentprofile-setdefaultprofile.md)|Ninguno|Todavía no documentado|
|[exportMobileConfig (función)](../api/intune-enrollment-enrollmentprofile-exportmobileconfig.md)|Cadena|Exporta la configuración móvil|
|[acción updateDeviceProfileAssignment](../api/intune-enrollment-enrollmentprofile-updatedeviceprofileassignment.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El GUID para el objeto|
|displayName|Cadena|Nombre del perfil|
|descripción|Cadena|Descripción del perfil|
|requiresUserAuthentication|Booleano|Indica si el perfil requiere autenticación de usuario|
|configurationEndpointUrl|Cadena|Dirección url de extremo de configuración que se usará para inscripción|
|enableAuthenticationViaCompanyPortal|Booleano|Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.enrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.enrollmentProfile",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "String",
  "enableAuthenticationViaCompanyPortal": true
}
```





