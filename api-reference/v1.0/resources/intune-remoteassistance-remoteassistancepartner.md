---
title: Tipo de recurso remoteAssistancePartner
description: Los recursos remoteAssistPartner representan los metadatos y el estado de un servicio de partner de asistencia remota específico.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dc0f788d9a083b1d1b6dda30170a06fd62d80908
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915581"
---
# <a name="remoteassistancepartner-resource-type"></a>Tipo de recurso remoteAssistancePartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Los recursos remoteAssistPartner representan los metadatos y el estado de un servicio de partner de asistencia remota específico.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar remoteAssistancePartners](../api/intune-remoteassistance-remoteassistancepartner-list.md)|Colección [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md)|Enumere las propiedades y las relaciones de los objetos [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).|
|[Obtener remoteAssistancePartner](../api/intune-remoteassistance-remoteassistancepartner-get.md)|[remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md)|Lea las propiedades y las relaciones del objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).|
|[Crear remoteAssistancePartner](../api/intune-remoteassistance-remoteassistancepartner-create.md)|[remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md)|Cree un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).|
|[Eliminar remoteAssistancePartner](../api/intune-remoteassistance-remoteassistancepartner-delete.md)|Ninguna|Elimina un [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).|
|[Actualizar remoteAssistancePartner](../api/intune-remoteassistance-remoteassistancepartner-update.md)|[remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md)|Actualice las propiedades de un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).|
|[Acción beginOnboarding](../api/intune-remoteassistance-remoteassistancepartner-beginonboarding.md)|Ninguna|Todavía no documentado|
|[Acción disconnect](../api/intune-remoteassistance-remoteassistancepartner-disconnect.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del partner.|
|displayName|String|Nombre para mostrar del partner.|
|onboardingUrl|String|Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.|
|onboardingStatus|[remoteAssistanceOnboardingStatus](../resources/intune-remoteassistance-remoteassistanceonboardingstatus.md)|TBD. Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.|
|lastConnectionDateTime|DateTimeOffset|Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.remoteAssistancePartner"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "id": "String (identifier)",
  "displayName": "String",
  "onboardingUrl": "String",
  "onboardingStatus": "String",
  "lastConnectionDateTime": "String (timestamp)"
}
```



