---
title: tipo de enumeración windowsUserAccountControlSettings
description: Valores posibles para la configuración de control de cuenta de usuario de Windows.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cd16db4236096687ddcc9f169dd657c938fd6815
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911815"
---
# <a name="windowsuseraccountcontrolsettings-enum-type"></a>tipo de enumeración windowsUserAccountControlSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para la configuración de control de cuenta de usuario de Windows.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Definido por el usuario, valor predeterminado, sin intención.|
|alwaysNotify|1|Notificarme siempre.|
|notifyOnAppChanges|2|Notificar en los cambios de la aplicación.|
|notifyOnAppChangesWithoutDimming|3|Notificar en los cambios de la aplicación sin atenuar el escritorio.|
|neverNotify|4|No notificar nunca.|





