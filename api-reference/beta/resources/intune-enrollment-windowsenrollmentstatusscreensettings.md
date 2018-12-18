---
title: tipo de recurso windowsEnrollmentStatusScreenSettings
description: Configuración de pantalla de estado de inscripción
author: tfitzmac
ms.openlocfilehash: 8ccf2565d722a09de5f08ebe7333436729ce1b2e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346931"
---
# <a name="windowsenrollmentstatusscreensettings-resource-type"></a>tipo de recurso windowsEnrollmentStatusScreenSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de pantalla de estado de inscripción
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|hideInstallationProgress|Boolean|Mostrar u ocultar el progreso de la instalación para el usuario|
|allowDeviceUseBeforeProfileAndAppInstallComplete|Boolean|Permitir o bloquear al usuario que utilice el dispositivo antes de la instalación de perfiles y la aplicación completa|
|blockDeviceSetupRetryByUser|Boolean|Permitir al usuario que vuelva a intentar la instalación en caso de error de instalación|
|allowLogCollectionOnInstallFailure|Boolean|Permitir o bloquear registro colección en caso de error de instalación|
|customErrorMessage|String|Establecer el mensaje de error personalizado para mostrar al producirse un error de instalación|
|installProgressTimeoutInMinutes|Int32|Establecer tiempo de espera de progreso de la instalación en minutos|
|allowDeviceUseOnInstallFailure|Boolean|Permitir que el usuario continuar utilizando el dispositivo en caso de error de instalación|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsEnrollmentStatusScreenSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsEnrollmentStatusScreenSettings",
  "hideInstallationProgress": true,
  "allowDeviceUseBeforeProfileAndAppInstallComplete": true,
  "blockDeviceSetupRetryByUser": true,
  "allowLogCollectionOnInstallFailure": true,
  "customErrorMessage": "String",
  "installProgressTimeoutInMinutes": 1024,
  "allowDeviceUseOnInstallFailure": true
}
```





