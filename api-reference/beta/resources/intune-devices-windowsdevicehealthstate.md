---
title: tipo de enumeración windowsDeviceHealthState
description: Estado de protección de extremo de equipo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 628450b33a219e8408d5c5887c6902b78ae02bd0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923946"
---
# <a name="windowsdevicehealthstate-enum-type"></a>tipo de enumeración windowsDeviceHealthState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de protección de extremo de equipo
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|clean|0|Equipo está limpio y no se requiere ninguna acción|
|fullScanPending|1|Equipo está en estado de examen completo pendiente|
|rebootPending|2|Equipo está en estado de reinicio pendiente|
|manualStepsPending|4|Equipo está en estado de pasos manuales pendiente|
|offlineScanPending|8|Equipo está en estado de análisis sin conexión pendiente|
|crítico|16|Equipo está en estado de error crítico|





