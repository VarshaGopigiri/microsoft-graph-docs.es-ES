---
title: Tipo de recurso iosNotificationSettings
description: Un elemento que describe la configuración de notificaciones.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 242a15d4b636cf73f0e9a9f29a3f53ce17f2fd00
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972981"
---
# <a name="iosnotificationsettings-resource-type"></a>Tipo de recurso iosNotificationSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Un elemento que describe la configuración de notificaciones.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|bundleID|Cadena|Id. de paquete de la aplicación en el que aplicar esa configuración de notificaciones.|
|appName|Cadena|Nombre de la aplicación que se asociará con el bundleID.|
|publicador|Cadena|Publicador que se asociará con el bundleID.|
|habilitado|Booleano|Indica si se permiten las notificaciones para esta aplicación.|
|showInNotificationCenter|Booleano|Indica si se pueden mostrar notificaciones en el centro de notificaciones.|
|showOnLockScreen|Booleano|Indica si se pueden mostrar notificaciones en la pantalla de bloqueo.|
|alertType|[iosNotificationAlertType](../resources/intune-deviceconfig-iosnotificationalerttype.md)|Indica el tipo de alerta para las notificaciones de esta aplicación. Los valores posibles son: `deviceDefault`, `banner`, `modal` y `none`.|
|badgesEnabled|Booleano|Indica si se permiten los distintivos para esta aplicación.|
|soundsEnabled|Booleano|Indica si se permiten los sonidos para esta aplicación.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNotificationSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNotificationSettings",
  "bundleID": "String",
  "appName": "String",
  "publisher": "String",
  "enabled": true,
  "showInNotificationCenter": true,
  "showOnLockScreen": true,
  "alertType": "String",
  "badgesEnabled": true,
  "soundsEnabled": true
}
```





