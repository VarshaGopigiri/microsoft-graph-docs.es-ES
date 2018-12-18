---
title: tipo enum de habilitación
description: 'Valores utilizados para indicar el estado de un dispositivo. '
author: tfitzmac
ms.openlocfilehash: 5b1d494fd116eab437b4654d396b029e1384a817
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356892"
---
# <a name="enablement-enum-type"></a>tipo enum de habilitación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores utilizados para indicar el estado de un dispositivo. 

Tenga en cuenta que hay una diferencia entre deshabilitado y no está definida.

## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|Valor predeterminado de dispositivo, sin intención.|
|enabled|1|Habilita a la configuración en el dispositivo.|
|deshabilitado|2|Deshabilita a la configuración en el dispositivo.|
