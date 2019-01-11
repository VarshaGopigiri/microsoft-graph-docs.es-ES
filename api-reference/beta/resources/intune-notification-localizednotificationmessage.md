---
title: Tipo de recurso localizedNotificationMessage
description: El contenido de texto de una plantilla de mensaje de notificación para la configuración regional.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 53a33c5d83821ff5131b601bd5687e7d98634c00
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825791"
---
# <a name="localizednotificationmessage-resource-type"></a>Tipo de recurso localizedNotificationMessage

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El contenido de texto de una plantilla de mensaje de notificación para la configuración regional.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar localizedNotificationMessages](../api/intune-notification-localizednotificationmessage-list.md)|Colección [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md)|Enumere las propiedades y las relaciones de los objetos [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).|
|[Obtener localizedNotificationMessage](../api/intune-notification-localizednotificationmessage-get.md)|[localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md)|Lea las propiedades y las relaciones del objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).|
|[Crear localizedNotificationMessage](../api/intune-notification-localizednotificationmessage-create.md)|[localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md)|Cree un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).|
|[Eliminar localizedNotificationMessage](../api/intune-notification-localizednotificationmessage-delete.md)|Ninguna|Elimina un [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).|
|[Actualizar localizedNotificationMessage](../api/intune-notification-localizednotificationmessage-update.md)|[localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md)|Actualice las propiedades de un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|configuración regional|String|La configuración regional para la que se destina este mensaje.|
|subject|String|El asunto de la plantilla del mensaje.|
|messageTemplate|String|El contenido de la plantilla del mensaje.|
|isDefault|Booleano|Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma. Solo se puede establecer esta marca. Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.localizedNotificationMessage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "locale": "String",
  "subject": "String",
  "messageTemplate": "String",
  "isDefault": true
}
```





