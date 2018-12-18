---
title: tipo de enumeración configurationManagerClientState
description: Estado de cliente del Administrador de configuración
author: tfitzmac
ms.openlocfilehash: dc67a5fb1c517e65da937996ed65adaa621fa3c5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354050"
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





