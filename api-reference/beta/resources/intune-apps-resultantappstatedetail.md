---
title: tipo de enumeración resultantAppStateDetail
description: Enum que indica obtener más información acerca de por qué una aplicación tiene un determinado estado de instalación.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5c5eb8c921be7c14a45c979a57ffcaa0704d9b4b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874147"
---
# <a name="resultantappstatedetail-enum-type"></a>tipo de enumeración resultantAppStateDetail

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Enum que indica obtener más información acerca de por qué una aplicación tiene un determinado estado de instalación.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|noAdditionalDetails|0|No hay detalles adicionales están disponibles.|
|seeInstallErrorCode|2000|No se pudo instalar la aplicación. Vea la propiedad de código de error para obtener más detalles.|
|seeUninstallErrorCode|4000|No se pudo desinstalar la aplicación. Vea la propiedad de código de error para obtener más detalles.|
|pendingReboot|5000|Debe reiniciar el dispositivo para completar la instalación de la aplicación.|
|platformNotApplicable|-1006|Aplicación no es aplicable a esta plataforma. (por ejemplo, aplicación de Android dirigida a IOS)|
|minimumCpuSpeedNotMet|-1005|Velocidad de la CPU en el dispositivo de destino es menor que el mínimo configurado.|
|minimumLogicalProcessorCountNotMet|-1004|Número de procesadores lógicos en el dispositivo de destino es menor que el mínimo configurado.|
|minimumPhysicalMemoryNotMet|-1003|Cantidad de memoria RAM en el dispositivo de destino es menor que el mínimo configurado.|
|minimumOsVersionNotMet|-1002|Versión del sistema operativo en el dispositivo de destino es menor que el mínimo configurado.|
|minimumDiskSpaceNotMet|-1001|Espacio en disco disponible en el dispositivo de destino es menor que el mínimo configurado.|
|processorArchitectureNotApplicable|-1000|Arquitectura de dispositivo (por ejemplo, x86 o amd64) no es aplicable para la aplicación.|





