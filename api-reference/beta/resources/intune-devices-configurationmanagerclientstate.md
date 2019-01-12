---
title: tipo de enumeración configurationManagerClientState
description: Estado de cliente del Administrador de configuración
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fc6f3f2db68273097d70ba9dccc6844b86afa3f6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923890"
---
# <a name="configurationmanagerclientstate-enum-type"></a>tipo de enumeración configurationManagerClientState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de cliente del Administrador de configuración
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|Agente de configuración del administrador es más antiguo que 1806 o no está instalado o este dispositivo no ha desprotegido en Intune durante más de 30 días.|
|instalado|1|El agente de configuración del administrador está instalado pero es posible que no se aparece en la consola de administrador de configuración todavía. Espere unas cuantas horas para que pueda actualizar.|
|buen estado|7|Este dispositivo pudo comprobar correctamente con el servicio de administrador de configuración.|
|installFailed|8|No se pudo instalar el agente de configuración del administrador.|
|updateFailed|11|Error al actualizar desde la versión x a y de la versión del agente de administrador de configuración. |
|communicationError|19|El agente de configuración del administrador puede ponerse en contacto con el servicio de administrador de configuración en el pasado, pero ahora ya no es capaz de. |





