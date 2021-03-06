---
title: tipo de recurso windowsEnrollmentStatusScreenSettings
description: Configuración de pantalla de estado de inscripción
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: abc48a1d63cc514d2ec887a7758e69a0ea8112a7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978574"
---
# <a name="windowsenrollmentstatusscreensettings-resource-type"></a>tipo de recurso windowsEnrollmentStatusScreenSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de pantalla de estado de inscripción
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|hideInstallationProgress|Booleano|Mostrar u ocultar el progreso de la instalación para el usuario|
|allowDeviceUseBeforeProfileAndAppInstallComplete|Booleano|Permitir o bloquear al usuario que utilice el dispositivo antes de la instalación de perfiles y la aplicación completa|
|blockDeviceSetupRetryByUser|Booleano|Permitir al usuario que vuelva a intentar la instalación en caso de error de instalación|
|allowLogCollectionOnInstallFailure|Booleano|Permitir o bloquear registro colección en caso de error de instalación|
|customErrorMessage|Cadena|Establecer el mensaje de error personalizado para mostrar al producirse un error de instalación|
|installProgressTimeoutInMinutes|Int32|Establecer tiempo de espera de progreso de la instalación en minutos|
|allowDeviceUseOnInstallFailure|Booleano|Permitir que el usuario continuar utilizando el dispositivo en caso de error de instalación|

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





